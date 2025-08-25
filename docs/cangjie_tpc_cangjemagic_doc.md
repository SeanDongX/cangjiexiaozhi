# Cangjie Magic Documentation

---

# Tutorial

# 用户教程

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [用户教程](#用户教程)
  - [Agent 定义](#agent-定义)
  - [编写提示词](#编写提示词)
    - [使用提示词模式](#使用提示词模式)
    - [自定义提示词模式](#自定义提示词模式)
  - [Agent 交互方法](#agent-交互方法)
    - [输入模板](#输入模板)
    - [对话历史](#对话历史)
  - [MCP 协议和工具](#mcp-协议和工具)
    - [工具函数编写](#工具函数编写)
    - [使用工具和 MCP 服务器](#使用工具和-mcp-服务器)
    - [工具额外属性设置](#工具额外属性设置)
  - [规划](#规划)
    - [Agent 执行 DSL（实验）](#agent-执行-dsl实验)
  - [外部知识](#外部知识)
  - [示例](#示例)
    - [示例 1: 命令行助手 Agent](#示例-1-命令行助手-agent)
  - [多 Agent 协作](#多-agent-协作)
    - [线性协同](#线性协同)
    - [主从协同](#主从协同)
    - [自由协同](#自由协同)
    - [Agent 协同子组构建](#agent-协同子组构建)
  - [快捷 AI 函数](#快捷-ai-函数)
  - [模型配置](#模型配置)
  - [常用 API 介绍](#常用-api-介绍)
    - [全局配置](#全局配置)
    - [Agent 类型](#agent-类型)
    - [Agent 劫持机制](#agent-劫持机制)
    - [内置 Agent](#内置-agent)
      - [`BaseAgent`](#baseagent)
      - [`DispatchAgent`](#dispatchagent)
      - [`ToolAgent`](#toolagent)
      - [`HumanAgent`](#humanagent)
    - [Jsonable 接口](#jsonable-接口)
    - [接入新模型](#接入新模型)
    - [自定义规划方法](#自定义规划方法)
    - [语义检索功能](#语义检索功能)
      - [向量模型](#向量模型)
      - [向量数据库](#向量数据库)
      - [索引映射表](#索引映射表)
      - [语义数据结构](#语义数据结构)
      - [使用示例](#使用示例)
    - [知识图谱](#知识图谱)
      - [MiniRag](#minirag)
      - [`实例化`](#实例化)
      - [`知识图谱构建`](#知识图谱构建)
      - [`知识图谱检索`](#知识图谱检索)
      - [使用示例](#使用示例-1)
        - [`知识图谱检索`](#知识图谱检索)
<!-- /code_chunk_output -->

Cangjie Agent DSL 是一个用于定义和管理 Agent 的专用语言。它允许开发人员通过结构化的系统提示词、工具和各类协作策略来增强 Agent 的功能。本手册将介绍如何使用 Cangjie Agent DSL 的各种功能，并通过实例帮助用户快速上手。

Cangjie Agent DSL 被设计为仓颉语言的 eDSL，即在仓颉语言中通过元编程机制实现了嵌入式的 DSL，且仓颉语言作为它的宿主语言。这意味着 Agent DSL 编写的代码最终都被转换为普通的仓颉代码，并最终由仓颉编译器完成编译。

## Agent 定义

目前，我们使用宏 `@agent` 修饰 `class` 类型来定义一个 Agent 类型。

```cangjie
@agent class Foo { }
```

宏 `@agent` 支持如下属性，具体属性可参考相应章节内容。

| 属性名 | 值类型 | 说明 |
|-------|-------|-------|
| `description` | `String` | Agent 的功能描述；默认未设置时，将由 LLM 从提示词中自动总结出 |
| `model` | `String` | 配置使用到的 LLM 模型服务；默认使用 gpt-4o |
| `tools` | `Array` | 配置能够使用的外部工具 |
| `rag` |   `Map` | 配置外部的知识源 |
| `memory` |  `Bool` | 是否使用记忆，即保存 Agent 的多次问答记录（目前记忆仅支持 in-memory 非持久化数据）；默认为 `false` |
| `executor` | `String` | 规划模式；默认为 `react` |
| `temperature` | `Float` | Agent 使用 LLM 时的 temperature 值；默认为 `0.5` |
| `enableToolFilter` | `Bool` | 启用工具过滤功能，Agent 在执行前会自动根据输入问题选择合适的工具集合；默认 `false` |
| `dump` | `Bool` | 调试代码用，是否打印 Agent 变换后的 AST；默认为 `false` |

## 编写提示词

每个 Agent 的核心是系统提示词，它定义了 Agent 的角色信息和执行步骤，使得大语言模型（LLM）能够更准确和快速地回答问题。在 Agent 定义中，`@prompt` 用于编写 Agent 的系统提示词。

- 在 `@prompt` 宏的作用域下，所有字符串字面量（包括插值字符串）会被依次拼接为完整的系统提示词。
- 在 `@prompt` 中能够访问仓颉语言的函数和成员变量。
- 每个 Agent 最多有一个 `@prompt` 定义。

**示例：字符串拼接**
以下代码将三个字符串依次拼接作为完整的 Agent 系统提示词，并且第三个插值字符串中调用了函数 `bar`。

```cangjie
@agent
class Foo {
    @prompt(
        "# This is a Foo agent"
        "## Description"
        "balabala ${bar()}"
    )
}
```

**示例：访问成员变量**

```cangjie
@agent
class Calculator {
    @prompt(
        """
        你是一个计算器，能够进行计算。
        你的名字是 ${name}-${version}。
        """
        "例如，你可以加法运算，1 + 2 = 3 ..."
    )
    private let name: String
    private let version: Int64
    ...
}

let calculator = Calculator(name: "aha", version: 1)
```

宏 `@prompt` 支持设置 `include` 属性，属性值为字符串。该字符串是一个文件路径，表示将文件内容作为 Agent 系统提示词。
- 当配置 `include` 属性后，`@prompt` 中编写的字面量将失效，不再作为系统提示词
- 若 `include` 指向的文件不存在，将抛出异常

**示例：使用外部文件编写系统提示词**

```cangjie
@agent
class Foo {
    @prompt[include: "./a.md"]()
}
```

### 使用提示词模式

良好的结构化提示词能够显著提升 LLM 的性能。通过定义统一的提示词语法，可以帮助开发者编写更加结构化的提示词。

**使用提示词模式**

宏 `@prompt`  支持设置 `pattern` 属性，其值应为提示词模式类型。使用提示词模式时，`@prompt` 作用域内必须编写满足模式的*提示词元素*而不是字符串字面量。

注意：`include` 属性和 `pattern` 属性无法同时使用；若两者同时出现将抛出异常。

**示例：使用提示词模式**

```cangjie
@agent
class Foo {
    @prompt[pattern: APE] (
        action: "帮助用户制定旅行路线",
        purpose: "让用户在计划的时间内尽可能多地参观景点并得到充分休息",
        expectation: "生成一条合理的旅行路线，包括时间、景点、通勤等信息"
    )
}
```

以下是目前已提供的提示词模式。

<table>
    <tr>
        <th>提示词模式</th>
        <th>说明</th>
    </tr>

<tr>
<td>

`APE`

</td>
<td>

`action`: 定义要完成的工作或活动
`purpose`: 定义为什么要开始这个行动
`expectation`: 陈述预期结果

</td>
</tr>
<tr>
<td>

`BROKE`

</td>
<td>

`background`: 描述背景并提供足够的信息
`role`: 指定代理的角色
`objectives`: 定义要实现的任务目标
`keyResult`: 定义关键的、可衡量的结果，以指导代理如何评估目标的实现情况
`evolve`: 通过实验和调整来测试结果，并在需要时进行优化

</td>
</tr>
<tr>
<td>

`COAST`

</td>
<td>

`context`: 为对话设定背景
`objective`: 描述目标
`action`: 解释所需的行动
`scenario`: 描述情景
`task`: 描述任务

</td>
</tr>
<tr>
<td>

`TAG`

</td>
<td>

`task`: 定义具体的任务
`action`: 描述需要做什么
`goal`: 解释最终目标

</td>
</tr>
<tr>
<td>

`RISE`

</td>
<td>

`role`: 指定代理的角色
`input`: 描述信息或资源
`steps`: 要求提供详细步骤
`expectation`: 描述期望的结果

</td>
</tr>
<tr>
<td>

`TRACE`

</td>
<td>

`task`: 定义具体的任务
`request`: 描述你的请求
`action`: 解释你需要的行动
`context`: 提供背景或情境
`example`: 给出一个示例以说明你的观点

</td>
</tr>
<tr>
<td>

`ERA`

</td>
<td>

`expectation`: 描述期望的结果
`role`: 指定代理的角色
`action`: 指定要采取的行动

</td>
</tr>
<tr>
<td>

`CARE`

</td>
<td>

`context`: 为讨论设定背景或情境
`action`: 描述你想做什么
`result`: 描述期望的结果
`example`: 给出一个示例以说明你的观点

</td>
</tr>
<tr>
<td>

`ROSES`

</td>
<td>

`role`: 指定代理的角色
`objective`: 陈述目标或目的
`scenario`: 描述情境
`expectation`: 定义期望的结果
`steps`: 达到解决方案所需的步骤

</td>
</tr>
<tr>
<td>

`ICIO`

</td>
<td>

`instruction`: 具体的任务指示给 AI
`context`: 提供更多背景信息给 AI
`input`: 告知模型需要处理的数据
`output`: 告知我们期望的输出类型或样式

</td>
</tr>
<tr>
<td>

`CRISPE`

</td>
<td>

`capacityAndRole`: 代理应扮演的角色
`insight`: 提供见解、背景和情境
`statement`: 你要求代理做什么
`personality`: 你希望代理以什么风格、个性或方式响应
`experiment`: 请求代理提供多个示例进行响应

</td>
</tr>
<tr>
<td>

`RACE`

</td>
<td>

`role`: 指定代理的角色
`action`: 详细说明要采取的行动
`context`: 提供相关情境的详细信息
`expectation`: 描述期望的结果

</td>
</tr>
<tr>
<td>

`SAGE`

</td>
<td>

`situation`: 描述执行任务的背景或环境
`action`: 具体指定需要采取的操作或步骤
`goal`: 说明任务完成后应达到的目的或效果
`expectation`: 具体说明对输出结果的要求

</td>
</tr>

</table>

### 自定义提示词模式

宏 `@promptPattern` 作用于 `class` 类型，可定义新的提示词模式。在被修饰的类定义中，宏 `@element` 用于修饰成员变量，可定义提示词元素。
- 每个元素必须是 `String` 类型，
- `description` 属性用于解释元素，不会影响最终提示词。

提示词模式类型必须实现 `toString` 方法，该方法用于构建提示词。

**示例：自定义提示词模式**

```cangjie
@promptPattern
class APE {
    @element[description: "定义任务"]
    let action: String

    @element[description: "定义任务原因"]
    let purpose: String

    @element[description: "清晰地定义期望结果"]
    let expectation: String

    public func toString(): String {
        return "...${action}...${purpose}...${expectation}..."
    }
}
```

## Agent 交互方法

由 `@agent` 定义的 Agent 都有一个默认方法 `func chat(question: ToString): String` 作为交互入口。

```cangjie
@agent class Foo { ... }

let agent = Foo()
let result = agent.chat("What's the weather today?")
println(result)
```

此外，通过 `chatGet` 能够让 Agent 能够直接返回一个数据类型而不仅仅是字符串。如果 Agent 未能生成满足要求的数据类型，则返回 `None`。方法定义如下：

```cangjie
func chatGet<T>(question: String): Option<T> where T <: Jsonable<T>
```

其中，`Jsonable` 接口 ([见章节](#jsonable-接口))约束了数据类型能够和 JSON 对象进行转换。基础类型 `Int/Int64/String` 均已实现该接口。

宏 `@jsonable` 用于自定义类型来自动实现该接口：

- `@jsonable` 用于修饰 `class` 类型，它通过代码转换的方式让所修饰的类型自动实现 `Jsonable` 接口
- 所修饰的类型中，可以使用 `@field` 添加对于成员变量的描述信息。如果不使用，成员变量将不携带描述信息

**示例：返回数据结构**

```cangjie
@jsonable
class MyDate {
    @field["Year of the foundation"]
    let year: Int64
    let month: Int64
}

@agent
class Foo { }

let agent = Foo()
let date = agent.chatGet<MyDate>("华为创建时间")
println(date.year)
println(date.month)
```

### 输入模板

`@agent` 定义 Agent 类型时，可以提供*输入模板*，即将输入问题模板化，模板中可编写*占位符变量*。在调用交互接口时仅提供占位符变量的取值。
宏 `@user` 用于定义输入模板：
- `@user` 和 `@prompt` 类似，它会依次将所有字符串字面量拼接作为完整的输入模板
- 在输入模板中的 `{variable}` 是占位符变量，其中变量名由大小写字母、数字和下划线组成
- 同 `@prompt` 一样，`@user` 支持 `include` 属性，并且属性值为文件路径；若设置该属性，文件内容将作为输入模板

在调用 `func chat(variables: Array<(String, ToString)>): String` 方法时，需要传入占位符变量和对应的值。
- 若 Agent 未提供输入模板，调用该方法将抛出 `UnsupportedException` 异常

**示例：使用输入模板**

```cangjie
@agent
class Foo {
    @prompt(
        "System: ..."
    )
    @user(
        "矩形的长为：{length} cm，宽为 {width} cm"
        "计算矩形的面积"
    )
}
let agent = Foo()
let area = agent.chat(
    ("length", 3),
    ("width", 4),
)
```

### 对话历史

和 Agent 的一次 `chat` 调用能构成 `ChatRound`，`Conversation` 维护多个对话过程，从而形成连续对轮的对话历史。

在调用 Agent 时，可以将 `Conversation` 作为 `AgentRequest` 的参数来让 Agent 基于对话完成作答。同时，通过 `AgentResponse` 的 `execution.chatRound` 属性来更新对话历史。

**示例：对话历史示例**

```cangjie
let agent = FooAgent()
let conversation = Conversation()
let resp = agent.chat(
    AgentRequest("Hello", conversation: conversation)
)
// 更新对话
conversation.addChatRound(resp.execution.chatRound)
let resp2 = agent.chat(
    AgentRequest("How are you", conversation: conversation)
)
```

## MCP 协议和工具

工具可以理解为 Agent 执行过程中能够执行的代码。当前 Agent 工具有两个来源：
- 使用 DSL 直接编写的工具函数
- 由 MCP 服务器提供的工具（MCP 服务器可视为*一组工具的集合*）

### 工具函数编写

宏 `@tool` 用于函数，将函数转换为**工具函数**，可被修饰的函数有：

- 全局函数
- `@agent` 定义的 Agent 类成员方法
- `@toolset` 定义的 `Toolset` 类型的成员方法

所有工具函数都有如下的属性：

- `description` 属性描述了工具的功能【必选】
- `parameters` 属性描述了函数参数的含义，它接收 `<parameter-name>: <parameter-description>` 的键值对【可选】
- `filterable` 是否可以被 Agent 过滤，配合 `@agent` 宏的 `enableToolFilter` 属性使用【可选】
- `terminal` 是否终止 Agent 执行，当设置为 `true` 时，Agent 执行这个工具后将直接结束，并且函数的返回值作为 Agent 执行结果【可选】
- `compressible`: 是否（使用 LLM）将工具的执行结果做总结压缩，仅当该属性设置为 `true` 且结果长度超过 `Config.resultSummarizeThreshold` 进行压缩【可选】

如果工具函数是全局函数或是在 Toolset 中，那么需要在 `tools` 属性中显式指定才能让 Agent 使用工具。

**示例：定义并配置全局工具**

```cangjie
@tool[description: "...",
      parameters: { arg: "..."}]
func foo(arg: String): String { ... }

@agent[
    tools: [foo]
]
class A { ... }
```

**示例：定义工具集类型并配置**

```cangjie
@toolset
class FooToolset {
    @tool[description: "..."]
    func foo(arg: String): String { ... }

    @tool[description: "..."]
    func bar(): String { ... }
}

@agent[
    tools: [FooToolset()]
]
class A { ... }
```

**示例：定义内部工具**

```cangjie
@agent
class A {
    @tool[description: "...",
          parameters: { str: "..." }]
    func bar(str: String): String { ... }
}
```

对于工具函数存在的限制：
- 当前工具函数的形参类型满足 `Jsonable` 接口
- 工具函数的返回值必须满足 `ToString` 接口，该接口方法的返回值将作为工具调用的返回值

### 使用工具和 MCP 服务器

Agent 通过 `tools` 属性配置使用的 MCP 服务器以及自定义工具函数。该属性接收多个 MCP 服务器/工具函数，每个配置可采用如下的语法：

- `stdio` 传输协议的 MCP 服务器，`stdioMCP(<command>, <env-kv-pair>*)`，编写启动 MCP 服务器的命令行以及可选的环境变量设置。例如，`stdioMCP("command and arguments", ENV_1: "value1", ENV_2, "value2")`。
- `http/sse` 传输协议的 MCP 服务器，`mcpHttp(<url>)`，编写 MCP 服务器的地址。例如， `httpMCP("https://abc.com/mcp")`。
- 工具函数 `<func-id>+`，例如，`foo, bar`。注意 ⚠️：如果工具被定义在 Agent 类的内部，那么它能被其所属的 Agent 直接使用，即**无需**在 `tools` 属性中显式指定。
- 工具集构造 `<expr>`，通常是工具集类型的实例化，例如 `MyToolset()`。

```cangjie
@agent[
    tools: [
        stdioMCP("node index.js args" ),
        stdioMCP("python main.py args", SOME_API_KEY: "xxx"),
        httpMCP("http://abc.mcp.server.com"),
        toolA,
        toolB,
        SomeToolset()
    ]
]
class Foo { ... }
```

我们也可以直接通过 API 方式给 Agent 配置 MCP 工具。

```cangjie
// 初始化 MCP client
let client = MCPClient("node", ["args"])
let agent = SomeAgent()
// 添加 MCP 工具
agent.toolManager.addTools(client.getTools())
```

⚠️注意：目前 MCP 服务器仅支持工具相关的 MCP 协议。

此外，在 `tools` 配置中**同样支持以 JSON 配置的语法设置 MCP 服务器**：

- `stdio` 传输，配置方式为：由 `command`（启动命令）和 `args`（启动参数）构成，并可选设置启动的环境变量  `env`。
- `HTTP SSE` 传输，配置方式为：通过 `url` 指定 MCP 服务器的地址

```cangjie
@agent[
    tools: [
        { command: "node", args: [ "index.js", "args" ] },
        { command: "python", args: [ "main.py", "args" ], env: { SOME_API_KEY: "xxx" } },
        { url: "http://abc.mcp.server.com" }
    ]
]
class Foo { ... }
```

### 工具额外属性设置

所有工具都允许通过特殊成员变量 `extra: HashMap<String, String>` 来保存额外的属性值。当前有两个特殊属性值：

- `filterable: "true" | "false"` 是否可以被 Agent 过滤，配合 `agent.toolManager.enableFilter` 设置使用
- `terminal: "true" | "false"` 是否终止 Agent 执行，当设置为 `true` 时，Agent 执行这个工具后将直接结束，并且函数的返回值作为 Agent 执行结果

**示例：设置工具额外属性**

```cangjie
let tool: Tool = getSomeTool()
tool.extra["filterable"] = "false"
tool.extra["terminal"] = "true"
```

## 规划

每个 Agent 有一个 `executor` 属性，用于指定使用哪个执行器（不同执行器使用不同的规划策略）。目前支持如下执行器：

| 规划名称  | 说明  |
|---|---|
| `naive`  | 直接问答  |
| `react` | Agent 每次选择使用一个工具完成一个求解步骤，然后根据工具的执行结果判断是否执行完成，不断迭代上述过程直至任务求解完成 |
| `plan-react` | 首先完成一次任务规划，然后对每个规划出来的子任务使用 React 模式进行求解 |
| `tool-loop` | 功能接近 `react`，但没有显式的思考过程 |

其中，`react` 和 `tool-loop` 执行器可以通过形式 `react:<number>` 类指定迭代的最大次数，如 `react:5`。

**示例：配置规划方法**

```cangjie
@agent[executor: "naive"]
class Foo{ }

@agent[executor: "react"]
class Bar{ }
```

### Agent 执行 DSL（实验）

除了直接使用 Magic 预先提供的规划方法外，还可以使用规划 DSL 去更细粒度地控制 Agent 执行过程。

**Agent Execution DSL 定义**：一种用于定义 LLM Agent 执行流程的“编程语言”，通过组合操作实现复杂策略

- **避免重复代码**：避免手写冗余模板代码
- **灵活定制**：能够轻易编写复杂的规划策略

**基本规则**

- 规划 DSL 在 `@agent` 内部 `@execution` 中使用；当使用规划 DSL 后，将忽略 `executor` 属性的配置。
- 管道符 `|>` 串联多个规划操作
- Agent 执行状态是*一个 Prompt 序列*
  - 每次令 LLM 执行完一个操作后，操作结果将添加到这个 Prompt 序列中

**使用示例**

```swift
@agent class Foo {
  @execution(
    plan |> loop(think |> action) |> answer
  )
}
```

流程图示

```
             plan         -> think         -> action ->       think -> ... -> answer
| SysPrompt | -> | SysPrompt | -> | SysPrompt |        | SysPrompt |
                 | Plan: ... |    | Plan: ... |        | Plan: ... |
                                  | Think: ... |       | Think: ... |
                                                       | Action: ... |
                                                       | Result: ... |
```

规划操作是从已有的规划方法中提取而来，将规划中常用的逻辑抽象为可组合的操作，包括三类：*基础操作*、*任务分解操作*、*条件控制操作*。

**基础操作速览**

| 操作符      | 作用             |
|-------------|----------------|
| `think`     | 生成推理步骤     |
| `action`    | 选择并执行工具   |
| `answer`    | 返回最终答案     |
| `plan`      | 制定计划     |
| `loop`      | 循环内部操作序列 |
| `tool`      | 依次执行工具函数序列，工具的参数由 LLM 自动生成 |
| `done`      | 检查是否终止     |

**复杂操作：任务分解&合并**

```swift
@agent class ResearchAssistant {
  @execution(
    divide |> each(tool(web_search)) |> summary |> answer
  )
  @tool
  func web_search(...) { ... }
}
```

| 操作符      | 作用             |
|-------------|----------------|
| `divide` | 由 LLM 拆分任务为子问题，子问题数由 LLM 自动决定 |
| `each` | 处理子任务 |
| `summary` | 汇总子任务结果 |

**复杂操作：条件控制**

```swift
@agent class Assistant {
  @execution(
    switch(
      onCase("问题是询问天气？", tool(weather_api)),
      onCase("问题是关于订单查询？", tool(db_query |> db_summary)),
      otherwise(think |> answer)
    )
  )
}
```

- `switch` 接受多个 `onCase` 子句
- 每个 `onCase` 子句由一个条件（自然语言表示）和操作序列组成
    - 当 `onCase` 中条件成立（根据当前执行状态），对应的操作序列继续执行
    - `onCase` 子句由上往下依次执行
- 若没有 `onCase` 成立，则执行 `otherwise` 子句


## 外部知识

除了系统提示词，外部知识也可以增强 Agent 的解决问题的能力。 Agent 能够从各类知识源中提取必要和有用的信息。

目前，Agent 的 `rag` 属性表明外部知识的数据源，它接受多个数据源配置，每个数据源包含如下的键值对：

| 属性  | 属性值 | 说明 |
|---|---|---|
| `source`  | `String \| Expr`  | 数据源 |
| `mode`  | `String`  | 使用模式，支持 `"static"` 和 `"dynamic"` 两种；默认为 `"static"` |
| `description`  | `String`  | 可进一步描述数据源，帮助 Agent 更加精准地获取数据 |

属性 `source` 表明数据的实际来源，支持两种类型：
- 合法路径指向*预置的文件类型*
    - 当前支持的文件类型包括 markdown, Sqlite 数据库
- 类型为 `Retriever` 的表达式

```cangjie
@agent[
  rag: { source: "path/to/some.md", mode: "dynamic" }
]
class Foo { }
```

⚠️注意：使用 Sqlite 数据库的功能需要配置 `cfg.toml` 中 `sqlite = "enable"`，且由于数据库使用了 Sqlite，所以需要安装三方依赖。详见 [third_party_libs.md](./third_party_libs.md)

## 示例

### 示例 1: 命令行助手 Agent

```cangjie
@agent[executor: "react"]
class CJCAgent {
    @prompt(
        """
        你是一个 CJC 命令行助理。
        你帮助用户根据他们的问题生成命令行。
        """
    )

    @tool[description: "获取 CJC 的使用手册"]
    private func getManual(): String {
        let subProcess: SubProcess = Process.start(
            "cjc", ["--help"], stdOut: ProcessRedirect.Pipe
        )
        let strReader: StringReader<InputStream> = StringReader(subProcess.stdOut)
        let result = strReader.readToEnd().trimAscii()
        return result
    }
}

let agent = CJCAgent()
let result = agent.chat("编译一个文件到 ARM 平台")
```

## 多 Agent 协作

多 Agent 可以被组织为组以进行高效协作。这些协作通常分为三类：

1. **线性协同**： Agent 按顺序操作，每个 Agent 接收前一个 Agent 的消息（包括结果和任务），进行处理，然后将结果传递给下一个 Agent 。
2. **主从协同**：一个 Agent 作为领导者，负责监督其他 Agent 的活动，其他 Agent 需向领导者报告。
3. **自由协同**：所有 Agent 作为一个平等的协作单元，进行组内讨论，每个 Agent 可以看见所有消息。

`AgentGroup` 接口用于抽象所有这些协作方式（详见 API 手册）。

### 线性协同

管道表达式 `|>` 用于将多个 Agent 组成为 `LinearGroup`。

```cangjie
let linearGroup: LinearGroup = ag1 |> ag2 |> ag3
```

### 主从协同

使用 `<=` 操作符将多个 Agent 组成 `LeaderGroup`，操作符前的 Agent 作为领导者，后面的值作为下属 Agent 的数组。

```cangjie
let leaderGroup: LeaderGroup = ag1 <= [ag2, ag3]
```

### 自由协同

使用 `|` 操作符将多个 Agent 组成 `FreeGroup`。

```cangjie
let freeGroup: FreeGroup = ag1 | ag2 | ag3
```

`FreeGroup` 还提供更为灵活的 `discuss` 方法。

```cangjie
public enum FreeGroupMode {
    | Auto // The speaker will be selected by LLM automatically
    | RoundRobin
}
class FreeGroup {
    public func discuss(topic!: String, initiator!: String, speech!: String,
                        mode!: FreeGroupMode = FreeGroupMode.Auto): String
    ...
}
```

`discuss` 方法能够指定：

- `topic` 讨论的主题（即需要解决的问题）
- `initiator` 第一个发言的 Agent
- `speech` 第一个发言 Agent 的内容
- `mode` 讨论模式，依次自动选择 Agent 发言或是按照轮询的方式

以下代码实现两个 Agent 进行猜数字游戏，参考 [AutoGen](https://github.com/microsoft/autogen/blob/main/website/docs/tutorial/human-in-the-loop.ipynb)。

```cangjie
@agent class AgentWithNumber {
    @prompt(
        "You are playing a game of guess-my-number. You have the "
        "number 33 in your mind, and I will try to guess it. "
        "If I guess too high, say 'too high', if I guess too low, say 'too low'."
    )
}

@agent class AgentGuessNumber {
    @prompt(
        "I have a number in my mind, and you will try to guess it. "
        "If I say 'too high', you should guess a lower number. If I say 'too low', "
        "you should guess a higher number. "
    )
}

func game() {
    let group = AgentWithNumber() | AgentGuessNumber()
    group.discuss(topic: "Number guessing game",
                  initiator: "AgentWithNumber",
                  speech: "I have a number between 1 and 70. Guess it!",
                  mode: FreeGroupMode.RoundRobin)
}
```

### Agent 协同子组构建

在构建线性协同时，不仅 Agent 能够参与，AgentGroup 同样能够直接参与构造。例如，

```cangjie
ag1 |> (ag2 <= [ag3]) |> ag4
```

上述代码构建了一个线性协同组，但同时第二个单元是一个主从协同组。此时，该主从协同组即为线性协同的**子组**。

然而，在构建主从协同和自由协同时无法直接将 `AgentGroup` 纳入构建；此时需要使用函数 `func subGroup(g: AgentGroup, description!: String): Agent` 将一个 Agent 协同组转换成可参与构建 Agent 协同组的子组对象。

```cangjie
ag1 | (ag2 <= [ag3]) | ag4 // Compilation error
ag1 | subGroup(ag2 <= [ag3], description: "An subgroup attempts to ...") | ag4 // Okay
```

## 快捷 AI 函数

`@ai` 可用于修饰函数，表明函数的执行将由 LLM 执行完成。`@ai` 修饰的函数必须是 `foreign` 函数，这相当于该函数的实现在模型侧，对当前代码而言是一个外部函数。要求：**函数的形参类型和返回值类型必须满足 `Jsonable` 接口**。并且，`@ai` 允许属性：

| 属性名 | 值类型 | 说明 |
|-------|-------|-------|
| `prompt` | `String` | AI 函数的额外知道 |
| `model` | `String` | 配置使用到的 LLM 模型服务；默认使用 gpt-4o |
| `tools` | `Array` | 配置能够使用的外部工具 |
| `temperature` | `Float` | Agent 使用 LLM 时的 temperature 值；默认为 `0.5` |
| `dump` | `Bool` | 调试代码用，是否打印 Agent 变换后的 AST；默认为 `false` |

**示例**：

```cangjie
@tool[description: "Fetches the html content of a URL."]
func fetch(url: String): String { ... }

@ai[
    prompt: "不超过 3 个关键字",
    tools: [fetch]
]
foreign func keywordsOf(url: String): Array<String>

main() { keywordsOf("https://cangjie-lang.cn/") }
```

## 模型配置

模型配置使用格式 `<provider>:<model>`，当前支持如下的模型服务商。

| 服务商名称  | 示例  | 配置说明 | 服务 URL 配置 |
|---|---|---|---|
| 阿里云 | `dashscope:qwen-plus` | `DASHSCOPE_API_KEY` | `DASHSCOPE_BASE_URL`，默认 `https://dashscope.aliyuncs.com/compatible-mode/v1` |
| DeepSeek | `deepseek:deepseek-chat` | `DEEPSEEK_API_KEY` | `DEEPSEEK_BASE_URL`，默认 `https://api.deepseek.com` |
|  火山方舟 | `ark:doubao-lite-4k` | `ARK_API_KEY` | `ARK_BASE_URL`，默认 `https://ark.cn-beijing.volces.com/api/v3` |
| Llama.cpp | `llamacpp` | 无需配置模型名称和 API Key | `LLAMACPP_BASE_URl`，默认 `http://localhost:8080` |
| Ollama | `ollama:phi-3` | 无需配置 API Key | `OLLAMA_BASE_URl`，默认 `http://localhost:11434` |
| OpenAI  | `openai:gpt-4o` | `OPENAI_API_KEY` | `OPENAI_BASE_URL`，默认 `https://api.openai.com/v1` |
| SiliconFlow | `siliconflow:deepseek-ai/DeepSeek-V3` | `SILICONFLOW_API_KEY` | `SILICONFLOW_BASE_URL`，默认 `https://api.siliconflow.cn/v1` |
| 智谱 AI | `zhipuai:glm-4` | `ZHIPUAI_API_KEY` | `ZHIPUAI_BASE_URL`，默认 `https://open.bigmodel.cn/api/paas/v4` |
| Google | `google:gemini-2.0-flash` | `GOOGLE_API_KEY` | `GOOGLE_BASE_URL`，默认 `https://generativelanguage.googleapis.com/v1beta/openai` |
| 月之暗面 | `moonshot:kimi-k2-0711-preview` | `MOONSHOT_API_KEY` | `MOONSHOT_BASE_URL`，默认 `https://api.moonshot.cn/v1` |
| OpenRouter | `openrouter:qwen/qwen3-coder:free` | `OPENROUTER_API_KEY` | `OPENROUTER_BASE_URL`，默认 `https://openrouter.ai/api/v1` |

模型配置不仅可以在 `@agent` 的 `model` 属性中使用，还可以直接通过 `ModelManager` 的静态成员方法来直接构造模型实例：`static func createChatModel(modelName: String): ChatModel`。

**模型支持列表**

|   | Chat | Embedding | Image |
|---|---|---|---|
| 阿里云 | ✔️ | ✔️ | ❌ |
| DeepSeek | ✔️ | ❌️ | ❌ |
| 火山方舟 | ✔️ | ✔️ | ❌ |
| Llama.cpp | ✔️ | ❌  | ❌ |
| Ollama | ✔️ | ✔️ | ❌ |
| OpenAI | ✔️ | ✔️ | ✔️ |
| SiliconFlow | ✔️ | ✔️ | ✔️ |
| 智谱 AI | ✔️ | ❌ | ❌ |
| Google | ✔️ | ❌ | ❌ |
| 月之暗面 | ✔️ | ❌ | ❌ |
| OpenRouter | ✔️ | ❌ | ❌ |

如果需要接入新的模型，可参考直接使用 API 设置（见下文）。

## 常用 API 介绍

本节中介绍的 API 可能不完全，详见 [API Reference](./api_reference.md)。

### 全局配置

类 `magic.config.Config` 提供如下的全局配置，所有的配置变量都可读写。

| 配置名称  | 类型 | 说明  | 默认值 |
|---|---|---|---|
|  `logLevel` | `LogLevel` |  日志级别  | `LogLevel.ERROR` |
| `logFile` | `String` | 日志文件路径 | `stdout` |
| `enableAgentLog` | `Bool` | 是否保存每个 Agent 单独日志  | `false` |
| `agentLogDir` | `String` | 每个 Agent 单独日志的存放目录 | `./logs/agent-logs` |
| `saveModelRequest` | `Bool` | 是否保存每个模型请求 | `false` |
| `modelRequestDir` | `String` | 模型请求存放目录 | `./logs/model-requests` |
| `defaultChatModel` | `Option<ChatModel>` | 默认的大语言模型 | `None` |
| `defaultEmbeddingModel` | `Option<EmbeddingModel>` | 默认的向量模型 | `None` |
| `externalScriptDir` | `String` | 保存外部脚本的目录 | `./external_scripts` |
| `defaultContextLen` | `Int` | LLM上下文长度 | `32000` |
| `defaultTokenizer` | `Option<Tokenizer>` | 设置默认的 tokenizer，用于计算提示词中的 token 数 | `UnicodeTokenizer()` |
| `enableFunctionCall` | `Bool` | 是否在 Agent 执行器中使用 LLM function call 能力（当前仅 `tool-loop/dsl` 两个执行器 | `false` |
| `maxReactNumber` | `Int` | React 模式的最大迭代次数 | `10` |
| `modelRetryNumber` | `Int` | 模型请求失败时的最大重试次数 | `3` |
| `env` | `HashMap<String,String>` | 设置环境变量 | - |

### Agent 类型

所有被 `@agent` 定义的类型都自动实现 `interface Agent`，具有如下的 API。这些 API 的用途是访问 Agent 的属性。

```cangjie
public interface Agent {
    /**
     * Name of the agent
     */
    prop name: String

    /**
     * Functionality description of the agent
     */
    prop description: String

    /**
     * Temerature the agent will pass to the LLM
     */
    mut prop temperature: Option<Float64>

    /**
     * System prompt of the agent
     */
    mut prop systemPrompt: String

    /**
     * Tools the agent can use
     */
    prop toolManager: ToolManager

    /**
     * Chat model the agent will use
     */
    mut prop model: Option<ChatModel>

    /**
     * The underlying agent executor
     */
    mut prop executor: AgentExecutor

    /**
     * Retreiver the agent can use
     */
    mut prop retriever: Option<Retriever>

    /**
     * Memory the agent will use
     */
    prop memory: Option<Memory>

    /**
     * Personal data the agent will use
     */
    prop personal: Option<Personal>

    /**
     * Set the agent interceptor
     */
    mut prop interceptor: Option<Interceptor>

    /**
     * Query the agent and get the answer
     */
    func chat(request: AgentRequest): String
}
```

其中 `func chat(request: AgentRequest): String` 方法是消息处理接口。
注意到，[章节](#agent-交互方法)中介绍的交互方法 `func chat(question: String): String` 是基于这一接口方法的封装。其中，

```cangjie
class AgentRequest {
    // The current user question
    public let question: String
    ...
}
```

### Agent 劫持机制

`Agent` 拥有可变属性 `mut prop interceptor: Interceptor` 可用于设置消息处理劫持 Agent。

```cangjie
enum InterceptorMode {
    | Always
    | Periodic(Int64)
    | Conditional((Request) -> Bool)
}

class Interceptor {
    public init(interceptorAgent: Agent, mode!: InterceptorMode = InterceptorMode.Always)
}
```

当设置劫持 Agent 后，每当 Agent 接收到消息（以 `Request` 类型表示）时，如果劫持条件成立，那么该消息将交由劫持 Agent 来处理，而不是原本 Agent 进行处理。有三种劫持模式判别条件是否成立：

- `Always` 永远劫持
- `Periodic` 周期性地劫持，即原本 Agent 每处理指定数量的消息后，下一条消息将被劫持
- `Conditional` 使用判别函数进行判断，如果函数返回 `true`，则劫持消息

```cangjie
let ag1 = Foo()
let ag2 = Bar()
ag1.interceptor = Interceptor(ag2, mode: InterceoptorMode.Periodic(2))

ag1.chat("msg 1")
ag1.chat("msg 2")
ag1.chat("msg 3") // ag2 will handle with this request message
```

### 内置 Agent

除了通过 `@agent` 定义 Agent 之外，当前框架内置如下的几种 Agent。

#### `BaseAgent`

`BaseAgent` 用于通过 API 调用的方式构造 Agent。

```cangjie
class BaseAgent <: Agent {
    public init(
        name!:         String                = "Base Agent",
        description!:  String                = "",
        temperature!:  Option<Float64>       = None,
        systemPrompt!: String                = "",
        toolManager!:  ToolManager           = SimpleToolManager(),
        model!:        Option<ChatModel>     = None,
        executor!:     Option<AgentExecutor> = None,
        retriever!:    Option<Retriever>     = None,
        memory!:       Option<Memory>        = None,
        interceptor!:  Option<Interceptor>   = None
    )
}
```

**示例：通过 `BaseAgent` 构造 Agent**

```cangjie
let agent= BaseAgent()
agent.systemPrompt = "New system prompt ..."
agent.model = ModelManager.createChatModel("ollama:phi3")
agent.toolManager.addTool(fooTool)
```

#### `DispatchAgent`

`DispatchAgent` 专用于在主从协同模式下完成任务分发

```cangjie
class DispatchAgent {
    public init(model!: String)
}
```

**示例**

```cangjie
let group = DiapatchAgent(model: "deepseek:deepseek-chat") <=[
    FooAgent(),
    BarAgent(),
    ...
]
```

#### `ToolAgent`

`ToolAgent` 不再使用大语言模型回复问题，而是直接执行提供的函数来产生回复。

```cangjie
class ToolAgent<T> where T <: Jsonable<T> {
    public init(fn!: (String) -> T)
}
```

使用该 Agent 配合线性协同，可完成类似 Langchain 的编排功能。

```cangjie
let group = FooAgent() |> ToolAgent(fn: { q: String => ...; }) |> BarAgent()
```

#### `HumanAgent`

`HumanAgent` 用户将用户作为 Agent 参与到 Agent 协同中。可将其视作特殊的 `ToolAgent`。

```cangjie
class HumanAgent {
    public init(qaFunc!: Option<(String) -> String> = None)
}
```

其中参数 `qaFunc` 可自定义，默认实现为将用户问题打之终端并接收用户输入作为回复。

```cangjie
let humanAgent = HumanAgent(qaFunc: { q: String => println(q); return "answer" })
let result = humanAgent.chat("question")
```

### Jsonable 接口

`Jsonable` 接口约束了类型能够和 JSON 数据进行互相转换。宏 `@jsonable` 能够为修饰的 `class/struct/enum` 类型自动实现该接口。

```cangjie
public interface Jsonable<T> {
    /**
     * Get the type schema of T
     */
    static func getTypeSchema(): TypeSchema

    /**
     * Deserialize from a Json string
     */
    static func fromJsonValue(json: JsonValue): T

    /**
     * Serialize to a Json string
     */
    func toJsonValue(): JsonValue
}
```

### 接入新模型

新模型可实现接口 `interface ChatModel`，然后通过 `agent.model` 属性进行设置。

模型相关类型在 `magic.core.model` 包中。

```cangjie
interface ChatModel <: Model {
    func create(req: ChatRequest): ChatResponse
    func asyncCreate(req: ChatRequest): AsyncChatResponse
}
```

使用到的消息类型在 `magic.core.message` 中。

```cangjie
public class ChatMessage <: ToString {
    public let name: String          // name of the sender
    public let role: ChatMessageRole // role of the sender
    public let content: String       // Content of the message
}
```

**示例：自定义对话模型**

```cangjie
@agent
class Foo { }

class NewModel <: ChatModel {
    public func create(req: ChatRequest): ChatResponse { ... }
    public func asyncCreate(req: ChatRequest): AsyncChatResponse { ... }
}

let foo = Foo()
foo.model = NewModel()
```

在自定义模型之后，可为模型注册名称，从而在 `@agent` 属性中可以直接配置使用。注册函数为 `ModelManager` 的成员方法 `func registerChatModel(name: String, buildFn: () -> ChatModel)`。
⚠️注意：需要确保模型注册在调用 Agent 实例方法之前。

**示例：注册自定义模型**

```cangjie
@agent[model: "newModel"]
class Foo { }

main() {
    ModelManager.register("newModel", { => NewModel() })
    let agent = Foo()
}
```

### 自定义规划方法

当预置的 `naive` 和 `react` 两种规划方法不满足需求时，可通过接口 `interface AgentExecutor` 开发新的执行器，然后通过 `agent.executor` 属性进行设置。

该接口相关类型在 `magic.core.agent` 包中。

```cangjie
interface AgentExecutor {
    func run(agent: Agent, request: AgentRequest): AgentResponse

    func asyncRun(agent: Agent, request: AgentRequest): AsyncAgentResponse
}
```

**示例：自定义Agent执行器**

```cangjie
@agent
class Foo { }

class NewExecutor <: AgentExecutor {
    func run(agent: Agent, request: AgentRequest): AgentResponse { ... }

    func asyncRun(agent: Agent, request: AgentRequest): AsyncAgentResponse { ... }
}

let foo = Foo()
foo.executor = NewExecutor()
```

在自定义执行器后，可为其注册名称，从而在 `@agent` 属性中可以直接配置使用。注册函数为 `AgentExecutorManager` 的成员方法 `func registerAgentExecutor(name: String, buildFn: () -> AgentExecutor)`。
⚠️注意️ ：需要确保模型注册在调用 Agent 实例方法之前。

**示例：注册自定义执行器**

```cangjie
@agent[executor: "newExecutor"]
class Foo { }

main() {
    AgentExecutorManager.register("newExecutor", { => NewExecutor() })
    let agent = Foo()
}
```

### 语义检索功能

语义检索功能被划分为如下几个模块：

- 向量模型：为数据结构的语义信息（`String` 类型）构建语义向量 `vector`
- 向量数据库：构建向量索引，即维护 `vector -> index` 的映射关系；提供向量检索
- 索引映射表：维护索引到数据的映射关系，即 `index -> 数据`
- 语义数据结构，将上述模块封装，提供便捷的使用接口

除向量模型外，本节中所有类型都定义在 `vdb` 子包中。

#### 向量模型

向量被定义如下。

```cangjie
class Vector {
    public init(data: Array<Float32>)
}
```

可使用 `VectorBuilder` 构建向量。

```cangjie
public class VectorBuilder {
    public VectorBuilder(model!: EmbeddingModel)

    public func createEmbeddingVector(content: String): Vector
}
```

目前支持如下两种 embedding 模型服务，位于 `model.openai/ollama` 子包中。

```cangjie
class OpenAIEmbeddingModel <: EmbeddingModel {
    ...
}

class OllamaEmbeddingModel <: EmbeddingModel {
    ...
}
```

可利用 `ModelManager.createEmbeddingModel` 方法来方便地构造模型实例。

**示例：构建向量**

```cangjie
let model = ModelManager.createEmbeddingModel("openai:text-embedding-ada-002")
let vecBuilder = VectorBuilder(model: model)
let vector= vecBuilder.createEmbeddingVector("第一条向量")
```

#### 向量数据库

向量数据库抽象为如下的接口。

```cangjie
public interface VectorDatabase<Self> {
    /**
     * Add the vector to the database
     * ATTENTION: index must start from 0
     */
    func addVector(vector: Vector): Unit

    /**
     * Query the database and find indexes of similar data
     */
    func search(queryVec: Vector, number!: Int64): Array<Int64>

    /**
     * Save to the file
     */
    func save(filePath: String): Unit

    /**
     * Load from the file
     */
    static func load(filePath: String): Self
}
```

目前支持的是 `InMemoryVectorDatabase` 和 `FaissVectorDatabase` 两个。

```cangjie
class FaissVectorBase {
    public init(dimension: Int64)
}

class InMemoryVectorDatabase {
    public init()
}
```

注意：如果使用 faiss 向量数据库，需要配置 `cfg.toml` 中 `faiss = "enable"` 且需要安装三方依赖。详见 [third_party_libs.md](./third_party_libs.md)

#### 索引映射表

索引映射表用于维护 `index -> 数据` 关系，被抽象为如下接口。

```cangjie
public interface IndexMap<Self, T> where T <: ToString {
    /**
     * The index is determined by the order in which it was added.
     */
    func add(content: T): Unit

    func get(index: Int64): T

    func save(filePath: String): Unit

    static func load(filePath: String): Self
}
```

目前提供了如下两种索引映射表：

`SimpleIndexMap` 支持保存数据类型为 `String`，即维护 `index -> String` 的映射关系。在持久化时，它会直接将映射关系保存为 JSON 文件。
```cangjie
class SimpleIndexMap <: IndexMap<SimpleIndexMap, String> { ... }
```

`JsonlIndexMap` 支持保存任意满足 `Jsonable` 的数据类型。在持久化时，它会将数据保存为 JSONL 文件，并且 index 即为文件行号。

```cangjie
class JsonlIndexMap<T> <: IndexMap<JsonlIndexMap<T>, T> where T <: Jsonable<T> & ToString
```

#### 语义数据结构

向量数据集一般不直接使用，而是被封装在两个数据结构 `SemanticMap` 和 `SemanticSet` 中。

```cangjie
public class SemanticMap<VDB, IMAP, T> where VDB <: VectorDatabase<VDB>,
                                             IMAP <: IndexMap<IMAP, T>,
                                             T <: ToString {
    /**
     * 实例化对象
     * @param vectorDB 是用于做相似度检索的向量数据库
     * @param embeddingModel 是用于做向量化的 embedding 模型；默认使用 OpenAI 的 text-embedding-ada-002
     */
    public init(vectorDB!: VDB,
                indexMap: IMAP,
                embeddingModel!: Option<EmbeddingModel> = None)

    /**
     * 主要用于设置 embedding 模型
     */
    public mut prop embeddingModel: EmbeddingModel

    /**
     * 插入新的键值对
     */
    public func put(key: String, value: T): Unit

    /**
     * 根据 key 对 map 进行语义检索，查找出相似的 value；
     * number 是查找的最大数量
     * minDistance 最小的相似度距离
     */
    public func search(query: String,
                       number!: Int64 = 5,
                       minDistance!: Float64 = 0.3): Array<T>

    /**
     * 构造 Retriever 对象
     */
    public func asRetriever(): Retriever

    /**
     * 保存到指定的目录下
     */
    public func save(dirPath: String): Unit

    /**
     * 根据目录路径加载数据
     */
    public static func load(dirPath: String): SemanticMap<VDB, IMAP, T>
}
```

另一个数据结构 `SemanticSet` 有相似 API，差异在于：它检索和查找的内容就是 value 本身。

```cangjie
public class SemanticSet<VDB, IMAP, T> where VDB <: VectorDatabase<VDB>,
                                             IMAP <: IndexMap<IMAP, T>,
                                             T <: ToString {
    public init(vectorDB!: VDB,
                indexMap: IMAP,
                embeddingModel!: Option<EmbeddingModel> = None)
    public mut prop embeddingModel: EmbeddingModel
    public func put(value: T): Unit
    public func search(query: String, number!: Int64 = 5, minDistance!: Float64 = 0.3): Array<T>
    public func save(dirPath: String): Unit
    public static func load(dirPath: String): SemanticSet<VDB, IMAP, T>
}
```

#### 使用示例

```cangjie
import magic.vdb.*

main() {
    let smap = SemanticMap(vectorDB: InMemoryVectorDatabase())
    smap.put("前往上海", "Plan A")
    smap.put("吃饭", "Plan B")
    smap.put("前往北京", "Plan C")
    smap.put("睡觉", "Plan D")
    let c = smap.search("前往上海", number: 2)
    println(c)
}
```

将向量数据库作为 retriever 添加到 agent 中使用。目前，使用的向量数据库只能作为 `Static` 模式使用。

```cangjie
let agent = FooAgent()
agent.retriever = smap.asRetriever()
```

### 知识图谱
#### MiniRag
基于MiniRag知识图谱的创建和使用，MiniRag使用到向量、kv和图存储，当前实现支持了本地存储。
https://github.com/HKUDS/MiniRAG
#### `实例化`
使用`MiniRagBuilder`来实例化MiniRag对象，用于后续的知识图谱的构建和基于图谱的检索。
实例化MiniRag需要指定ChatModel、Tokenizer、EmbeddingModel
基于当前可用的tokenizer(详见api_reference.md)需要下载对应的tokenizer配置文件
如:
[OpenAI CL100K](https://openaipublic.blob.core.windows.net/encodings/cl100k_base.tiktoken)需要下载cl100k_base.tiktoken文件
[DeepSeek-V3](https://huggingface.co/deepseek-ai/DeepSeek-V3/tree/main)等开源模型需要下载对应的tokenizer.json和tokenizer_config.json文件
其他配置见`MiniRagBuilder`接口文档。
```cangjie
import magic.config.Config
import magic.rag.graph.{MiniRagBuilder, MiniRagConfig, MiniRag}
import magic.model.ollama.OllamaEmbeddingModel
import magic.tokenizer.Cl100kTokenizer
func instantiateMiniRag(): MiniRag {
    Config.env["DEEPSEEK_API_KEY"] = "<your api key>"
    let model = ModelManager.createChatModel("<Chat Model Name>")
    let embed = OllamaEmbeddingModel("<Embedding Model Name>", baseURL: "<Embedding Model URL>")
    let tokenizer = Cl100kTokenizer("<Your TickToken File Location>")
    let config = MiniRagConfig(model, embed, tokenizer)
    MiniRagBuilder(config).build()
}
```
#### `知识图谱构建`
```cangjie
func buildGraph(): Unit {
    let miniRag:MiniRag = instantiateMiniRag()
    let content:String = "<Text Read From File>"
    miniRag.insert(content)
    miniRag.commit()
}
```

#### `知识图谱检索`
```cangjie
func search(query:String): String {
    let miniRag = instantiateMiniRag()
    let retriever = miniRag.asRetriever()
    let response = retriever.search(query)
    response.toPrompt()
}
```

#### 使用示例
[使用示例](../src/examples/mini_rag/main.cj)

---

# Installation

# Install Cangjie Magic

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Install Cangjie Magic](#install-cangjie-magic)
  - [Cangjie 通用版/General Edition](#cangjie-通用版general-edition)
    - [下载/Download Cangjie Magic ](#下载download-cangjie-magic)
    - [引用/Import Cangjie Magic](#引用import-cangjie-magic)
    - [Quick Start](#quick-start)
  - [Cangjie 鸿蒙版/HarmonyOS Edition](#cangjie-鸿蒙版harmonyos-edition)
  - [Other build configuration](#other-build-configuration)
    - [Options](#options)

<!-- /code_chunk_output -->


**⚠️注意**
目前代码仅在 [Cangjie LTS 通用版](https://cangjie-lang.cn/download/1.0.0)（即 1.0.0）和 鸿蒙外发版（即 0.53.18）上能够正确编译执行。如果使用了其他版本的 Cangjie SDK，可能需要直接修改 Cangjie Magic 源代码进行适配。

**⚠️ Note**  
The code currently compiles and runs correctly only on [Cangjie LTS General Edition](https://cangjie-lang.cn/download/1.0.0) (v1.0.0) and **HarmonyOS Release Edition (v0.53.18)**. If you use other versions of the Cangjie SDK, you may need to modify the Cangjie Magic source code directly to adapt.  

## Cangjie 通用版/General Edition

### 下载/Download Cangjie Magic 

下载仓颉 Magic 源代码。使用 Git 运行以下命令：

Download the source code of Cangjie Magic. Using git, run:

```bash
git clone https://gitcode.com/Cangjie-TPC/CangjieMagic.git -b dev
```

### 引用/Import Cangjie Magic

在依赖 Cangjie Magic 的项目中配置 `cjpm.toml`

Set the `cjpm.toml` of your project that uses Cangjie Magic

```toml
[dependencies]
magic = { path = "<local-path-to-Cangjie-Magic>" }  # 请注意路径字符串中的"\"是否存在转义,若是请全部转换为"\\"以避免路径解析错误
```

注意：如果你开发了命令行程序，必须通过 `cjpm run --name <your-package-name>` 运行你所编写的程序

NOTE: For CLI tools, you **must** execute your program using `cjpm run --name <your-package-name>`.  

📝 在使用本项目时，一般使用如下的 `import` 规则:

📝 When using this project, follow the import conventions below:

```cangjie
import magic.dsl.*
import magic.prelude.*
```

### Quick Start

**步骤** 1️⃣: 运行 `cjpm init --name <package-name>` 创建新项目

**Step** 1️⃣: Run `cjpm init` to create a new project

**步骤** 2️⃣: 将以下代码复制到 `main.cj` 文件

**Step** 2️⃣: Copy the following code to the `main.cj` file

```cangjie
import magic.dsl.*
import magic.prelude.*
import magic.config.Config

@agent[model: "deepseek:deepseek-chat"]
class BlackCatAssistant {
    @prompt(
        "你是黑猫警长的助手"
        "当接到群众通知后，你需要唱起黑猫警长的专属 BGM 并安抚群众情绪"
    )
}

main() {
    Config.env["DEEPSEEK_API_KEY"] = "<your api key>"

    let agent = BlackCatAssistant()
    let result = agent.chat("一只耳来啦")
    println(result)
}
```

**步骤** 3️⃣: 设置 API 密钥，也可更换使用的 LLM 模型

**Step** 3️⃣: Set the API key, and you can also change the LLM to use

**步骤** 4️⃣: 运行 `cjpm run --name <package-name>` 启动程序

**Step** 4️⃣: Run `cjpm run --name <package-name>` to start the program

如果在 MacOS 上执行程序有报错：`stdx` 中的库无法打开（例如 `'...dylib' not valid for use in process: library load disallowed by system policy`），执行以下命令（注意修改所下载的 `stdx` 库路径）：

If you encounter an error when running a program on macOS: a library in `stdx` fails to open (e.g., `'...dylib' not valid for use in process: library load disallowed by system policy`), execute the following command (note to modify the path of the downloaded `stdx` library accordingly)b

```bash
sudo xattr -rd com.apple.quarantine /path/to/stdx/dylib
```

## Cangjie 鸿蒙版/HarmonyOS Edition

**方式** 1️⃣: 直接配置 git 依赖

**Approach** 1️⃣：Configure Git dependency directly

```toml
[dependencies]
    magic = {
        git = "https://gitcode.com/Cangjie-TPC/CangjieMagic.git", 
        tag = "harmony_os_edition"
    }
```

**方式** 2️⃣: 下载 Cangjie Magic 并配置本地源码依赖

**Approach** 2️⃣：Download Cangjie Magic and use a local dependency

- 使用 git，执行

  Using Git, run

```bash
git clone https://gitcode.com/Cangjie-TPC/CangjieMagic.git -b harmony_os_edition
```

- 设置 `cjpm.toml` 文件

  Set the `cjpm.toml` file

```toml
[dependencies]
    magic = { path = "<local-path-to-Cangjie-Magic>" }  # 请注意路径字符串中的"\"是否存在转义,若是请全部转换为"\\"以避免路径解析错误
```

## Other build configuration

### Options

在本项目的 `cjpm.toml` 中提供如下的条件编译选项

The `cjpm.toml` of Cangjie Magic provides the following conditional compilation options:  

| 选项  | 可选值  | 说明 |
|---|---|---|
| `faiss`  | `enable\|disable`  | 是否构建 `faiss` 向量数据库 <br> Whether to build `faiss` vector database support |
| `sqlite`  | `enable\|disable`  | 是否构建支持 `sqlite` 数据库的 RAG 功能 <br> Whether to build SQLite database support for RAG functionality |
| `http`  | `curl\|cj`  | 使用 `curl` 或是仓颉标准库 http 包发送 http 请求 <br> Use `curl` or Cangjie’s standard HTTP library for requests |
| `llamacpp`  | `enable\|disable` | 是否使用 llamacpp，当前不需要启用 <br> Whether to enable llamacpp (currently not required) |

**📌 额外说明/Additional notes**

- 如果构建 `faiss`、`sqlite` 或是 `llamacpp`，需要构建对应的二进制库（详见 [third_party_libs.md](./docs/third_party_libs.md)），添加到目录（例如 `./libs`）并修改 `cjpm.toml`:

  If building `faiss`, `sqlite`, or `llamacpp`, you need to compile the corresponding binary libraries (see [third_party_libs.md](../docs/third_party_libs.md)), place them in a directory (e.g., `./libs`), and modify `cjpm.toml`:  

    ```toml
    [ffi.c]
    sqlite = { path = "./libs/" }
    faiss_c = { path = "./libs/" }
    ```

- 如果使用 `curl` 发送 http 请求需要自行安装

  If using `curl` for HTTP requests, install it separately



---

# API Reference

# API Reference

- 📁 [agent](./package_docs/agent.md)
- 📁 [agent_executor](./package_docs/agent_executor.md)
- 📁 [agent_executor.common](./package_docs/agent_executor.common.md)
- 📁 [agent_executor.naive](./package_docs/agent_executor.naive.md)
- 📁 [agent_executor.react](./package_docs/agent_executor.react.md)
- 📁 [agent_executor.tool_loop](./package_docs/agent_executor.tool_loop.md)
- 📁 [agent_group](./package_docs/agent_group.md)
- 📁 [config](./package_docs/config.md)
- 📁 [core.agent](./package_docs/core.agent.md)
- 📁 [core.memory](./package_docs/core.memory.md)
- 📁 [core.message](./package_docs/core.message.md)
- 📁 [core.model](./package_docs/core.model.md)
- 📁 [core.rag](./package_docs/core.rag.md)
- 📁 [core.tokenizer](./package_docs/core.tokenizer.md)
- 📁 [core.tool](./package_docs/core.tool.md)
- 📁 [instrumentor](./package_docs/instrumentor.md)
- 📁 [jsonable](./package_docs/jsonable.md)
- 📁 [log](./package_docs/log.md)
- 📁 [mcp](./package_docs/mcp.md)
- 📁 [memory](./package_docs/memory.md)
- 📁 [model](./package_docs/model.md)
- 📁 [parser](./package_docs/parser.md)
- 📁 [rag](./package_docs/rag.md)
- 📁 [rag.splitter](./package_docs/rag.splitter.md)
- 📁 [storage](./package_docs/storage.md)
- 📁 [storage.graph](./package_docs/storage.graph.md)
- 📁 [storage.kv](./package_docs/storage.kv.md)
- 📁 [storage.vdb](./package_docs/storage.vdb.md)
- 📁 [tokenizer](./package_docs/tokenizer.md)
- 📁 [tool](./package_docs/tool.md)
- 📁 [vdb](./package_docs/vdb.md)




---

# Package Documentation

## Package agent
- [Package agent](#package-agent)
  - [class AgentExecutionInfo](#class-agentexecutioninfo)
    - [func addMessage](#func-addmessage)
    - [func addMessages](#func-addmessages)
    - [func addQuestion](#func-addquestion)
    - [func addStepMessage](#func-addstepmessage)
    - [prop chatRound](#prop-chatround)
    - [func init](#func-init)
    - [prop messages](#prop-messages)
    - [func removeLastMessage](#func-removelastmessage)
    - [prop retrievalInfo](#prop-retrievalinfo)
    - [func setAnswer](#func-setanswer)
    - [prop verboseInfo](#prop-verboseinfo)
  - [class BaseAgent](#class-baseagent)
    - [prop description](#prop-description)
    - [prop executor](#prop-executor)
    - [func init](#func-init-1)
    - [prop interceptor](#prop-interceptor)
    - [prop memory](#prop-memory)
    - [prop model](#prop-model)
    - [prop name](#prop-name)
    - [prop retriever](#prop-retriever)
    - [prop systemPrompt](#prop-systemprompt)
    - [prop temperature](#prop-temperature)
    - [prop toolManager](#prop-toolmanager)
  - [class ConversationAgent](#class-conversationagent)
    - [func asyncChat](#func-asyncchat)
    - [func chat](#func-chat)
    - [func init](#func-init-1)
  - [class DispatchAgent](#class-dispatchagent)
    - [func asyncChat](#func-asyncchat-1)
    - [func chat](#func-chat-1)
    - [func init](#func-init-1)
  - [class GroupAsAgent](#class-groupasagent)
    - [func asyncChat](#func-asyncchat-1)
    - [func chat](#func-chat-1)
    - [func init](#func-init-1)
  - [class HumanAgent](#class-humanagent)
    - [func chat](#func-chat-1)
    - [func init](#func-init-1)
  - [class ToolAgent<T>](#class-toolagent<t>)
    - [func chat](#func-chat-1)
    - [func init](#func-init-1)
  - [class ToolSelectAgent](#class-toolselectagent)
    - [func chat](#func-chat-1)
    - [func init](#func-init-1)
    - [func select](#func-select)

### class AgentExecutionInfo
#### func addMessage
```
public func addMessage(msg: Message): Unit
```
- Description: Adds a message to the message list
- Parameters:
  - `msg`: `Message`, The message to add

#### func addMessages
```
public func addMessages(msgs: Array<Message>): Unit
```
- Description: Adds multiple messages to the message list
- Parameters:
  - `msgs`: `Array<Message>`, The messages to add

#### func addQuestion
```
public func addQuestion(question: String): Unit
```
- Description: Adds a question to the message list
- Parameters:
  - `question`: `String`, The question to add

#### func addStepMessage
```
public func addStepMessage(msg: Message): Unit
```
- Description: Adds a message to both the message list and step messages
- Parameters:
  - `msg`: `Message`, The message to add

#### prop chatRound
```
override public prop chatRound: ChatRound
```
- Description: Gets the chat round information

#### func init
```
public init(agent: Agent)
```
- Description: Initializes the AgentExecutionInfo with the given agent
- Parameters:
  - `agent`: `Agent`, The agent to initialize with

#### prop messages
```
override public prop messages: MessageList
```
- Description: Gets the message list

#### func removeLastMessage
```
public func removeLastMessage(): Unit
```
- Description: Removes the last message from the message list

#### prop retrievalInfo
```
override public prop retrievalInfo: ArrayList<RetrievalInfo>
```
- Description: Bookkeeping information during the agent execution

#### func setAnswer
```
override public func setAnswer(answer: String): Unit
```
- Description: Sets the answer
- Parameters:
  - `answer`: `String`, The answer to set

#### prop verboseInfo
```
override public prop verboseInfo: Iterator<String>
```
- Description: Gets verbose information, only accessible when verbose is set to true in AgentRequest


### class BaseAgent
#### prop description
```
prop description: String
```
- Description: Gets the description of the agent

#### prop executor
```
prop executor: AgentExecutor
```
- Description: Gets or sets the executor for the agent

#### func init
```
init(model: ChatModel, name: String = "Base Agent", description: String = "", temperature: Option<Float64> = None, systemPrompt: String = "", toolManager: ToolManager = SimpleToolManager(), executor: Option<AgentExecutor> = None, retriever: Option<Retriever> = None, memory: Option<Memory> = None, interceptor: Option<Interceptor> = None)
```
- Description: Constructor for BaseAgent class
- Parameters:
  - `model`: `ChatModel`, The chat model to be used by the agent
  - `name`: `String`, The name of the agent, defaults to "Base Agent"
  - `description`: `String`, Description of the agent, defaults to empty string
  - `temperature`: `Option<Float64>`, Temperature parameter for the agent, defaults to None
  - `systemPrompt`: `String`, System prompt for the agent, defaults to empty string
  - `toolManager`: `ToolManager`, Tool manager for the agent, defaults to SimpleToolManager
  - `executor`: `Option<AgentExecutor>`, Executor for the agent, defaults to None
  - `retriever`: `Option<Retriever>`, Retriever for the agent, defaults to None
  - `memory`: `Option<Memory>`, Memory for the agent, defaults to None
  - `interceptor`: `Option<Interceptor>`, Interceptor for the agent, defaults to None

#### prop interceptor
```
prop interceptor: Option<Interceptor>
```
- Description: Gets or sets the interceptor for the agent

#### prop memory
```
prop memory: Option<Memory>
```
- Description: Gets or sets the memory for the agent

#### prop model
```
prop model: ChatModel
```
- Description: Gets or sets the chat model for the agent

#### prop name
```
prop name: String
```
- Description: Gets the name of the agent

#### prop retriever
```
prop retriever: Option<Retriever>
```
- Description: Gets or sets the retriever for the agent

#### prop systemPrompt
```
prop systemPrompt: String
```
- Description: Gets or sets the system prompt for the agent

#### prop temperature
```
prop temperature: Option<Float64>
```
- Description: Gets or sets the temperature parameter for the agent

#### prop toolManager
```
prop toolManager: ToolManager
```
- Description: Gets the tool manager for the agent


### class ConversationAgent
#### func asyncChat
```
func asyncChat(request: AgentRequest): AsyncAgentResponse
```
- Description: Processes an asynchronous chat request, wraps the response, and returns it.
- Parameters:
  - `request`: `AgentRequest`, The asynchronous chat request to be processed.

#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Processes a chat request, saves the conversation, and returns the response.
- Parameters:
  - `request`: `AgentRequest`, The chat request to be processed.

#### func init
```
init(agent: Agent)
```
- Description: Initializes a new ConversationAgent with the given agent.
- Parameters:
  - `agent`: `Agent`, The agent to be wrapped as a conversation agent.


### class DispatchAgent
#### func asyncChat
```
func asyncChat(request: AgentRequest): AsyncAgentResponse
```
- Description: Processes the chat request asynchronously and dispatches it to the appropriate agent.
- Parameters:
  - `request`: `AgentRequest`, The request containing the user's question.

#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Processes the chat request and dispatches it to the appropriate agent.
- Parameters:
  - `request`: `AgentRequest`, The request containing the user's question.

#### func init
```
init(model: String)
```
- Description: Initializes the DispatchAgent with the specified model.
- Parameters:
  - `model`: `String`, The model to be used by the DispatchAgent.


### class GroupAsAgent
#### func asyncChat
```
func asyncChat(request: AgentRequest): AsyncAgentResponse
```
- Description: Dispatches the chat request asynchronously to the group and returns the response.
- Parameters:
  - `request`: `AgentRequest`, The chat request to be dispatched asynchronously.

#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Dispatches the chat request to the group and returns the response.
- Parameters:
  - `request`: `AgentRequest`, The chat request to be dispatched.

#### func init
```
init(group: AgentGroup, description!: String)
```
- Description: Initializes the GroupAsAgent with a group and description.
- Parameters:
  - `group`: `AgentGroup`, The group of agents to dispatch the question to.
  - `description`: `String`, The description of the agent.


### class HumanAgent
#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Processes the chat request by delegating the question to the configured question-answer function and returns the response.
- Parameters:
  - `request`: `AgentRequest`, The request containing the question to be answered.

#### func init
```
init(qaFunc!: Option<(String) -> String> = None)
```
- Description: Initializes the HumanAgent with an optional question-answer function. If not provided, defaults to a console UI.
- Parameters:
  - `qaFunc!`: `Option<(String) -> String>`, An optional function that takes a string question and returns a string answer.


### class ToolAgent<T>
#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Processes the agent request by executing the provided function and returns an agent response.
- Parameters:
  - `request`: `AgentRequest`, The request containing the question to be processed by the agent.

#### func init
```
init(fn!: (String) -> T)
```
- Description: Initializes the ToolAgent with a function that takes a String and returns a generic type T.
- Parameters:
  - `fn!`: `(String) -> T`, A function that processes a String input and returns a generic type T.


### class ToolSelectAgent
#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Processes the agent request and returns a response.
- Parameters:
  - `request`: `AgentRequest`, The request to be processed by the agent.

#### func init
```
init(model: ChatModel, tools: Array<Tool>)
```
- Description: Initializes the ToolSelectAgent with a chat model and a list of tools.
- Parameters:
  - `model`: `ChatModel`, The chat model to be used by the agent.
  - `tools`: `Array<Tool>`, A list of tools available for selection.

#### func select
```
func select(question: String): Option<ToolRequest>
```
- Description: Selects a proper tool for the given question.
- Parameters:
  - `question`: `String`, The question for which a tool needs to be selected.


## Package agent_executor
- [Package agent_executor](#package-agent_executor)
  - [struct AgentExecutorManager](#struct-agentexecutormanager)
    - [func create](#func-create)
    - [func register](#func-register)
    - [func register](#func-register-1)

### struct AgentExecutorManager
#### func create
```
public static func create(name: String): AgentExecutor
```
- Description: Creates an agent executor based on the provided name.
- Parameters:
  - `name`: `String`, The name of the executor to create.

#### func register
```
public static func register(name: String, buildFn: () -> AgentExecutor): Unit
```
- Description: Registers a new agent executor builder with a specific name and a build function.
- Parameters:
  - `name`: `String`, The name of the executor to register.
  - `buildFn`: `() -> AgentExecutor`, A function that builds the executor.

#### func register
```
public static func register(checkFn: (String) -> Bool, buildFn: (String) -> AgentExecutor): Unit
```
- Description: Registers a new agent executor builder with a check function and a build function.
- Parameters:
  - `checkFn`: `(String) -> Bool`, A function that checks if the executor name matches.
  - `buildFn`: `(String) -> AgentExecutor`, A function that builds the executor.


## Package agent_executor.common
- [Package agent_executor.common](#package-agent_executor.common)
  - [class ConsolePrinter](#class-consoleprinter)
    - [func dump](#func-dump)
    - [func init](#func-init)
    - [func init](#func-init-1)
    - [func print](#func-print)

### class ConsolePrinter
#### func dump
```
dump(): Unit
```
- Description: Starts the dumping process of verbose information.

#### func init
```
init(chunks: Iterator<String>)
```
- Description: Constructor that initializes the ConsolePrinter with an iterator of strings.
- Parameters:
  - `chunks`: `Iterator<String>`, An iterator providing chunks of strings to be printed.

#### func init
```
init(asyncResponse: AsyncAgentResponse)
```
- Description: Constructor that initializes the ConsolePrinter with an asynchronous agent response.
- Parameters:
  - `asyncResponse`: `AsyncAgentResponse`, An asynchronous response containing verbose information for debugging.

#### func print
```
print(asyncResponse: AsyncAgentResponse, verbose: Bool = false): Unit
```
- Description: Prints the asynchronous response data, optionally including verbose debugging information.
- Parameters:
  - `asyncResponse`: `AsyncAgentResponse`, The asynchronous response to be printed.
  - `verbose`: `Bool`, If true, includes verbose debugging information in the output.


## Package agent_executor.naive
- [Package agent_executor.naive](#package-agent_executor.naive)
  - [class NaiveExecutor](#class-naiveexecutor)
    - [func asyncRun](#func-asyncrun)
    - [prop name](#prop-name)
    - [func run](#func-run)

### class NaiveExecutor
#### func asyncRun
```
public override func asyncRun(agent: Agent, request: AgentRequest): AsyncAgentResponse
```
- Description: Executes the agent's task asynchronously.
- Parameters:
  - `agent`: `Agent`, The agent to be executed.
  - `request`: `AgentRequest`, The request containing the task details.

#### prop name
```
override public prop name: String
```
- Description: Gets the name of the executor.

#### func run
```
public override func run(agent: Agent, request: AgentRequest): AgentResponse
```
- Description: Executes the agent's task synchronously.
- Parameters:
  - `agent`: `Agent`, The agent to be executed.
  - `request`: `AgentRequest`, The request containing the task details.


## Package agent_executor.react
- [Package agent_executor.react](#package-agent_executor.react)
  - [class ReactExecutor](#class-reactexecutor)
    - [func asyncRun](#func-asyncrun)
    - [prop name](#prop-name)
    - [func run](#func-run)

### class ReactExecutor
#### func asyncRun
```
override public func asyncRun(agent: Agent, request: AgentRequest): AsyncAgentResponse
```
- Description: Executes the agent's task in an asynchronous manner.
- Parameters:
  - `agent`: `Agent`, The agent to be executed.
  - `request`: `AgentRequest`, The request containing the task details.

#### prop name
```
override public prop name: String
```
- Description: Gets the name of the executor.

#### func run
```
override public func run(agent: Agent, request: AgentRequest): AgentResponse
```
- Description: Executes the agent's task in a synchronous manner.
- Parameters:
  - `agent`: `Agent`, The agent to be executed.
  - `request`: `AgentRequest`, The request containing the task details.


## Package agent_executor.tool_loop
- [Package agent_executor.tool_loop](#package-agent_executor.tool_loop)
  - [class ToolLoopExecutor](#class-toolloopexecutor)
    - [func asyncRun](#func-asyncrun)
    - [prop name](#prop-name)
    - [func run](#func-run)

### class ToolLoopExecutor
#### func asyncRun
```
func asyncRun(agent: Agent, request: AgentRequest): AsyncAgentResponse
```
- Description: Executes the agent's task asynchronously and returns a future response.
- Parameters:
  - `agent`: `Agent`, The agent to be executed.
  - `request`: `AgentRequest`, The request containing the task details.

#### prop name
```
prop name: String
```
- Description: Returns the name of the executor as 'tool-loop'.

#### func run
```
func run(agent: Agent, request: AgentRequest): AgentResponse
```
- Description: Executes the agent's task synchronously and returns the response.
- Parameters:
  - `agent`: `Agent`, The agent to be executed.
  - `request`: `AgentRequest`, The request containing the task details.


## Package agent_group
- [Package agent_group](#package-agent_group)
  - [interface AgentCollaboration](#interface-agentcollaboration)
    - [func ()](#func-())
    - [func ()](#func-()-1)
    - [func <=](#func-<=)
    - [func |](#func-|)
  - [class FreeGroup](#class-freegroup)
    - [func chat](#func-chat)
    - [func chat](#func-chat-1)
    - [func discuss](#func-discuss)
    - [func init](#func-init)
    - [func operator []](#func-operator-[])
    - [func operator |](#func-operator-|)
  - [enum FreeGroupMode](#enum-freegroupmode)
    - [enumeration Auto](#enumeration-auto)
    - [enumeration RoundRobin](#enumeration-roundrobin)
  - [class LeaderGroup](#class-leadergroup)
    - [func asyncChat](#func-asyncchat)
    - [func chat](#func-chat-1)
    - [func chat](#func-chat-1)
    - [func operator []](#func-operator-[]-1)
  - [class LinearGroup](#class-lineargroup)
    - [func asyncChat](#func-asyncchat-1)
    - [func chat](#func-chat-1)
    - [func chat](#func-chat-1)
    - [func operator []](#func-operator-[]-1)

### interface AgentCollaboration
#### func operator ()
```
operator func ()(prev: Agent): LinearGroup
```
- Description: Creates a LinearGroup from a single agent.
- Parameters:
  - `prev`: `Agent`, The agent to start the linear group.

#### func operator ()
```
operator func ()(prev: LinearGroup): LinearGroup
```
- Description: Extends an existing LinearGroup.
- Parameters:
  - `prev`: `LinearGroup`, The existing linear group to extend.

#### func operator <=
```
operator func <=(members: Array<Agent>): LeaderGroup
```
- Description: Creates a LeaderGroup from an array of agents.
- Parameters:
  - `members`: `Array<Agent>`, An array of agents to form the group.

#### func operator |
```
operator func |(member: Agent): FreeGroup
```
- Description: Creates a FreeGroup with a single agent.
- Parameters:
  - `member`: `Agent`, The agent to include in the free group.


### class FreeGroup
#### func chat
```
chat(request: AgentRequest): AgentResponse
```
- Description: Processes a chat request with default maximum rounds
- Parameters:
  - `request`: `AgentRequest`, The chat request to process

#### func chat
```
chat(request: AgentRequest, maxRound: Int64): AgentResponse
```
- Description: Processes a chat request with specified maximum rounds
- Parameters:
  - `request`: `AgentRequest`, The chat request to process
  - `maxRound`: `Int64`, Maximum number of discussion rounds

#### func discuss
```
discuss(topic: String, initiator: String, speech: String, mode: FreeGroupMode = FreeGroupMode.Auto, maxRound: Int64 = DISCUSSION_MAX_ROUND): String
```
- Description: Initiates a discussion with specified parameters and mode
- Parameters:
  - `topic`: `String`, Topic of the discussion
  - `initiator`: `String`, Name of the initiator
  - `speech`: `String`, Initial speech content
  - `mode`: `FreeGroupMode`, Mode of discussion (Auto or RoundRobin)
  - `maxRound`: `Int64`, Maximum number of discussion rounds

#### func init
```
init(a: Agent, b: Agent)
```
- Description: Initializes a FreeGroup with two agents
- Parameters:
  - `a`: `Agent`, First agent to add to the group
  - `b`: `Agent`, Second agent to add to the group

#### func operator operator []
```
operator [](memberName: String): Agent
```
- Description: Accesses an agent member by name
- Parameters:
  - `memberName`: `String`, Name of the agent to access

#### func operator operator |
```
operator |(member: Agent): FreeGroup
```
- Description: Adds a new member to the group
- Parameters:
  - `member`: `Agent`, Agent to add to the group


### enum FreeGroupMode
####  Auto
```
Auto
```
- Description: The speaker will be selected by LLM automatically

####  RoundRobin
```
RoundRobin
```
- Description: 


### class LeaderGroup
#### func asyncChat
```
func asyncChat(request: AgentRequest): AsyncAgentResponse
```
- Description: Processes a chat request asynchronously and returns an asynchronous agent response.
- Parameters:
  - `request`: `AgentRequest`, The chat request to be processed asynchronously.

#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Processes a chat request and returns an agent response.
- Parameters:
  - `request`: `AgentRequest`, The chat request to be processed.

#### func chat
```
func chat(request: AgentRequest, maxRound: Int64): AgentResponse
```
- Description: Processes a chat request with a specified maximum number of rounds and returns an agent response.
- Parameters:
  - `request`: `AgentRequest`, The chat request to be processed.
  - `maxRound`: `Int64`, The maximum number of rounds for the chat.

#### func operator operator []
```
operator func [](memberName: String): Agent
```
- Description: Retrieves an agent member by name.
- Parameters:
  - `memberName`: `String`, The name of the agent member to retrieve.


### class LinearGroup
#### func asyncChat
```
func asyncChat(request: AgentRequest): AsyncAgentResponse
```
- Description: Processes a chat request asynchronously through all agents in the group sequentially.
- Parameters:
  - `request`: `AgentRequest`, The initial request to be processed by the agent group.

#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Processes a chat request through all agents in the group sequentially.
- Parameters:
  - `request`: `AgentRequest`, The initial request to be processed by the agent group.

#### func chat
```
func chat(request: AgentRequest, maxRound: Int64): AgentResponse
```
- Description: Processes a chat request through all agents in the group sequentially with a specified maximum number of rounds.
- Parameters:
  - `request`: `AgentRequest`, The initial request to be processed by the agent group.
  - `maxRound`: `Int64`, The maximum number of rounds for processing the request.

#### func operator operator []
```
operator func [](memberName: String): Agent
```
- Description: Throws an UnsupportedException when trying to access an agent by name.
- Parameters:
  - `memberName`: `String`, The name of the agent to access.


## Package config
- [Package config](#package-config)
  - [class Config](#class-config)
    - [var agentLogDir](#var-agentlogdir)
    - [var codeInterpreterDir](#var-codeinterpreterdir)
    - [var defaultChatModel](#var-defaultchatmodel)
    - [var defaultContextLen](#var-defaultcontextlen)
    - [var defaultEmbeddingModel](#var-defaultembeddingmodel)
    - [var defaultTokenizer](#var-defaulttokenizer)
    - [var enableAgentLog](#var-enableagentlog)
    - [let env](#let-env)
    - [var filterThink](#var-filterthink)
    - [var httpConnectTimeout](#var-httpconnecttimeout)
    - [var httpReadTimeout](#var-httpreadtimeout)
    - [var logFile](#var-logfile)
    - [var logLevel](#var-loglevel)
    - [var maxReactNumber](#var-maxreactnumber)
    - [var modelRequestDir](#var-modelrequestdir)
    - [var modelRetryNumber](#var-modelretrynumber)
    - [var outputRepairRetryNumber](#var-outputrepairretrynumber)
    - [prop resourceDir](#prop-resourcedir)
    - [var saveCodeInterpreter](#var-savecodeinterpreter)
    - [var saveModelRequest](#var-savemodelrequest)
  - [struct EnvWrapper](#struct-envwrapper)
    - [func operator []](#func-operator-[])
    - [func operator []](#func-operator-[]-1)

### class Config
#### var agentLogDir
```
static var agentLogDir = "./logs/agent-logs"
```
- Description: Directory used to save agent logs.

#### var codeInterpreterDir
```
static var codeInterpreterDir = "./logs/code-interpreter-scripts"
```
- Description: Directory used to save scripts generated by code interpreter tools.

#### var defaultChatModel
```
static var defaultChatModel = Option<ChatModel>.None
```
- Description: Default chat model.

#### var defaultContextLen
```
static var defaultContextLen = 32000
```
- Description: Default context length.

#### var defaultEmbeddingModel
```
static var defaultEmbeddingModel = Option<EmbeddingModel>.None
```
- Description: Default embedding model.

#### var defaultTokenizer
```
static var defaultTokenizer = Option<Tokenizer>.None
```
- Description: Default tokenizer.

#### var enableAgentLog
```
static var enableAgentLog = false
```
- Description: Whether to enable agent log. If enabled, agent logs will be saved to the separate files.

#### let env
```
static let env = EnvWrapper()
```
- Description: Provide a way to easily get/set environment variables.

#### var filterThink
```
static var filterThink = false
```
- Description: Whether filter <think> messages generated by reasoning LLMs. Only takes effect under synchronous call.

#### var httpConnectTimeout
```
static var httpConnectTimeout = 60000
```
- Description: The max connection timeout in http requests. MS.

#### var httpReadTimeout
```
static var httpReadTimeout = 60000
```
- Description: The max read timeout in http requests. MS.

#### var logFile
```
static var logFile: String = "stderr"
```
- Description: File used to save logs. If set to "stderr", logs will be printed to standard error. If set to a file path, logs will be saved to that file.

#### var logLevel
```
static var logLevel = LogLevel.ERROR
```
- Description: The logging level for the application.

#### var maxReactNumber
```
static var maxReactNumber = 10
```
- Description: The max number of react execution steps.

#### var modelRequestDir
```
static var modelRequestDir = "./logs/model-requests"
```
- Description: Directory used to save model requests.

#### var modelRetryNumber
```
static var modelRetryNumber = 3
```
- Description: The max retry number when failing to valid get LLM responses.

#### var outputRepairRetryNumber
```
static var outputRepairRetryNumber = 3
```
- Description: The max retry number when failing to generate outputs of required json schema.

#### prop resourceDir
```
static mut prop resourceDir: String
```
- Description: Resource directory for the application. Throws an exception if not set.

#### var saveCodeInterpreter
```
static var saveCodeInterpreter = false
```
- Description: Whether to save code interpreter scripts generated by code interpreter tools.

#### var saveModelRequest
```
static var saveModelRequest = false
```
- Description: Whether to save model requests.


### struct EnvWrapper
#### func operator operator []
```
operator func [](name: String): Option<String>
```
- Description: Gets the value of an environment variable by name.
- Parameters:
  - `name`: `String`, The name of the environment variable.

#### func operator operator []
```
operator func [](name: String, value!: String): Unit
```
- Description: Sets the value of an environment variable.
- Parameters:
  - `name`: `String`, The name of the environment variable.
  - `value`: `String`, The value to set for the environment variable.


## Package core.agent
- [Package core.agent](#package-core.agent)
  - [interface Agent](#interface-agent)
    - [func asyncChat](#func-asyncchat)
    - [func chat](#func-chat)
    - [prop description](#prop-description)
    - [prop executor](#prop-executor)
    - [prop interceptor](#prop-interceptor)
    - [prop memory](#prop-memory)
    - [prop model](#prop-model)
    - [prop name](#prop-name)
    - [prop retriever](#prop-retriever)
    - [prop systemPrompt](#prop-systemprompt)
    - [prop temperature](#prop-temperature)
    - [prop toolManager](#prop-toolmanager)
  - [interface AgentExecution](#interface-agentexecution)
    - [prop chatRound](#prop-chatround)
    - [prop messages](#prop-messages)
    - [prop retrievalInfo](#prop-retrievalinfo)
    - [func setAnswer](#func-setanswer)
    - [prop verboseInfo](#prop-verboseinfo)
  - [class AgentExecutionException](#class-agentexecutionexception)
    - [func init](#func-init)
  - [interface AgentExecutor](#interface-agentexecutor)
    - [func asyncRun](#func-asyncrun)
    - [prop name](#prop-name-1)
    - [func run](#func-run)
  - [interface AgentGroup](#interface-agentgroup)
    - [func asyncChat](#func-asyncchat-1)
    - [func chat](#func-chat-1)
    - [func chat](#func-chat-1)
    - [func operator []](#func-operator-[])
  - [class AgentRequest](#class-agentrequest)
    - [let conversation](#let-conversation)
    - [func init](#func-init-1)
    - [let maxTool](#let-maxtool)
    - [let question](#let-question)
    - [let verbose](#let-verbose)
  - [struct AgentResponse](#struct-agentresponse)
    - [let content](#let-content)
    - [prop execution](#prop-execution)
    - [func init](#func-init-1)
    - [func init](#func-init-1)
  - [class AsyncAgentResponse](#class-asyncagentresponse)
    - [prop content](#prop-content)
    - [prop execution](#prop-execution-1)
    - [func init](#func-init-1)
    - [func init](#func-init-1)
    - [func next](#func-next)
  - [class Interceptor](#class-interceptor)
    - [func init](#func-init-1)
  - [enum InterceptorMode](#enum-interceptormode)
    - [enumeration Always](#enumeration-always)
    - [enumeration Conditional](#enumeration-conditional)
    - [enumeration Periodic](#enumeration-periodic)

### interface Agent
#### func asyncChat
```
func asyncChat(request: AgentRequest): AsyncAgentResponse
```
- Description: Query the agent and get the answer. It returns the agent reply in stream
- Parameters:
  - `request`: `AgentRequest`, The request to the agent

#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Query the agent and get the answer. It may throw AgentExecutionException
- Parameters:
  - `request`: `AgentRequest`, The request to the agent

#### prop description
```
prop description: String
```
- Description: Functionality description of the agent

#### prop executor
```
mut prop executor: AgentExecutor
```
- Description: The underlying agent executor

#### prop interceptor
```
mut prop interceptor: Option<Interceptor>
```
- Description: Set the agent interceptor

#### prop memory
```
mut prop memory: Option<Memory>
```
- Description: Memory the agent will use

#### prop model
```
mut prop model: ChatModel
```
- Description: Chat model the agent will use

#### prop name
```
prop name: String
```
- Description: Name of the agent

#### prop retriever
```
mut prop retriever: Option<Retriever>
```
- Description: Retriever the agent can use

#### prop systemPrompt
```
mut prop systemPrompt: String
```
- Description: System prompt of the agent

#### prop temperature
```
mut prop temperature: Option<Float64>
```
- Description: Temperature the agent will pass to the LLM

#### prop toolManager
```
prop toolManager: ToolManager
```
- Description: Tools the agent can use


### interface AgentExecution
#### prop chatRound
```
prop chatRound: ChatRound
```
- Description: The current chat round, including the question, internal assistant execution messages, and the answer

#### prop messages
```
prop messages: MessageList
```
- Description: Complete messages, including system prompts, user questions, internal assistant messages

#### prop retrievalInfo
```
prop retrievalInfo: ArrayList<RetrievalInfo>
```
- Description: RAG info when used

#### func setAnswer
```
func setAnswer(answer: String): Unit
```
- Description: Internally used thought it's public
- Parameters:
  - `answer`: `String`, The answer to set

#### prop verboseInfo
```
prop verboseInfo: Iterator<String>
```
- Description: Only access this field when setting verbose: true in AgentRequest


### class AgentExecutionException
#### func init
```
init(msg: String)
```
- Description: Initializes a new instance of the AgentExecutionException class with a specified error message.
- Parameters:
  - `msg`: `String`, The error message that explains the reason for the exception.


### interface AgentExecutor
#### func asyncRun
```
func asyncRun(agent: Agent, request: AgentRequest): AsyncAgentResponse
```
- Description: Runs the agent asynchronously with the given request and returns a response
- Parameters:
  - `agent`: `Agent`, The agent to be executed
  - `request`: `AgentRequest`, The request to be processed by the agent

#### prop name
```
prop name: String
```
- Description: Name of the executor

#### func run
```
func run(agent: Agent, request: AgentRequest): AgentResponse
```
- Description: Runs the agent with the given request and returns a response
- Parameters:
  - `agent`: `Agent`, The agent to be executed
  - `request`: `AgentRequest`, The request to be processed by the agent


### interface AgentGroup
#### func asyncChat
```
func asyncChat(request: AgentRequest): AsyncAgentResponse
```
- Description: Asynchronously chat with the agent group using a request
- Parameters:
  - `request`: `AgentRequest`, The request to send to the agent group

#### func chat
```
func chat(request: AgentRequest): AgentResponse
```
- Description: Chat with the agent group using a request
- Parameters:
  - `request`: `AgentRequest`, The request to send to the agent group

#### func chat
```
func chat(request: AgentRequest, maxRound!: Int64): AgentResponse
```
- Description: Chat with the agent group using a request and a maximum number of rounds
- Parameters:
  - `request`: `AgentRequest`, The request to send to the agent group
  - `maxRound!`: `Int64`, The maximum number of rounds for the chat

#### func operator operator []
```
operator func [](memberName: String): Agent
```
- Description: Find the agent according to its name
- Parameters:
  - `memberName`: `String`, The name of the agent to find


### class AgentRequest
#### let conversation
```
let conversation: Option<Conversation>
```
- Description: Conversation between the user and agent

#### func init
```
public init(question: String, conversation!: Option<Conversation> = None, verbose!: Bool = false, maxTool!: Int64 = 10)
```
- Description: Constructor for AgentRequest
- Parameters:
  - `question`: `String`, The current user question
  - `conversation`: `Option<Conversation>`, Conversation between the user and agent
  - `verbose`: `Bool`, Dump internal execution information
  - `maxTool`: `Int64`, The maximum number of tools that can be used when enable tool filter

#### let maxTool
```
let maxTool: Int64
```
- Description: The maximum number of tools that can be used when enable tool filter

#### let question
```
let question: String
```
- Description: The current user question

#### let verbose
```
let verbose: Bool
```
- Description: Dump internal execution information


### struct AgentResponse
#### let content
```
let content: String
```
- Description: The execution result

#### prop execution
```
prop execution: AgentExecution
```
- Description: Gets the execution details

#### func init
```
public init(content: String)
```
- Description: Initializes the AgentResponse with content
- Parameters:
  - `content`: `String`, The execution result

#### func init
```
public init(content: String, execution!: AgentExecution)
```
- Description: Initializes the AgentResponse with content and execution details
- Parameters:
  - `content`: `String`, The execution result
  - `execution`: `AgentExecution`, The execution details


### class AsyncAgentResponse
#### prop content
```
public prop content: String
```
- Description: The execution result. This is a synchronous method, which will wait until the executor completes

#### prop execution
```
prop execution: AgentExecution
```
- Description: The asynchronous execution response from an agent executor

#### func init
```
public init(chunks: Iterator<String>)
```
- Description: Constructor for AsyncAgentResponse with chunks
- Parameters:
  - `chunks`: `Iterator<String>`, Iterator of strings representing chunks of data

#### func init
```
public init(chunks: Iterator<String>, execution: AgentExecution)
```
- Description: Constructor for AsyncAgentResponse with chunks and execution
- Parameters:
  - `chunks`: `Iterator<String>`, Iterator of strings representing chunks of data
  - `execution`: `AgentExecution`, Agent execution context

#### func next
```
override public func next(): Option<String>
```
- Description: Gets the next chunk of data


### class Interceptor
#### func init
```
init(agent: Agent, mode: InterceptorMode = InterceptorMode.Always)
```
- Description: Initializes a new Interceptor instance with the specified agent and mode.
- Parameters:
  - `agent`: `Agent`, The agent to be used by the interceptor.
  - `mode`: `InterceptorMode`, The mode in which the interceptor operates. Defaults to InterceptorMode.Always.


### enum InterceptorMode
####  Always
```
Always
```
- Description: Always intercept the request

####  Conditional
```
Conditional((AgentRequest) -> Bool)
```
- Description: Intercept the request when the condition is true
- Parameters:
  - `condition`: `(AgentRequest) -> Bool`, The condition function to determine interception

####  Periodic
```
Periodic(Int64)
```
- Description: Intercept the request periodically
- Parameters:
  - `period`: `Int64`, The interval period for interception


## Package core.memory
- [Package core.memory](#package-core.memory)
  - [interface Memory](#interface-memory)
    - [func search](#func-search)
    - [func update](#func-update)

### interface Memory
#### func search
```
func search(question: String): Array<String>
```
- Description: According to the user question, find related content in the memory
- Parameters:
  - `question`: `String`, The user question to search for in the memory

#### func update
```
func update(segment: String): Unit
```
- Description: Update the memory
- Parameters:
  - `segment`: `String`, The segment to update in the memory


## Package core.message
- [Package core.message](#package-core.message)
  - [struct ChatRound](#struct-chatround)
    - [func toString](#func-tostring)
  - [class Conversation](#class-conversation)
    - [func []](#func-[])
    - [func addChatRound](#func-addchatround)
    - [func addChatRound](#func-addchatround-1)
    - [func clear](#func-clear)
    - [func init](#func-init)
    - [func init](#func-init-1)
    - [func isEmpty](#func-isempty)
    - [func iterator](#func-iterator)
    - [prop size](#prop-size)
  - [class Message](#class-message)
    - [func assistant](#func-assistant)
    - [let content](#let-content)
    - [let image](#let-image)
    - [func init](#func-init-1)
    - [let name](#let-name)
    - [let reason](#let-reason)
    - [let role](#let-role)
    - [func system](#func-system)
    - [func toLogString](#func-tologstring)
    - [func toString](#func-tostring-1)
    - [func user](#func-user)
  - [enum MessageRole](#enum-messagerole)
    - [func !=](#func-!=)
    - [func ==](#func-==)
    - [enumeration Assistant](#enumeration-assistant)
    - [enumeration System](#enumeration-system)
    - [enumeration Unknown](#enumeration-unknown)
    - [enumeration User](#enumeration-user)
    - [func fromStr](#func-fromstr)
    - [func toString](#func-tostring-1)

### struct ChatRound
#### func toString
```
override public func toString(): String
```
- Description: Converts the ChatRound object to a string representation.


### class Conversation
#### func operator []
```
public operator func [](index: Int64): ChatRound
```
- Description: Retrieves the ChatRound at the specified index.
- Parameters:
  - `index`: `Int64`, The index of the ChatRound to retrieve.

#### func addChatRound
```
public func addChatRound(round: ChatRound): Unit
```
- Description: Adds a ChatRound to the Conversation.
- Parameters:
  - `round`: `ChatRound`, The ChatRound to add.

#### func addChatRound
```
public func addChatRound(question: String, answer: String, steps!: MessageList = MessageList()): Unit
```
- Description: Creates and adds a ChatRound to the Conversation with the given question, answer, and optional steps.
- Parameters:
  - `question`: `String`, The question part of the ChatRound.
  - `answer`: `String`, The answer part of the ChatRound.
  - `steps`: `MessageList`, Optional execution step messages.

#### func clear
```
public func clear(): Unit
```
- Description: Removes all ChatRounds from the Conversation.

#### func init
```
public init()
```
- Description: Initializes an empty Conversation.

#### func init
```
public init(round: ChatRound)
```
- Description: Initializes a Conversation with a single ChatRound.
- Parameters:
  - `round`: `ChatRound`, The initial ChatRound to add to the Conversation.

#### func isEmpty
```
public func isEmpty(): Bool
```
- Description: Checks if the Conversation is empty.

#### func iterator
```
override public func iterator(): Iterator<ChatRound>
```
- Description: Returns an iterator over the ChatRounds in the Conversation.

#### prop size
```
public prop size: Int64
```
- Description: Gets the number of ChatRounds in the Conversation.


### class Message
#### func assistant
```
public static func assistant(content: String, name!: String = ""): Message
```
- Description: Creates an assistant message
- Parameters:
  - `content`: `String`, Content of the assistant message
  - `name`: `String`, Name of the assistant

#### let content
```
public let content: String
```
- Description: Content of the message

#### let image
```
public let image: Option<String>
```
- Description: URL or base64 encoded image

#### func init
```
public init(role: MessageRole, content: String, name!: String = "", image!: Option<String> = None, reason!: Option<String> = None)
```
- Description: Initializes a new Message instance
- Parameters:
  - `role`: `MessageRole`, Role of the sender
  - `content`: `String`, Content of the message
  - `name`: `String`, Name of the sender
  - `image`: `Option<String>`, URL or base64 encoded image
  - `reason`: `Option<String>`, Reasoning content generated by a model

#### let name
```
public let name: String
```
- Description: Name of the sender

#### let reason
```
public let reason: Option<String>
```
- Description: Reasoning content generated by a model

#### let role
```
public let role: MessageRole
```
- Description: Role of the sender

#### func system
```
public static func system(content: String): Message
```
- Description: Creates a system message
- Parameters:
  - `content`: `String`, Content of the system message

#### func toLogString
```
public func toLogString(): String
```
- Description: Converts the message to a log-friendly string representation

#### func toString
```
public func toString(): String
```
- Description: Converts the message to a string representation

#### func user
```
public static func user(content: String, image!: Option<String> = None): Message
```
- Description: Creates a user message
- Parameters:
  - `content`: `String`, Content of the user message
  - `image`: `Option<String>`, URL or base64 encoded image


### enum MessageRole
#### func operator !=
```
public operator func !=(other: MessageRole): Bool
```
- Description: Compares two MessageRole instances for inequality
- Parameters:
  - `other`: `MessageRole`, The other MessageRole to compare with

#### func operator ==
```
public operator func ==(other: MessageRole): Bool
```
- Description: Compares two MessageRole instances for equality
- Parameters:
  - `other`: `MessageRole`, The other MessageRole to compare with

####  Assistant
```
Assistant
```
- Description: Represents an assistant message role

####  System
```
System
```
- Description: Represents a system message role

####  Unknown
```
Unknown
```
- Description: Represents an unknown message role

####  User
```
User
```
- Description: Represents a user message role

#### func fromStr
```
public static func fromStr(str: String): MessageRole
```
- Description: Converts a string to the corresponding MessageRole
- Parameters:
  - `str`: `String`, The string representation of the message role

#### func toString
```
func toString(): String
```
- Description: Converts the MessageRole to its string representation


## Package core.model
- [Package core.model](#package-core.model)
  - [struct AsyncChatChunk](#struct-asyncchatchunk)
    - [func toString](#func-tostring)
  - [class AsyncChatResponse](#class-asyncchatresponse)
    - [let chunks](#let-chunks)
    - [func iter](#func-iter)
    - [prop messageList](#prop-messagelist)
    - [let model](#let-model)
    - [func toString](#func-tostring-1)
    - [prop usage](#prop-usage)
  - [interface ChatModel](#interface-chatmodel)
    - [func asyncCreate](#func-asynccreate)
    - [prop contextLength](#prop-contextlength)
    - [func create](#func-create)
  - [class ChatRequest](#class-chatrequest)
    - [func init](#func-init)
    - [func init](#func-init-1)
    - [func init](#func-init-1)
    - [let messageList](#let-messagelist)
    - [let stop](#let-stop)
    - [let temperature](#let-temperature)
    - [func toString](#func-tostring-1)
  - [struct ChatResponse](#struct-chatresponse)
    - [func init](#func-init-1)
    - [let messageList](#let-messagelist-1)
    - [let model](#let-model-1)
    - [func toString](#func-tostring-1)
    - [let usage](#let-usage)
  - [class ChatUsage](#class-chatusage)
    - [let completionTokens](#let-completiontokens)
    - [func init](#func-init-1)
    - [let promptTokens](#let-prompttokens)
    - [let timeCost](#let-timecost)
    - [func toString](#func-tostring-1)
    - [let totalTokens](#let-totaltokens)
  - [interface EmbeddingModel](#interface-embeddingmodel)
    - [func create](#func-create-1)
  - [struct EmbeddingRequest](#struct-embeddingrequest)
    - [let dimensions](#let-dimensions)
    - [func init](#func-init-1)
    - [let prompt](#let-prompt)
  - [struct EmbeddingResponse](#struct-embeddingresponse)
    - [let data](#let-data)
    - [func init](#func-init-1)
    - [func toString](#func-tostring-1)
  - [interface ImageModel](#interface-imagemodel)
    - [func create](#func-create-1)
  - [struct ImageRequest](#struct-imagerequest)
  - [struct ImageResponse](#struct-imageresponse)
  - [interface Model](#interface-model)
    - [prop name](#prop-name)
    - [prop provider](#prop-provider)
  - [class ModelException](#class-modelexception)
    - [func init](#func-init-1)

### struct AsyncChatChunk
#### func toString
```
override public func toString(): String
```
- Description: Converts the AsyncChatChunk object to a string representation.


### class AsyncChatResponse
#### let chunks
```
public let chunks: Iterator<AsyncChatChunk>
```
- Description: An iterator over the chunks of the chat response.

#### func iter
```
public func iter(withReason!: Bool = true): Iterator<String>
```
- Description: Returns an iterator over the chat response strings, optionally including the reason.
- Parameters:
  - `withReason`: `Bool`, Whether to include the reason in the iterator.

#### prop messageList
```
public prop messageList: MessageList
```
- Description: Gets the list of messages from the chat response, waiting for completion if necessary.

#### let model
```
public let model: String
```
- Description: The model used for the chat response.

#### func toString
```
public func toString(): String
```
- Description: Converts the AsyncChatResponse object to a string representation.

#### prop usage
```
public prop usage: Option<ChatUsage>
```
- Description: Gets the usage information of the chat response if it has finished.


### interface ChatModel
#### func asyncCreate
```
func asyncCreate(request: ChatRequest): AsyncChatResponse
```
- Description: Asynchronous API of the chat model
- Parameters:
  - `request`: `ChatRequest`, The chat request

#### prop contextLength
```
prop contextLength: Int64
```
- Description: The context length of the chat model

#### func create
```
func create(request: ChatRequest): ChatResponse
```
- Description: Synchronous API of the chat model
- Parameters:
  - `request`: `ChatRequest`, The chat request


### class ChatRequest
#### func init
```
init(message: String)
```
- Description: Constructor that initializes the chat request with a single user message
- Parameters:
  - `message`: `String`, The user message to initialize the chat request

#### func init
```
init(messages: Array<Message>, temperature!: Option<Float64> = None, stop!: Option<Array<String>> = None)
```
- Description: Constructor that initializes the chat request with an array of messages and optional parameters
- Parameters:
  - `messages`: `Array<Message>`, Array of messages to initialize the chat request
  - `temperature`: `Option<Float64>`, Optional temperature setting for the chat request
  - `stop`: `Option<Array<String>>`, Optional stop conditions for the chat request

#### func init
```
init(messageList: MessageList, temperature!: Option<Float64> = None, stop!: Option<Array<String>> = None)
```
- Description: Constructor that initializes the chat request with a MessageList and optional parameters
- Parameters:
  - `messageList`: `MessageList`, MessageList to initialize the chat request
  - `temperature`: `Option<Float64>`, Optional temperature setting for the chat request
  - `stop`: `Option<Array<String>>`, Optional stop conditions for the chat request

#### let messageList
```
let messageList: MessageList
```
- Description: List of messages in the chat request

#### let stop
```
let stop: Option<Array<String>>
```
- Description: Optional stop conditions for the chat request

#### let temperature
```
let temperature: Option<Float64>
```
- Description: Optional temperature setting for the chat request

#### func toString
```
func toString(): String
```
- Description: Converts the chat request to a string representation


### struct ChatResponse
#### func init
```
init(messageList: MessageList, model: String, usage: Option<ChatUsage> = None)
```
- Description: Initializes a new ChatResponse with the given message list, model, and optional usage statistics.
- Parameters:
  - `messageList`: `MessageList`, List of messages to include in the response.
  - `model`: `String`, The model used for generating the response.
  - `usage`: `Option<ChatUsage>`, Optional usage statistics for the response.

#### let messageList
```
let messageList: MessageList
```
- Description: List of messages in the chat response.

#### let model
```
let model: String
```
- Description: The model used for generating the chat response.

#### func toString
```
func toString(): String
```
- Description: Converts the ChatResponse to a string representation.

#### let usage
```
let usage: Option<ChatUsage>
```
- Description: Usage statistics of the chat response.


### class ChatUsage
#### let completionTokens
```
let completionTokens: Int64
```
- Description: Number of tokens used in the completion

#### func init
```
init(promptTokens: Int64, completionTokens: Int64, totalTokens: Int64, timeCost: Option<Duration>)
```
- Description: Constructor for ChatUsage
- Parameters:
  - `promptTokens`: `Int64`, Number of tokens used in the prompt
  - `completionTokens`: `Int64`, Number of tokens used in the completion
  - `totalTokens`: `Int64`, Total number of tokens used
  - `timeCost`: `Option<Duration>`, Time cost of the operation

#### let promptTokens
```
let promptTokens: Int64
```
- Description: Number of tokens used in the prompt

#### let timeCost
```
let timeCost: Option<Duration>
```
- Description: Time cost of the operation

#### func toString
```
func toString(): String
```
- Description: Converts the ChatUsage object to a string representation

#### let totalTokens
```
let totalTokens: Int64
```
- Description: Total number of tokens used


### interface EmbeddingModel
#### func create
```
func create(request: EmbeddingRequest): EmbeddingResponse
```
- Description: Creates an embedding based on the provided request.
- Parameters:
  - `request`: `EmbeddingRequest`, The request containing the data needed to create an embedding.


### struct EmbeddingRequest
#### let dimensions
```
let dimensions: Option<Int64>
```
- Description: Optional dimensions for the embedding output

#### func init
```
init(prompt: String, dimensions!: Option<Int> = None)
```
- Description: Initializes an EmbeddingRequest with the given prompt and optional dimensions
- Parameters:
  - `prompt`: `String`, The input prompt for generating embeddings
  - `dimensions`: `Option<Int>`, Optional dimensions for the embedding output

#### let prompt
```
let prompt: String
```
- Description: The input prompt for generating embeddings


### struct EmbeddingResponse
#### let data
```
let data: Array<Float64>
```
- Description: An array of floating-point numbers representing the embedding data

#### func init
```
init(data: Array<Float64>)
```
- Description: Initializes the EmbeddingResponse with the given data
- Parameters:
  - `data`: `Array<Float64>`, An array of floating-point numbers representing the embedding data

#### func toString
```
func toString(): String
```
- Description: Converts the embedding data to a string representation


### interface ImageModel
#### func create
```
func create(request: ImageRequest): ImageResponse
```
- Description: Creates an image based on the provided request.
- Parameters:
  - `request`: `ImageRequest`, The request containing details for image creation.


### struct ImageRequest

### struct ImageResponse

### interface Model
#### prop name
```
prop name: String
```
- Description: The model name, e.g., gpt-4o

#### prop provider
```
prop provider: String
```
- Description: The provider name of the model, e.g., openai


### class ModelException
#### func init
```
init(msg: String)
```
- Description: Constructor for ModelException
- Parameters:
  - `msg`: `String`, The error message for the exception


## Package core.rag
- [Package core.rag](#package-core.rag)
  - [class Document](#class-document)
    - [func !=](#func-!=)
    - [func ==](#func-==)
    - [let content](#let-content)
    - [func deserialize](#func-deserialize)
    - [func fromJsonValue](#func-fromjsonvalue)
    - [func getTypeSchema](#func-gettypeschema)
    - [let id](#let-id)
    - [func init](#func-init)
    - [func init](#func-init-1)
    - [let metadata](#let-metadata)
    - [func serialize](#func-serialize)
    - [func toJsonString](#func-tojsonstring)
    - [func toJsonValue](#func-tojsonvalue)
    - [func toPrompt](#func-toprompt)
    - [func toString](#func-tostring)
  - [interface Retrieval](#interface-retrieval)
    - [prop sources](#prop-sources)
  - [struct RetrievalInfo](#struct-retrievalinfo)
  - [interface Retriever](#interface-retriever)
    - [prop description](#prop-description)
    - [prop mode](#prop-mode)
    - [func search](#func-search)
  - [class RetrieverException](#class-retrieverexception)
    - [func init](#func-init-1)
  - [enum RetrieverMode](#enum-retrievermode)
    - [func !=](#func-!=-1)
    - [func ==](#func-==-1)
    - [enumeration Dynamic](#enumeration-dynamic)
    - [enumeration Static](#enumeration-static)

### class Document
#### func operator !=
```
public operator func !=(other: Document): Bool
```
- Description: Checks if two documents are not equal
- Parameters:
  - `other`: `Document`, Document to compare with

#### func operator ==
```
public operator func ==(other: Document): Bool
```
- Description: Checks if two documents are equal
- Parameters:
  - `other`: `Document`, Document to compare with

#### let content
```
public let content: String
```
- Description: Content of the document

#### func deserialize
```
public static func deserialize(dm: DataModel)
```
- Description: Deserializes a document from a data model
- Parameters:
  - `dm`: `DataModel`, Data model to deserialize

#### func fromJsonValue
```
public static func fromJsonValue(json: JsonValue): Document
```
- Description: Creates a document from a JSON value
- Parameters:
  - `json`: `JsonValue`, JSON value to deserialize

#### func getTypeSchema
```
public static func getTypeSchema(): TypeSchema
```
- Description: Returns the type schema of the document

#### let id
```
public let id: String
```
- Description: Unique identifier for the document

#### func init
```
public init(content: String, metadata!: HashMap<String, String> = HashMap())
```
- Description: Initializes a document with content and optional metadata
- Parameters:
  - `content`: `String`, Content of the document
  - `metadata`: `HashMap<String, String>`, Metadata associated with the document

#### func init
```
public init(id: String, content: String, metadata!: HashMap<String, String>)
```
- Description: Initializes a document with id, content, and metadata
- Parameters:
  - `id`: `String`, Unique identifier for the document
  - `content`: `String`, Content of the document
  - `metadata`: `HashMap<String, String>`, Metadata associated with the document

#### let metadata
```
public let metadata: HashMap<String, String>
```
- Description: Metadata associated with the document

#### func serialize
```
public func serialize(): DataModel
```
- Description: Serializes the document to a data model

#### func toJsonString
```
public func toJsonString(): String
```
- Description: Converts the document to a JSON string

#### func toJsonValue
```
public func toJsonValue(): JsonValue
```
- Description: Converts the document to a JSON value

#### func toPrompt
```
public override func toPrompt(): String
```
- Description: Converts the document to a prompt string

#### func toString
```
public override func toString(): String
```
- Description: Converts the document to a string representation


### interface Retrieval
#### prop sources
```
prop sources: Array<Document>
```
- Description: Result of the retriever


### struct RetrievalInfo

### interface Retriever
#### prop description
```
prop description: String
```
- Description: Describe what the retriever will search. Used under the dynamic mode.

#### prop mode
```
mut prop mode: RetrieverMode
```
- Description: The mode of the retriever.

#### func search
```
func search(query: String): Retrieval
```
- Description: Search for a query.
- Parameters:
  - `query`: `String`, The query to search for.


### class RetrieverException
#### func init
```
init(msg: String)
```
- Description: Constructor for RetrieverException
- Parameters:
  - `msg`: `String`, The error message for the exception


### enum RetrieverMode
#### func operator !=
```
operator func !=(other: RetrieverMode): Bool
```
- Description: Compares two RetrieverMode instances for inequality
- Parameters:
  - `other`: `RetrieverMode`, The other RetrieverMode instance to compare with

#### func operator ==
```
operator func ==(other: RetrieverMode): Bool
```
- Description: Compares two RetrieverMode instances for equality
- Parameters:
  - `other`: `RetrieverMode`, The other RetrieverMode instance to compare with

####  Dynamic
```
Dynamic
```
- Description: The retriever will be used during the agent solving the problem

####  Static
```
Static
```
- Description: The retriever will be used to search related content before the agent answer the question


## Package core.tokenizer
- [Package core.tokenizer](#package-core.tokenizer)
  - [interface Tokenizer](#interface-tokenizer)
    - [func countToken](#func-counttoken)
    - [func decode](#func-decode)
    - [func encode](#func-encode)

### interface Tokenizer
#### func countToken
```
func countToken(input: String): Int64
```
- Description: Counts the number of tokens in the given input string.
- Parameters:
  - `input`: `String`, The input string whose tokens are to be counted.

#### func decode
```
func decode(tokens: Array<UInt32>): String
```
- Description: Decodes an array of unsigned 32-bit integers back into a string.
- Parameters:
  - `tokens`: `Array<UInt32>`, The array of tokens to be decoded.

#### func encode
```
func encode(input: String): Array<UInt32>
```
- Description: Encodes a given input string into an array of unsigned 32-bit integers.
- Parameters:
  - `input`: `String`, The input string to be encoded.


## Package core.tool
- [Package core.tool](#package-core.tool)
  - [interface Tool](#interface-tool)
    - [prop description](#prop-description)
    - [prop examples](#prop-examples)
    - [prop extra](#prop-extra)
    - [func invoke](#func-invoke)
    - [prop name](#prop-name)
    - [prop parameters](#prop-parameters)
    - [prop retType](#prop-rettype)
  - [class ToolException](#class-toolexception)
    - [func init](#func-init)
    - [let reason](#let-reason)
  - [interface ToolManager](#interface-toolmanager)
    - [func addTool](#func-addtool)
    - [func addTools](#func-addtools)
    - [func clear](#func-clear)
    - [func delTool](#func-deltool)
    - [prop enableFilter](#prop-enablefilter)
    - [func filterTool](#func-filtertool)
    - [func findTool](#func-findtool)
    - [func getTools](#func-gettools)
  - [struct ToolParameter](#struct-toolparameter)
    - [let description](#let-description)
    - [func init](#func-init-1)
    - [let name](#let-name)
    - [let typeSchema](#let-typeschema)
  - [struct ToolRequest](#struct-toolrequest)
    - [func toString](#func-tostring)
  - [struct ToolResponse](#struct-toolresponse)
    - [let content](#let-content)
    - [func init](#func-init-1)
    - [let isError](#let-iserror)
  - [struct ToolSearchConfig](#struct-toolsearchconfig)

### interface Tool
#### prop description
```
prop description: String
```
- Description: Description of the tool. LLM will choose the tool according to the description

#### prop examples
```
prop examples: Array<String>
```
- Description: Examples of how to call the tool. Optional.

#### prop extra
```
prop extra: HashMap<String, String>
```
- Description: Extra customized attributes

#### func invoke
```
func invoke(args: HashMap<String, JsonValue>): ToolResponse
```
- Description: Arguments and their values are grouped in a hash map
- Parameters:
  - `args`: `HashMap<String, JsonValue>`, Arguments and their values

#### prop name
```
prop name: String
```
- Description: Unique id of a tool

#### prop parameters
```
prop parameters: Array<ToolParameter>
```
- Description: Type schema of tool inputs

#### prop retType
```
prop retType: TypeSchema
```
- Description: Return type of the tool. Not used currently.


### class ToolException
#### func init
```
init(reason: String)
```
- Description: Initializes a new instance of ToolException with the specified reason
- Parameters:
  - `reason`: `String`, The reason for the exception

#### let reason
```
let reason: String
```
- Description: The reason for the exception


### interface ToolManager
#### func addTool
```
func addTool(tool: Tool): Unit
```
- Description: Add a new tool
- Parameters:
  - `tool`: `Tool`, The tool to be added

#### func addTools
```
func addTools(tools: Array<Tool>): Unit
```
- Description: Add new tools
- Parameters:
  - `tools`: `Array<Tool>`, The tools to be added

#### func clear
```
func clear(): Unit
```
- Description: Delete all tools

#### func delTool
```
func delTool(tool: Tool): Unit
```
- Description: Delete a tool if it exists
- Parameters:
  - `tool`: `Tool`, The tool to be deleted

#### prop enableFilter
```
prop enableFilter: Bool
```
- Description: Whether filtering tools is enabled

#### func filterTool
```
func filterTool(question: String, config: ToolSearchConfig): Array<Tool>
```
- Description: Filter related tools to the question
- Parameters:
  - `question`: `String`, The question to filter tools
  - `config`: `ToolSearchConfig`, The configuration for tool search

#### func findTool
```
func findTool(name: String): Option<Tool>
```
- Description: Find a tool according to its name
- Parameters:
  - `name`: `String`, The name of the tool to find

#### func getTools
```
func getTools(): Array<Tool>
```
- Description: Get all tools


### struct ToolParameter
#### let description
```
let description: String
```
- Description: The description of the tool parameter.

#### func init
```
public init(name: String, description: String, typeSchema: TypeSchema)
```
- Description: Initializes a new ToolParameter with the specified name, description, and type schema.
- Parameters:
  - `name`: `String`, The name of the tool parameter.
  - `description`: `String`, The description of the tool parameter.
  - `typeSchema`: `TypeSchema`, The type schema of the tool parameter.

#### let name
```
let name: String
```
- Description: The name of the tool parameter.

#### let typeSchema
```
let typeSchema: TypeSchema
```
- Description: The type schema of the tool parameter.


### struct ToolRequest
#### func toString
```
override public func toString(): String
```
- Description: Converts the ToolRequest object to a string representation.


### struct ToolResponse
#### let content
```
let content: String
```
- Description: Content of the tool response

#### func init
```
init(content: String, isError: Bool = false)
```
- Description: Initializes a ToolResponse with content and error status
- Parameters:
  - `content`: `String`, Content of the tool response
  - `isError`: `Bool`, Indicates if the tool response is an error, defaults to false

#### let isError
```
let isError: Bool
```
- Description: Indicates if the tool response is an error


### struct ToolSearchConfig

## Package instrumentor
- [Package instrumentor](#package-instrumentor)
  - [class Instrumentor](#class-instrumentor)
    - [var AFTER_AGENT_RUN_FN](#var-after_agent_run_fn)
    - [var AFTER_TOOL_CALL_FN](#var-after_tool_call_fn)
    - [var BEFORE_AGENT_RUN_FN](#var-before_agent_run_fn)
    - [var BEFORE_CHAT_MODEL_FN](#var-before_chat_model_fn)
    - [var BEFORE_CHAT_MODEL_FN2](#var-before_chat_model_fn2)
    - [var BEFORE_TOOL_CALL_FN](#var-before_tool_call_fn)
    - [func registerAfterAgentRun](#func-registerafteragentrun)
    - [func registerAfterToolCall](#func-registeraftertoolcall)
    - [func registerBeforeAgentRun](#func-registerbeforeagentrun)
    - [func registerBeforeChatModel](#func-registerbeforechatmodel)
    - [func registerBeforeChatModel](#func-registerbeforechatmodel-1)
    - [func registerBeforeToolCall](#func-registerbeforetoolcall)

### class Instrumentor
#### var AFTER_AGENT_RUN_FN
```
static var AFTER_AGENT_RUN_FN: Option<(Agent, AgentRequest, AgentResponse) -> Option<AgentResponse>>
```
- Description: A static variable that holds a function to be called after agent run.

#### var AFTER_TOOL_CALL_FN
```
static var AFTER_TOOL_CALL_FN: Option<(Agent, ToolRequest, ToolResponse) -> Option<ToolResponse>>
```
- Description: A static variable that holds a function to be called after tool call.

#### var BEFORE_AGENT_RUN_FN
```
static var BEFORE_AGENT_RUN_FN: Option<(Agent, AgentRequest) -> Option<AgentResponse>>
```
- Description: A static variable that holds a function to be called before agent run.

#### var BEFORE_CHAT_MODEL_FN
```
static var BEFORE_CHAT_MODEL_FN: Option<(ChatModel, ChatRequest) -> Option<ChatResponse>>
```
- Description: A static variable that holds a function to be called before chat model processing.

#### var BEFORE_CHAT_MODEL_FN2
```
static var BEFORE_CHAT_MODEL_FN2: Option<(String, ChatModel, ChatRequest) -> Option<ChatResponse>>
```
- Description: A static variable that holds a function to be called before chat model processing, with an additional String parameter.

#### var BEFORE_TOOL_CALL_FN
```
static var BEFORE_TOOL_CALL_FN: Option<(Agent, ToolRequest) -> Option<ToolResponse>>
```
- Description: A static variable that holds a function to be called before tool call.

#### func registerAfterAgentRun
```
static func registerAfterAgentRun(fn: (Agent, AgentRequest, AgentResponse) -> Option<AgentResponse>)
```
- Description: Registers a function to be called after agent run.
- Parameters:
  - `fn`: `(Agent, AgentRequest, AgentResponse) -> Option<AgentResponse>`, The function to register.

#### func registerAfterToolCall
```
static func registerAfterToolCall(fn: (Agent, ToolRequest, ToolResponse) -> Option<ToolResponse>)
```
- Description: Registers a function to be called after tool call.
- Parameters:
  - `fn`: `(Agent, ToolRequest, ToolResponse) -> Option<ToolResponse>`, The function to register.

#### func registerBeforeAgentRun
```
static func registerBeforeAgentRun(fn: (Agent, AgentRequest) -> Option<AgentResponse>)
```
- Description: Registers a function to be called before agent run.
- Parameters:
  - `fn`: `(Agent, AgentRequest) -> Option<AgentResponse>`, The function to register.

#### func registerBeforeChatModel
```
static func registerBeforeChatModel(fn: (ChatModel, ChatRequest) -> Option<ChatResponse>)
```
- Description: Registers a function to be called before chat model processing.
- Parameters:
  - `fn`: `(ChatModel, ChatRequest) -> Option<ChatResponse>`, The function to register.

#### func registerBeforeChatModel
```
static func registerBeforeChatModel(fn: (String, ChatModel, ChatRequest) -> Option<ChatResponse>)
```
- Description: Registers a function to be called before chat model processing, with an additional String parameter.
- Parameters:
  - `fn`: `(String, ChatModel, ChatRequest) -> Option<ChatResponse>`, The function to register.

#### func registerBeforeToolCall
```
static func registerBeforeToolCall(fn: (Agent, ToolRequest) -> Option<ToolResponse>)
```
- Description: Registers a function to be called before tool call.
- Parameters:
  - `fn`: `(Agent, ToolRequest) -> Option<ToolResponse>`, The function to register.


## Package jsonable
- [Package jsonable](#package-jsonable)
  - [struct FieldSchema](#struct-fieldschema)
  - [interface Jsonable](#interface-jsonable)
    - [func fromJsonValue](#func-fromjsonvalue)
    - [func getTypeSchema](#func-gettypeschema)
  - [class JsonableException](#class-jsonableexception)
    - [func init](#func-init)
  - [interface ToJsonValue](#interface-tojsonvalue)
    - [func toJsonValue](#func-tojsonvalue)
  - [enum TypeSchema](#enum-typeschema)
    - [enumeration Arr](#enumeration-arr)
    - [enumeration Boolean](#enumeration-boolean)
    - [enumeration Float](#enumeration-float)
    - [enumeration Int](#enumeration-int)
    - [enumeration Obj](#enumeration-obj)
    - [enumeration Str](#enumeration-str)
    - [func toJsonValue](#func-tojsonvalue-1)
    - [func toString](#func-tostring)

### struct FieldSchema

### interface Jsonable
#### func fromJsonValue
```
static func fromJsonValue(json: JsonValue): T
```
- Description: Deserializes an object of type T from a JsonValue.
- Parameters:
  - `json`: `JsonValue`, The JsonValue to deserialize from.

#### func getTypeSchema
```
static func getTypeSchema(): TypeSchema
```
- Description: Retrieves the type schema of the generic type T.


### class JsonableException
#### func init
```
public init(msg: String)
```
- Description: Constructs a JsonableException with the specified error message.
- Parameters:
  - `msg`: `String`, The error message describing the exception.


### interface ToJsonValue
#### func toJsonValue
```
func toJsonValue(): JsonValue
```
- Description: Converts the implementing object to a JsonValue.


### enum TypeSchema
####  Arr
```
Arr(TypeSchema)
```
- Description: Represents an array type with elements of the specified TypeSchema.
- Parameters:
  - `TypeSchema`: `TypeSchema`, The type schema of the array elements.

####  Boolean
```
Boolean
```
- Description: Represents a boolean type.

####  Float
```
Float
```
- Description: Represents a floating-point type.

####  Int
```
Int
```
- Description: Represents an integer type.

####  Obj
```
Obj(Array<FieldSchema>)
```
- Description: Represents an object type with fields specified by an array of FieldSchema.
- Parameters:
  - `Array<FieldSchema>`: `Array<FieldSchema>`, An array of FieldSchema defining the object's fields.

####  Str
```
Str
```
- Description: Represents a string type.

#### func toJsonValue
```
func toJsonValue(): JsonValue
```
- Description: Converts the TypeSchema to a JsonValue representation.

#### func toString
```
func toString(): String
```
- Description: Converts the TypeSchema to a string representation.


## Package log
- [Package log](#package-log)
  - [struct LogUtils](#struct-logutils)
    - [func debug](#func-debug)
    - [func debug](#func-debug-1)
    - [func error](#func-error)
    - [func error](#func-error-1)
    - [func info](#func-info)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
  - [struct LogUtils](#struct-logutils-1)
    - [func debug](#func-debug-1)
    - [func debug](#func-debug-1)
    - [func debug](#func-debug-1)
    - [func error](#func-error-1)
    - [func error](#func-error-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)
    - [func info](#func-info-1)

### struct LogUtils
#### func debug
```
public static func debug(msg: String): Unit
```
- Description: Logs a debug message.
- Parameters:
  - `msg`: `String`, The debug message to log.

#### func debug
```
public static func debug(name: String, msg: String): Unit
```
- Description: Logs a debug message with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the debug message.
  - `msg`: `String`, The debug message to log.

#### func error
```
public static func error(msg: String): Unit
```
- Description: Logs an error message.
- Parameters:
  - `msg`: `String`, The error message to log.

#### func error
```
public static func error(name: String, msg: String): Unit
```
- Description: Logs an error message with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the error message.
  - `msg`: `String`, The error message to log.

#### func info
```
public static func info(msg: String): Unit
```
- Description: Logs an info message.
- Parameters:
  - `msg`: `String`, The info message to log.

#### func info
```
public static func info(name: String, msg: String): Unit
```
- Description: Logs an info message with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the info message.
  - `msg`: `String`, The info message to log.

#### func info
```
public static func info(msg: Message): Unit
```
- Description: Logs an info message for a chat message.
- Parameters:
  - `msg`: `Message`, The chat message to log.

#### func info
```
public static func info(name: String, msg: Message): Unit
```
- Description: Logs an info message for a chat message with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the info message.
  - `msg`: `Message`, The chat message to log.

#### func info
```
public static func info(history: MessageList): Unit
```
- Description: Logs info messages for a list of chat messages.
- Parameters:
  - `history`: `MessageList`, The list of chat messages to log.

#### func info
```
public static func info(name: String, history: MessageList): Unit
```
- Description: Logs info messages for a list of chat messages with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the info messages.
  - `history`: `MessageList`, The list of chat messages to log.

#### func info
```
public static func info(messages: Array<Message>): Unit
```
- Description: Logs info messages for an array of chat messages.
- Parameters:
  - `messages`: `Array<Message>`, The array of chat messages to log.

#### func info
```
public static func info(name: String, messages: Array<Message>): Unit
```
- Description: Logs info messages for an array of chat messages with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the info messages.
  - `messages`: `Array<Message>`, The array of chat messages to log.


### struct LogUtils
#### func debug
```
public static func debug(msg: String): Unit
```
- Description: Logs a debug message.
- Parameters:
  - `msg`: `String`, The debug message to log.

#### func debug
```
public static func debug(name: String, msg: String): Unit
```
- Description: Logs a debug message with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the debug message.
  - `msg`: `String`, The debug message to log.

#### func debug
```
public static func debug(ex: Exception): Unit
```
- Description: Logs the stack trace of an exception as debug messages.
- Parameters:
  - `ex`: `Exception`, The exception whose stack trace is to be logged.

#### func error
```
public static func error(msg: String): Unit
```
- Description: Logs an error message.
- Parameters:
  - `msg`: `String`, The error message to log.

#### func error
```
public static func error(name: String, msg: String): Unit
```
- Description: Logs an error message with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the error message.
  - `msg`: `String`, The error message to log.

#### func info
```
public static func info(msg: String): Unit
```
- Description: Logs an informational message.
- Parameters:
  - `msg`: `String`, The informational message to log.

#### func info
```
public static func info(name: String, msg: String): Unit
```
- Description: Logs an informational message with a name prefix.
- Parameters:
  - `name`: `String`, The name prefix for the informational message.
  - `msg`: `String`, The informational message to log.

#### func info
```
public static func info(msg: Message): Unit
```
- Description: Logs a chat message as an informational message.
- Parameters:
  - `msg`: `Message`, The chat message to log.

#### func info
```
public static func info(name: String, msg: Message): Unit
```
- Description: Logs a chat message with a name prefix as an informational message.
- Parameters:
  - `name`: `String`, The name prefix for the chat message.
  - `msg`: `Message`, The chat message to log.

#### func info
```
public static func info(history: MessageList): Unit
```
- Description: Logs a list of chat messages as informational messages.
- Parameters:
  - `history`: `MessageList`, The list of chat messages to log.

#### func info
```
public static func info(name: String, history: MessageList): Unit
```
- Description: Logs a list of chat messages with a name prefix as informational messages.
- Parameters:
  - `name`: `String`, The name prefix for the chat messages.
  - `history`: `MessageList`, The list of chat messages to log.

#### func info
```
public static func info(messages: Array<Message>): Unit
```
- Description: Logs an array of chat messages as informational messages.
- Parameters:
  - `messages`: `Array<Message>`, The array of chat messages to log.

#### func info
```
public static func info(name: String, messages: Array<Message>): Unit
```
- Description: Logs an array of chat messages with a name prefix as informational messages.
- Parameters:
  - `name`: `String`, The name prefix for the chat messages.
  - `messages`: `Array<Message>`, The array of chat messages to log.


## Package mcp
- [Package mcp](#package-mcp)
  - [interface MCPClient](#interface-mcpclient)
    - [func callTool](#func-calltool)
    - [func callTool](#func-calltool-1)
    - [func getTools](#func-gettools)
  - [class SseMCPClient](#class-ssemcpclient)
    - [func init](#func-init)
  - [class StdioMCPClient](#class-stdiomcpclient)
    - [func init](#func-init-1)
  - [class StdioMCPServer](#class-stdiomcpserver)
    - [func init](#func-init-1)
    - [func start](#func-start)
    - [func startWith](#func-startwith)
    - [func startWith](#func-startwith-1)
  - [enum ToolCallContent](#enum-toolcallcontent)
    - [enumeration Image](#enumeration-image)
    - [enumeration Text](#enumeration-text)
    - [func fromJsonValue](#func-fromjsonvalue)
    - [func getTypeSchema](#func-gettypeschema)
    - [func getValue](#func-getvalue)
    - [func toJsonValue](#func-tojsonvalue)

### interface MCPClient
#### func callTool
```
func callTool(name: String, args: Array<(String, ToJsonValue)>): ToolResponse
```
- Description: Calls a tool with the specified name and arguments.
- Parameters:
  - `name`: `String`, The name of the tool to call.
  - `args`: `Array<(String, ToJsonValue)>`, The arguments to pass to the tool.

#### func callTool
```
func callTool(name: String, args: Array<(String, JsonValue)>): ToolResponse
```
- Description: Calls a tool with the specified name and arguments.
- Parameters:
  - `name`: `String`, The name of the tool to call.
  - `args`: `Array<(String, JsonValue)>`, The arguments to pass to the tool.

#### func getTools
```
func getTools(): Array<Tool>
```
- Description: Retrieves a list of available tools.


### class SseMCPClient
#### func init
```
init(url: String)
```
- Description: Initializes the SSE MCP client with the provided URL
- Parameters:
  - `url`: `String`, The URL to initialize the client with


### class StdioMCPClient
#### func init
```
init(command: String, args: Array<String>, env: Array<(String, String)> = [])
```
- Description: Initializes the StdioMCPClient with the specified command, arguments, and environment variables.
- Parameters:
  - `command`: `String`, The command to start the MCP server process.
  - `args`: `Array<String>`, The arguments to pass to the MCP server process.
  - `env`: `Array<(String, String)>`, The environment variables for the MCP server process. Defaults to an empty array.


### class StdioMCPServer
#### func init
```
init(tools: Array<Tool>)
```
- Description: Initialize the StdioMCPServer with an array of tools.
- Parameters:
  - `tools`: `Array<Tool>`, An array of tools to initialize the server.

#### func start
```
func start(): Unit
```
- Description: Start the server by initializing it and entering the loop.

#### func startWith
```
static func startWith(agents: Array<Agent>): Unit
```
- Description: Merge all tools of each agent and start a MCP server for these tools.
- Parameters:
  - `agents`: `Array<Agent>`, An array of agents whose tools will be merged.

#### func startWith
```
static func startWith(tools: Array<Tool>): Unit
```
- Description: Start a MCP server for the provided tools.
- Parameters:
  - `tools`: `Array<Tool>`, An array of tools to start the server with.


### enum ToolCallContent
####  Image
```
Image(ImageContent)
```
- Description: Represents an image content in a tool call

####  Text
```
Text(TextContent)
```
- Description: Represents a text content in a tool call

#### func fromJsonValue
```
public static func fromJsonValue(json: JsonValue): ToolCallContent
```
- Description: Converts a JSON value to ToolCallContent
- Parameters:
  - `json`: `JsonValue`, The JSON value to convert

#### func getTypeSchema
```
public static func getTypeSchema(): TypeSchema
```
- Description: Gets the type schema for ToolCallContent

#### func getValue
```
public func getValue(): String
```
- Description: Gets the string value of the tool call content

#### func toJsonValue
```
public func toJsonValue(): JsonValue
```
- Description: Converts ToolCallContent to a JSON value


## Package memory
- [Package memory](#package-memory)
  - [class ShortMemory](#class-shortmemory)
    - [func search](#func-search)
    - [func update](#func-update)

### class ShortMemory
#### func search
```
func search(question: String): Array<String>
```
- Description: According to the user question, find related content in the memory.
- Parameters:
  - `question`: `String`, The user question to search for related content in the memory.

#### func update
```
func update(segment: String): Unit
```
- Description: Add a segment of text to the memory.
- Parameters:
  - `segment`: `String`, The segment of text to be added to the memory.


## Package model
- [Package model](#package-model)
  - [class ModelConfig](#class-modelconfig)
    - [func init](#func-init)
  - [struct ModelManager](#struct-modelmanager)
    - [func createChatModel](#func-createchatmodel)
    - [func createChatModel](#func-createchatmodel-1)
    - [func createEmbeddingModel](#func-createembeddingmodel)
    - [func createEmbeddingModel](#func-createembeddingmodel-1)
    - [func createImageModel](#func-createimagemodel)
    - [func createImageModel](#func-createimagemodel-1)
    - [func registerChatModel](#func-registerchatmodel)
    - [func registerEmbeddingModel](#func-registerembeddingmodel)
    - [func registerImageModel](#func-registerimagemodel)
  - [struct ModelUtils](#struct-modelutils)
    - [func agentMakeChat](#func-agentmakechat)
    - [func makeChat](#func-makechat)
    - [func makeChat](#func-makechat-1)
    - [func makeChatGet](#func-makechatget)

### class ModelConfig
#### func init
```
public init(provider: String, kind: String, name: String, apiKey: String = "", baseURL: String = "", contextLength: ?Int64 = None)
```
- Description: Initializes a new ModelConfig instance with the specified parameters. If apiKey or baseURL are not provided, default values will be used.
- Parameters:
  - `provider`: `String`, The provider name for the model.
  - `kind`: `String`, The kind of the model.
  - `name`: `String`, The name of the model.
  - `apiKey`: `String`, The API key for the model. If not specified, a default key will be used.
  - `baseURL`: `String`, The base URL for the model. If not specified, a default URL will be used.
  - `contextLength`: `?Int64`, The context length for the model. If not specified, a default length will be used.


### struct ModelManager
#### func createChatModel
```
public static func createChatModel(modelName: String, temperature: Option<Float64> = None): ChatModel
```
- Description: Creates a chat model with the specified name and optional temperature.
- Parameters:
  - `modelName`: `String`, The name of the chat model to create.
  - `temperature`: `Option<Float64>`, The temperature parameter for the chat model. If not specified, a default value will be used.

#### func createChatModel
```
public static func createChatModel(modelConfig: ModelConfig, temperature: Option<Float64> = None): ChatModel
```
- Description: Creates a chat model with the specified model configuration and optional temperature.
- Parameters:
  - `modelConfig`: `ModelConfig`, The configuration for the chat model.
  - `temperature`: `Option<Float64>`, The temperature parameter for the chat model. If not specified, a default value will be used.

#### func createEmbeddingModel
```
public static func createEmbeddingModel(modelName: String): EmbeddingModel
```
- Description: Creates an embedding model with the specified name.
- Parameters:
  - `modelName`: `String`, The name of the embedding model to create.

#### func createEmbeddingModel
```
public static func createEmbeddingModel(modelConfig: ModelConfig): EmbeddingModel
```
- Description: Creates an embedding model with the specified model configuration.
- Parameters:
  - `modelConfig`: `ModelConfig`, The configuration for the embedding model.

#### func createImageModel
```
public static func createImageModel(modelName: String): ImageModel
```
- Description: Creates an image model with the specified name.
- Parameters:
  - `modelName`: `String`, The name of the image model to create.

#### func createImageModel
```
public static func createImageModel(modelConfig: ModelConfig): ImageModel
```
- Description: Creates an image model with the specified model configuration.
- Parameters:
  - `modelConfig`: `ModelConfig`, The configuration for the image model.

#### func registerChatModel
```
public static func registerChatModel(modelName: String, buildFn: () -> ChatModel): Unit
```
- Description: Registers a chat model with the specified name and build function.
- Parameters:
  - `modelName`: `String`, The name of the chat model to register.
  - `buildFn`: `() -> ChatModel`, A function that builds the chat model.

#### func registerEmbeddingModel
```
public static func registerEmbeddingModel(modelName: String, buildFn: () -> EmbeddingModel): Unit
```
- Description: Registers an embedding model with the specified name and build function.
- Parameters:
  - `modelName`: `String`, The name of the embedding model to register.
  - `buildFn`: `() -> EmbeddingModel`, A function that builds the embedding model.

#### func registerImageModel
```
public static func registerImageModel(modelName: String, buildFn: () -> ImageModel): Unit
```
- Description: Registers an image model with the specified name and build function.
- Parameters:
  - `modelName`: `String`, The name of the image model to register.
  - `buildFn`: `() -> ImageModel`, A function that builds the image model.

### struct ModelUtils

#### func makeChat
```
public static func makeChat(model: ChatModel, messageList: MessageList, temperature!: Option<Float64> = None, stop!: Option<Array<String>> = None): Option<Message>
```
- Description: Creates a chat message using a chat model and message list with optional temperature and stop parameters.
- Parameters:
  - `model`: `ChatModel`, The chat model to use for generating the message.
  - `messageList`: `MessageList`, The list of messages to use as context.
  - `temperature`: `Option<Float64>`, Optional parameter to control the randomness of the output.
  - `stop`: `Option<Array<String>>`, Optional parameter to specify stop sequences for the chat.

#### func makeChat
```
public static func makeChat(name: String, model: ChatModel, messageList: MessageList, temperature!: Option<Float64> = None, stop!: Option<Array<String>> = None): Option<Message>
```
- Description: Creates a chat message with a specified name using a chat model and message list with optional temperature and stop parameters.
- Parameters:
  - `name`: `String`, The name associated with the chat.
  - `model`: `ChatModel`, The chat model to use for generating the message.
  - `messageList`: `MessageList`, The list of messages to use as context.
  - `temperature`: `Option<Float64>`, Optional parameter to control the randomness of the output.
  - `stop`: `Option<Array<String>>`, Optional parameter to specify stop sequences for the chat.

#### func makeChat
```
public static func makeChat(name: String, model: ChatModel, messages: Array<Message>, temperature!: Option<Float64> = None, stop!: Option<Array<String>> = None): Option<Message>
```
- Description: Creates a chat message with a specified name using a chat model and array of messages with optional temperature and stop parameters.
- Parameters:
  - `name`: `String`, The name associated with the chat.
  - `model`: `ChatModel`, The chat model to use for generating the message.
  - `messages`: `Array<Message>`, The array of messages to use as context.
  - `temperature`: `Option<Float64>`, Optional parameter to control the randomness of the output.
  - `stop`: `Option<Array<String>>`, Optional parameter to specify stop sequences for the chat.

#### func makeChatGet
```
public static func makeChatGet<T>(name: String, model: ChatModel, messages: Array<Message>, getFn!: (Message) -> Option<T>): Option<T>
```
- Description: Creates a chat message and applies a get function to the result, returning an optional value of type T.
- Parameters:
  - `name`: `String`, The name associated with the chat.
  - `model`: `ChatModel`, The chat model to use for generating the message.
  - `messages`: `Array<Message>`, The array of messages to use as context.
  - `getFn`: `(Message) -> Option<T>`, The function to apply to the generated message.


## Package parser
- [Package parser](#package-parser)
  - [struct OutputParserUtils](#struct-outputparserutils)
    - [func extractFirstCode](#func-extractfirstcode)
    - [func extractLastCode](#func-extractlastcode)
    - [func parseToolRequest](#func-parsetoolrequest)
  - [class ParserException](#class-parserexception)
    - [func init](#func-init)
    - [let reason](#let-reason)

### struct OutputParserUtils
#### func extractFirstCode
```
public static func extractFirstCode(str: String, lang: String): Option<String>
```
- Description: Extracts the first code block from a string for a specified language.
- Parameters:
  - `str`: `String`, The input string containing the code blocks.
  - `lang`: `String`, The programming language of the code block to extract.

#### func extractLastCode
```
public static func extractLastCode(str: String, lang: String): Option<String>
```
- Description: Extracts the last code block from a string for a specified language.
- Parameters:
  - `str`: `String`, The input string containing the code blocks.
  - `lang`: `String`, The programming language of the code block to extract.

#### func parseToolRequest
```
public static func parseToolRequest(str: String): ToolRequest
```
- Description: Parses a tool request from a JSON string.
- Parameters:
  - `str`: `String`, The JSON string representing the tool request.


### class ParserException
#### func init
```
init(reason: String)
```
- Description: Initializes a new ParserException with the given reason
- Parameters:
  - `reason`: `String`, The reason for the parser exception

#### let reason
```
let reason: String
```
- Description: The reason for the parser exception


## Package rag
- [Package rag](#package-rag)
  - [struct RetrieverUtils](#struct-retrieverutils)
    - [func createRetriever](#func-createretriever)
    - [func createRetriever](#func-createretriever-1)

### struct RetrieverUtils
#### func createRetriever
```
public static func createRetriever(agent: Agent, source: String, mode: Option<RetrieverMode>, description: Option<String>): Retriever
```
- Description: Creates a retriever based on the specified source and parameters.
- Parameters:
  - `agent`: `Agent`, The agent to be used for the retriever.
  - `source`: `String`, The source of the retriever. Can be a SQLite path, SQLite path with table name, or a Markdown path.
  - `mode`: `Option<RetrieverMode>`, The mode of the retriever. If not specified, defaults to Static.
  - `description`: `Option<String>`, The description of the retriever. If not specified, a default description is used.

#### func createRetriever
```
public static func createRetriever(_agent: Agent, source: Retriever, mode: Option<RetrieverMode>, description: Option<String>): Retriever
```
- Description: Creates a retriever wrapper around an existing retriever.
- Parameters:
  - `_agent`: `Agent`, The agent to be used for the retriever.
  - `source`: `Retriever`, The existing retriever to be wrapped.
  - `mode`: `Option<RetrieverMode>`, The mode of the retriever. If not specified, defaults to Static.
  - `description`: `Option<String>`, The description of the retriever. If not specified, a default description is used.


## Package rag.splitter
- [Package rag.splitter](#package-rag.splitter)
  - [class CharacterTextSplitter](#class-charactertextsplitter)
    - [func split](#func-split)
  - [class DocumentLoader](#class-documentloader)
    - [func load](#func-load)
    - [func loadSplit](#func-loadsplit)
  - [class MarkdownSplitter](#class-markdownsplitter)
    - [func init](#func-init)
    - [func split](#func-split-1)
  - [class RecursiveCharacterTextSplitter](#class-recursivecharactertextsplitter)
    - [func init](#func-init-1)
    - [func split](#func-split-1)
  - [interface Splitter](#interface-splitter)
    - [func split](#func-split-1)

### class CharacterTextSplitter
#### func split
```
public override func split(text: String): Array<Document>
```
- Description: Splits the input text into an array of Document objects based on the specified chunk size and separator.
- Parameters:
  - `text`: `String`, The input text to be split into documents.


### class DocumentLoader
#### func load
```
func load(): Array<Document>
```
- Description: Loads documents from a file path and returns them as an array.

#### func loadSplit
```
func loadSplit(splitter: Splitter): Array<Document>
```
- Description: Loads documents from a file path, splits them using the provided splitter, and returns them as an array.
- Parameters:
  - `splitter`: `Splitter`, The splitter used to divide the document content.


### class MarkdownSplitter
#### func init
```
public init(headersToSplit: Array<(String, String)> = DEFAULT_HEADERS_TO_SPLIT, returnEachLine: Bool = false, stripHeader: Bool = true)
```
- Description: Initializes the MarkdownSplitter with specified headers to split, whether to return each line with associated headers, and whether to strip split headers from the content.
- Parameters:
  - `headersToSplit`: `Array<(String, String)>`, Headers we want to track.
  - `returnEachLine`: `Bool`, Whether to return each line with associated headers.
  - `stripHeader`: `Bool`, Whether to strip split headers from the content of the chunk.

#### func split
```
override public func split(text: String): Array<Document>
```
- Description: Splits the markdown file into an array of documents based on the specified headers.
- Parameters:
  - `text`: `String`, The markdown file to split.


### class RecursiveCharacterTextSplitter
#### func init
```
init(separators!: Array<String> = ["\n\n", "\n", " ", ""], chunkSize!: Int64 = 1024, chunkOverlap!: Int64 = 256, keepSeparator!: Bool = false)
```
- Description: Initializes the RecursiveCharacterTextSplitter with specified separators, chunk size, chunk overlap, and keep separator flag.
- Parameters:
  - `separators`: `Array<String>`, An array of strings used as separators for splitting text. Defaults to ["\n\n", "\n", " ", ""].
  - `chunkSize`: `Int64`, The maximum size of each chunk. Defaults to 1024.
  - `chunkOverlap`: `Int64`, The number of characters that chunks should overlap. Defaults to 256.
  - `keepSeparator`: `Bool`, A flag indicating whether to keep the separator in the split chunks. Defaults to false.

#### func split
```
split(text: String): Array<Document>
```
- Description: Splits the input text into an array of Document objects using the specified separators.
- Parameters:
  - `text`: `String`, The text to be split into chunks.


### interface Splitter
#### func split
```
func split(text: String): Array<Document>
```
- Description: Splits the input text into an array of documents.
- Parameters:
  - `text`: `String`, The text to be split.


## Package storage
- [Package storage](#package-storage)
  - [interface LocalStorage](#interface-localstorage)
    - [func close](#func-close)
    - [prop collection](#prop-collection)
    - [func commit](#func-commit)
    - [func reset](#func-reset)
    - [prop workspace](#prop-workspace)

### interface LocalStorage
#### func close
```
func close(): Unit
```
- Description: Closes the storage connection

#### prop collection
```
prop collection: String
```
- Description: Represents the collection name

#### func commit
```
func commit(): Unit
```
- Description: Commits changes to the storage

#### func reset
```
func reset(): Unit
```
- Description: Resets the storage to its initial state

#### prop workspace
```
prop workspace: String
```
- Description: Represents the workspace path


## Package storage.graph
- [Package storage.graph](#package-storage.graph)
  - [class BaseGraph<V, E>](#class-basegraph<v,-e>)
    - [func clear](#func-clear)
    - [func getAllNodes](#func-getallnodes)
    - [func getEdges](#func-getedges)
    - [func getIncomingEdgesOf](#func-getincomingedgesof)
    - [func getOutgoingEdgesOf](#func-getoutgoingedgesof)
    - [func getVertex](#func-getvertex)
    - [func getVertexTypes](#func-getvertextypes)
    - [func getVertices](#func-getvertices)
    - [func hasEdge](#func-hasedge)
    - [func hasVertex](#func-hasvertex)
    - [func removeEdge](#func-removeedge)
    - [func removeVertex](#func-removevertex)
    - [func upsertEdge](#func-upsertedge)
    - [func upsertVertex](#func-upsertvertex)
  - [class BaseLocalGraphStorage<V, E>](#class-baselocalgraphstorage<v,-e>)
    - [func close](#func-close)
    - [prop collection](#prop-collection)
    - [func commit](#func-commit)
    - [func getAllVertices](#func-getallvertices)
    - [func getEdge](#func-getedge)
    - [func getEdges](#func-getedges-1)
    - [func getIncomingEdgesOf](#func-getincomingedgesof-1)
    - [func getOutgoingEdgesOf](#func-getoutgoingedgesof-1)
    - [func getVertex](#func-getvertex-1)
    - [func getVertexTypes](#func-getvertextypes-1)
    - [func hasEdge](#func-hasedge-1)
    - [func hasVertex](#func-hasvertex-1)
    - [func init](#func-init)
    - [func removeEdge](#func-removeedge-1)
    - [func removeVertex](#func-removevertex-1)
    - [func reset](#func-reset)
    - [func upsertEdge](#func-upsertedge-1)
    - [func upsertVertex](#func-upsertvertex-1)
    - [prop workspace](#prop-workspace)
  - [class Edge<E>](#class-edge<e>)
    - [func !=](#func-!=)
    - [func ==](#func-==)
    - [prop data](#prop-data)
    - [func deserialize](#func-deserialize)
    - [prop eType](#prop-etype)
    - [func fromJson](#func-fromjson)
    - [func hashCode](#func-hashcode)
    - [func init](#func-init-1)
    - [func serialize](#func-serialize)
    - [prop srcId](#prop-srcid)
    - [prop tgtId](#prop-tgtid)
    - [func toJsonString](#func-tojsonstring)
    - [prop uniqueId](#prop-uniqueid)
    - [prop weight](#prop-weight)
  - [interface GraphStorage<V, E>](#interface-graphstorage<v,-e>)
    - [func getAllVertices](#func-getallvertices-1)
    - [func getEdge](#func-getedge-1)
    - [func getEdges](#func-getedges-1)
    - [func getIncomingEdgesOf](#func-getincomingedgesof-1)
    - [func getOutgoingEdgesOf](#func-getoutgoingedgesof-1)
    - [func getVertex](#func-getvertex-1)
    - [func getVertexTypes](#func-getvertextypes-1)
    - [func hasEdge](#func-hasedge-1)
    - [func hasVertex](#func-hasvertex-1)
    - [func removeEdge](#func-removeedge-1)
    - [func removeVertex](#func-removevertex-1)
    - [func upsertEdge](#func-upsertedge-1)
    - [func upsertVertex](#func-upsertvertex-1)
  - [class IllegalEdgeException](#class-illegaledgeexception)
    - [func init](#func-init-1)
  - [interface LocalGraphStorage<V, E>](#interface-localgraphstorage<v,-e>)
  - [class NodeContainer<V, E>](#class-nodecontainer<v,-e>)
    - [func addIncomingEdge](#func-addincomingedge)
    - [func addOutgoingEdge](#func-addoutgoingedge)
    - [prop incoming](#prop-incoming)
    - [prop outgoing](#prop-outgoing)
    - [func removeIncomingEdge](#func-removeincomingedge)
    - [func removeOutgoingEdge](#func-removeoutgoingedge)
    - [prop vertex](#prop-vertex)
  - [class Vertex<V>](#class-vertex<v>)
    - [func !=](#func-!=-1)
    - [func ==](#func-==-1)
    - [prop data](#prop-data-1)
    - [func deserialize](#func-deserialize-1)
    - [func fromJsonString](#func-fromjsonstring)
    - [func hashCode](#func-hashcode-1)
    - [prop id](#prop-id)
    - [func init](#func-init-1)
    - [func serialize](#func-serialize-1)
    - [func toJsonString](#func-tojsonstring-1)
    - [prop vType](#prop-vtype)

### class BaseGraph<V, E>
#### func clear
```
func clear(): Unit
```
- Description: Clears the graph

#### func getAllNodes
```
func getAllNodes(): Array<NodeContainer<V, E>>
```
- Description: Gets all node containers

#### func getEdges
```
func getEdges(srcId: String, tgtId: String): Array<Edge<E>>
```
- Description: Gets edges between two vertices
- Parameters:
  - `srcId`: `String`, The source vertex ID
  - `tgtId`: `String`, The target vertex ID

#### func getIncomingEdgesOf
```
func getIncomingEdgesOf(id: String): Array<Edge<E>>
```
- Description: Gets incoming edges of a vertex
- Parameters:
  - `id`: `String`, The vertex ID

#### func getOutgoingEdgesOf
```
func getOutgoingEdgesOf(id: String): Array<Edge<E>>
```
- Description: Gets outgoing edges of a vertex
- Parameters:
  - `id`: `String`, The vertex ID

#### func getVertex
```
func getVertex(id: String): ?Vertex<V>
```
- Description: Gets a vertex by ID
- Parameters:
  - `id`: `String`, The vertex ID

#### func getVertexTypes
```
func getVertexTypes(): Set<String>
```
- Description: Gets all vertex types

#### func getVertices
```
func getVertices(): Array<Vertex<V>>
```
- Description: Gets all vertices

#### func hasEdge
```
func hasEdge(srcId: String, tgtId: String): Bool
```
- Description: Checks if an edge exists between two vertices
- Parameters:
  - `srcId`: `String`, The source vertex ID
  - `tgtId`: `String`, The target vertex ID

#### func hasVertex
```
func hasVertex(id: String): Bool
```
- Description: Checks if a vertex exists
- Parameters:
  - `id`: `String`, The vertex ID

#### func removeEdge
```
func removeEdge(e: Edge<E>): Unit
```
- Description: Removes an edge
- Parameters:
  - `e`: `Edge<E>`, The edge to remove

#### func removeVertex
```
func removeVertex(id: String): Unit
```
- Description: Removes a vertex by ID
- Parameters:
  - `id`: `String`, The vertex ID

#### func upsertEdge
```
func upsertEdge(e: Edge<E>): Unit
```
- Description: Updates or inserts an edge
- Parameters:
  - `e`: `Edge<E>`, The edge to upsert

#### func upsertVertex
```
func upsertVertex(v: Vertex<V>): Unit
```
- Description: Updates or inserts a vertex
- Parameters:
  - `v`: `Vertex<V>`, The vertex to upsert


### class BaseLocalGraphStorage<V, E>
#### func close
```
public func close(): Unit
```
- Description: Closes the graph storage.

#### prop collection
```
public prop collection: String
```
- Description: Gets the collection name of the graph storage.

#### func commit
```
public func commit(): Unit
```
- Description: Commits all changes to the graph storage.

#### func getAllVertices
```
public func getAllVertices(): Array<Vertex<V>>
```
- Description: Retrieves all vertices in the graph.

#### func getEdge
```
public func getEdge(srcId: String, tgtId: String, eType: String): Option<Edge<E>>
```
- Description: Retrieves an edge between the source and target vertices with the specified type.
- Parameters:
  - `srcId`: `String`, The ID of the source vertex.
  - `tgtId`: `String`, The ID of the target vertex.
  - `eType`: `String`, The type of the edge to retrieve.

#### func getEdges
```
public func getEdges(srcId: String, tgtId: String): Array<Edge<E>>
```
- Description: Retrieves all edges between the source and target vertices.
- Parameters:
  - `srcId`: `String`, The ID of the source vertex.
  - `tgtId`: `String`, The ID of the target vertex.

#### func getIncomingEdgesOf
```
public func getIncomingEdgesOf(id: String): Array<Edge<E>>
```
- Description: Retrieves all incoming edges of a vertex.
- Parameters:
  - `id`: `String`, The ID of the vertex.

#### func getOutgoingEdgesOf
```
public func getOutgoingEdgesOf(id: String): Array<Edge<E>>
```
- Description: Retrieves all outgoing edges of a vertex.
- Parameters:
  - `id`: `String`, The ID of the vertex.

#### func getVertex
```
public func getVertex(id: String): Option<Vertex<V>>
```
- Description: Retrieves a vertex by its ID.
- Parameters:
  - `id`: `String`, The ID of the vertex to retrieve.

#### func getVertexTypes
```
public func getVertexTypes(): Set<String>
```
- Description: Retrieves all vertex types in the graph.

#### func hasEdge
```
public func hasEdge(srcId: String, tgtId: String): Bool
```
- Description: Checks if an edge exists between the source and target vertices.
- Parameters:
  - `srcId`: `String`, The ID of the source vertex.
  - `tgtId`: `String`, The ID of the target vertex.

#### func hasVertex
```
public func hasVertex(id: String): Bool
```
- Description: Checks if a vertex with the given ID exists in the graph.
- Parameters:
  - `id`: `String`, The ID of the vertex to check.

#### func init
```
public init(workspace!: String = ".storage", collection!: String = "default")
```
- Description: Initializes the graph storage with the specified workspace and collection.
- Parameters:
  - `workspace`: `String`, The workspace directory for storage.
  - `collection`: `String`, The collection name for the graph.

#### func removeEdge
```
public func removeEdge(e: Edge<E>): Unit
```
- Description: Removes an edge from the graph.
- Parameters:
  - `e`: `Edge<E>`, The edge to remove.

#### func removeVertex
```
public func removeVertex(id: String): Unit
```
- Description: Removes a vertex from the graph.
- Parameters:
  - `id`: `String`, The ID of the vertex to remove.

#### func reset
```
public func reset(): Unit
```
- Description: Resets the graph storage by clearing all data.

#### func upsertEdge
```
public func upsertEdge(edge: Edge<E>): Unit
```
- Description: Inserts or updates an edge in the graph.
- Parameters:
  - `edge`: `Edge<E>`, The edge to insert or update.

#### func upsertVertex
```
public func upsertVertex(vertex: Vertex<V>): Unit
```
- Description: Inserts or updates a vertex in the graph.
- Parameters:
  - `vertex`: `Vertex<V>`, The vertex to insert or update.

#### prop workspace
```
public prop workspace: String
```
- Description: Gets the workspace directory of the graph storage.


### class Edge<E>
#### func operator !=
```
operator func !=(other: Edge<E>): Bool
```
- Description: Checks if two edges are not equal
- Parameters:
  - `other`: `Edge<E>`, The other edge to compare

#### func operator ==
```
operator func ==(other: Edge<E>): Bool
```
- Description: Checks if two edges are equal
- Parameters:
  - `other`: `Edge<E>`, The other edge to compare

#### prop data
```
prop data: Option<E>
```
- Description: Gets the edge data

#### func deserialize
```
static func deserialize(dm: DataModel)
```
- Description: Deserializes a DataModel to an Edge
- Parameters:
  - `dm`: `DataModel`, The DataModel to deserialize

#### prop eType
```
prop eType: String
```
- Description: Gets the edge type

#### func fromJson
```
static func fromJson(str: String): Edge<E>
```
- Description: Creates an edge from a JSON string
- Parameters:
  - `str`: `String`, The JSON string

#### func hashCode
```
func hashCode(): Int64
```
- Description: Computes the hash code of the edge

#### func init
```
init(srcId: String, tgtId: String, eType!: String = "DEFAULT", weight!: Float64 = 1.0, data!: Option<E> = None)
```
- Description: Constructor for Edge
- Parameters:
  - `srcId`: `String`, The source vertex ID
  - `tgtId`: `String`, The target vertex ID
  - `eType`: `String`, The edge type
  - `weight`: `Float64`, The edge weight
  - `data`: `Option<E>`, The edge data

#### func serialize
```
func serialize(): DataModel
```
- Description: Serializes the edge to a DataModel

#### prop srcId
```
prop srcId: String
```
- Description: Gets the source vertex ID

#### prop tgtId
```
prop tgtId: String
```
- Description: Gets the target vertex ID

#### func toJsonString
```
func toJsonString(): String
```
- Description: Converts the edge to a JSON string

#### prop uniqueId
```
prop uniqueId: String
```
- Description: Gets the unique ID of the edge

#### prop weight
```
mut prop weight: Float64
```
- Description: Gets or sets the edge weight


### interface GraphStorage<V, E>
#### func getAllVertices
```
func getAllVertices(): Array<Vertex<V>>
```
- Description: Retrieves all vertices in the graph.

#### func getEdge
```
func getEdge(srcId: String, tgtId: String, eType: String): Option<Edge<E>>
```
- Description: Retrieves an edge between the source and target vertices with the specified type.
- Parameters:
  - `srcId`: `String`, The ID of the source vertex.
  - `tgtId`: `String`, The ID of the target vertex.
  - `eType`: `String`, The type of the edge to retrieve.

#### func getEdges
```
func getEdges(srcId: String, tgtId: String): Array<Edge<E>>
```
- Description: Retrieves all edges between the source and target vertices.
- Parameters:
  - `srcId`: `String`, The ID of the source vertex.
  - `tgtId`: `String`, The ID of the target vertex.

#### func getIncomingEdgesOf
```
func getIncomingEdgesOf(id: String): Array<Edge<E>>
```
- Description: Retrieves all incoming edges of a vertex.
- Parameters:
  - `id`: `String`, The ID of the vertex.

#### func getOutgoingEdgesOf
```
func getOutgoingEdgesOf(id: String): Array<Edge<E>>
```
- Description: Retrieves all outgoing edges of a vertex.
- Parameters:
  - `id`: `String`, The ID of the vertex.

#### func getVertex
```
func getVertex(id: String): Option<Vertex<V>>
```
- Description: Retrieves a vertex by its ID.
- Parameters:
  - `id`: `String`, The ID of the vertex to retrieve.

#### func getVertexTypes
```
func getVertexTypes(): Set<String>
```
- Description: Retrieves all vertex types in the graph.

#### func hasEdge
```
func hasEdge(srcId: String, tgtId: String): Bool
```
- Description: Checks if an edge exists between the source and target vertices.
- Parameters:
  - `srcId`: `String`, The ID of the source vertex.
  - `tgtId`: `String`, The ID of the target vertex.

#### func hasVertex
```
func hasVertex(id: String): Bool
```
- Description: Checks if a vertex with the given ID exists in the graph.
- Parameters:
  - `id`: `String`, The ID of the vertex to check.

#### func removeEdge
```
func removeEdge(e: Edge<E>): Unit
```
- Description: Removes an edge from the graph.
- Parameters:
  - `e`: `Edge<E>`, The edge to remove.

#### func removeVertex
```
func removeVertex(id: String): Unit
```
- Description: Removes a vertex from the graph.
- Parameters:
  - `id`: `String`, The ID of the vertex to remove.

#### func upsertEdge
```
func upsertEdge(edge: Edge<E>): Unit
```
- Description: Inserts or updates an edge in the graph.
- Parameters:
  - `edge`: `Edge<E>`, The edge to insert or update.

#### func upsertVertex
```
func upsertVertex(vertex: Vertex<V>): Unit
```
- Description: Inserts or updates a vertex in the graph.
- Parameters:
  - `vertex`: `Vertex<V>`, The vertex to insert or update.


### class IllegalEdgeException
#### func init
```
init(message: String)
```
- Description: Constructor for IllegalEdgeException
- Parameters:
  - `message`: `String`, The error message


### interface LocalGraphStorage<V, E>

### class NodeContainer<V, E>
#### func addIncomingEdge
```
func addIncomingEdge(e: Edge<E>): Unit
```
- Description: Adds an incoming edge to the node
- Parameters:
  - `e`: `Edge<E>`, The edge to add

#### func addOutgoingEdge
```
func addOutgoingEdge(e: Edge<E>): Unit
```
- Description: Adds an outgoing edge to the node
- Parameters:
  - `e`: `Edge<E>`, The edge to add

#### prop incoming
```
prop incoming: Set<Edge<E>>
```
- Description: Gets the set of incoming edges

#### prop outgoing
```
prop outgoing: Set<Edge<E>>
```
- Description: Gets the set of outgoing edges

#### func removeIncomingEdge
```
func removeIncomingEdge(e: Edge<E>): Unit
```
- Description: Removes an incoming edge from the node
- Parameters:
  - `e`: `Edge<E>`, The edge to remove

#### func removeOutgoingEdge
```
func removeOutgoingEdge(e: Edge<E>): Unit
```
- Description: Removes an outgoing edge from the node
- Parameters:
  - `e`: `Edge<E>`, The edge to remove

#### prop vertex
```
mut prop vertex: Vertex<V>
```
- Description: Gets or sets the vertex of the node


### class Vertex<V>
#### func operator !=
```
operator func !=(other: Vertex<V>): Bool
```
- Description: Checks if two vertices are not equal
- Parameters:
  - `other`: `Vertex<V>`, The other vertex to compare

#### func operator ==
```
operator func ==(other: Vertex<V>): Bool
```
- Description: Checks if two vertices are equal
- Parameters:
  - `other`: `Vertex<V>`, The other vertex to compare

#### prop data
```
prop data: Option<V>
```
- Description: Gets the vertex data

#### func deserialize
```
static func deserialize(dm: DataModel): Vertex<V>
```
- Description: Deserializes a DataModel to a Vertex
- Parameters:
  - `dm`: `DataModel`, The DataModel to deserialize

#### func fromJsonString
```
static func fromJsonString(str: String): Vertex<V>
```
- Description: Creates a vertex from a JSON string
- Parameters:
  - `str`: `String`, The JSON string

#### func hashCode
```
func hashCode(): Int64
```
- Description: Computes the hash code of the vertex

#### prop id
```
prop id: String
```
- Description: Gets the vertex ID

#### func init
```
init(id: String, vType!: String = "DEFAULT", data!: Option<V> = None)
```
- Description: Constructor for Vertex
- Parameters:
  - `id`: `String`, The vertex ID
  - `vType`: `String`, The vertex type
  - `data`: `Option<V>`, The vertex data

#### func serialize
```
func serialize(): DataModel
```
- Description: Serializes the vertex to a DataModel

#### func toJsonString
```
func toJsonString(): String
```
- Description: Converts the vertex to a JSON string

#### prop vType
```
prop vType: String
```
- Description: Gets the vertex type


## Package storage.kv
- [Package storage.kv](#package-storage.kv)
  - [class JsonKVStorage<T>](#class-jsonkvstorage<t>)
    - [func close](#func-close)
    - [prop collection](#prop-collection)
    - [func commit](#func-commit)
    - [func get](#func-get)
    - [func init](#func-init)
    - [func insertInc](#func-insertinc)
    - [func remove](#func-remove)
    - [func reset](#func-reset)
    - [func upsert](#func-upsert)
    - [prop workspace](#prop-workspace)
  - [interface KVStorage<T>](#interface-kvstorage<t>)
    - [func get](#func-get-1)
    - [func remove](#func-remove-1)
    - [func upsert](#func-upsert-1)
  - [interface LocalKVStorage<T>](#interface-localkvstorage<t>)

### class JsonKVStorage<T>
#### func close
```
public func close(): Unit
```
- Description: Closes the storage.

#### prop collection
```
public prop collection: String
```
- Description: Gets the name of the collection.

#### func commit
```
public func commit(): Unit
```
- Description: Commits all changes to the storage.

#### func get
```
public func get(id: String): Option<T>
```
- Description: Retrieves the value associated with the specified ID.
- Parameters:
  - `id`: `String`, The ID of the value to retrieve.

#### func init
```
public init(workspace!: String = ".storage", collection!: String = "default")
```
- Description: Initializes a new instance of JsonKVStorage with specified workspace and collection.
- Parameters:
  - `workspace`: `String`, The directory path where the storage files will be kept. Defaults to '.storage'.
  - `collection`: `String`, The name of the collection. Defaults to 'default'.

#### func insertInc
```
public func insertInc(value: T): String
```
- Description: Inserts a value with an auto-incremented ID.
- Parameters:
  - `value`: `T`, The value to insert.

#### func remove
```
public func remove(id: String): Option<T>
```
- Description: Removes the value associated with the specified ID.
- Parameters:
  - `id`: `String`, The ID of the value to remove.

#### func reset
```
public func reset(): Unit
```
- Description: Clears all data in the storage and commits the changes.

#### func upsert
```
public func upsert(id: String, value: T): Unit
```
- Description: Updates or inserts a value with the specified ID.
- Parameters:
  - `id`: `String`, The ID of the value to update or insert.
  - `value`: `T`, The value to update or insert.

#### prop workspace
```
public prop workspace: String
```
- Description: Gets the workspace directory path.


### interface KVStorage<T>
#### func get
```
func get(id: String): Option<T>
```
- Description: Retrieves a value associated with the given ID.
- Parameters:
  - `id`: `String`, The identifier of the value to retrieve.

#### func remove
```
func remove(id: String): Option<T>
```
- Description: Removes a value associated with the given ID.
- Parameters:
  - `id`: `String`, The identifier of the value to remove.

#### func upsert
```
func upsert(id: String, value: T): Unit
```
- Description: Updates or inserts a value associated with the given ID.
- Parameters:
  - `id`: `String`, The identifier of the value to update or insert.
  - `value`: `T`, The value to be updated or inserted.


### interface LocalKVStorage<T>

## Package storage.vdb
- [Package storage.vdb](#package-storage.vdb)
  - [class FaissVectorStorage](#class-faissvectorstorage)
    - [func add](#func-add)
    - [func close](#func-close)
    - [prop collection](#prop-collection)
    - [func commit](#func-commit)
    - [prop embeddingModel](#prop-embeddingmodel)
    - [func init](#func-init)
    - [func query](#func-query)
    - [func queryWithScore](#func-querywithscore)
    - [func reset](#func-reset)
    - [prop workspace](#prop-workspace)
  - [class JsonMemoryVectorStorage](#class-jsonmemoryvectorstorage)
    - [func add](#func-add-1)
    - [func close](#func-close-1)
    - [prop collection](#prop-collection-1)
    - [func commit](#func-commit-1)
    - [prop embeddingModel](#prop-embeddingmodel-1)
    - [func init](#func-init-1)
    - [func query](#func-query-1)
    - [func queryWithScore](#func-querywithscore-1)
    - [func reset](#func-reset-1)
    - [prop workspace](#prop-workspace-1)
  - [interface LocalVectorStorage](#interface-localvectorstorage)
  - [interface VectorStorage](#interface-vectorstorage)
    - [func add](#func-add-1)
    - [prop embeddingModel](#prop-embeddingmodel-1)
    - [func query](#func-query-1)
    - [func queryWithScore](#func-querywithscore-1)

### class FaissVectorStorage
#### func add
```
func add(doc: Document): Unit
```
- Description: Adds a document to the vector database.
- Parameters:
  - `doc`: `Document`, The document to add.

#### func close
```
func close(): Unit
```
- Description: Closes the vector database.

#### prop collection
```
prop collection: String
```
- Description: Gets the collection name.

#### func commit
```
func commit(): Unit
```
- Description: Commits changes to the vector database and index.

#### prop embeddingModel
```
prop embeddingModel: EmbeddingModel
```
- Description: Gets the embedding model.

#### func init
```
init(embeddingModel: EmbeddingModel, workspace: String = ".storage", collection: String = "default")
```
- Description: Initializes the FaissVectorStorage with the given embedding model, workspace path, and collection name.
- Parameters:
  - `embeddingModel`: `EmbeddingModel`, The embedding model to be used for vector creation.
  - `workspace`: `String`, The path to the workspace directory. Defaults to ".storage".
  - `collection`: `String`, The name of the collection. Defaults to "default".

#### func query
```
func query(query: String, topK: Int64, threshold: Float64 = 0.6): Array<Document>
```
- Description: Queries the vector database for documents similar to the given query string.
- Parameters:
  - `query`: `String`, The query string to search for.
  - `topK`: `Int64`, The number of top results to return.
  - `threshold`: `Float64`, The minimum similarity threshold for results. Defaults to 0.6.

#### func queryWithScore
```
func queryWithScore(query: String, topK: Int64, threshold: Float64 = 0.6): Array<(Document, Float64)>
```
- Description: Queries the vector database for documents similar to the given query string, including similarity scores.
- Parameters:
  - `query`: `String`, The query string to search for.
  - `topK`: `Int64`, The number of top results to return.
  - `threshold`: `Float64`, The minimum similarity threshold for results. Defaults to 0.6.

#### func reset
```
func reset(): Unit
```
- Description: Resets the vector database and index.

#### prop workspace
```
prop workspace: String
```
- Description: Gets the workspace path.


### class JsonMemoryVectorStorage
#### func add
```
public func add(doc: Document): Unit
```
- Description: Adds a document to the storage.
- Parameters:
  - `doc`: `Document`, The document to add.

#### func close
```
public func close(): Unit
```
- Description: Closes the storage.

#### prop collection
```
public prop collection: String
```
- Description: Gets the collection name.

#### func commit
```
public func commit(): Unit
```
- Description: Commits changes to the storage.

#### prop embeddingModel
```
public prop embeddingModel: EmbeddingModel
```
- Description: Gets the embedding model.

#### func init
```
public init(embeddingModel: EmbeddingModel, workspace!: String = ".storage", collection!: String = "default")
```
- Description: Initializes the JsonMemoryVectorStorage with the given embedding model, workspace, and collection.
- Parameters:
  - `embeddingModel`: `EmbeddingModel`, The embedding model to use for vector creation.
  - `workspace`: `String`, The workspace directory for storage. Defaults to '.storage'.
  - `collection`: `String`, The collection name. Defaults to 'default'.

#### func query
```
public func query(query: String, topK: Int64, threshold!: Float64 = 0.6): Array<Document>
```
- Description: Queries the storage for documents matching the query string.
- Parameters:
  - `query`: `String`, The query string.
  - `topK`: `Int64`, The maximum number of documents to return.
  - `threshold`: `Float64`, The minimum similarity threshold. Defaults to 0.6.

#### func queryWithScore
```
public func queryWithScore(query: String, topK: Int64, threshold!: Float64 = 0.6): Array<(Document, Float64)>
```
- Description: Queries the storage for documents matching the query string and returns them with their similarity scores.
- Parameters:
  - `query`: `String`, The query string.
  - `topK`: `Int64`, The maximum number of documents to return.
  - `threshold`: `Float64`, The minimum similarity threshold. Defaults to 0.6.

#### func reset
```
public func reset(): Unit
```
- Description: Resets the storage to its initial state.

#### prop workspace
```
public prop workspace: String
```
- Description: Gets the workspace directory.


### interface LocalVectorStorage

### interface VectorStorage
#### func add
```
func add(doc: Document): Unit
```
- Description: Adds a document to the vector storage
- Parameters:
  - `doc`: `Document`, The document to add to the storage

#### prop embeddingModel
```
prop embeddingModel: EmbeddingModel
```
- Description: The embedding model used for vector storage

#### func query
```
func query(query: String, topK: Int64, threshold!: Float64): Array<Document>
```
- Description: Queries the vector storage with a given query string and returns top K documents above the threshold
- Parameters:
  - `query`: `String`, The query string to search for
  - `topK`: `Int64`, The number of top documents to return
  - `threshold!`: `Float64`, The minimum similarity score threshold for documents to be returned

#### func queryWithScore
```
func queryWithScore(query: String, topK: Int64, threshold!: Float64): Array<(Document, Float64)>
```
- Description: Queries the vector storage with a given query string and returns top K documents with their scores above the threshold
- Parameters:
  - `query`: `String`, The query string to search for
  - `topK`: `Int64`, The number of top documents to return
  - `threshold!`: `Float64`, The minimum similarity score threshold for documents to be returned


## Package tokenizer
- [Package tokenizer](#package-tokenizer)
  - [class AbstractBPETokenizer](#class-abstractbpetokenizer)
    - [func countToken](#func-counttoken)
    - [func decode](#func-decode)
    - [func encode](#func-encode)
  - [class BPETokenizer](#class-bpetokenizer)
    - [func init](#func-init)
  - [struct BPETokenizerConfig](#struct-bpetokenizerconfig)
    - [func deserialize](#func-deserialize)
  - [class Cl100kTokenizer](#class-cl100ktokenizer)
    - [func init](#func-init-1)
  - [interface JsonDeserializable<T>](#interface-jsondeserializable<t>)
    - [func fromJson](#func-fromjson)
    - [func serialize](#func-serialize)
  - [class Pair<T>](#class-pair<t>)
    - [func !=](#func-!=)
    - [func ==](#func-==)
    - [func hashCode](#func-hashcode)
    - [func init](#func-init-1)
    - [prop left](#prop-left)
    - [prop right](#prop-right)
  - [struct TokenizerJson](#struct-tokenizerjson)
    - [func deserialize](#func-deserialize-1)
  - [class TokenizerLoader](#class-tokenizerloader)
    - [func default](#func-default)
    - [func load](#func-load)
  - [enum TokenizerType](#enum-tokenizertype)
    - [enumeration Cl100k](#enumeration-cl100k)
    - [enumeration DeepSeek](#enumeration-deepseek)
    - [enumeration Qwen](#enumeration-qwen)
    - [func fromString](#func-fromstring)
    - [func toString](#func-tostring)
  - [class UnicodeTokenizer](#class-unicodetokenizer)
    - [func countToken](#func-counttoken-1)
    - [func decode](#func-decode-1)
    - [func encode](#func-encode-1)

### class AbstractBPETokenizer
#### func countToken
```
public func countToken(input: String): Int64
```
- Description: Counts the number of tokens in a string.
- Parameters:
  - `input`: `String`, The string to count tokens in.

#### func decode
```
public func decode(tokens: Array<UInt32>): String
```
- Description: Decodes an array of token IDs into a string.
- Parameters:
  - `tokens`: `Array<UInt32>`, The array of token IDs to decode.

#### func encode
```
public func encode(input: String): Array<UInt32>
```
- Description: Encodes a string into an array of token IDs.
- Parameters:
  - `input`: `String`, The string to encode.


### class BPETokenizer
#### func init
```
init(modelPath: String)
```
- Description: Initializes the BPETokenizer with the specified model path.
- Parameters:
  - `modelPath`: `String`, The path to the model files.


### struct BPETokenizerConfig
#### func deserialize
```
static func deserialize(dm: DataModel): BPETokenizerConfig
```
- Description: Deserializes a DataModel into a BPETokenizerConfig object.
- Parameters:
  - `dm`: `DataModel`, The DataModel to deserialize.


### class Cl100kTokenizer
#### func init
```
init(path: String)
```
- Description: Initializes the Cl100kTokenizer with a configuration file path.
- Parameters:
  - `path`: `String`, The path to the configuration file.


### interface JsonDeserializable<T>
#### func fromJson
```
static func fromJson(str: String)
```
- Description: Deserializes a JSON string into an object.
- Parameters:
  - `str`: `String`, The JSON string to deserialize.

#### func serialize
```
func serialize(): DataModel
```
- Description: Serializes the object into a DataModel.


### class Pair<T>
#### func operator !=
```
public operator func !=(other: Pair<T>): Bool
```
- Description: Checks if two pairs are not equal.
- Parameters:
  - `other`: `Pair<T>`, The other pair to compare with.

#### func operator ==
```
public operator func ==(other: Pair<T>): Bool
```
- Description: Checks if two pairs are equal.
- Parameters:
  - `other`: `Pair<T>`, The other pair to compare with.

#### func hashCode
```
public func hashCode(): Int64
```
- Description: Computes the hash code of the pair.

#### func init
```
public init(left: T, right: T)
```
- Description: Initializes a new Pair with the given left and right values.
- Parameters:
  - `left`: `T`, The left value of the pair.
  - `right`: `T`, The right value of the pair.

#### prop left
```
public prop left: T
```
- Description: Gets the left value of the pair.

#### prop right
```
public prop right: T
```
- Description: Gets the right value of the pair.


### struct TokenizerJson
#### func deserialize
```
static func deserialize(dm: DataModel): TokenizerJson
```
- Description: Deserializes a DataModel into a TokenizerJson object.
- Parameters:
  - `dm`: `DataModel`, The DataModel to deserialize.


### class TokenizerLoader
#### func default
```
func default(): Tokenizer
```
- Description: Returns the default tokenizer based on configuration or falls back to UnicodeTokenizer

#### func load
```
func load(tokenizerType: TokenizerType, vocabPath: String): Tokenizer
```
- Description: Loads a tokenizer of the specified type with the given vocabulary path
- Parameters:
  - `tokenizerType`: `TokenizerType`, The type of tokenizer to load
  - `vocabPath`: `String`, The path to the vocabulary file for the tokenizer


### enum TokenizerType
####  Cl100k
```
Cl100k
```
- Description: Represents the Cl100k tokenizer type

####  DeepSeek
```
DeepSeek
```
- Description: Represents the DeepSeek tokenizer type

####  Qwen
```
Qwen
```
- Description: Represents the Qwen tokenizer type

#### func fromString
```
func fromString(ttype: String): TokenizerType
```
- Description: Converts a string to the corresponding TokenizerType enum value
- Parameters:
  - `ttype`: `String`, The string representation of the tokenizer type

#### func toString
```
func toString()
```
- Description: Converts the tokenizer type to a string representation


### class UnicodeTokenizer
#### func countToken
```
func countToken(input: String): Int64
```
- Description: Counts the number of tokens in a string, adjusting for different character types.
- Parameters:
  - `input`: `String`, The string for which tokens are to be counted.

#### func decode
```
func decode(tokens: Array<UInt32>): String
```
- Description: Decodes an array of tokens into a string.
- Parameters:
  - `tokens`: `Array<UInt32>`, An array of tokens to be decoded.

#### func encode
```
func encode(input: String): Array<UInt32>
```
- Description: Encodes a string into an array of tokens.
- Parameters:
  - `input`: `String`, The string to be encoded.


## Package tool
- [Package tool](#package-tool)
  - [class NativeFuncTool](#class-nativefunctool)
    - [func addExamples](#func-addexamples)
    - [prop description](#prop-description)
    - [prop examples](#prop-examples)
    - [func init](#func-init)
    - [func invoke](#func-invoke)
    - [prop name](#prop-name)
    - [prop parameters](#prop-parameters)
    - [prop retType](#prop-rettype)
  - [class RetrieverTool](#class-retrievertool)
    - [prop description](#prop-description-1)
    - [prop examples](#prop-examples-1)
    - [func init](#func-init-1)
    - [func invoke](#func-invoke-1)
    - [prop name](#prop-name-1)
    - [prop parameters](#prop-parameters-1)
    - [prop retType](#prop-rettype-1)
  - [class SimpleToolManager](#class-simpletoolmanager)
    - [func addTool](#func-addtool)
    - [func addTools](#func-addtools)
    - [func clear](#func-clear)
    - [func delTool](#func-deltool)
    - [prop enableFilter](#prop-enablefilter)
    - [func filterTool](#func-filtertool)
    - [func findTool](#func-findtool)
    - [func getTools](#func-gettools)
    - [func init](#func-init-1)
    - [func init](#func-init-1)

### class NativeFuncTool
#### func addExamples
```
public func addExamples(examples: Array<String>): Unit
```
- Description: Adds examples to the tool.
- Parameters:
  - `examples`: `Array<String>`, An array of example strings to add.

#### prop description
```
public prop description: String
```
- Description: Gets the description of the tool.

#### prop examples
```
public prop examples: Array<String>
```
- Description: Gets the examples of the tool.

#### func init
```
public init(name!: String, description!: String, parameters!: Array<(String, String, TypeSchema)> = [], retType!: TypeSchema = TypeSchema.Str, examples!: Array<String> = [], filterable!: Bool = true, terminal!: Bool = false, execFn!: Option<ExecFn> = None)
```
- Description: Initializes a new instance of NativeFuncTool with the specified parameters.
- Parameters:
  - `name`: `String`, The name of the tool.
  - `description`: `String`, A description of the tool.
  - `parameters`: `Array<(String, String, TypeSchema)>`, An array of tuples representing the parameters of the tool.
  - `retType`: `TypeSchema`, The return type schema of the tool.
  - `examples`: `Array<String>`, An array of example strings.
  - `filterable`: `Bool`, Indicates whether the tool is filterable.
  - `terminal`: `Bool`, Indicates whether the tool is terminal.
  - `execFn`: `Option<ExecFn>`, An optional execution function.

#### func invoke
```
override public func invoke(args: HashMap<String, JsonValue>): ToolResponse
```
- Description: Invokes the native function with the specified arguments.
- Parameters:
  - `args`: `HashMap<String, JsonValue>`, A map of arguments represented as JSON values.

#### prop name
```
public prop name: String
```
- Description: Gets the name of the tool.

#### prop parameters
```
public prop parameters: Array<ToolParameter>
```
- Description: Gets the parameters of the tool.

#### prop retType
```
public prop retType: TypeSchema
```
- Description: Gets the return type schema of the tool.


### class RetrieverTool
#### prop description
```
prop description: String
```
- Description: Returns the description of the tool. If the retriever's description is empty, it returns a default description.

#### prop examples
```
prop examples: Array<String>
```
- Description: Returns examples of tool usage.

#### func init
```
init(retriever: Retriever)
```
- Description: Initializes the RetrieverTool with a retriever instance.
- Parameters:
  - `retriever`: `Retriever`, The retriever instance to be used for searching.

#### func invoke
```
func invoke(args: HashMap<String, JsonValue>): ToolResponse
```
- Description: Invokes the tool with the provided arguments and returns a response.
- Parameters:
  - `args`: `HashMap<String, JsonValue>`, The arguments for the tool, including the query to search.

#### prop name
```
prop name: String
```
- Description: Returns the name of the tool.

#### prop parameters
```
prop parameters: Array<ToolParameter>
```
- Description: Returns the parameters required by the tool.

#### prop retType
```
prop retType: TypeSchema
```
- Description: Returns the return type schema of the tool.


### class SimpleToolManager
#### func addTool
```
override public func addTool(tool: Tool): Unit
```
- Description: Adds a tool to the manager.
- Parameters:
  - `tool`: `Tool`, The tool to be added.

#### func addTools
```
override public func addTools(tools: Array<Tool>): Unit
```
- Description: Adds multiple tools to the manager.
- Parameters:
  - `tools`: `Array<Tool>`, An array of tools to be added.

#### func clear
```
override public func clear(): Unit
```
- Description: Clears all tools from the manager.

#### func delTool
```
override public func delTool(tool: Tool): Unit
```
- Description: Removes a tool from the manager.
- Parameters:
  - `tool`: `Tool`, The tool to be removed.

#### prop enableFilter
```
override public prop enableFilter: Bool
```
- Description: Gets the current filter status.

#### func filterTool
```
override public func filterTool(question: String, config: ToolSearchConfig): Array<Tool>
```
- Description: Filters tools based on a question and configuration.
- Parameters:
  - `question`: `String`, The question used for filtering tools.
  - `config`: `ToolSearchConfig`, The configuration for tool search.

#### func findTool
```
override public func findTool(name: String): Option<Tool>
```
- Description: Finds a tool by its name.
- Parameters:
  - `name`: `String`, The name of the tool to find.

#### func getTools
```
override public func getTools(): Array<Tool>
```
- Description: Retrieves all tools in the manager.

#### func init
```
public init()
```
- Description: Initializes a SimpleToolManager with filter disabled by default.

#### func init
```
public init(tools: Collection<Tool>, enableFilter: Bool = false)
```
- Description: Initializes a SimpleToolManager with a collection of tools and an optional filter setting.
- Parameters:
  - `tools`: `Collection<Tool>`, A collection of tools to be managed.
  - `enableFilter`: `Bool`, A boolean flag to enable or disable tool filtering.


## Package vdb
- [Package vdb](#package-vdb)
  - [class FaissVectorDatabase](#class-faissvectordatabase)
    - [func addVector](#func-addvector)
    - [func close](#func-close)
    - [func init](#func-init)
    - [func load](#func-load)
    - [func save](#func-save)
    - [func search](#func-search)
  - [class InMemoryVectorDatabase](#class-inmemoryvectordatabase)
    - [func addVector](#func-addvector-1)
    - [func load](#func-load-1)
    - [func save](#func-save-1)
    - [func search](#func-search-1)
    - [func setVector](#func-setvector)
  - [interface IndexMap](#interface-indexmap)
    - [func add](#func-add)
    - [func get](#func-get)
    - [func load](#func-load-1)
    - [func save](#func-save-1)
  - [class JsonlIndexMap](#class-jsonlindexmap)
    - [func add](#func-add-1)
    - [func get](#func-get-1)
    - [func init](#func-init-1)
    - [func load](#func-load-1)
    - [func save](#func-save-1)
  - [struct SearchResult](#struct-searchresult)
    - [let dist](#let-dist)
    - [let index](#let-index)
    - [func init](#func-init-1)
  - [class SemanticMap](#class-semanticmap)
    - [func asRetriever](#func-asretriever)
    - [prop embeddingModel](#prop-embeddingmodel)
    - [let indexMap](#let-indexmap)
    - [func init](#func-init-1)
    - [func load](#func-load-1)
    - [func put](#func-put)
    - [func save](#func-save-1)
    - [func search](#func-search-1)
    - [let vectorDB](#let-vectordb)
  - [class SemanticSet](#class-semanticset)
    - [func asRetriever](#func-asretriever-1)
    - [prop embeddingModel](#prop-embeddingmodel-1)
    - [func init](#func-init-1)
    - [func load](#func-load-1)
    - [func put](#func-put-1)
    - [func save](#func-save-1)
    - [func search](#func-search-1)
  - [class SimpleIndexMap](#class-simpleindexmap)
    - [func add](#func-add-1)
    - [func deserialize](#func-deserialize)
    - [func get](#func-get-1)
    - [func load](#func-load-1)
    - [func save](#func-save-1)
    - [func serialize](#func-serialize)
    - [func set](#func-set)
  - [class Vector](#class-vector)
    - [func init](#func-init-1)
    - [let vector](#let-vector)
  - [class VectorBuilder](#class-vectorbuilder)
    - [func createEmbeddingVector](#func-createembeddingvector)
  - [interface VectorDatabase](#interface-vectordatabase)
    - [func addVector](#func-addvector-1)
    - [func load](#func-load-1)
    - [func save](#func-save-1)
    - [func search](#func-search-1)

### class FaissVectorDatabase
#### func addVector
```
func addVector(vector: Vector): Unit
```
- Description: Adds a vector to the database.
- Parameters:
  - `vector`: `Vector`, The vector to be added to the database.

#### func close
```
func close(): Unit
```
- Description: Closes the database and releases all allocated resources.

#### func init
```
init(dimension: Int64 = 1536)
```
- Description: Initializes a new FaissVectorDatabase with the specified dimension.
- Parameters:
  - `dimension`: `Int64`, The dimension of the vectors to be stored in the database. Defaults to 1536.

#### func load
```
static func load(filePath: String): FaissVectorDatabase
```
- Description: Loads a FaissVectorDatabase from the specified file path.
- Parameters:
  - `filePath`: `String`, The path from which the database will be loaded.

#### func save
```
func save(filePath: String): Unit
```
- Description: Saves the database to the specified file path.
- Parameters:
  - `filePath`: `String`, The path where the database will be saved.

#### func search
```
func search(queryVec: Vector, number: Int64 = 5, minDistance: Float64 = 0.6): Array<SearchResult>
```
- Description: Searches the database for vectors similar to the query vector.
- Parameters:
  - `queryVec`: `Vector`, The query vector for which similar vectors are to be found.
  - `number`: `Int64`, The maximum number of results to return. Defaults to 5.
  - `minDistance`: `Float64`, The minimum distance threshold for results. Defaults to 0.6.


### class InMemoryVectorDatabase
#### func addVector
```
func addVector(vector: Vector): Unit
```
- Description: Adds a vector to the vector buffer and returns the index where it was stored.
- Parameters:
  - `vector`: `Vector`, The vector to be added.

#### func load
```
static func load(filePath: String): InMemoryVectorDatabase
```
- Description: Attempts to load the vector database from a file, but currently throws an UnsupportedException.
- Parameters:
  - `filePath`: `String`, The file path from which the vector database should be loaded.

#### func save
```
func save(filePath: String): Unit
```
- Description: Attempts to save the vector database to a file, but currently throws an UnsupportedException.
- Parameters:
  - `filePath`: `String`, The file path where the vector database should be saved.

#### func search
```
func search(queryVec: Vector, number: Int64 = 5, minDistance: Float64 = 0.6): Array<SearchResult>
```
- Description: Searches for the most similar vectors to the query vector based on cosine similarity.
- Parameters:
  - `queryVec`: `Vector`, The query vector for which similar vectors are to be found.
  - `number`: `Int64`, The number of most similar vectors to return.
  - `minDistance`: `Float64`, The minimum cosine similarity threshold for vectors to be considered similar.

#### func setVector
```
func setVector(index: Int64, vector: Vector): Unit
```
- Description: Sets a vector at the specified index in the vector buffer.
- Parameters:
  - `index`: `Int64`, The index where the vector will be stored.
  - `vector`: `Vector`, The vector to be stored.


### interface IndexMap
#### func add
```
func add(content: T): Unit
```
- Description: Adds content to the index map. The index is determined by the order in which it was added.
- Parameters:
  - `content`: `T`, The content to be added to the index map.

#### func get
```
func get(index: Int64): T
```
- Description: Retrieves the content at the specified index.
- Parameters:
  - `index`: `Int64`, The index of the content to retrieve.

#### func load
```
static func load(filePath: String): Self
```
- Description: Loads the index map from the specified file path.
- Parameters:
  - `filePath`: `String`, The file path from which the index map will be loaded.

#### func save
```
func save(filePath: String): Unit
```
- Description: Saves the index map to the specified file path.
- Parameters:
  - `filePath`: `String`, The file path where the index map will be saved.


### class JsonlIndexMap
#### func add
```
override public func add(content: T): Unit
```
- Description: Adds a content of type T to the JsonlIndexMap.
- Parameters:
  - `content`: `T`, The content to be added to the map.

#### func get
```
override public func get(index: Int64): T
```
- Description: Retrieves the content at the specified index.
- Parameters:
  - `index`: `Int64`, The index of the content to retrieve.

#### func init
```
public init()
```
- Description: Initializes a new JsonlIndexMap with an empty ArrayList.

#### func load
```
redef public static func load(filePath: String): JsonlIndexMap<T>
```
- Description: Loads a JsonlIndexMap from a file containing JSONL formatted data.
- Parameters:
  - `filePath`: `String`, The path of the file to load the JsonlIndexMap from.

#### func save
```
override public func save(filePath: String): Unit
```
- Description: Saves the contents of the JsonlIndexMap to a file in JSONL format.
- Parameters:
  - `filePath`: `String`, The path of the file where the contents will be saved.


### struct SearchResult
#### let dist
```
let dist: Float64
```
- Description: The distance of the search result

#### let index
```
let index: Int64
```
- Description: The index of the search result

#### func init
```
init(index: Int64, dist: Float64)
```
- Description: Initializes a new SearchResult with the given index and distance
- Parameters:
  - `index`: `Int64`, The index of the search result
  - `dist`: `Float64`, The distance of the search result


### class SemanticMap
#### func asRetriever
```
public func asRetriever(): Retriever
```
- Description: Converts the semantic map to a retriever

#### prop embeddingModel
```
public mut prop embeddingModel: EmbeddingModel
```
- Description: Embedding model property with getter and setter

#### let indexMap
```
public let indexMap: IMAP
```
- Description: Index map instance

#### func init
```
public init(vectorDB: VDB, indexMap: IMAP, embeddingModel: Option<EmbeddingModel> = None)
```
- Description: Constructor for SemanticMap
- Parameters:
  - `vectorDB`: `VDB`, Vector database instance
  - `indexMap`: `IMAP`, Index map instance
  - `embeddingModel`: `Option<EmbeddingModel>`, Optional embedding model

#### func load
```
public static func load(dirPath: String): SemanticMap<VDB, IMAP, T>
```
- Description: Loads a semantic map from disk
- Parameters:
  - `dirPath`: `String`, Directory path to load from

#### func put
```
public func put(key: String, value: T): Unit
```
- Description: Adds a key-value pair to the semantic map
- Parameters:
  - `key`: `String`, Key string
  - `value`: `T`, Value to be stored

#### func save
```
public func save(dirPath: String): Unit
```
- Description: Saves the semantic map to disk
- Parameters:
  - `dirPath`: `String`, Directory path to save to

#### func search
```
public func search(query: String, number: Int64 = 5, minDistance: Float64 = 0.3): Array<T>
```
- Description: Find similar data
- Parameters:
  - `query`: `String`, Query string
  - `number`: `Int64`, Number of results to return
  - `minDistance`: `Float64`, Minimum distance threshold for results

#### let vectorDB
```
public let vectorDB: VDB
```
- Description: Vector database instance


### class SemanticSet
#### func asRetriever
```
public func asRetriever(): Retriever
```
- Description: Converts the SemanticSet into a Retriever.

#### prop embeddingModel
```
public mut prop embeddingModel: EmbeddingModel
```
- Description: Gets or sets the embedding model used by the SemanticSet.

#### func init
```
public init(vectorDB!: VDB, indexMap!: IMAP, embeddingModel!: Option<EmbeddingModel> = None)
```
- Description: Initializes a new instance of SemanticSet with the specified vector database, index map, and optional embedding model.
- Parameters:
  - `vectorDB`: `VDB`, The vector database to be used.
  - `indexMap`: `IMAP`, The index map to be used.
  - `embeddingModel`: `Option<EmbeddingModel>`, The optional embedding model to be used.

#### func load
```
public static func load(dirPath: String): SemanticSet<VDB, IMAP, T>
```
- Description: Loads a SemanticSet from the specified directory.
- Parameters:
  - `dirPath`: `String`, The directory path from which the SemanticSet will be loaded.

#### func put
```
public func put(value: T): Unit
```
- Description: Adds a value to the SemanticSet.
- Parameters:
  - `value`: `T`, The value to be added.

#### func save
```
public func save(dirPath: String): Unit
```
- Description: Saves the SemanticSet to the specified directory.
- Parameters:
  - `dirPath`: `String`, The directory path where the SemanticSet will be saved.

#### func search
```
public func search(query: String, number!: Int64 = 5, minDistance!: Float64 = 0.3): Array<T>
```
- Description: Searches the SemanticSet for values matching the query.
- Parameters:
  - `query`: `String`, The query string to search for.
  - `number`: `Int64`, The maximum number of results to return.
  - `minDistance`: `Float64`, The minimum distance threshold for results.


### class SimpleIndexMap
#### func add
```
func add(content: String): Unit
```
- Description: Adds content to the next available index.
- Parameters:
  - `content`: `String`, The content to be added.

#### func deserialize
```
static func deserialize(dm: DataModel): SimpleIndexMap
```
- Description: Deserializes a DataModel into a SimpleIndexMap.
- Parameters:
  - `dm`: `DataModel`, The DataModel to be deserialized.

#### func get
```
func get(index: Int64): String
```
- Description: Retrieves the content at the specified index.
- Parameters:
  - `index`: `Int64`, The index from which the content will be retrieved.

#### func load
```
static func load(filePath: String): SimpleIndexMap
```
- Description: Loads a SimpleIndexMap from a file.
- Parameters:
  - `filePath`: `String`, The path of the file from which the SimpleIndexMap will be loaded.

#### func save
```
func save(filePath: String): Unit
```
- Description: Saves the SimpleIndexMap to a file.
- Parameters:
  - `filePath`: `String`, The path of the file where the SimpleIndexMap will be saved.

#### func serialize
```
func serialize(): DataModel
```
- Description: Serializes the SimpleIndexMap into a DataModel.

#### func set
```
func set(index: Int64, content: String): Unit
```
- Description: Sets the content at the specified index.
- Parameters:
  - `index`: `Int64`, The index where the content will be set.
  - `content`: `String`, The content to be set at the specified index.


### class Vector
#### func init
```
init(vec: Array<Float64>)
```
- Description: Initializes a new Vector instance with the given array of Float64 values
- Parameters:
  - `vec`: `Array<Float64>`, An array of Float64 values used to initialize the vector

#### let vector
```
let vector: Array<Float64>
```
- Description: A constant array of Float64 values representing the vector components


### class VectorBuilder
#### func createEmbeddingVector
```
func createEmbeddingVector(content: String): Vector
```
- Description: Creates an embedding vector from the given content.
- Parameters:
  - `content`: `String`, The input content to create the embedding vector from.


### interface VectorDatabase
#### func addVector
```
func addVector(vector: Vector): Unit
```
- Description: Add the vector to the database
- Parameters:
  - `vector`: `Vector`, The vector to be added to the database

#### func load
```
static func load(filePath: String): Self
```
- Description: Load from the file
- Parameters:
  - `filePath`: `String`, The file path to load the database from

#### func save
```
func save(filePath: String): Unit
```
- Description: Save to the file
- Parameters:
  - `filePath`: `String`, The file path to save the database

#### func search
```
func search(queryVec: Vector, number!: Int64, minDistance!: Float64): Array<SearchResult>
```
- Description: Query the database and find indexes of similar data
- Parameters:
  - `queryVec`: `Vector`, The query vector
  - `number!`: `Int64`, The number of results to return
  - `minDistance!`: `Float64`, The minimum distance threshold for results


