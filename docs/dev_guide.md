# Summary file: summary_cjnative.md

- [初识仓颉语言]()
    - [初识仓颉语言](source_zh_cn/first_understanding/basic.md)
    - [安装仓颉工具链](source_zh_cn/first_understanding/install.md)
    - [运行第一个仓颉程序](source_zh_cn/first_understanding/hello_world.md)
- [基本概念]()
    - [标识符](source_zh_cn/basic_programming_concepts/identifier.md)
    - [程序结构](source_zh_cn/basic_programming_concepts/program_structure.md)
    - [表达式](source_zh_cn/basic_programming_concepts/expression.md)
    - [函数](source_zh_cn/basic_programming_concepts/function.md)
- [基础数据类型]()
    - [基本操作符](source_zh_cn/basic_data_type/basic_operators.md)
    - [整数类型](source_zh_cn/basic_data_type/integer.md)
    - [浮点类型](source_zh_cn/basic_data_type/float.md)
    - [布尔类型](source_zh_cn/basic_data_type/bool.md)
    - [字符类型](source_zh_cn/basic_data_type/characters.md)
    - [字符串类型](source_zh_cn/basic_data_type/strings.md)
    - [元组类型](source_zh_cn/basic_data_type/tuple.md)
    - [数组类型](source_zh_cn/basic_data_type/array.md)
    - [区间类型](source_zh_cn/basic_data_type/range.md)
    - [Unit 类型](source_zh_cn/basic_data_type/unit.md)
    - [Nothing 类型](source_zh_cn/basic_data_type/nothing.md)
- [函数]()
    - [定义函数](source_zh_cn/function/define_functions.md)
    - [调用函数](source_zh_cn/function/call_functions.md)
    - [函数类型](source_zh_cn/function/first_class_citizen.md)
    - [嵌套函数](source_zh_cn/function/nested_functions.md)
    - [Lambda 表达式](source_zh_cn/function/lambda.md)
    - [闭包](source_zh_cn/function/closure.md)
    - [函数调用语法糖](source_zh_cn/function/function_call_desugar.md)
    - [函数重载](source_zh_cn/function/function_overloading.md)
    - [操作符重载](source_zh_cn/function/operator_overloading.md)
    - [const 函数和常量求值](source_zh_cn/function/const_func_and_eval.md)
- [结构类型]()
    - [定义 struct 类型](source_zh_cn/struct/define_struct.md)
    - [创建 struct 实例](source_zh_cn/struct/create_instance.md)
    - [mut 函数](source_zh_cn/struct/mut.md)
- [枚举类型和模式匹配]()
    - [枚举类型](source_zh_cn/enum_and_pattern_match/enum.md)
    - [Option 类型](source_zh_cn/enum_and_pattern_match/option_type.md)
    - [模式概述](source_zh_cn/enum_and_pattern_match/pattern_overview.md)
    - [模式的 Refutability](source_zh_cn/enum_and_pattern_match/pattern_refutability.md)
    - [match 表达式](source_zh_cn/enum_and_pattern_match/match.md)
    - [其他使用模式的地方](source_zh_cn/enum_and_pattern_match/other.md)
- [类和接口]()
    - [类](source_zh_cn/class_and_interface/class.md)
    - [接口](source_zh_cn/class_and_interface/interface.md)
    - [属性](source_zh_cn/class_and_interface/prop.md)
    - [子类型关系](source_zh_cn/class_and_interface/subtype.md)
    - [类型转换](source_zh_cn/class_and_interface/typecast.md)
- [泛型]()
    - [泛型概述](source_zh_cn/generic/generic_overview.md)
    - [泛型函数](source_zh_cn/generic/generic_function.md)
    - [泛型接口](source_zh_cn/generic/generic_interface.md)
    - [泛型类](source_zh_cn/generic/generic_class.md)
    - [泛型结构体](source_zh_cn/generic/generic_struct.md)
    - [泛型枚举](source_zh_cn/generic/generic_enum.md)
    - [泛型类型的子类型关系](source_zh_cn/generic/generic_subtype.md)
    - [类型别名](source_zh_cn/generic/typealias.md)
    - [泛型约束](source_zh_cn/generic/generic_constraint.md)
- [扩展]()
    - [扩展概述](source_zh_cn/extension/extend_overview.md)
    - [直接扩展](source_zh_cn/extension/direct_extension.md)
    - [接口扩展](source_zh_cn/extension/interface_extension.md)
    - [访问规则](source_zh_cn/extension/access_rules.md)
- [Collection 类型]()
    - [基础 Collection 类型概述](source_zh_cn/collections/collection_overview.md)
    - [ArrayList](source_zh_cn/collections/collection_arraylist.md)
    - [HashSet](source_zh_cn/collections/collection_hashset.md)
    - [HashMap](source_zh_cn/collections/collection_hashmap.md)
    - [Iterable 和 Collections](source_zh_cn/collections/collection_iterable_collections.md)
- [包]()
    - [包的概述](source_zh_cn/package/package_overview.md)
    - [包的声明](source_zh_cn/package/package_name.md)
    - [顶层声明的可见性](source_zh_cn/package/toplevel_access.md)
    - [包的导入](source_zh_cn/package/import.md)
    - [程序入口](source_zh_cn/package/entry.md)
- [异常处理]()
    - [定义异常](source_zh_cn/error_handle/exception_overview.md)
    - [throw 和处理异常](source_zh_cn/error_handle/handle.md)
    - [常见运行时异常](source_zh_cn/error_handle/common_runtime_exceptions.md)
    - [使用 Option](source_zh_cn/error_handle/use_option.md)
- [并发编程]()
    - [并发概述](source_zh_cn/concurrency/concurrency_overview.md)
    - [创建线程](source_zh_cn/concurrency/create_thread.md)
    - [访问线程](source_zh_cn/concurrency/use_thread.md)
    - [终止线程](source_zh_cn/concurrency/terminal_thread.md)
    - [同步机制](source_zh_cn/concurrency/sync.md)
    - [线程睡眠指定时长 sleep](source_zh_cn/concurrency/sleep.md)
- [基础 I/O 操作]()
    - [I/O 流概述](source_zh_cn/Basic_IO/basic_IO_overview.md)
    - [I/O 节点流](source_zh_cn/Basic_IO/basic_IO_source_stream.md)
    - [I/O 处理流](source_zh_cn/Basic_IO/basic_IO_process_stream.md)
- [网络编程]()
    - [网络编程概述](source_zh_cn/Net/net_overview.md)
    - [Socket 编程](source_zh_cn/Net/net_socket.md)
    - [HTTP 编程](source_zh_cn/Net/net_http.md)
    - [WebSocket 编程](source_zh_cn/Net/net_websocket.md)
- [宏]()
    - [宏的简介](source_zh_cn/Macro/macro_introduction.md)
    - [Tokens 相关类型和 quote 表达式](source_zh_cn/Macro/Tokens_types_and_quote_expressions.md)
    - [语法节点](source_zh_cn/Macro/sytax_node.md)
    - [宏的实现](source_zh_cn/Macro/implementation_of_macros.md)
    - [编译、报错与调试](source_zh_cn/Macro/compiling_error_reporting_and_debugging.md)
    - [宏包定义和导入](source_zh_cn/Macro/defining_and_importing_macro_package.md)
    - [内置编译标记](source_zh_cn/Macro/builtin_compilation_flags.md)
    - [实用案例](source_zh_cn/Macro/pratical_case.md)
- [反射和注解]()
    - [动态特性](source_zh_cn/reflect_and_annotation/dynamic_feature.md)
    - [注解](source_zh_cn/reflect_and_annotation/anno.md)
- [跨语言互操作]()
    - [仓颉-C 互操作](source_zh_cn/FFI/cangjie-c.md)
- [编译和构建]()
    - [cjc 使用](source_zh_cn/compile_and_build/cjc_usage.md)
    - [cjpm 介绍](source_zh_cn/compile_and_build/cjpm_usage.md)
    - [条件编译](source_zh_cn/compile_and_build/conditional_compilation.md)
- [部署和运行]()
    - [部署仓颉运行时](source_zh_cn/deploy_and_run/runtime_deploy.md)
    - [运行仓颉可执行程序](source_zh_cn/deploy_and_run/run.md)
- [附录]()
    - [cjc 编译选项](source_zh_cn/Appendix/compile_options.md)
    - [Linux 版本工具链的支持与安装](source_zh_cn/Appendix/linux_toolchain_install.md)
    - [runtime 环境变量使用手册](source_zh_cn/Appendix/runtime_env.md)
    - [关键字](source_zh_cn/Appendix/keyword.md)
    - [操作符](source_zh_cn/Appendix/operator.md)
    - [操作符函数](source_zh_cn/Appendix/operator_function.md)
    - [TokenKind 类型](source_zh_cn/Appendix/tokenkind_type.md)
    - [仓颉包兼容性检查](source_zh_cn/Appendix/cangjie_package_compatibility.md)


---

<!-- Content from source_zh_cn/first_understanding/basic.md -->
# 初识仓颉语言

仓颉编程语言是一种面向全场景应用开发的通用编程语言，可以兼顾开发效率和运行性能，并提供良好的编程体验，主要具有如下特点：

- **多后端支持**：仓颉编程语言支持 CJNative 和 CJVM 两种后端。其中 CJNative 后端将代码编译为原生二进制代码，直接在操作系统层面上运行；CJVM 后端将代码编译为字节码，基于 VM（虚拟机）进行运行。本文档适配 CJNative 后端。
- **语法简明高效**：仓颉编程语言提供了一系列简明高效的语法，旨在减少冗余书写、提升开发效率，例如插值字符串、主构造函数、Flow 表达式、`match` 和重导出等语法，让开发者可以用较少编码表达相关逻辑。
- **多范式编程**：仓颉编程语言支持函数式、命令式和面向对象等多范式编程，融合了高阶函数、代数数据类型、模式匹配、泛型等函数式语言的先进特性，还有封装、接口、继承、子类型多态等支持模块化开发的面向对象语言特性，以及值类型、全局函数等简洁高效的命令式语言特性。开发者可以根据开发偏好或应用场景，选用不同的编程范式。
- **类型安全**：仓颉编程语言是静态强类型语言，通过编译时类型检查尽早识别程序错误，降低运行时风险，也便于代码维护。同时，仓颉编译器提供了强大的类型推断能力，可以减少类型标注工作，提高开发效率。
- **内存安全**：仓颉编程语言支持自动内存管理，并在运行时进行数组下标越界检查、溢出检查等操作，确保运行时内存安全。
- **高效并发**：仓颉编程语言提供了用户态轻量化线程（原生协程），以及简单易用的并发编程机制，保证并发场景的高效开发和运行。
- **兼容语言生态**：仓颉编程语言支持和 C 等编程语言的互操作，并采用便捷的声明式编程范式，可实现对其他语言库的高效复用和生态兼容。
- **领域易扩展**：仓颉编程语言提供了基于词法宏的元编程能力，支持在编译时变换代码。此外，还提供了尾随 `lambda`、属性、操作符重载、部分关键字可省略等特性，开发者可由此深度定制程序的语法和语义，这有利于内嵌式领域专用语言（Embedded Domain Specific Languages，EDSL）的构建。
- **助力 UI 开发**：UI 开发是构建端侧应用的重要环节，基于仓颉编程语言的元编程和尾随 `lambda` 等特性，用户可以搭建声明式 UI 开发框架，提升 UI 开发效率和体验。
- **内置库功能丰富**：仓颉编程语言提供了功能丰富的内置库，涉及数据结构、常用算法、数学计算、正则匹配、系统交互、文件操作、网络通信、数据库访问、日志打印、解压缩、编解码、加解密和序列化等功能。


---

<!-- Content from source_zh_cn/first_understanding/install.md -->
# 安装仓颉工具链

在开发仓颉程序时，必用的工具之一是仓颉编译器，它可以将仓颉源代码编译为可运行的二进制文件，但现代编程语言的配套工具并不止于此，实际上，仓颉为开发者提供了编译器、调试器、包管理器、静态检查工具、格式化工具和覆盖率统计工具等一整套仓颉开发工具链，同时提供了友好的安装和使用方式，基本能做到“开箱即用”。

目前仓颉工具链已适配部分版本的 Linux、macOS 和 Windows 平台，但是仅针对部分 Linux 发行版做了完整功能测试，详情可参阅附录[Linux 版本工具链的支持与安装](../Appendix/linux_toolchain_install.md)章节，在暂未进行过完整功能测试的平台上，仓颉工具链的功能完整性不受到保证。此外，当前 Windows 平台上的仓颉编译器基于 MinGW 实现，相较于 Linux 版本的仓颉编译器，功能会有部分欠缺。

## Linux / macOS

### 环境准备

#### Linux

Linux 版仓颉工具链的系统环境要求如下：

| 架构    | 环境要求                                                     |
| ------- | ------------------------------------------------------------ |
| x86_64  | glibc 2.22，Linux Kernel 4.12 或更高版本，系统安装 libstdc++ 6.0.24 或更高版本 |
| aarch64 | glibc 2.27，Linux Kernel 4.15 或更高版本，系统安装 libstdc++ 6.0.24 或更高版本 |

除此之外，对于 Ubuntu 18.04，还需要安装相应的依赖软件包：

```bash
$ apt-get install binutils libc-dev libc++-dev libgcc-7-dev
```

更多 Linux 发行版的依赖安装命令可以参见附录[Linux 版本工具链的支持与安装](../Appendix/linux_toolchain_install.md)章节。

此外，仓颉工具链还依赖 OpenSSL 3 组件，由于该组件可能无法从以上发行版的默认软件源直接安装，因此需要自行手动安装，安装方式请参考附录[Linux 版本工具链的支持与安装](../Appendix/linux_toolchain_install.md)章节。

#### macOS

macOS 版仓颉工具链支持在 macOS 12.0 及以上版本运行。

使用 macOS 版本前需要安装相应的依赖软件包，可以通过执行以下命令安装：

```bash
$ brew install libffi
```

### 安装指导

首先请前往仓颉官方发布渠道，下载适配平台架构的安装包：

- `cangjie-sdk-linux-x64-x.y.z.tar.gz`：适用于 x86_64 架构 Linux 系统的仓颉工具链
- `cangjie-sdk-linux-aarch64-x.y.z.tar.gz`：适用于 aarch64 架构 Linux 系统的仓颉工具链
- `cangjie-sdk-mac-x64-x.y.z.tar.gz`：适用于 x86_64 架构 macOS 系统的仓颉工具链
- `cangjie-sdk-mac-aarch64-x.y.z.tar.gz`：适用于 aarch64/arm64 架构 macOS 系统的仓颉工具链

假设这里选择了 `cangjie-sdk-linux-x64-x.y.z.tar.gz`，下载到本地后，请执行如下命令解压：

```bash
tar xvf cangjie-sdk-linux-x64-x.y.z.tar.gz
```

解压完成，可以在当前工作路径下看到一个名为 `cangjie` 的目录，其中存放了仓颉工具链的全部内容，请执行如下命令完成仓颉工具链的安装配置：

```bash
source cangjie/envsetup.sh
```

为了验证是否安装成功，可以执行如下命令：

```bash
cjc -v
```

其中 `cjc` 是仓颉编译器的可执行文件名，如果在命令行中看到了仓颉编译器版本信息，表示已经成功安装了仓颉工具链。值得说明的是，`envsetup.sh` 脚本只是在当前 shell 环境中配置了工具链相关的环境变量，所以仓颉工具链仅在当前 shell 环境中可用，在新的 shell 环境中，需要重新执行 `envsetup.sh` 脚本配置环境。

若想使仓颉工具链的环境变量配置在 `shell` 启动时自动生效，可以在 `$HOME/.bashrc` 或 `$HOME/.zshrc`（依 `shell` 种类而定）等 `shell` 初始化配置文件的最后加入以下命令：

```shell
# 假设仓颉安装包解压在 /home/user/cangjie 中
source /home/user/cangjie/envsetup.sh  # 即 envsetup.sh 的绝对路径
```

配置完成后 shell 启动即可直接使用仓颉编译工具链。

### 卸载与更新

在 Linux 和 macOS 平台，删除上述仓颉工具链的安装包目录，同时移除上述环境变量（最简单的，可以新开一个 shell 环境），即可完成卸载。

```bash
$ rm -rf <path>/<to>/cangjie
```

若需要更新仓颉工具链，需要先卸载当前版本，然后按上述指导重新安装最新版本的仓颉工具链。

## Windows

本节以 Windows 10 平台为例，介绍仓颉工具链的安装方式。

### 安装指导

在 Windows 平台上，仓颉为开发者提供了 `exe` 和 `zip` 两种格式的安装包，请前往仓颉官方发布渠道，选择和下载适配平台架构的 Windows 版安装包。

- 如果选择 `exe` 格式的安装包（例如 `cangjie-sdk-windows-x64-x.y.z.exe`），请直接执行此文件，跟随安装向导点击操作，即可完成安装。

- 如果选择 `zip` 格式的安装包（例如 `cangjie-sdk-windows-x64-x.y.z.zip`），请将它解压到适当目录，在安装包中，仓颉为开发者提供了三种不同格式的安装脚本，分别是 `envsetup.bat`，`envsetup.ps1` 和 `envsetup.sh`，可以根据使用习惯及环境配置，选择一种执行：

    - 若使用 Windows 命令提示符（CMD）环境，请执行：

        ```bash
        path\to\cangjie\envsetup.bat
        ```

    - 若使用 PowerShell 环境，请执行：

        ```bash
        . path\to\cangjie\envsetup.ps1
        ```

    - 若使用 MSYS shell、bash 等环境，请执行：

        ```bash
        source path/to/cangjie/envsetup.sh
        ```

    为了验证是否安装成功，请在以上命令环境中继续执行 `cjc -v` 命令，如果输出了仓颉编译器版本信息，表示已经成功安装了仓颉工具链。

**值得注意的是**，基于 zip 安装包和执行脚本的安装方式，类似于 Linux 平台，即 envsetup 脚本所配置的环境变量，只在当前命令行环境中有效，如果打开新的命令行窗口，需要重新执行 envsetup 脚本配置环境。此时，若想使仓颉工具链的环境变量配置在命令提示符或终端启动时自动生效，可以对系统进行如下配置：

- 若使用 bash 环境，可以根据如下步骤操作：

    在 `$HOME/.bashrc` 初始化配置文件的最后加入以下命令（`$HOME` 为当前用户目录的路径）：

    ```shell
    # 假设仓颉安装包解压在 /home/user/cangjie 中
    source /home/user/cangjie/envsetup.sh  # 即 envsetup.sh 的绝对路径
    ```

    配置完成后 bash 启动即可直接使用仓颉编译工具链。

- 若使用 Windows 命令提示符（CMD）、PowerShell 或其他环境，可以根据如下步骤操作：

    1. 在 Windows 搜索框中，搜索 “查看高级系统设置” 并打开对应窗口；

    2. 单击 “环境变量” 按钮；

    3. 执行如下操作，配置 CANGJIE_HOME 变量：

        1. 在 “用户变量”（为当前用户进行配置）或 “系统变量”（为系统所有用户进行配置）区域中，查看是否已有 CANGJIE_HOME 环境变量。若没有，则单击 “新建” 按钮，并在 “变量名” 字段中输入 `CANGJIE_HOME` ；若有，则说明该环境可能已经进行过仓颉配置，如果想要继续为当前的仓颉版本进行配置并覆盖原配置，请单击 “编辑” 按钮，进入 “编辑系统变量” 窗口。

        2. 在 “变量值” 字段中输入仓颉安装包的解压路径，若原先已经存在路径，则使用新的路径覆盖原有的路径，例如仓颉安装包解压在 `D:\cangjie` ，则输入 `D:\cangjie` 。

        3. 配置完成后， “编辑用户变量” 或 “编辑系统变量” 窗口中显示的变量名为 `CANGJIE_HOME` 、变量值为  `D:\cangjie` 。确认路径正确配置后单击 “确定” 。

    4. 执行如下操作，配置 Path 变量：

        1. 在 “用户变量”（为当前用户进行配置）或 “系统变量”（为系统所有用户进行配置）区域中，找到并选择 Path 变量，单击 “编辑” 按钮，进入 “编辑环境变量” 窗口。

        2. 分别单击 “新建” 按钮，并分别输入 `%CANGJIE_HOME%\bin` 、 `%CANGJIE_HOME%\tools\bin` 、 `%CANGJIE_HOME%\tools\lib` 、 `%CANGJIE_HOME%\runtime\lib\windows_x86_64_llvm` (`%CANGJIE_HOME%` 为仓颉安装包的解压路径)。例如，仓库安装包解压在 `D:\cangjie` ，则新建的环境变量分别为： `D:\cangjie\bin` 、 `D:\cangjie\tools\bin` 、 `D:\cangjie\tools\lib` 、 `D:\cangjie\runtime\lib\windows_x86_64_llvm` 。

        3. （仅适用于为当前用户设置）单击 “新建” 按钮，并输入当前用户目录路径，并在路径后面添加 `.cjpm\bin` 。例如用户路径在 `C:\Users\bob` ，则输入 `C:\Users\bob\.cjpm\bin` 。

        4. 配置完成后应能在 “编辑环境变量” 窗口中看到配置的路径如下所示。确认路径正确配置后单击 “确定” 。

           ```text
           D:\cangjie\bin
           D:\cangjie\tools\bin
           D:\cangjie\tools\lib
           D:\cangjie\runtime\lib\windows_x86_64_llvm
           C:\Users\bob\.cjpm\bin
           ```

    5. 单击 “确定” 按钮，退出 “环境变量” 窗口；

    6. 单击 “确定” 按钮，完成设置。

    > **注意：**
    >
    > 设置完成后可能需要重启命令行窗口或重启系统以让设置生效。

    配置完成后 Windows 命令提示符（CMD）或 PowerShell 启动即可直接使用仓颉编译工具链。

### 卸载与更新

- 如果选择 `exe` 格式的安装包进行的安装，运行仓颉安装目录下的 `unins000.exe` 可执行文件，跟随卸载向导点击操作，即可完成卸载。

- 如果选择 `zip` 格式的安装包进行的安装，删除仓颉工具链的安装包目录，同时移除上述环境变量设置（若有），即可完成卸载。

若需要更新仓颉工具链，需要先卸载当前版本，然后按上述指导重新安装最新版本的仓颉工具链。


---

<!-- Content from source_zh_cn/first_understanding/hello_world.md -->
# 运行第一个仓颉程序

万事俱备，开始编写和运行第一个仓颉程序吧！

首先，请在适当目录下新建一个名为 `hello.cj` 的文本文件，并向文件中写入以下仓颉代码：

<!-- verify -->

```cangjie
// hello.cj
main() {
    println("你好，仓颉")
}
```

在这段代码中，使用了仓颉的注释语法，可以在 `//` 符号之后写单行注释，也可以在一对 `/*` 和 `*/` 符号之间写多行注释，这与 C/C++ 等语言的注释语法相同。注释内容不影响程序的编译和运行。

然后，请在此目录下执行如下命令：

```bash
cjc hello.cj -o hello
```

这里仓颉编译器会将 `hello.cj` 中的源代码编译为此平台上的可执行文件 `hello`，在命令行环境中运行此文件，将看到程序输出了如下内容：

```text
你好，仓颉
```

> **注意：**
>
> 以上编译命令是针对 Linux 和 macOS 平台的，如果使用 Windows 平台，只需要将编译命令改为 `cjc hello.cj -o hello.exe` 即可。


---

<!-- Content from source_zh_cn/basic_programming_concepts/identifier.md -->
# 标识符

在仓颉编程语言中，开发者可以给一些程序元素命名，这些名字被称为“标识符”。

学习标识符之前，需要了解一些 Unicode 字符集概念。在 Unicode 标准中，`XID_Start` 和 `XID_Continue` 属性用于标记可以作为 Unicode 标识符（Identifier）的起始字符和后续字符，其详细定义请参见 [Unicode 标准文档](https://www.unicode.org/reports/tr31/tr31-37.html)。其中， `XID_Start` 包含中文和英文等字符，`XID_Continue` 包含中文、英文和阿拉伯数字等字符。仓颉语言使用 Unicode 标准 15.0.0 。

仓颉编程语言的标识符分为普通标识符和原始标识符两类，它们遵从不同的命名规则。

**普通标识符**不能和仓颉关键字相同，其取自以下两类字符序列：

- 由 `XID_Start` 字符开头，后接任意长度的 `XID_Continue` 字符。
- 由一个`_`开头，后接至少一个 `XID_Continue` 字符。

仓颉把所有标识符识别为 [Normalization Form C (NFC)](https://www.unicode.org/reports/tr15/tr15-53.html) 后的形式。两个标识符如果在 NFC 后相等，则被认为是相同的标识符。

例如，以下每行字符串都是合法的普通标识符：

```text
abc
_abc
abc_
a1b2c3
a_b_c
a1_b2_c3
仓颉
__こんにちは
```

以下每行字符串都是不合法的普通标识符：

```text
ab&c  // & 不是 XID_Continue 字符
3abc  // 阿拉伯数字不是 XID_Start 字符，因此，数字不能作为起始字符
_     // _ 后至少需要有一个 XID_Continue 字符
while // while 是仓颉关键字，普通标识符不能使用仓颉关键字
```

**原始标识符**是在普通标识符或仓颉关键字的首尾加上一对反引号，主要用于将仓颉关键字作为标识符的场景。

例如，以下每行字符串都是合法的原始标识符：

```text
`abc`
`_abc`
`a1b2c3`
`if`
`while`
`à֮̅̕b`
```

以下每行字符串，由于反引号内的部分是不合法的普通标识符，所以它们整体也是不合法的原始标识符：

```text
`ab&c`
`3abc`
```


---

<!-- Content from source_zh_cn/basic_programming_concepts/program_structure.md -->
# 程序结构

通常，开发者会在扩展名为 `.cj` 的文本文件中编写仓颉程序，这些程序和文件也被称为源代码和源文件。在程序开发的最后阶段，这些源代码将被编译为特定格式的二进制文件。

在仓颉程序的顶层作用域中，可以定义一系列的变量、函数和自定义类型（如 `struct`、`class`、`enum` 和 `interface` 等），其中的变量和函数分别被称为**全局变量**和**全局函数**。如果要将仓颉程序编译为可执行文件，需要在顶层作用域中定义一个 `main` 函数作为**程序入口**，它可以有 `Array<String>` 类型的参数，也可以没有参数，它的返回值类型可以是整数类型或 `Unit` 类型。

> **注意：**
>
> 定义 `main` 函数时，不需要写 `func` 修饰符。此外，如果需要获取程序启动时的命令行参数，可以声明和使用 `Array<String>` 类型参数。

例如，在以下程序中，在顶层作用域定义了全局变量 `a` 和全局函数 `b`，还有自定义类型 `C`、`D` 和 `E`，以及作为程序入口的 `main` 函数。

<!-- compile -->

```cangjie
// example.cj
let a = 2023
func b() {}
struct C {}
class D {}
enum E { F | G }

main() {
    println(a)
}
```

在非顶层作用域中不能定义上述自定义类型，但可以定义变量和函数，称之为**局部变量**和**局部函数**。特别地，对于定义在自定义类型中的变量和函数，称之为**成员变量**和**成员函数**。

> **注意：**
>
> `enum` 和 `interface` 中仅支持定义成员函数，不支持定义成员变量。

例如，在以下程序中，在顶层作用域定义了全局函数 `a` 和自定义类型 `A`，在函数 `a` 中定义了局部变量 `b` 和局部函数 `c`，在自定义类型 `A` 中定义了成员变量 `b` 和成员函数 `c`。

<!-- verify -->

```cangjie
// example.cj
func a() {
    let b = 2023
    func c() {
        println(b)
    }
    c()
}

class A {
    let b = 2024
    public func c() {
        println(b)
    }
}

main() {
    a()
    A().c()
}
```

运行以上程序，将输出：

```text
2023
2024
```

## 变量

在仓颉编程语言中，一个变量由对应的变量名、数据（值）和若干属性构成，开发者通过变量名访问变量对应的数据，但访问操作需要遵从相关属性的约束（如数据类型、可变性和可见性等）。

变量定义的具体形式为：

```text
修饰符 变量名: 变量类型 = 初始值
```

其中**修饰符**用于设置变量的各类属性，可以有一个或多个，常用的修饰符包括：

- 可变性修饰符：`let` 与 `var`，分别对应不可变和可变属性，可变性决定了变量被初始化后其值还能否改变，仓颉变量也由此分为不可变变量和可变变量两类。
- `const` 修饰符：`const` 是一种特殊的变量修饰符。它用于声明常量，要求在声明时必须初始化，一旦被赋值，其值就不能被改变。这与`let` 修饰符类似，都具有不可变的特性，但`const` 在使用上有更严格的限制。
- 可见性修饰符：`private` 与 `public` 等，影响全局变量和成员变量的可引用范围，详见后续章节的相关介绍。
- 静态性修饰符：`static`，影响成员变量的存储和引用方式，详见后续章节的相关介绍。

变量均支持赋值操作符（`=`），与类型无关。`let` 修饰的变量只能被赋值一次，即初始化；`var` 修饰的变量可以被多次赋值。

在定义仓颉变量时，可变性修饰符是必要的，在此基础上，还可以根据需要添加其他修饰符。

- **变量名**应是一个合法的仓颉标识符。
- **变量类型**指定了变量所持有数据的类型。当初始值具有明确类型时，可以省略变量类型标注，此时编译器可以自动推断出变量类型。
- **初始值**是一个仓颉表达式，用于初始化变量，如果标注了变量类型，需要保证初始值类型和变量类型一致。在定义全局变量或静态成员变量时，必须指定初始值。在定义局部变量或实例成员变量时，可以省略初始值，但需要标注变量类型，同时要在此变量被引用前完成初始化，否则编译会报错。

例如，下列程序定义了三个 `Int64` 类型的变量（分别为不可变变量 `a` 、可变变量 `b` 和 const 变量 `c` ）。随后修改了变量 `b` 的值，同时将 `b` 的值赋值给`a`，并调用 `println` 函数打印 `a`， `b` 和`c` 的值。

<!-- verify -->

```cangjie
main() {
    let a: Int64
    var b: Int64 = 14
    const c: Int64 = 13
    b = 12
    a = b // A variable modified by let can only be assigned once, that is, initialized
    println("${a}, ${b}, ${c}")
}
```

编译运行此程序，将输出：

```text
12, 12, 13
```

如果尝试修改不可变变量，编译时会报错，例如：

<!-- compile.error -->

```cangjie
main() {
    let pi: Float64 = 3.14159
    pi = 2.71828 // Error, cannot assign to immutable value
}
```

当初始值具有明确类型时，可以省略变量类型标注，例如：

<!-- verify -->

```cangjie
main() {
    let a: Int64 = 2023
    let b = a
    println("a - b = ${a - b}")
}
```

其中变量 `b` 的类型可以由其初值 `a` 的类型自动推断为 `Int64`，所以此程序也可以被正常编译和运行，将输出：

```text
a - b = 0
```

在定义局部变量时，可以不进行初始化，但一定要在变量被引用前赋予初值，例如：

<!-- verify -->

```cangjie
main() {
    let text: String
    text = "仓颉造字"
    println(text)
}
```

编译运行此程序，将输出：

```text
仓颉造字
```

在定义全局变量和静态成员变量时必须初始化，否则编译会报错，例如：

<!-- compile.error -->

```cangjie
let global: Int64 // Error, variable in top-level scope must be initialized

main(): Unit{

}
```

<!-- compile.error -->

```cangjie
class Player {
    static let score: Int32 // Error, static variable 'score' needs to be initialized when declaring
}
```

需要注意的是，当编译器无法判断某些场景是否一定会被初始化或无法判断是否重复初始化了不可变变量时，会倾向于保守策略进行编译报错，见如下示例：

<!-- compile.error -->

```cangjie
func calc(a: Int32){
    println(a)
    return a * a
}
main() {
    let a: String
    if(calc(32) == 0){
      a = "1"
    }
    a = "2" // Error, cannot assign to immutable value
}
```

此外，对于 [try-catch](../error_handle/handle.md#普通-try-表达式) 场景，编译器会假设 try 块总是全部被执行，且总是抛异常，从而进行相关报错，见如下示例：
<!-- compile.error -->

```cangjie
main() {
    let a: String
    try {
        a = "1"
    } catch (_) {
        a = "2" // Error, cannot assign to immutable value
    }
}
```

## `const` 变量

`const` 变量是一种特殊的变量，它以关键字 `const` 修饰，定义在编译时完成求值，并且在运行时不可改变的变量。例如，下面的例子定义了万有引力常数 `G`：

<!-- verify -const -->

```cangjie
const G = 6.674e-11
```

`const` 变量可以省略类型标注，但是不可省略初始化表达式。`const` 变量可以是全局变量，局部变量，静态成员变量。但是 `const` 变量不能在扩展中定义。`const` 变量可以访问对应类型的所有实例成员，也可以调用对应类型的所有非 `mut` 实例成员函数。

下例定义了一个 `struct`，记录行星的质量和半径，同时定义了一个 `const` 成员函数 `gravity` 用来计算该行星对距离为 `r` 质量为 `m` 的物体的万有引力：

<!-- verify -const -->

```cangjie
struct Planet {
    const Planet(let mass: Float64, let radius: Float64) {}

    const func gravity(m: Float64, r: Float64) {
        G * mass * m / r**2
    }
}

main() {
    const myMass = 71.0
    const earth = Planet(5.972e24, 6.378e6)
    println(earth.gravity(myMass, earth.radius))
}
```

编译执行得到地球对地面上一个质量为 71 kg 的成年人的万有引力：

<!-- verify -const -->

```text
695.657257
```

`const` 变量初始化后该类型实例的所有成员都是 `const` 的（深度 `const`，包含成员的成员），因此不能被用于左值。

<!-- compile.error -->

```cangjie
main() {
    const myMass = 71.0
    myMass = 70.0 // Error, cannot assign to immutable value
}
```

### 值类型和引用类型变量

从编译器实现层面看，任何变量总会关联一个值（一般是通过内存地址/寄存器关联），只是在使用时，对有些变量，将直接取用这个值本身，这被称为**值类型变量**；而对另一些变量，将这个值作为索引、取用这个索引指示的数据，这被称为**引用类型变量**。值类型变量通常在线程栈上分配，每个变量都有自己的数据副本；引用类型变量通常在进程堆中分配，多个变量可引用同一数据对象，对一个变量执行的操作可能会影响其他变量。

从语言层面看，值类型变量对它所绑定的数据/存储空间是独占的，而引用类型变量所绑定的数据/存储空间可以和其他引用类型变量共享。

基于上述原理，在使用值类型变量和引用类型变量时，会存在一些行为差异，以下几点值得注意：

1. 在给值类型变量赋值时，一般会产生拷贝操作，且原来绑定的数据/存储空间会被覆盖。在给引用类型变量赋值时，只是改变了引用关系，原来绑定的数据/存储空间不会被覆盖。
2. 用 `let` 定义的变量，要求变量被初始化后都不能再赋值。对于引用类型，这只是限定了引用关系不可改变，但是所引用的数据是可以被修改的。

在仓颉编程语言中，`class` 和 `Array` 等类型属于引用类型，其他基础数据类型和 `struct` 等类型属于值类型。

例如，以下程序演示了 `struct` 和 `class` 类型变量的行为差异：

<!-- verify -->

```cangjie
struct Copy {
    var data = 2012
}

class Share {
    var data = 2012
}

main() {
    let c1 = Copy()
    var c2 = c1
    c2.data = 2023
    println("${c1.data}, ${c2.data}")

    let s1 = Share()
    let s2 = s1
    s2.data = 2023
    println("${s1.data}, ${s2.data}")
}
```

运行以上程序，将输出：

```text
2012, 2023
2023, 2023
```

由此可以看出，对于值类型的 `Copy` 类型变量，在赋值时总是获取 `Copy` 实例的拷贝，如 `c2 = c1`，随后对 `c2` 成员的修改并不影响 `c1`。对于引用类型的 `Share` 类型变量，在赋值时将建立变量和实例之间的引用关系，如 `s2 = s1`，随后对 `s2` 成员的修改会影响 `s1`。

如果将以上程序中的 `var c2 = c1` 改成 `let c2 = c1`，则编译会报错，例如：

<!-- compile.error -->

```cangjie
struct Copy {
    var data = 2012
}

main() {
    let c1 = Copy()
    let c2 = c1
    c2.data = 2023 // Error, cannot assign to immutable value
}
```

## 作用域

在前文中，初步介绍了如何给仓颉程序元素命名。实际上，除了变量，还可以给函数和自定义类型等命名，在程序中将使用这些名字访问对应的程序元素。

但在实际应用中，需要考虑一些特殊情况：

- 当程序规模较大时，那些简短的名字很容易重复，即产生命名冲突。
- 结合运行时考虑，在有些代码片段中，另一些程序元素是无效的，对它们的引用会导致运行时错误。例如，某些变量在超出其所在作用域之后。
- 在某些逻辑构造中，为了表达元素之间的包含关系，不应通过名字直接访问子元素，而是要通过其父元素名间接访问。

为了应对这些问题，现代编程语言引入了“作用域”的概念及设计，将名字和程序元素的绑定关系限制在一定范围里。不同作用域之间可以是并列或无关的，也可以是嵌套或包含关系。一个作用域将明确开发者能用哪些名字访问哪些程序元素，具体规则是：

1. 当前作用域中定义的程序元素与名字的绑定关系，在当前作用域和其内层作用域中是有效的，可以通过此名字直接访问对应的程序元素。
2. 内层作用域中定义的程序元素与名字的绑定关系，在外层作用域中无效。
3. 内层作用域可以使用外层作用域中的名字重新定义绑定关系，根据规则 1，此时内层作用域中的命名相当于遮盖了外层作用域中的同名定义，对此称内层作用域的级别比外层作用域的级别高。

在仓颉编程语言中，用一对大括号“\{\}”包围一段仓颉代码，即构造了一个新的作用域，其中可以继续使用大括号“\{\}”包围仓颉代码，由此产生了嵌套作用域，这些作用域均服从上述规则。特别的，在一个仓颉源文件中，不被任何大括号“\{\}”包围的代码，它们所属的作用域被称为“顶层作用域”，即当前文件中“最外层”的作用域，按上述规则，其作用域级别最低。

> **注意：**
>
> 仓颉不允许使用单独的大括号“\{\}”，大括号必须依赖 if、match、函数体、类体、结构体等其他语法结构存在。

例如在以下名为 `test.cj` 的仓颉源文件里，在顶层作用域中定义了名字 `element`，它和字符串“仓颉”绑定，而 `main` 和 `if` 引导的代码块中也定义了名字 `element`，分别对应整数 9 和整数 2023。由上述作用域规则，在第 4 行，`element` 的值为“仓颉”，在第 8 行，`element` 的值为 2023，在第 10 行，`element` 的值为 9。

<!-- verify -->

```cangjie
// test.cj
let element = "仓颉"
main() {
    println(element)
    let element = 9
    if (element > 0) {
        let element = 2023
        println(element)
    }
    println(element)
}
```

运行以上程序，将输出：

```text
仓颉
2023
9
```


---

<!-- Content from source_zh_cn/basic_programming_concepts/expression.md -->
# 表达式

在一些传统编程语言中，一个表达式由一个或多个操作数（operand）通过零个或多个操作符（operator）组合而成。表达式总是隐含着一个计算过程，因此每个表达式都会有一个计算结果。对于只有操作数而没有操作符的表达式，其计算结果就是操作数自身。对于包含操作符的表达式，计算结果是对操作数执行操作符定义的计算而得到的值。在这种定义下的表达式也被称为算术运算表达式。操作符优先级请参见[操作符](../Appendix/operator.md)章节。

在仓颉编程语言中，简化并延伸了表达式的传统定义——凡是可求值的语言元素都是表达式。因此，仓颉不仅有传统的算术运算表达式，还有条件表达式、循环表达式和 `try` 表达式等，它们都可以被求值，并作为值去使用，如作为变量定义的初值和函数实参等。此外，因为仓颉是强类型的编程语言，所以仓颉表达式不仅可求值，还有确定的类型。

> **注意：**
>
> 为了清晰地划分不同的程序语句或表达式，仓颉采用分号（`;`）进行分隔。如果一条语句独占一行，该分号可以省略，但一行存在多条语句，这些语句必须用分号进行分隔。

仓颉编程语言的各种表达式将在后续章节中逐一介绍，本节介绍最常用的条件表达式、循环表达式以及部分控制转移表达式（`break`、`continue`）。

任何一段程序的执行流程，只会涉及三种基本结构——顺序结构、分支结构和循环结构。实际上，分支结构和循环结构，是由某些指令控制当前顺序执行流产生跳转而得到的，它们让程序能够表达更复杂的逻辑。在仓颉中，这种用来控制执行流的语言元素就是条件表达式和循环表达式。

在仓颉编程语言中，条件表达式是 `if` 表达式，其值与类型需要根据使用场景来确定。循环表达式有三种：`for-in` 表达式、`while` 表达式和 `do-while` 表达式，它们的类型都是 `Unit`，值为 `()`。

在仓颉程序中，由一对大括号“{}”包围起来的一组表达式，被称为“代码块”，它将作为程序的一个顺序执行流，其中的表达式将按编码顺序依次执行。如果代码块中有至少一个表达式，规定此代码块的值与类型等于其中最后一个表达式的值与类型，如果代码块中没有表达式，规定这种空代码块的类型为 `Unit`，值为 `()`。

> **注意：**
>
> 代码块本身不是一个表达式，不能被单独使用，它将依附于函数、条件表达式和循环表达式等执行和求值。

## if 表达式

`if` 表达式的基本形式为：

```text
if (条件) {
  分支 1
} else {
  分支 2
}
```

其中“条件”可以是一个布尔类型的表达式，或者一个 “let pattern” （语法糖），或者多个 “let pattern” 和布尔类型的表达式之间通过逻辑与或逻辑或直接连接形成的表达式，涉及 “let pattern” 的介绍和示例，参照[涉及 “let pattern” 的“条件”示例](#涉及-let-pattern-的条件示例)。

当表达式和模式匹配成功时，该模式匹配的值为 true，此时执行 `if` 分支对应的代码块；反之，为 false，执行 `else` 分支代码块，`else` 分支可以不存在。

“分支 1”和“分支 2”是两个代码块。`if` 表达式将按如下规则执行：

1. 计算“条件”表达式，如果值为 `true` 则转到第 2 步，值为 `false` 则转到第 3 步。
2. 执行“分支 1”，转到第 4 步。
3. 执行“分支 2”，转到第 4 步。
4. 继续执行 `if` 表达式后面的代码。

在一些场景中，可能只关注条件成立时该做些什么，所以 `else` 和对应的代码块是允许省略的。

如下程序演示了 `if` 表达式的基本用法：

<!-- run -->

```cangjie
import std.random.Random

main() {
    let number: Int8 = Random().nextInt8()
    println(number)
    if (number % 2 == 0) {
        println("偶数")
    } else {
        println("奇数")
    }
}
```

在这段程序中，使用仓颉标准库的 `random` 包生成了一个随机整数，然后使用 `if` 表达式判断这个整数是否能被 2 整除，并在不同的条件分支中打印“偶数”或“奇数”。

仓颉编程语言是强类型的，`if` 表达式的条件只能是布尔类型，不能使用整数或浮点数等类型，和 C 语言等不同，仓颉不以条件取值是否为 0 作为分支选择依据，例如以下程序将编译报错（此外，后文的[错误的表达式示例](#错误的表达式示例)补充了更多错误的表达式用例场景，可对比参照）：

<!-- compile.error -->

```cangjie
main() {
    let number = 1
    if (number) { // 编译错误，类型不匹配
        println("非零数")
    }
}
```

在许多场景中，当一个条件不成立时，可能还要判断另一个或多个条件，再执行对应的动作。仓颉允许在 `else` 之后跟随新的 `if` 表达式，由此支持多级条件判断和分支执行，例如：

<!-- run -->

```cangjie
import std.random.Random

main() {
    let speed = Random().nextFloat64() * 20.0
    println("${speed} km/s")
    if (speed > 16.7) {
        println("第三宇宙速度，鹊桥相会")
    } else if (speed > 11.2) {
        println("第二宇宙速度，嫦娥奔月")
    } else if (speed > 7.9) {
        println("第一宇宙速度，腾云驾雾")
    } else {
        println("脚踏实地，仰望星空")
    }
}
```

`if` 表达式的值与类型，需要根据使用形式与场景来确定：

- 当含 `else` 分支的 `if` 表达式被求值时，需要根据求值上下文确定 `if` 表达式的类型：

    - 如果上下文明确要求值类型为 `T`，则 `if` 表达式各分支代码块的类型必须是 `T` 的子类型，这时 `if` 表达式的类型被确定为 `T`，如果不满足子类型约束，编译会报错。具体示例如下，由于变量 `b` 的类型 Int64 与各分支代码块的类型不满足子类型约束，因此编译报错：

        <!-- compile.error -->

        ```cangjie
        var a = 10
        var b: Int64 = if(a == 10) { // Error, mismatched types
            "this is 10"
        }else {
            "this is not 10"
        }
        ```

    - 如果上下文没有明确的类型要求，则 `if` 表达式的类型是其各分支代码块类型的最小公共父类型，如果最小公共父类型不存在，编译会报错。具体示例如下，由于字符串和数值类型不存在最小公共父类型，因此编译报错：

        <!-- compile.error -->

        ```cangjie
        var a = 10
        var b = if(a == 10) { // Error, types Struct-String and Int64 of the two branches of this 'if' expression mismatch
            "this is 10"
        }else {
            20
        }
        ```

  如果编译通过，则 `if` 表达式的值就是所执行分支代码块的值。

- 如果含 `else` 分支的 `if` 表达式没有被求值，在这种场景里，开发者一般只想在不同分支里做不同操作，不会关注各分支最后一个表达式的值与类型，为了不让上述类型检查规则影响这一思维习惯，仓颉规定这种场景下的 `if` 表达式类型为 `Unit`、值为 `()`，且各分支不参与上述类型检查。
- 对于不含 `else` 分支的 `if` 表达式，由于 `if` 分支也可能不被执行，所以规定这类 `if` 表达式的类型为 `Unit`、值为 `()`。

例如，以下程序基于 `if` 表达式求值，模拟一次简单的模数转换过程：

<!-- run -->

```cangjie
main() {
    let zero: Int8 = 0
    let one: Int8 = 1
    let voltage = 5.0
    let bit = if (voltage < 2.5) {
        zero
    } else {
        one
    }
}
```

在以上程序中，`if` 表达式作为变量定义的初值使用，由于变量 `bit` 没有被标注类型、需要从初值中推导，所以 `if` 表达式的类型取为两个分支代码块类型的最小公共父类型。根据前文对“代码块”的介绍，可知两个分支代码块类型都是 `Int8`，所以 `if` 表达式的类型被确定为 `Int8`，其值为所执行分支即 `else` 分支代码块的值，所以变量 `bit` 的类型为 `Int8`、值为 1。

### 涉及 “let pattern” 的“条件”示例

“let pattern” 属于语法糖。一个 “let pattern” 的构成为 `let pattern <- expression`，其中各字段含义为：

- `pattern` ：模式，用于匹配 `expression` 的值类型和内容。
- `<-` ：模式匹配操作符。
- `expression` ：表达式，该表达式求值后，再和模式进行匹配。`expression` 表达式的优先级不能低于 `..` 运算符，但是可以用 `()` 改变优先级。运算符优先级请参见[操作符](../Appendix/operator.md)。

此处介绍“条件”是两个 “let pattern” 进行逻辑与或逻辑或操作以及 “let pattern” 与其他表达式进行逻辑与或逻辑或操作的示例。

<!-- run -expression_example5 -->

```cangjie
main() {
    let a = Some(3)
    let c = if (let Some(b) <- a) {
            1 // 模式匹配成功，c = 1
        } else {
            2
        }
    let d = Some(1)

    if (let Some(e) <- a && let Some(f) <- d) { // 两种模式都匹配，条件的值为真
        println("${e} ${f}") // print 3 1
    }

    if (let Some(f) <- d && f > 3) { // 模式匹配；f = 1，f > 3 检查失败，跳转到 else 分支
        println("${f}")
    } else {
        println("d is None or value of d is less or equal to 3") // 打印该行
    }

    if (let Some(_) <- a || let Some(_) <- d) { // 枚举模式通过||连接，没有变量绑定，正确
        println("at least one of a and d is Some") // 打印该行
    } else {
        println("both a and d are None")
    }

    let g = 3
    if (let Some(_) <- a || g > 1) {
        println("this") // 打印该行
    } else {
        println("that")
    }
}
```

“let pattern” 中表达式部分运算符优先级不能低于 `..` 运算符，此处介绍对应的错误和正确示例。其中， [`Option` 类型](../enum_and_pattern_match/option_type.md)的相关介绍在后文给出。

<!-- compile.error -->

```cangjie
if (let Some(a) <- fun() as Option<Int64>) {}   // 解析错误，`as` 的优先级低于  `..`
if (let Some(a) <- (fun() as Option<Int64>)) {} // 正确
if (let Some(a) <- b && a + b > 3) {}           // 正确，解析为 (let Some(a) <- b) && (a + b > 3)
if (let m <- 0..generateSomeInt()) {}           // 正确
```

### 错误的表达式示例

此处介绍错误的“条件”示例。

<!-- compile.error -->

```cangjie
if (let Some(a) <- b || a > 1) {} // 由 `||` 连接的条件不能使用会绑定变量的 enum 模式
if (let Some(a) <- b && a + 1) {} // `&&` 右侧既不是 let pattern，也不是类型为 Bool 的普通表达式
if (a > 3 && let Some(a) <- b) {} // a 由 Some(a) pattern 绑定，不能在绑定它的 pattern 左侧使用
if (let Some(a) <- b && a > 3) {
    println("${a} > 3")
} else {
    println("${a} < 3") // a 只能在 if 分支使用，不能在 else 分支使用
}
if (let Some(a) <- b where a > 3) {} // 使用 `&&` 表示条件检查，而不是 `where`
```

## while 表达式

`while` 表达式的基本形式为：

```text
while (条件) {
  循环体
}
```

其中“条件”同 `if` 表达式的“条件”，“循环体”是一个代码块。`while` 表达式将按如下规则执行：

1. 计算“条件”表达式，如果值为 `true` 则转第 2 步，值为 `false` 转第 3 步。
2. 执行“循环体”，转第 1 步。
3. 结束循环，继续执行 `while` 表达式后面的代码。

例如，以下程序使用 `while` 表达式，基于二分法，近似计算数字 2 的平方根：

<!-- verify -->

```cangjie
main() {
    var root = 0.0
    var min = 1.0
    var max = 2.0
    var error = 1.0
    let tolerance = 0.1 ** 10

    while (error ** 2 > tolerance) {
        root = (min + max) / 2.0
        error = root ** 2 - 2.0
        if (error > 0.0) {
            max = root
        } else {
            min = root
        }
    }
    println("2 的平方根约等于：${root}")
}
```

运行以上程序，将输出：

```text
2 的平方根约等于：1.414215
```

## do-while 表达式

`do-while` 表达式的基本形式为：

```text
do {
  循环体
} while (条件)
```

其中“条件”是布尔类型表达式，“循环体”是一个代码块。`do-while` 表达式将按如下规则执行：

1. 执行“循环体”，转第 2 步。
2. 计算“条件”表达式，如果值为 `true` 则转第 1 步，值为 `false` 转第 3 步。
3. 结束循环，继续执行 `do-while` 表达式后面的代码。

例如，以下程序使用 `do-while` 表达式，基于蒙特卡洛算法，近似计算圆周率的值：

<!-- run -->

```cangjie
import std.random.Random

main() {
    let random = Random()
    var totalPoints = 0
    var hitPoints = 0

    do {
        // 在 ((0, 0), (1, 1)) 这个正方形中随机取点
        let x = random.nextFloat64()
        let y = random.nextFloat64()
        // 判断是否落在正方形内接圆里
        if ((x - 0.5) ** 2 + (y - 0.5) ** 2 < 0.25) {
            hitPoints++
        }
        totalPoints++
    } while (totalPoints < 1000000)

    let pi = 4.0 * Float64(hitPoints) / Float64(totalPoints)
    println("圆周率近似值为：${pi}")
}
```

运行以上程序，将输出：

```text
圆周率近似值为：3.141872
```

> **说明：**
>
> 由于算法涉及随机数，所以每次运行程序输出的数值可能都不同，但都会约等于 3.14。

## for-in 表达式

`for-in` 表达式可以遍历那些扩展了迭代器接口 `Iterable<T>` 的类型实例。`for-in` 表达式的基本形式为：

```text
for (迭代变量 in 序列) {
  循环体
}
```

其中“循环体”是一个代码块。“迭代变量”是单个标识符或由多个标识符构成的元组，用于绑定每轮遍历中由迭代器指向的数据，可以作为“循环体”中的局部变量使用。“序列”是一个表达式，它只会被计算一次，遍历是针对此表达式的值进行的，其类型必须扩展了迭代器接口 `Iterable<T>`。`for-in` 表达式将按如下规则执行：

1. 计算“序列”表达式，将其值作为遍历对象，并初始化遍历对象的迭代器。
2. 更新迭代器，如果迭代器终止，转第 4 步，否则转第 3 步。
3. 将当前迭代器指向的数据与“迭代变量”绑定，并执行“循环体”，转第 2 步。
4. 结束循环，继续执行 `for-in` 表达式后面的代码。

> **说明：**
>
> 仓颉内置的区间和数组等类型已经扩展了 `Iterable<T>` 接口。

例如，以下程序使用 `for-in` 表达式，遍历中国地支字符构成的[数组](../basic_data_type/array.md) `noumenonArray`，输出农历 2024 年各月的干支纪法：

<!-- verify -->

```cangjie
main() {
    let metaArray = [r'甲', r'乙', r'丙', r'丁', r'戊', r'己', r'庚', r'辛', r'壬', r'癸']
    let noumenonArray = [r'寅', r'卯', r'辰', r'巳', r'午', r'未', r'申', r'酉', r'戌', r'亥', r'子', r'丑']
    let year = 2024

    // 年份对应的天干索引
    let metaOfYear = ((year % 10) + 10 - 4) % 10
    // 此年首月对应的天干索引
    var index = (2 * metaOfYear + 3) % 10 - 1

    println("农历 2024 年各月干支：")
    for (noumenon in noumenonArray) {
        print("${metaArray[index]}${noumenon} ")
        index = (index + 1) % 10
    }
}
```

其中 `r` 开头的字符表示[字符类型字面量](../basic_data_type/characters.md#字符类型字面量)。运行以上程序，将输出：

```text
农历 2024 年各月干支：
丙寅 丁卯 戊辰 己巳 庚午 辛未 壬申 癸酉 甲戌 乙亥 丙子 丁丑
```

### 遍历区间

`for-in` 表达式可以遍历区间类型实例，例如：

<!-- verify -->

```cangjie
main() {
    var sum = 0
    for (i in 1..=100) {
        sum += i
    }
    println(sum)
}
```

运行以上程序，将输出：

```text
5050
```

关于区间类型的详细内容，请参见基本数据类型[区间类型](../basic_data_type/range.md)。

### 遍历元组构成的序列

如果一个序列的元素是元组类型，则使用 `for-in` 表达式遍历时，“迭代变量”可以写成元组形式，以此实现对序列元素的解构，例如：

<!-- verify -->

```cangjie
main() {
    let array = [(1, 2), (3, 4), (5, 6)]
    for ((x, y) in array) {
        println("${x}, ${y}")
    }
}
```

运行以上程序，将输出：

```text
1, 2
3, 4
5, 6
```

### 迭代变量不可修改

在 `for-in` 表达式的循环体中，不能修改迭代变量，例如以下程序在编译时会报错：

<!-- compile.error -->

```cangjie
main() {
    for (i in 0..5) {
        i = i * 10 // 错误，不能对已初始化的 `let` 常量赋值
        println(i)
    }
}
```

### 使用通配符 _ 代替迭代变量

在一些应用场景中，只需要循环执行某些操作，但并不使用迭代变量，这时可以使用通配符 `_` 代替迭代变量，例如：

<!-- verify -->

```cangjie
main() {
    var number = 2
    for (_ in 0..5) {
        number *= number
    }
    println(number)
}
```

运行以上程序，将输出：

```text
4294967296
```

> **注意：**
>
> 在这种场景下，如果使用普通的标识符定义迭代变量，编译会输出“unused variable”告警，使用通配符 `_` 则可以避免这一告警。

### where 条件

在部分循环遍历场景中，对于特定取值的迭代变量，可能需要直接跳过，进入下一轮循环。虽然可以使用 `if` 表达式和 `continue` 表达式在循环体中实现这一逻辑，但仓颉为此提供了更便捷的表达方式——可以在所遍历的“序列”之后用 `where` 关键字引导一个布尔表达式，这样在每次将进入循环体执行前，会先计算此表达式。如果值为 `true` 则执行循环体，反之直接进入下一轮循环。例如：

<!-- verify -->

```cangjie
main() {
    for (i in 0..8 where i % 2 == 1) { // i 为奇数才会执行循环体
        println(i)
    }
}
```

运行以上程序，将输出：

```text
1
3
5
7
```

## break 与 continue 表达式

在循环结构的程序中，有时需要根据特定条件提前结束循环或跳过本轮循环，为此仓颉引入了 `break` 与 `continue` 表达式，它们可以出现在循环表达式的循环体中，`break` 用于终止当前循环表达式的执行、转去执行循环表达式之后的代码，`continue` 用于提前结束本轮循环、进入下一轮循环。`break` 与 `continue` 表达式的类型都是 [`Nothing`](../basic_data_type/nothing.md)。

例如，以下程序使用 `for-in` 表达式和 `break` 表达式，在给定的整数数组中，找到第一个能被 5 整除的数字：

<!-- verify -->

```cangjie
main() {
    let numbers = [12, 18, 25, 36, 49, 55]
    for (number in numbers) {
        if (number % 5 == 0) {
            println(number)
            break
        }
    }
}
```

当 `for-in` 迭代至 `numbers` 数组的第三个数 25 时，由于 25 可以被 5 整除，所以将执行 `if` 分支中的 `println` 和 `break`，`break` 将终止 `for-in` 循环，`numbers`中的后续数字不会被遍历到。因此运行以上程序，将输出：

```text
25
```

以下程序使用 `for-in` 表达式和 `continue` 表达式，将给定整数数组中的奇数打印出来：

<!-- verify -->

```cangjie
main() {
    let numbers = [12, 18, 25, 36, 49, 55]
    for (number in numbers) {
        if (number % 2 == 0) {
            continue
        }
        println(number)
    }
}
```

在循环迭代中，当 `number` 是偶数时，`continue` 将被执行，这会提前结束本轮循环，进入下一轮循环，`println` 不会被执行。因此运行以上程序，将输出：

```text
25
49
55
```


---

<!-- Content from source_zh_cn/basic_programming_concepts/function.md -->
# 函数

仓颉使用关键字 `func` 来表示函数定义的开始，`func` 之后依次是函数名、参数列表、可选的函数返回值类型、函数体。其中，函数名可以是任意的合法标识符，参数列表定义在一对圆括号内（多个参数间使用逗号分隔），参数列表和函数返回值类型（如果存在）之间使用冒号分隔，函数体定义在一对花括号内。

函数定义举例：

<!-- compile -->

```cangjie
func add(a: Int64, b: Int64): Int64 {
    return a + b
}
```

上例中定义了一个名为 `add` 的函数，其参数列表由两个 `Int64` 类型的参数 `a` 和 `b` 组成，函数返回值类型为 `Int64`，函数体中将 `a` 和 `b` 相加并返回。

详细介绍可参见[定义函数](../function/define_functions.md)模块介绍。


---

<!-- Content from source_zh_cn/basic_data_type/basic_operators.md -->
# 基本操作符

操作符是执行特定的数学运算或逻辑操作的符号。例如，数学运算符号的加号（`+`）可将两个数相加（如：`let i = 1 + 2`），逻辑操作符号的逻辑与（`&&`）可用于组合并确保多个条件判断均满足（如：`if (i > 0 && i < 10)`）。

仓颉编程语言不仅支持各种常用的操作符，同时为了减少常见编码错误对它们做了部分改进。如：赋值表达式（包含赋值操作符的表达式）的类型是 Unit，值是 ()，如果将 `if(a == 3)` 写成 `if(a = 3)`，赋值表达式的返回值不是布尔类型，因此会编译报错，这样可以避免将判等操作符（`==`）误写成赋值操作符（`=`）的问题。算术操作符（`+`、`-`、`*`、`/`、`%` 等）的结果会被检测并禁止值溢出，以此来避免保存变量时由于变量大于或小于其类型所能承载的范围时导致的异常结果。

仓颉编程语言还提供了区间操作符，例如 `a..b` 或 `a..=b`，这方便表达一个区间内的数值。

本章节只描述了仓颉编程语言中的基本操作符，其他操作符参见附录中的[操作符](../Appendix/operator.md)。如何进行自定义类型的操作符重载参见[操作符重载](../function/operator_overloading.md)章节。

## 赋值操作符

用于将左操作数的值修改为右操作数的值，要求右操作数的类型是左操作数类型的子类型。对赋值表达式求值时，总是先计算 `=` 右边的表达式，再计算 `=` 左边的表达式，最后进行赋值。

<!-- compile.error -->

```cangjie
main(): Int64 {
    var a = 1
    var b = 1
    a = (b = 0) // 编译错误，赋值表达式的类型是 Unit，值是 ()
    if (a = 5) { // 编译错误，赋值表达式的类型是 Unit，值是 ()
    }
    a = b = 0 // 语法错误，不支持链式使用赋值

    return 0
}
```

多赋值表达式是一种特殊的赋值表达式，多赋值表达式等号左边必须是一个 tuple（[元组](tuple.md)） ，这个 tuple 里面的元素必须都是左值，等号右边的表达式也必须是 tuple 类型，右边 tuple 每个元素的类型必须是对应位置左值类型的子类型。**值得注意的是当左侧 tuple 中出现 _ 时，表示忽略等号右侧 tuple 对应位置处的求值结果**（意味着这个位置处的类型检查总是可以通过的）。多赋值表达式可以将右边的 tuple 类型的值，一次性赋值给左边 tuple 内的对应左值，省去逐个赋值的代码。

<!-- run -->

```cangjie
main(): Int64 {
    var a: Int64
    var b: Int64
    (a, b) = (1, 2) // a = 1, b = 2
    (a, b) = (b, a) // 交换, a = 2, b = 1
    (a, _) = (3, 4) // a = 3
    (_, _) = (5, 6) // 无赋值
    return 0
}
```

## 算术操作符

仓颉编程语言支持的算术操作符包括：一元负号（`-`）、加（`+`）、减（`-`）、乘（`*`）、除（`/`）、取余（`%`）、求幂（`**`）。除了一元负号是一元前缀操作符，其他操作符均是二元中缀操作符。

一元负号（`-`）的操作数只能是数值类型的表达式。一元前缀负号表达式的值等于操作数取负的值，类型和操作数的类型相同：

<!-- compile -->

```cangjie
    let num1: Int64 = 8
    let num2 = -num1 // num2 = -8, 其数据类型为“Int64”。
    let num3 = -(-num1) // num3 = 8, 其数据类型为“Int64”。
```

对于二元操作符 `*`、`/`、`%`、`+` 和 `-`，要求两个操作数的类型相同。其中 `%` 的操作数只支持整数类型；`*`、`/`、`+` 和 `-` 的操作数可以是任意数值类型。

> **注意：**
>
> - 除法（`/`）的操作数为整数时，将非整数值向 0 的方向舍入为整数。
> - 整数取余运算 `a % b` 的值定义为 `a - b * (a / b)`。
> - 加法操作符也可用于字符串的拼接。

<!-- compile -->

```cangjie
    let a = 2 + 3    // a = 5
    let b = 3 - 1    // b = 2
    let c = 3 * 4    // c = 12
    let d = 7 / 3    // d = 2
    let e = 7 / -3   // e = -2, 当遇到“-”时，它具有更高的优先级。
    let f = -7 / 3   // f = -2
    let g = -7 / -3  // g = 2, 当遇到“-”时，它具有更高的优先级。
    let h = 4 % 3    // h = 1
    let i = 4 % -3   // i = 1, 当遇到“-”时，它具有更高的优先级。
    let j = -4 % 3   // j = -1
    let k = -4 % -3  // k = -1, 当遇到“-”时，它具有更高的优先级。

    let s1 = "abc"
    var s2 = "ABC"
    let r1 = s1 + s2 // r1 = "abcABC"
```

`**` 表示求幂运算（如 `x**y` 表示计算底数 x 的 y 次幂）。`**` 的左操作数只能为 Int64 类型或 Float64 类型。

> **注意：**
>
> 当左操作类型为 Int64 时，右操作数只能为 UInt64 类型，表达式的类型为 Int64。
> 当左操作类型为 Float64 时，右操作数只能为 Int64 类型或 Float64 类型，表达式的类型为 Float64。

<!-- compile -->

```cangjie
    let p1 = 2 ** 3                  // p1 = 8
    let p2 = 2 ** UInt64(3 ** 2)     // p2 = 512
    let p3 = 2.0 ** 3                // p3 = 8.0
    let p4 = 2.0 ** 3 ** 2           // p4 = 512.0
    let p5 = 2.0 ** 3.0              // p5 = 8.0
    let p6 = 2.0 ** 3.0 ** 2.0       // p6 = 512.0
```

## 复合赋值操作符

仓颉编程语言也提供 `**=`、`*=`、`/=`、`%=`、`+=`、`-=`、`<<=`、`>>=`、`&=`、`^=`、`|=`、`&&=` 和 `||=` 复合赋值操作符，简单示例如下：

<!-- compile -->

```cangjie
    var a: Int64 = 10
    a += 2   // a = 12
    a -= 2   // a = 10
    a **= 2  // a = 100
    a *= 2   // a = 200
    a /= 10  // a = 20
    a %= 6   // a = 2
    a <<= 2  // a = 8
```

对于复合赋值表达式求值时，总是先计算 `=` 左边的表达式的左值，然后根据这个左值取右值，然后将该右值与 `=` 右边的表达式做计算（若有短路规则会继续遵循短路规则），最后赋值。因为复合赋值表达式也是一个赋值表达式，所以复合赋值操作符也是非结合的。复合赋值表达式同样要求两个操作数的类型相同。

<!-- compile -->

```cangjie
func foo(p: Point): Point {
    p.x += 10
    return p
}

open class Point {
    var x: Int64 = 0
    public init (a: Int64) {
        x = a
    }
}

main() {
    var a = Point(9)    // a.x == 9
    var b = 2

    foo(a).x += (b + b) // a.x == 23
    println(a.x)
}
```

上述示例即可看出复合赋值表达式求值的顺序，首先计算表达式 `foo(a).x` 的值，得到 `a.x` 为 19；之后将表达式 `b + b` 计算后得到的值与 `a.x` 相加。

## 关系操作符

关系操作符包括六种：相等（`==`）、不等（`!=`）、小于（`<`）、小于等于（`<=`）、大于（`>`）、大于等于（`>=`）。关系操作符都是二元操作符，并且要求两个操作数的类型是一样的。关系表达式的类型是 Bool 类型，即值只可能是 true 或 false。

关系表达式举例：

<!-- compile -->

```cangjie
main(): Int64 {
    3 < 4        // true
    3 <= 3       // true
    3 > 4        // false
    3 >= 3       // true
    3.14 == 3.15 // false
    3.14 != 3.15 // true
    return 0
}
```

对于元组类型，当且仅当所有元素均支持使用 `==` 进行值判等（使用 `!=` 进行值判不等）时，此元组类型才支持使用 `==` 进行值判等（使用 `!=` 进行值判不等）；否则，此元组类型不支持 `==` 和 `!=`（如果使用 `==` 和 `!=`，编译报错）。两个同类型的元组实例相等，当且仅当相同位置（index）的元素全部相等（意味着它们的长度相等）。

<!-- compile.error -->

```cangjie
    var isTrue: Bool = (1, 3) == (0, 2) // false
    isTrue = (1, "123") == (1.0, 2)      // 编译错误，两个操作数的类型不一致
    isTrue = (1, _) == (1.0, _)          // 编译错误，通配符不可作为元组中元素进行匹配
```

## coalescing 操作符

coalescing 操作符使用 `??` 表示，`??` 是二元中缀操作符。coalescing 操作符用于 [Option 类型](../enum_and_pattern_match/option_type.md)的解构。

`e1 ?? e2` 表达式，在 e1 的值等于 `Option<T>.Some(v)` 时，`e1 ?? e2` 的值等于 v 的值（此时，不会再去对 e2 求值，即满足 “短路求值”）；在 e1 的值等于 `Option<T>.None` 时，`e1 ?? e2` 的值等于 e2 的值。

coalescing 表达式使用举例：

<!-- run -->

```cangjie
main(): Int64 {
    let v1 = Option<Int64>.Some(100)
    let v2 = Option<Int64>.None
    let r1 = v1 ?? 0
    let r2 = v2 ?? 0
    print("${r1}") // 100
    print("${r2}") // 0
    return 0
}
```

## 区间操作符

区间操作符有两种：`..` 和 `..=`，分别用于创建 “左闭右开” 和 “左闭右闭” 的区间实例。关于它们的介绍，请参见 [区间类型](./range.md)。

## 逻辑操作符

仓颉编程语言支持三种逻辑操作符：逻辑非（`!`）、逻辑与（`&&`）、逻辑或（`||`）。

逻辑非（`!`）是一元操作符，它的作用是对其操作数的布尔值取反：`!false` 的值等于 `true`，`!true` 的值等于 `false`。

<!-- compile -->

```cangjie
    var a: Bool = true     // a = true
    var b: Bool = !a       // b = false
    var c: Bool = !false   // c = true
```

逻辑与（`&&`）和逻辑或（`||`）均是二元操作符。对于表达式 `expr1 && expr2`，只有当 `expr1` 和 `expr2` 的值均等于 `true` 时，它的值才等于 `true`；对于表达式 `expr1 || expr2`，只有当 `expr1` 和 `expr2` 的值均等于 `false` 时，它的值才等于 `false`。

<!-- compile -->

```cangjie
    var a: Bool = true && true    // a = true
    var b: Bool = true && false   // b = false
    var c: Bool = false && false  // c = false
    var d: Bool = false && true   // d = false

    a = true || true              // a = true
    b = true || false             // b = true
    c = false || false            // c = false
    d = false || true             // d = true
```

逻辑与（`&&`）和逻辑或（`||`）采用短路求值策略：计算 `expr1 && expr2` 时，当 `expr1=false` 则无需对 `expr2` 求值，整个表达式的值为 `false`；计算 `expr1 || expr2` 时，当 `expr1=true` 则无需对 `expr2` 求值，整个表达式的值为 `true`。

<!-- run -->

```cangjie
func isEven(a: Int64): Bool {
    if((a % 2) == 0) {
         println("${a} is an even number")
         true
    } else {
        println("${a} is not an even number")
        false
    }
}


main() {
    var a: Bool = isEven(2) && isEven(20)
    var b: Bool = isEven(3) && isEven(30) // isEven(3)返回值是false, b 值为false，无需对isEven(30)求值

    a = isEven(4) || isEven(40)  // isEven(4)返回值是true, a 值为true，无需对isEven(40)求值
    b = isEven(5) || isEven(50)
}
```

## 位运算操作符

仓颉编程语言支持一种一元前缀位运算操作符：按位求反（`!`），以及五种二元中缀位运算操作符：左移（`<<`）、右移（`>>`）、按位与（`&`）、按位异或（`^`）和按位或（`|`）。位运算操作符的操作数只能为整数类型，通过将操作数视为二进制序列，然后在每一位上进行逻辑运算（0 视为 false，1 视为 true ）或移位操作来实现位运算。

对于移位操作符，要求其操作数必须是整数类型（但两个操作数可以是不同的整数类型，例如：左操作数是 Int8，右操作数是 Int16），并且无论左移还是右移，右操作数都不允许为负数（对于编译时可检查出的此类错误，编译报错，如果运行时发生此错误，则抛出异常）。对于无符号数的移位操作，移位和补齐规则是：左移低位补 0 高位丢弃，右移高位补 0 低位丢弃。对于有符号数的移位操作，移位和补齐规则是：

1. 正数和无符号数的移位补齐规则一致;
2. 负数左移低位补 0 高位丢弃；
3. 负数右移高位补 1 低位丢弃。

另外，如果右移或左移的位数（右操作数）等于或者大于操作数的宽度，则为移位越界，如果编译时可以检测到则报错，否则运行时抛出异常。

<!-- compile -->

```cangjie
    var a = !10                 // -11，符合移位和补齐规则
    a = !20                     // -21，符合移位和补齐规则
    a = 10 << 1                 // 20，符合移位和补齐规则
    // a = 1000 << -1           // 编译报错，移位操作溢出（右操作数都不允许为负数）
    // a = 1000 << 100000000000 // 编译报错，移位操作溢出（移位越界）
    a = 10 << 1 << 1            // 40，符合移位和补齐规则
    a = 10 >> 1                 // 5，符合移位和补齐规则
    a = 10 & 15                 // 10
    a = 10 ^ 15                 // 5
    a = 10 | 15                 // 15
    a = (1 ^ (8 & 15)) | 24     // 25
```

## 自增自减操作符

自增（`++`）和自减（`--`）操作符实现对值的加 1 和减 1 操作，且只能作为后缀操作符使用。自增（`++`）和自减（`--`）操作符是非结合的。

对于表达式 `expr++` （或 `expr--` ），规定如下：

1. `expr` 的类型必须是整数类型；
2. 因为 `expr++` （或 `expr--` ）是 `expr += 1`（或 `expr -= 1` ）的语法糖，所以此 expr 同时必须也是可被赋值的；
3. `expr++`（或 `expr--` ）的类型为 Unit。

自增（自减）表达式举例：

<!-- compile.error -->

```cangjie
    var i: Int32 = 5
    i++              // i = 6
    i--              // i = 5
    i--++            // 语法错误
    var j = 0
    j = i--          // 语义错误
```


---

<!-- Content from source_zh_cn/basic_data_type/integer.md -->
# 整数类型

整数类型分为有符号（signed）整数类型和无符号（unsigned）整数类型。

**有符号整数类型**包括 `Int8`、`Int16`、`Int32`、`Int64` 和 `IntNative`，分别用于表示编码长度为 `8-bit`、`16-bit`、`32-bit`、`64-bit` 和平台相关大小的有符号整数值的类型。

**无符号整数类型**包括 `UInt8`、`UInt16`、`UInt32`、`UInt64` 和 `UIntNative`，分别用于表示编码长度为 `8-bit`、`16-bit`、`32-bit`、`64-bit` 和平台相关大小的无符号整数值的类型。

对于编码长度为 `N` 的有符号整数类型，其表示范围为：$-2^{N-1} \sim 2^{N-1}-1$；对于编码长度为 `N` 的无符号整数类型，其表示范围为：$0 \sim 2^{N}-1$。下表列出了所有整数类型的表示范围：

| 类型         | 表示范围                                                                                |
|:-----------|:------------------------------------------------------------------------------------|
| Int8       | $-2^7 \sim 2^7-1 (-128 \sim 127)$                                                   |
| Int16      | $-2^{15} \sim 2^{15}-1 (-32,768 \sim 32,767)$                                       |
| Int32      | $-2^{31} \sim 2^{31}-1 (-2,147,483,648 \sim 2,147,483,647)$                         |
| Int64      | $-2^{63} \sim 2^{63}-1 (-9,223,372,036,854,775,808 \sim 9,223,372,036,854,775,807)$ |
| IntNative  | platform dependent                                                                  |
| UInt8      | $0 \sim 2^8-1 (0 \sim 255)$                                                         |
| UInt16     | $0 \sim 2^{16}-1 (0 \sim 65,535)$                                                   |
| UInt32     | $0 \sim 2^{32}-1 (0 \sim 4,294,967,295)$                                            |
| UInt64     | $0 \sim 2^{64}-1 (0 \sim 18,446,744,073,709,551,615)$                               |
| UIntNative | platform dependent                                                                  |

程序具体使用哪种整数类型，取决于该程序中需要处理的整数的性质和范围。在 `Int64` 类型适合的情况下，首选 `Int64` 类型，因为 `Int64` 的表示范围足够大，并且[整数类型字面量](./integer.md#整数类型字面量)在没有类型上下文的情况下默认推断为 `Int64` 类型，可以避免不必要的类型转换。同时，仓颉编程语言中的 `IntNative` 和 `UIntNative`，分别为有符号和无符号整数类型，提供与当前系统一致的位宽长度。这意味二者大小取决于运行它们的平台，使得其在跨平台开发中能够自动适应系统的位宽。

## 整数类型字面量

整数类型字面量有 4 种进制表示形式：二进制（使用 `0b` 或 `0B` 前缀）、八进制（使用 `0o` 或 `0O` 前缀）、十进制（没有前缀）、十六进制（使用 `0x` 或 `0X` 前缀）。例如，对于十进制数 `24`，表示成二进制是 `0b00011000`（或 `0B00011000`），表示成八进制是 `0o30`（或 `0O30`），表示成十六进制是 `0x18`（或 `0X18`）。

在各进制表示中，可以使用下划线 `_` 充当分隔符的作用，方便识别数值的位数，如 `0b0001_1000`。

对于整数类型字面量，如果它的值超出了上下文要求的整数类型的表示范围，编译器将会报错。

<!-- compile.error -->

```cangjie
let x: Int8 = 128          // Error, 128 out of the range of Int8
let y: UInt8 = 256         // Error, 256 out of the range of UInt8
let z: Int32 = 0x8000_0000 // Error, 0x8000_0000 out of the range of Int32
```

在使用整数类型字面量时，可以通过加入后缀来明确整数字面量的类型，后缀与类型的对应为：

|  后缀  | 类型  |  后缀  | 类型   |
| :----- | :---- | :----  | :----- |
| i8     | Int8  | u8     | UInt8  |
| i16    | Int16 | u16    | UInt16 |
| i32    | Int32 | u32    | UInt32 |
| i64    | Int64 | u64    | UInt64 |

加入了后缀的整数字面量可以通过以下方式使用：

<!-- compile -->

```cangjie
var x = 100i8  // x is 100 with type Int8
var y = 0x10u64 // y is 16 with type UInt64
var z = 0o432i32  // z is 282 with type Int32
```

## 字符字节字面量

仓颉编程语言支持字符字节字面量，以方便使用 ASCII 码表示 `UInt8` 类型的值。字符字节字面量由字符 b、一对标识首尾的单引号、以及一个 `ASCII` 字符组成，例如：

<!-- compile -->

```cangjie
var a = b'x'                    // a is 120 with type UInt8
var b = b'\n'                   // b is 10 with type UInt8
var c = b'\u{78}'               // c is 120 with type UInt8
c = b'\u{90}' - b'\u{66}' + c   // c is 162 with type UInt8
```

`b'x'` 表示类型为 UInt8 大小是 120 的字面值。另外还可以通过 `b'\u{78}'` 这种转义形式表示类型为 `UInt8`，16 进制大小为 0x78 或 10 进制大小为 120 的字面值。需要注意的是，`\u` 内部最多有两位 16 进制数，并且值必须小于 256（十进制）。

## 整数类型支持的操作

整数类型默认支持的操作符包括：算术操作符、位操作符、关系操作符、自增和自减操作符、复合赋值操作符。各操作符的优先级参见附录中的[操作符](../Appendix/operator.md)。

整数类型之间、整数类型和浮点类型之间可以互相转换，整数类型可以转换为字符类型，具体的类型转换语法及规则请参见[数值类型之间的转换](../class_and_interface/typecast.md#数值类型之间的转换)。

> **注意：**
>
> 本章所提及的某个类型支持的操作，均是指在没有[操作符重载](../function/operator_overloading.md)的前提下。


---

<!-- Content from source_zh_cn/basic_data_type/float.md -->
# 浮点类型

浮点类型包括 `Float16`、 `Float32` 和 `Float64`，分别用于表示编码长度为 `16-bit`、 `32-bit` 和 `64-bit` 的浮点数（带小数部分的数字，如 3.14159、8.24 和 0.1 等）的类型。`Float16`、 `Float32` 和 `Float64` 分别对应 IEEE 754 中的半精度格式（即 binary16）、单精度格式（即 binary32）和双精度格式（即 binary64）。

`Float64` 的精度（有效数字位）约为 15 位，`Float32` 的精度（有效数字位）约为 6 位，`Float16` 的精度（有效数字位）约为 3 位。使用哪种浮点类型，取决于代码中需要处理的浮点数的性质和范围。在多种浮点类型都适合的情况下，首选精度高的浮点类型，因为精度低的浮点类型的累计计算误差很容易扩散，并且它能精确表示的整数范围也很有限。

## 浮点类型字面量

浮点类型字面量有两种进制表示形式：十进制、十六进制。在十进制表示中，一个浮点字面量至少要包含一个整数部分或一个小数部分，没有小数部分时必须包含指数部分（以 `e` 或 `E` 为前缀，底数为 10）。在十六进制表示中，一个浮点字面量除了至少要包含一个整数部分或小数部分（以 `0x` 或 `0X` 为前缀），同时必须包含指数部分（以 `p` 或 `P` 为前缀，底数为 2）。

下面的例子展示了浮点字面量的使用：

<!-- compile -->

```cangjie
let a: Float32 = 3.14       // a is 3.140000 with type Float32
let b: Float32 = 2e3        // b is 2000.000000 with type Float32
let c: Float32 = 2.4e-1     // c is 0.240000 with type Float32
let d: Float64 = .123e2     // d is 12.300000 with type Float64
let e: Float64 = 0x1.1p0    // e is 1.062500 with type Float64
let f: Float64 = 0x1p2      // f is 4.000000 with type Float64
let g: Float64 = 0x.2p4     // g is 2.000000 with type Float64
```

在使用十进制浮点数字面量时，可以通过加入后缀来明确浮点数字面量的类型，后缀与类型的对应为：

|  后缀 | 类型    |
| :---- | :------ |
| f16   | Float16 |
| f32   | Float32 |
| f64   | Float64 |

加入了后缀的浮点数字面量可以像下面的方式来使用：

<!-- compile -->

```cangjie
let a = 3.14f32   // a is 3.140000 with type Float32
let b = 2e3f32    // b is 2000.000000 with type Float32
let c = 2.4e-1f64 // c is 0.240000 with type Float64
let d = .123e2f64 // d is 12.300000 with type Float64
```

## 浮点类型支持的操作

浮点类型默认支持的操作符包括：算术操作符、关系操作符、复合赋值操作符。浮点类型不支持自增和自减操作符。

浮点类型之间、浮点类型和整数类型之间可以互相转换，具体的类型转换语法及规则请参见[数值类型之间的转换](../class_and_interface/typecast.md#数值类型之间的转换)。


---

<!-- Content from source_zh_cn/basic_data_type/bool.md -->
# 布尔类型

布尔类型使用 `Bool` 表示，用来表示逻辑中的真和假。

## 布尔类型字面量

布尔类型只有两个字面量：`true` 和 `false`。

下面的例子展示了布尔字面量的使用：

<!-- compile -->

```cangjie
let a: Bool = true
let b: Bool = false
```

## 布尔类型支持的操作

布尔类型支持的操作符包括：逻辑操作符（逻辑非 `!`，逻辑与 `&&`，逻辑或 `||`）、部分关系操作符（`==` 和 `!=`）、部分复合赋值操作符（`&&=` 和 `||=`）。


---

<!-- Content from source_zh_cn/basic_data_type/characters.md -->
# 字符类型

字符类型使用 `Rune` 表示，可以表示 Unicode 字符集中的所有字符。

## 字符类型字面量

字符类型字面量有三种形式：单个字符、转义字符和通用字符。一个 `Rune` 字面量由字符 `r` 开头，后跟一个由一对单引号或双引号包含的字符。

**单个字符**的字符字面量举例：

<!-- compile -->

```cangjie
let a: Rune = r'a'
let b: Rune = r"b"
```

**转义字符**是指在一个字符序列中对后面的字符进行另一种解释的字符。转义字符使用转义符号 `\` 开头，后面加需要转义的字符。举例如下：

<!-- compile -->

```cangjie
let slash: Rune = r'\\'
let newLine: Rune = r'\n'
let tab: Rune = r'\t'
```

**通用字符**以 `\u` 开头，后面加上定义在一对花括号中的 1~8 个十六进制数，即可表示对应的 Unicode 值代表的字符。举例如下：

<!-- verify -->

```cangjie
main() {
    let he: Rune = r'\u{4f60}'
    let llo: Rune = r'\u{597d}'
    print(he)
    print(llo)
}
```

编译并执行上述代码，输出结果为：

```text
你好
```

## 字符类型支持的操作

字符类型支持的操作符包括：关系操作符，即小于（`<`）、大于（`>`）、小于等于（`<=`）、大于等于（`>=`）、相等（`==`）、不等（`!=`）。比较的是字符的 Unicode 值。

`Rune` 可以转换为 `UInt32`，整数类型可以转换为 `Rune`，具体的类型转换语法及规则请参见[`Rune` 到 `UInt32` 和整数类型到 `Rune` 的转换](../class_and_interface/typecast.md#rune-到-uint32-和整数类型到-rune-的转换)。


---

<!-- Content from source_zh_cn/basic_data_type/strings.md -->
# 字符串类型

字符串类型使用 `String` 表示，用于表达文本数据，由一串 Unicode 字符组合而成。

## 字符串字面量

字符串字面量分为三类：单行字符串字面量，多行字符串字面量，多行原始字符串字面量。

**单行字符串字面量**的内容定义在一对单引号或一对双引号之内，引号中的内容可以是任意数量的（除了用于定义字符串字面量的非转义的引号和单独出现的 `\` 之外的）任意字符。单行字符串字面量只能写在同一行，不能跨越多行。举例如下：

<!-- compile -->

```cangjie
let s1: String = ""
let s2 = 'Hello Cangjie Lang'
let s3 = "\"Hello Cangjie Lang\""
let s4 = 'Hello Cangjie Lang\n'
```

**多行字符串字面量**开头结尾需各存在三个双引号（`"""`）或三个单引号（`'''`）。字面量的内容从开头的三个引号换行后的第一行开始，到遇到的第一个非转义的三个引号为止，之间的内容可以是任意数量的（除单独出现的 `\` 之外的）任意字符。不同于单行字符串字面量，多行字符串字面量可以跨越多行。举例如下：

<!-- compile -->

```cangjie
let s1: String = """
    """
let s2 = '''
    Hello,
    Cangjie Lang'''
```

**多行原始字符串字面量**以一个或多个井号（`#`）和一个单引号（`'`）或双引号（`"`）开头，后跟任意数量的合法字符，直到出现与字符串开头相同的引号和与字符串开头相同数量的井号为止。在当前文件结束之前，如果还没遇到匹配的双引号和相同个数的井号，则编译报错。与多行字符串字面量一样，原始多行字符串字面量可以跨越多行。不同之处在于，转义规则不适用于多行原始字符串字面量，字面量中的内容会维持原样（转义字符不会被转义，如下例中 `s2` 中的 `\n` 不是换行符，而是由 `\` 和 `n` 组成的字符串 `\n`）。举例如下：

<!-- compile -->

```cangjie
let s1: String = #""#
let s2 = ##'#'\n'## // 输出结果为：#'\n
let s3 = ###"
    Hello,
    Cangjie
    Lang"### // 该变量当中的换行、缩进等也会被保留
```

对于形如 `left = right` 的赋值操作，如果左操作数的类型是 `Byte`（内置类型 `UInt8` 的别名），并且右操作数是一个表示 ASCII 字符的字符串字面量，那么右操作数的字符串将分别被强制转换为 `Byte` 类型，再进行赋值；如果左操作数的类型是 `Rune`，并且右操作数是一个单字符的字符串字面量，那么右操作数的字符串将分别被强制转换为 `Rune` 类型，再进行赋值。

<!-- verify -->

```cangjie
main() {
    var b: Byte = "0"
    print(b)
    b = "1"
    print(b)
    var r: Rune = "0"
    print(r)
    r = "1"
    print(r)
}
```

编译并执行上述代码，输出结果为：

```text
484901
```

## 插值字符串

插值字符串是一种包含一个或多个插值表达式的字符串字面量（不适用于多行原始字符串字面量），通过将表达式插入到字符串中，可以有效避免字符串拼接的问题。插值字符串经常出现在 `println` 函数中输出非字符串类型的变量值，例如 `println("${x}")`。

插值表达式必须用花括号 `{}` 包起来，并在 `{}` 之前加上 `$` 前缀。`{}` 中可以包含一个或者多个声明或表达式。

当插值字符串求值时，每个插值表达式所在位置会被 `{}` 中的最后一项的值替换，整个插值字符串最终仍是一个字符串。

下面是插值字符串的简单示例：

<!-- verify -->

```cangjie
main() {
    let fruit = "apples"
    let count = 10
    let s = "There are ${count * count} ${fruit}"
    println(s)

    let r = 2.4
    let area = "The area of a circle with radius ${r} is ${let PI = 3.141592; PI * r * r}"
    println(area)
}
```

编译并执行上述代码，输出结果为：

```text
There are 100 apples
The area of a circle with radius 2.400000 is 18.095570
```

## 字符串类型支持的操作

字符串类型支持使用关系操作符进行比较，支持使用 `+` 进行拼接。下面的例子展示了字符串类型的判等和拼接：

<!-- verify -->

```cangjie
main() {
    let s1 = "abc"
    var s2 = "ABC"
    let r1 = s1 == s2
    println("The result of 'abc' == 'ABC' is: ${r1}")
    let r2 = s1 + s2
    println("The result of 'abc' + 'ABC' is: ${r2}")
}
```

编译并执行上述代码，输出结果为：

```text
The result of 'abc' == 'ABC' is: false
The result of 'abc' + 'ABC' is: abcABC
```

字符串还支持其他常见操作，例如拆分、替换等。下面给出部分常见操作：

<!-- run -->

```cangjie
main() {
    var s1 = "abc"
    var s2 = "ABCabc"
    var s3 = "abcyyabcqqabcbc"
    let r1 = s2.contains(s1)    // 判断s2中是否包含字符串s1
    println(r1)                 // true
    let r2 = s3.split(s1)       //对原字符串 s2 按照字符串 s1 分隔符分割，指定是否删除空串
    println(r2[1])              // yy
    s1 = s2
    println(s1)                 // ABCabc
}
```


---

<!-- Content from source_zh_cn/basic_data_type/tuple.md -->
# 元组类型

元组（Tuple）可以将多个不同的类型组合在一起，成为一个新的类型。元组类型使用 `(T1, T2, ..., TN)` 表示，其中 `T1` 到 `TN` 可以是任意类型，不同类型间使用逗号（ `,` ）连接。元组至少是二元，例如，`(Int64, Float64)` 表示一个二元组类型，`(Int64, Float64, String)` 表示一个三元组类型。

元组的长度是固定的，即一旦定义了一个元组类型的实例，它的长度不能再被更改。

元组类型是不可变类型，即一旦定义了一个元组类型的实例，它的内容（即单个元素）不能再被更新。但整个元组可被覆盖替换，例如：

<!-- compile.error -->

```cangjie
let tuple1 = (8, false)
var tuple2 = (true, 9, 20)
tuple2 = tuple1         // Error, mismatched types
tuple2[0] = false       // Error, 'tuple element' can not be assigned

var tuple3 = (9, true)
tuple3 = tuple1
println(tuple3[0])      // 8
println(tuple3[1])      // false
```

## 元组类型的字面量

元组类型的字面量使用 `(e1, e2, ..., eN)` 表示，其中 `e1` 到 `eN` 是表达式，多个表达式之间使用逗号分隔。下面的例子中，分别定义了一个 `(Int64, Float64)` 类型的变量 `x`，以及一个 `(Int64, Float64, String)` 类型的变量 `y`，并且使用元组类型的字面量为它们定义了初值：

<!-- compile -->

```cangjie
let x: (Int64, Float64) = (3, 3.141592)
let y: (Int64, Float64, String) = (3, 3.141592, "PI")
```

元组支持通过 `t[index]` 的方式访问某个具体位置的元素，其中 `t` 是一个元组，`index` 是下标，并且 `index` 只能是从 `0` 开始且小于元组元素个数的整数类型字面量，否则编译报错。下面的例子中，使用 `pi[0]` 和 `pi[1]` 可以分别访问二元组 `pi` 的第一个元素和第二个元素。
<!-- verify -->

```cangjie
main() {
    var pi = (3.14, "PI")
    println(pi[0])
    println(pi[1])
}
```

编译并执行上述代码，输出结果为：

```text
3.140000
PI
```

在赋值表达式中，可使用元组进行多赋值，参见[赋值操作符](./basic_operators.md#赋值操作符)章节。

## 元组类型的类型参数

可以为元组类型标记显式的类型参数名，下面例子中的 `name` 和 `price` 就是 `类型参数名`。

<!-- verify -->

```cangjie
func getFruitPrice(): (name: String, price: Int64) {
    return ("banana", 10)
}

main() {
    let tmp = getFruitPrice()
    var a = tmp[0]
    var b = tmp[1]
    b++
    println("b = ${b}, tmp[1] = ${tmp[1]}")
}
```

编译并执行上面的代码，会输出：

```text
b = 11, tmp[1] = 10
```

对于一个元组类型，只允许统一写类型参数名，或者统一不写类型参数名，不允许交替存在，并且参数名本身不能作为变量使用或用于访问元组中元素。

<!-- compile.error -->

```cangjie
let a: (name: String, Int64) = ("banana", 5) // Error, in a parameter type list, either all parameters must be named, or none of them
let b: (name: String, price: Int64) = ("banana", 5) // OK
b.name // Error, undeclared identifier 'name'
```


---

<!-- Content from source_zh_cn/basic_data_type/array.md -->
# 数组类型

## Array

可以使用 Array 类型来构造单一元素类型，有序序列的数据。

仓颉使用 `Array<T>` 来表示 Array 类型。T 表示 Array 的元素类型，T 可以是任意类型。

<!-- compile.error -array_example -->

```cangjie
var a: Array<Int64> = [0, 0, 0, 0] // Array whose element type is Int64
var b: Array<String> = ["a1", "a2", "a3"] // Array whose element type is String
```

元素类型不相同的 Array 是不相同的类型，所以它们之间不可以互相赋值。

因此以下例子是不合法的。

<!-- compile.error -array_example -->

```cangjie
b = a // Type mismatch
```

可以轻松使用字面量来初始化一个 Array，只需要使用方括号将逗号分隔的值列表括起来即可。

编译器会根据上下文自动推断 Array 字面量的类型。

<!-- compile -->

```cangjie
let a: Array<String> = [] // Created an empty Array whose element type is String
let b = [1, 2, 3, 3, 2, 1] // Created a Array whose element type is Int64, containing elements 1, 2, 3, 3, 2, 1
```

也可以使用构造函数的方式构造一个指定元素类型的 Array。其中， repeat 属于 Array 构造函数中的一个命名参数。

需要注意的是，当通过 repeat 指定的初始值初始化 Array 时，该构造函数不会拷贝 repeat，如果 repeat 是一个引用类型，构造后数组的每一个元素都将指向相同的引用。

<!-- compile -->

```cangjie
let a = Array<Int64>() // Created an empty Array whose element type is Int64
let c = Array<Int64>(3, repeat: 0) // Created an Array whose element type is Int64, length is 3 and all elements are initialized as 0
let d = Array<Int64>(3, {i => i + 1}) // Created an Array whose element type is Int64, length is 3 and all elements are initialized by the initialization function
```

示例中 `let d = Array<Int64>(3, {i => i + 1})` 使用了 [lambda 表达式](../function/lambda.md)作为初始化函数来初始化数组中的每一个元素，即 `{i => i + 1}`。

### 访问 Array 成员

当需要对 Array 的所有元素进行访问时，可以使用 for-in 循环遍历 Array 的所有元素。

Array 是按元素插入顺序排列的，因此对 Array 遍历的顺序总是恒定的。

<!-- verify -->

```cangjie
main() {
    let arr = [0, 1, 2]
    for (i in arr) {
        println("The element is ${i}")
    }
}
```

编译并执行上面的代码，会输出：

```text
The element is 0
The element is 1
The element is 2
```

当需要知道某个 Array 包含的元素个数时，可以使用 size 属性获得对应信息。

<!-- verify -->

```cangjie
main() {
    let arr = [0, 1, 2]
    if (arr.size == 0) {
        println("This is an empty array")
    } else {
        println("The size of array is ${arr.size}")
    }
}
```

编译并执行上面的代码，会输出：

```text
The size of array is 3
```

当想访问单个指定位置的元素时，可以使用下标语法访问（下标的类型必须是 Int64）。非空 Array 的第一个元素总是从位置 0 开始的。可以从 0 开始访问 Array 的任意一个元素，直到最后一个位置（Array 的 size - 1）。索引值不能使用负数或者大于等于 size，当编译器能检查出索引值非法时，会在编译时报错，否则会在运行时抛异常。

<!-- compile.error -->

```cangjie
main() {
    let arr = [0, 1, 2]
    let a = arr[0] // a == 0
    let b = arr[1] // b == 1
    let c = arr[-1] // array size is '3', but access index is '-1', which would overflow
}
```

如果想获取某一段 Array 的元素，可以在下标中传入 Range 类型的值，就可以一次性取得 Range 对应范围的一段 Array。

<!-- compile -->

```cangjie
let arr1 = [0, 1, 2, 3, 4, 5, 6]
let arr2 = arr1[0..5] // arr2 contains the elements 0, 1, 2, 3, 4
```

当 Range 字面量在下标语法中使用时，可以省略 start 或 end。

当省略 start 时，Range 会从 0 开始；当省略 end 时，Range 的 end 会延续到最后一位。

<!-- compile -->

```cangjie
let arr1 = [0, 1, 2, 3, 4, 5, 6]
let arr2 = arr1[..3] // arr2 contains elements 0, 1, 2
let arr3 = arr1[2..] // arr3 contains elements 2, 3, 4, 5, 6
```

### 修改 Array

Array 是一种长度不变的 [Collection 类型](../../source_zh_cn/collections/collection_overview.md)，因此 Array 没有提供添加和删除元素的成员函数。

但是 Array 允许对其中的元素进行修改，同样使用下标语法。

<!-- verify -->

```cangjie
main() {
    let arr = [0, 1, 2, 3, 4, 5]
    arr[0] = 3
    println("The first element is ${arr[0]}")
}
```

编译并执行上面的代码，会输出：

```text
The first element is 3
```

Array 虽然是 struct 类型，但其内部持有的只是元素的引用，因此在作为表达式使用时不会拷贝副本，同一个 Array 实例的所有引用都会共享同样的元素数据。

因此对 Array 元素的修改会影响到该实例的所有引用。

<!-- compile -->

```cangjie
let arr1 = [0, 1, 2]
let arr2 = arr1
arr2[0] = 3
// arr1 contains elements 3, 1, 2
// arr2 contains elements 3, 1, 2
```

## VArray

除了引用类型的数组 Array，仓颉还引入了值类型数组 `VArray<T, $N>` ，其中 `T` 表示该值类型数组的元素类型，`$N` 是一个固定的语法。通过 `$` 加上一个 `Int64` 类型的数值字面量表示这个值类型数组的长度。需要注意的是，`VArray<T, $N>` 不能省略 `<T, $N>`，且使用类型别名时，不允许拆分 `VArray` 关键字与其泛型参数。

与频繁使用引用类型 Array 相比，使用值类型 VArray 可以减少堆上内存分配和垃圾回收的压力。但是需要注意的是，由于值类型本身在传递和赋值时的拷贝，会产生额外的性能开销，因此建议不要在性能敏感场景使用较大长度的 `VArray`。值类型和引用类型的特点请参见[值类型和引用类型变量](../basic_programming_concepts/program_structure.md#值类型和引用类型变量)。
<!-- compile.error -->

```cangjie
type varr1 = VArray<Int64, $3> // OK
type varr2 = VArray // Error
```

> **注意：**
>
> 由于运行时后端限制，当前 `VArray<T, $N>` 的元素类型 `T` 或 `T` 的成员不能包含引用类型、枚举类型、Lambda 表达式（`CFunc` 除外）以及未实例化的泛型类型。

`VArray` 可以由一个数组的字面量来进行初始化，左值 `a` 必须标识出 `VArray` 的实例化类型：

<!-- compile -->

```cangjie
var a: VArray<Int64, $3> = [1, 2, 3]
```

同时，它拥有两个构造函数：

<!-- compile -->

```cangjie
// VArray<T, $N>(initElement: (Int64) -> T)
let b = VArray<Int64, $5>({ i => i }) // [0, 1, 2, 3, 4]
// VArray<T, $N>(repeat!: T)
let c = VArray<Int64, $5>(repeat: 0) // [0, 0, 0, 0, 0]
```

除此之外，`VArray<T, $N>` 类型提供了两个成员方法：

- 用于下标访问和修改的 `[]` 操作符方法：

  <!-- compile -->

  ```cangjie
  var a: VArray<Int64, $3> = [1, 2, 3]
  let i = a[1] // i is 2
  a[2] = 4 // a is [1, 2, 4]
  ```

  下标访问的下标类型必须为 `Int64`。

- 用于获取 `VArray` 长度的 `size` 成员：

  <!-- compile -->

  ```cangjie
  var a: VArray<Int64, $3> = [1, 2, 3]
  let s = a.size // s is 3
  ```

  size 属性的类型为 `Int64`。

此外，`VArray` 还支持仓颉与 C 语言互操作场景使用，相关内容请参见[数组](../FFI/cangjie-c.md#数组)。


---

<!-- Content from source_zh_cn/basic_data_type/range.md -->
# 区间类型

区间类型用于表示拥有固定步长的序列，区间类型是一个[泛型](../generic/generic_overview.md)，使用 `Range<T>` 表示。当 `T` 被实例化为不同类型时，要求此类型必须支持关系操作符，并且可以和 `Int64` 类型的值做加法，这会得到不同的区间类型。例如，最常用的 `Range<Int64>` 用于表示整数区间。

每个区间类型的实例都会包含 `start`、`end` 和 `step` 三个值。其中，`start` 和 `end` 分别表示序列的起始值和终止值，`step` 表示序列中前后两个元素之间的差值（即步长）；`start` 和 `end` 的类型相同（即 `T` 被实例化的类型），`step` 类型是 `Int64`，并且它的值不能等于 `0`。

下面的例子给出了区间类型的实例化方式（关于区间类型定义和其中的属性，详见《仓颉编程语言库 API》）：

<!-- compile -->

```cangjie
// Range<T>(start: T, end: T, step: Int64, hasStart: Bool, hasEnd: Bool, isClosed: Bool)
let r1 = Range<Int64>(0, 10, 1, true, true, true) // r1 contains 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
let r2 = Range<Int64>(0, 10, 1, true, true, false) // r2 contains 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
let r3 = Range<Int64>(10, 0, -2, true, true, false) // r3 contains 10, 8, 6, 4, 2
```

## 区间类型字面量

区间字面量有两种形式：“左闭右开”区间和“左闭右闭”区间。

- “左闭右开”区间的格式是 `start..end : step`，它表示一个从 `start` 开始，以 `step` 为步长，到 `end`（不包含 `end`）为止的区间；
- “左闭右闭”区间的格式是 `start..=end : step`，它表示一个从 `start` 开始，以 `step` 为步长，到 `end`（包含 `end`）为止的区间。

下面的例子定义了若干区间类型的变量：

<!-- compile -->

```cangjie
let n = 10
let r1 = 0..10 : 1   // r1 contains 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
let r2 = 0..=n : 1   // r2 contains 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
let r3 = n..0 : -2   // r3 contains 10, 8, 6, 4, 2
let r4 = 10..=0 : -2 // r4 contains 10, 8, 6, 4, 2, 0
```

区间字面量中，可以不写 `step`，此时 `step` 默认等于 `1`，但是`step` 的值不能等于 `0`。另外，区间也有可能是空的（即不包含任何元素的空序列），举例如下：
<!-- compile.error -->

```cangjie
let r5 = 0..10   // the step of r5 is 1, and r5 contains 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
let r6 = 0..10 : 0 // Error, step cannot be 0

let r7 = 10..0 : 1 // r7 to r10 are empty ranges
let r8 = 0..10 : -1
let r9 = 10..=0 : 1
let r10 = 0..=10 : -1
```

> **注意：**
>
> - 表达式 `start..end : step` 中，当 `step > 0` 且 `start >= end`，或者 `step < 0` 且 `start <= end` 时，`start..end : step` 是一个空区间；
> - 表达式 `start..=end : step` 中，当 `step > 0` 且 `start > end`，或者 `step < 0` 且 `start < end` 时，`start..=end : step` 是一个空区间。


---

<!-- Content from source_zh_cn/basic_data_type/unit.md -->
# Unit 类型

对于那些只关心副作用而不关心值的表达式，它们的类型是 `Unit`。例如，`print` 函数、赋值表达式、复合赋值表达式、自增和自减表达式、循环表达式，它们的类型都是 `Unit`。

`Unit` 类型只有一个值，也是它的字面量：`()`。除了赋值、判等和判不等外，`Unit` 类型不支持其他操作。


---

<!-- Content from source_zh_cn/basic_data_type/nothing.md -->
# Nothing 类型

`Nothing` 是一种特殊的类型，它不包含任何值，并且 `Nothing` 类型是所有类型的子类型（这当中也包括 [`Unit` 类型](unit.md)）。

`break`、`continue`、`return` 和 `throw` 表达式的类型是 `Nothing`，程序执行到这些表达式时，它们之后的代码将不会被执行。`return` 只能在函数体中使用，`break`、`continue` 只能在循环体中使用，参考如下示例：

<!-- compile.error -->

```cangjie
while (true) {
    func f() {
        break // Error, break must be used directly inside a loop
    }
    let g = { =>
        continue // Error, continue must be used directly inside a loop
    }
}
```

由于函数的形参和其默认值不属于该函数的函数体，所以下面例子中的 return 表达式缺少包围它的函数体——它既不属于外层函数 `f`（因为内层函数定义 `g` 已经开始），也不在内层函数 `g` 的函数体中（该用例相关内容，请参考[嵌套函数](../function/nested_functions.md)）：

<!-- compile.error -->

```cangjie
func f() {
    func g(x!: Int64 = return) { // Error, return must be used inside a function body
        0
    }
    1
}
```

> **注意：**
>
> 目前编译器还不允许在使用类型的地方显式地使用 Nothing 类型。


---

<!-- Content from source_zh_cn/function/define_functions.md -->
# 定义函数

仓颉使用关键字 `func` 来表示函数定义的开始，`func` 之后依次是函数名、参数列表、可选的函数返回值类型、函数体。其中，函数名可以是任意的合法标识符，参数列表定义在一对圆括号内（多个参数间使用逗号分隔），参数列表和函数返回值类型（如果存在）之间使用冒号分隔，函数体定义在一对花括号内。

函数定义举例：

<!-- compile -->

```cangjie
func add(a: Int64, b: Int64): Int64 {
    return a + b
}
```

上例中定义了一个名为 `add` 的函数，其参数列表由两个 `Int64` 类型的参数 `a` 和 `b` 组成，函数返回值类型为 `Int64`，函数体中将 `a` 和 `b` 相加并返回。

下面依次对函数定义中的参数列表、函数返回值类型和函数体作进一步介绍。

## 参数列表

一个函数可以拥有 0 个或多个参数，这些参数均定义在函数的参数列表中。根据函数调用时是否需要给定参数名，可以将参数列表中的参数分为两类：非命名参数和命名参数。

非命名参数的定义方式是 `p: T`，其中 `p` 表示参数名，`T` 表示参数 `p` 的类型，参数名和其类型间使用冒号连接。例如，上例中 `add` 函数的两个参数 `a` 和 `b` 均为非命名参数。

命名参数的定义方式是 `p!: T`，与非命名参数的不同是在参数名 `p` 之后多了一个 `!`。可以将上例中 `add` 函数的两个非命名参数修改为命名参数，如下所示：

<!-- compile -->

```cangjie
func add(a!: Int64, b!: Int64): Int64 {
    return a + b
}
```

命名参数还可以设置默认值，通过 `p!: T = e` 方式将参数 `p` 的默认值设置为表达式 `e` 的值。例如，可以将上述 `add` 函数的两个参数的默认值都设置为 `1`：

<!-- compile -->

```cangjie
func add(a!: Int64 = 1, b!: Int64 = 1): Int64 {
    return a + b
}
```

> **注意：**
>
> 只能为命名参数设置默认值，不能为非命名参数设置默认值。

参数列表中可以同时定义非命名参数和命名参数，但是需要注意的是，非命名参数只能定义在命名参数之前，也就意味着命名参数之后不能再出现非命名参数。例如，下例中 `add` 函数的参数列表定义是不合法的：

<!-- compile.error -->

```cangjie
func add(a!: Int64, b: Int64): Int64 { // Error, named parameter 'a' must be defined after non-named parameter 'b'
    return a + b
}
```

非命名参数和命名参数的主要差异在于调用时的不同，具体可参见下文[调用函数](./call_functions.md)中的介绍。

函数参数均为不可变变量，在函数定义内不能对其赋值。

<!-- compile.error -->

```cangjie
func add(a: Int64, b: Int64): Int64 {
    a = a + b // Error
    return a
}
```

函数参数作用域从定义处起至函数体结束：

<!-- compile.error -->

```cangjie
func add(a: Int64, b: Int64): Int64 {
    var a_ = a // OK
    var b = b  // Error, redefinition of declaration 'b'
    return a
}
```

## 函数返回值类型

函数返回值类型是函数被调用后得到的值的类型。函数定义时，返回值类型是可选的：可以显式地定义返回值类型（返回值类型定义在参数列表和函数体之间），也可以不定义返回值类型，交由编译器推导确定。

当显式地定义了函数返回值类型时，就要求函数体的类型（关于如何确定函数体的类型可参见下节[函数体](./define_functions.md#函数体)）、函数体中所有 `return e` 表达式中 `e` 的类型是返回值类型的子类型。例如，对于上述 `add` 函数，显式地定义了它的返回值类型为 `Int64`；如果将函数体中的 `return a + b` 修改为 `return (a, b)`，则会因为类型不匹配而报错：

<!-- compile.error -->

```cangjie
// Error, the type of the expression after return does not match the return type of the function
func add(a: Int64, b: Int64): Int64 {
    return (a, b)
}
```

在函数定义时如果未显式定义返回值类型，编译器将根据函数体的类型以及函数体中所有的 `return` 表达式来共同推导出函数的返回值类型。例如，下例中 `add` 函数的返回值类型虽然被省略，但编译器可以根据 `return a + b` 推导出 `add` 函数的返回值类型是 `Int64`：

<!-- compile -->

```cangjie
func add(a: Int64, b: Int64) {
    return a + b
}
```

> **注意：**
>
> 函数的返回值类型并不是任何情况下都可以被推导出来的，如果返回值类型推导失败，编译器会报错。
>
> 指定返回类型为 Unit 时，编译器会在函数体中所有可能返回的地方自动插入表达式 return ()，使得函数的返回类型总是为 Unit。

## 函数体

函数体中定义了函数被调用时执行的操作，通常包含一系列的变量定义和表达式，也可以包含新的函数定义（即嵌套函数）。如下 `add` 函数的函数体中首先定义了 `Int64` 类型的变量 `r`（初始值为 `0`），接着将 `a + b` 的值赋值给 `r`，最后将 `r` 的值返回：

<!-- compile -->

```cangjie
func add(a: Int64, b: Int64) {
    var r = 0
    r = a + b
    return r
}
```

在函数体的任意位置都可以使用 `return` 表达式来终止函数的执行并返回。`return` 表达式有两种形式：`return` 和 `return expr`（`expr` 是一个表达式）。

对于 `return expr`，要求 `expr` 的类型与函数定义中的返回值类型保持一致。例如，下例中会因为 `return 100` 中 `100` 类型（`Int64`）和函数 `foo` 的返回值类型（`String`）不同而报错。

<!-- compile.error -->

```cangjie
// Error, cannot convert an integer literal to type 'Struct-String'
func foo(): String {
    return 100
}
```

对于 `return`，其等价于 `return ()`，所以要求函数的返回值类型为 `Unit`。

<!-- compile -->

```cangjie
func add(a: Int64, b: Int64) {
    var r = 0
    r = a + b
    return r
}

func foo(): Unit {
    add(1, 2)
    return
}
```

> **注意：**
>
> `return` 表达式作为一个整体，其类型并不由后面跟随的表达式决定，而是 `Nothing` 类型。

在函数体内定义的变量属于局部变量的一种（如上例中的 `r` 变量），它的作用域从其定义之后开始到函数体结束。

对于一个局部变量，允许在其外层作用域中定义同名变量，并且在此局部变量的作用域内，局部变量会“遮盖”外层作用域的同名变量。例如：

<!-- compile -->

```cangjie
let r = 0
func add(a: Int64, b: Int64) {
    var r = 0
    r = a + b
    return r
}
```

上例中，`add` 函数之前定义了 `Int64` 类型的全局变量 `r`，同时 `add` 函数体内定义了同名的局部变量 `r`，那么在函数体内，所有使用变量 `r` 的地方（如 `r = a + b`），用到的将是局部变量 `r`，即（在函数体内）局部变量 `r` “遮盖”了全局变量 `r`。

[函数返回值类型](./define_functions.md#函数返回值类型)中提到函数体也是有类型的，函数体的类型是函数体内最后一“项”的类型：若最后一项为表达式，则函数体的类型是此表达式的类型，若最后一项为变量定义或函数声明，或函数体为空，则函数体的类型为 `Unit`。例如：

<!-- compile -->

```cangjie
func add(a: Int64, b: Int64): Int64 {
    a + b
}
```

上例中，因为函数体的最后一“项”是 `Int64` 类型的表达式（即 `a + b`），所以函数体的类型也是 `Int64`，与函数定义的返回值类型相匹配。又如，下例中函数体的最后一项是 `print` 函数调用，所以函数体的类型是 `Unit`，同样与函数定义的返回值类型相匹配：

<!-- compile -->

```cangjie
func foo(): Unit {
    let s = "Hello"
    print(s)
}
```


---

<!-- Content from source_zh_cn/function/call_functions.md -->
# 调用函数

函数调用的形式为 `f(arg1, arg2, ..., argn)`。其中，`f` 是要调用的函数的名字，`arg1` 到 `argn` 是 `n` 个调用时的参数（称为实参），要求每个实参的类型必须是对应参数类型的子类型。实参可以有 0 个或多个，当实参个数为 0 时，调用方式为 `f()`。

根据函数定义时参数是非命名参数还是命名参数的差异，函数调用时传实参的方式也有所不同：对于非命名参数，它对应的实参是一个表达式；对于命名参数，它对应的实参需要使用 `p: e` 的形式，其中 `p` 是命名参数的名字，`e` 是表达式（即传递给参数 `p` 的值）。

非命名参数调用举例：

<!-- verify -->

```cangjie
func add(a: Int64, b: Int64) {
    return a + b
}

main() {
    let x = 1
    let y = 2
    let r = add(x, y)
    println("The sum of x and y is ${r}")
}
```

执行结果为：

```text
The sum of x and y is 3
```

命名参数调用举例：

<!-- verify -->

```cangjie
func add(a: Int64, b!: Int64) {
    return a + b
}

main() {
    let x = 1
    let y = 2
    let r = add(x, b: y)
    println("The sum of x and y is ${r}")
}
```

执行结果为：

```text
The sum of x and y is 3
```

对于多个命名参数，调用时的传参顺序可以和定义时的参数顺序不同。例如，下例中调用 `add` 函数时 `b` 可以出现在 `a` 之前：

<!-- verify -->

```cangjie
func add(a!: Int64, b!: Int64) {
    return a + b
}

main() {
    let x = 1
    let y = 2
    let r = add(b: y, a: x)
    println("The sum of x and y is ${r}")
}
```

执行结果为：

```text
The sum of x and y is 3
```

对于拥有默认值的命名参数，调用时如果没有传实参，那么此参数将使用默认值作为实参的值。例如，下例中调用 `add` 函数时没有为参数 `b` 传实参，那么参数 `b` 的值等于其定义时的默认值 `2`：

<!-- verify -->

```cangjie
func add(a: Int64, b!: Int64 = 2) {
    return a + b
}

main() {
    let x = 1
    let r = add(x)
    println("The sum of x and y is ${r}")
}
```

执行结果为：

```text
The sum of x and y is 3
```

对于拥有默认值的命名参数，调用时也可以为其传递新的实参，此时命名参数的值等于新的实参的值，即定义时的默认值将失效。例如，下例中调用 `add` 函数时为参数 `b` 传了新的实参值 `20`，那么参数 `b` 的值就等于 `20`：

<!-- verify -->

```cangjie
func add(a: Int64, b!: Int64 = 2) {
    return a + b
}

main() {
    let x = 1
    let r = add(x, b: 20)
    println("The sum of x and y is ${r}")
}
```

执行结果为：

```text
The sum of x and y is 21
```


---

<!-- Content from source_zh_cn/function/first_class_citizen.md -->
# 函数类型

仓颉编程语言中，函数是一等公民（first-class citizens），可以作为函数的参数或返回值，也可以赋值给变量。因此函数本身也有类型，称之为函数类型。

函数类型由函数的参数类型和返回类型组成，参数类型和返回类型之间使用 `->` 连接。参数类型使用圆括号 `()` 括起来，可以有 0 个或多个参数，如果参数超过一个，参数类型之间使用逗号（`,`）分隔。

例如：

<!-- compile -->

```cangjie
func hello(): Unit {
    println("Hello!")
}
```

上述示例定义了一个函数，函数名为 hello，其类型是 `() -> Unit`，表示该函数没有参数，返回类型为 `Unit`。

以下给出另一些示例：

- 示例：函数名为 `display`，其类型是 `(Int64) -> Unit`，表示该函数有一个参数，参数类型为 `Int64`，返回类型为 `Unit`。

    <!-- compile -->

    ```cangjie
    func display(a: Int64): Unit {
        println(a)
    }
    ```

- 示例：函数名为 `add`，其类型是 `(Int64, Int64) -> Int64`，表示该函数有两个参数，两个参数类型均为 `Int64`，返回类型为 `Int64`。

    <!-- compile -->

    ```cangjie
    func add(a: Int64, b: Int64): Int64 {
        a + b
    }
    ```

- 示例：函数名为 `returnTuple`，其类型是 `(Int64, Int64) -> (Int64, Int64)`，两个参数类型均为 `Int64`, 返回类型为元组类型：`(Int64, Int64)`。

    <!-- compile -->

    ```cangjie
    func returnTuple(a: Int64, b: Int64): (Int64, Int64) {
        (a, b)
    }
    ```

## 函数类型的类型参数

可以为函数类型标记显式的类型参数名，下面例子中的 `name` 和 `price` 就是 `类型参数名`。

<!-- run -->

```cangjie
func showFruitPrice(name: String, price: Int64) {
    println("fruit: ${name} price: ${price} yuan")
}

main() {
    let fruitPriceHandler: (name: String, price: Int64) -> Unit
    fruitPriceHandler = showFruitPrice
    fruitPriceHandler("banana", 10)
}
```

另外对于一个函数类型，只允许统一写类型参数名，或者统一不写类型参数名，不能交替存在。

<!-- compile.error -->

```cangjie
let handler: (name: String, Int64) -> Int64   // Error
```

## 函数类型作为参数类型

示例：函数名为 `printAdd`，其类型是 `((Int64, Int64) -> Int64, Int64, Int64) -> Unit`，表示该函数有三个参数，参数类型分别为函数类型 `(Int64, Int64) -> Int64` 和两个 `Int64`，返回类型为 `Unit`。

<!-- compile -->

```cangjie
func printAdd(add: (Int64, Int64) -> Int64, a: Int64, b: Int64): Unit {
    println(add(a, b))
}
```

## 函数类型作为返回类型

函数类型可以作为另一个函数的返回类型。

如下示例中，函数名为 `returnAdd`，其类型是 `() -> (Int64, Int64) -> Int64`，表示该函数无参数，返回类型为函数类型 `(Int64, Int64) -> Int64`。注意，`->` 是右结合的。

<!-- run -->

```cangjie
func add(a: Int64, b: Int64): Int64 {
    a + b
}

func returnAdd(): (Int64, Int64) -> Int64 {
    add
}

main() {
    var a = returnAdd()
    println(a(1,2))
}
```

## 函数类型作为变量类型

函数名本身也是表达式，它的类型为对应的函数类型。

<!-- compile -->

```cangjie
func add(p1: Int64, p2: Int64): Int64 {
    p1 + p2
}

let f: (Int64, Int64) -> Int64 = add
```

上述示例中，函数名是 `add`，其类型为 `(Int64, Int64) -> Int64`。变量 `f` 的类型与 `add` 类型相同，`add` 被用来初始化 `f`。

若一个函数在当前作用域中被重载（见[函数重载](./function_overloading.md)）了，那么直接使用该函数名作为表达式可能产生歧义，如果产生歧义编译器会报错，例如：

<!-- compile.error -->

```cangjie
func add(i: Int64, j: Int64) {
    i + j
}

func add(i: Float64, j: Float64) {
    i + j
}

main() {
    var f = add   // Error, ambiguous function 'add'
    var plus: (Int64, Int64) -> Int64 = add  // OK
}
```


---

<!-- Content from source_zh_cn/function/nested_functions.md -->
# 嵌套函数

定义在源文件顶层的函数被称为全局函数。定义在函数体内的函数被称为嵌套函数。

使用范围：

- 嵌套函数的作用域仅限于其所在的外部函数。嵌套函数可以访问外部函数的变量和参数，但外部函数不能直接访问嵌套函数的内部变量。
- 嵌套函数可以被外部函数调用，也可以被外部函数返回。

生命周期：

- 嵌套函数的生命周期与外部函数紧密相关。每次外部函数调用时，嵌套函数被创建；外部函数执行完毕后，嵌套函数通常被销毁，除非通过返回或闭包被外部引用。

使用规则和注意事项：

- 仅在对应外部函数中使用嵌套函数。
- 避免过度嵌套。这会使代码结构变得复杂，难以理解和维护，因此避免过多嵌套导致代码混乱。
- 注意闭包的使用。如果嵌套函数被返回并作为闭包使用，需要注意闭包可能会捕获外部函数的变量，导致外部函数的变量在外部函数结束后仍然被占用，从而影响内存管理。

示例，函数 `foo` 内定义了一个嵌套函数 `nestAdd`，可以在 `foo` 内调用该嵌套函数 `nestAdd`，也可以将嵌套函数 `nestAdd` 作为返回值返回，在 `foo` 外对其进行调用：

<!-- verify -->

```cangjie
func foo() {
    func nestAdd(a: Int64, b: Int64) {
        a + b + 3
    }

    println(nestAdd(1, 2))  // 6

    return nestAdd
}

main() {
    let f = foo()
    let x = f(1, 2)
    println("result: ${x}")
}
```

程序会输出：

```text
6
result: 6
```


---

<!-- Content from source_zh_cn/function/lambda.md -->
# Lambda 表达式

## Lambda 表达式定义

Lambda 表达式是一种匿名函数（即没有函数名的函数），其核心设计目的是在程序中快速定义简短的函数逻辑，无需显式声明函数名称。这一概念起源于数学中的 λ 演算（lambda calculus），后被引入多种编程语言（如 C++、Python、C# 等），用于简化代码并提升灵活性。仓颉编程语言中也引入了 Lambda 表达式，具体使用介绍将在本小节展开介绍。

Lambda 表达式的语法为如下形式： `{ p1: T1, ..., pn: Tn => expressions | declarations }`。

其中，`=>` 之前为参数列表，多个参数之间使用 `,` 分隔，每个参数名和参数类型之间使用 `:` 分隔。`=>` 之前也可以没有参数。`=>` 之后为 Lambda 表达式体，是一组表达式或声明序列。Lambda 表达式的参数名的作用域与函数的相同，为 Lambda 表达式的函数体部分，其作用域级别可视为与 Lambda 表达式的函数体内定义的变量等同。

<!-- compile -->

```cangjie
let f1 = { a: Int64, b: Int64 => a + b }

var display = { =>   // Parameterless lambda expression.
    println("Hello")
    println("World")
}
```

Lambda 表达式不管有没有参数，都不可以省略 `=>`，除非其作为[尾随 lambda](./function_call_desugar.md#尾随-lambda)。例如：

<!-- compile -->

```cangjie
var display = { => println("Hello") }

func f2(lam: () -> Unit) {}
let f2Res = f2 { println("World") } // OK to omit the =>
```

Lambda 表达式中参数的类型标注可缺省。以下情形中，若参数类型省略，编译器会尝试进行类型推断，当编译器无法推断出类型时会编译报错：

- Lambda 表达式赋值给变量时，其参数类型根据变量类型推断；
- Lambda 表达式作为函数调用表达式的实参使用时，其参数类型根据函数的形参类型推断。

<!-- compile -->

```cangjie
// The parameter types are inferred from the type of the variable sum1
var sum1: (Int64, Int64) -> Int64 = { a, b => a + b }

var sum2: (Int64, Int64) -> Int64 = { a: Int64, b => a + b }

func f(a1: (Int64) -> Int64): Int64 {
    a1(1)
}

main(): Int64 {
    // The parameter type of lambda is inferred from the type of function f
    f({ a2 => a2 + 10 })
}
```

Lambda 表达式中不支持声明返回类型，其返回类型总是从上下文中推断出来，若无法推断则报错。

- 若上下文明确指定了 Lambda 表达式的返回类型，则其返回类型为上下文指定的类型。

    - Lambda 表达式赋值给变量时，其返回类型根据变量类型推断返回类型：

      <!-- compile -->

      ```cangjie
      let f: () -> Unit = { => println(10) }
      ```

    - Lambda 表达式作为参数使用时，其返回类型根据使用处所在的函数调用的形参类型推断：

      <!-- compile -->

      ```cangjie
      func f(a1: (Int64) -> Int64): Int64 {
        a1(1)
      }

      main(): Int64 {
        f({ a2: Int64 => a2 + 10 })
      }
      ```

    - Lambda 表达式作为返回值使用时，其返回类型根据使用处所在函数的返回类型推断：

      <!-- compile -->

      ```cangjie
      func f(): (Int64) -> Int64 {
        { a: Int64 => a }
      }
      ```

- 若上下文中类型未明确，与推导函数的返回值类型类似，编译器会根据 Lambda 表达式体中所有 return 表达式 `return xxx` 中 xxx 的类型，以及 Lambda 表达式体的类型，来共同推导出 Lambda 表达式的返回类型。

    - `=>` 右侧的内容与普通函数体的规则一样，返回类型为 `Int64`:

      <!-- compile -->

      ```cangjie
      let sum1 = { a: Int64, b: Int64 => a + b }
      ```

    - `=>` 的右侧为空，返回类型为 `Unit`:

      <!-- compile -->

      ```cangjie
      let f = { => }
      ```

## Lambda 表达式调用

Lambda 表达式支持立即调用，例如：

<!-- compile -->

```cangjie
let r1 = { a: Int64, b: Int64 => a + b }(1, 2) // r1 = 3
let r2 = { => 123 }()                          // r2 = 123
```

Lambda 表达式也可以赋值给一个变量，使用变量名进行调用，例如：

<!-- compile -->

```cangjie
func f() {
    var g = { x: Int64 => println("x = ${x}") }
    g(2)
}
```


---

<!-- Content from source_zh_cn/function/closure.md -->
# 闭包

一个函数或 lambda 从定义它的静态作用域中捕获了变量，函数或 lambda 和捕获的变量一起被称为一个闭包，这样即使脱离了闭包定义所在的作用域，闭包也能正常运行。

函数或 lambda 的定义中对于以下几种变量的访问，称为变量捕获：

- 函数的参数缺省值中访问了本函数之外定义的局部变量；

- 函数或 lambda 内访问了本函数或本 lambda 之外定义的局部变量;

- `class`/`struct` 内定义的不是成员函数的函数或 lambda 访问了实例成员变量或 `this`。

以下情形的变量访问不是变量捕获：

- 对定义在本函数或本 lambda 内的局部变量的访问；

- 对本函数或本 lambda 的形参的访问；

- 对全局变量和静态成员变量的访问；

- 对实例成员变量在实例成员函数或属性中的访问。由于实例成员函数或属性将 `this` 作为参数传入，在实例成员函数或属性内通过 `this` 访问所有实例成员变量。

变量的捕获发生在闭包定义时，因此变量捕获有以下规则：

- 被捕获的变量必须在闭包定义时可见，否则编译报错；

- 被捕获的变量必须在闭包定义时已经完成初始化，否则编译报错。

示例 1：闭包 `add`，捕获了 `let` 声明的局部变量 `num`，之后通过返回值返回到 `num` 定义的作用域之外，调用 `add` 时仍可正常访问 `num`。

<!-- verify -->

```cangjie
func returnAddNum(): (Int64) -> Int64 {
    let num: Int64 = 10

    func add(a: Int64) {
        return a + num
    }
    add
}

main() {
    let f = returnAddNum()
    println(f(10))
}
```

程序输出的结果为：

```text
20
```

示例 2：捕获的变量必须在闭包定义时可见。

<!-- compile.error -->

```cangjie
func f() {
    let x = 99
    func f1() {
        println(x)
    }
    let f2 = { =>
        println(y)  // Error, cannot capture 'y' which is not defined yet
    }
    let y = 88
    f1()            // Print 99
    f2()
}
```

示例 3：捕获的变量必须在闭包定义前完成初始化。

<!-- compile.error -error-->

```cangjie
func f() {
    let x: Int64
    func f1() {
        println(x) // Error, x is not initialized yet
    }
    x = 99
    f1()
}
```

示例 4：如果捕获的变量是引用类型，可修改其可变实例成员变量的值。

<!-- run -->

```cangjie
class C {
    public var num: Int64 = 0
}

func returnIncrementer(): () -> Unit {
    let c: C = C()

    func incrementer() {
        c.num++
    }

    incrementer
}

main() {
    let f = returnIncrementer()
    f() // c.num increases by 1
}
```

示例 5：为了防止捕获了 `var` 声明变量的闭包逃逸，这类闭包只能被调用，不能作为一等公民使用，包括不能赋值给变量，不能作为实参或返回值使用，不能直接将闭包的名字作为表达式使用。其中，闭包逃逸是指在函数执行完毕后仍然可以在函数外部被调用的闭包。

<!-- compile.error -->

```cangjie
func f() {
    var x = 1
    let y = 2

    func g() {
        println(x)  // OK, captured a mutable variable.
    }
    let b = g       // Error, g cannot be assigned to a variable

    g               // Error, g cannot be used as an expression
    g()             // OK, g can be invoked

    g               // Error, g cannot be used as a return value
}
```

示例 6：需要注意的是，捕获具有传递性。如果一个函数 `f` 调用了捕获 `var` 变量的函数 `g`，且 `g` 捕获的 `var` 变量不在函数 `f` 内定义，那么函数 `f` 同样捕获了 `var` 变量，此时，`f` 也不能作为一等公民使用。

示例 6.1：`g` 捕获了 `var` 声明的变量 `x`，`f` 调用了 `g`，且 `g` 捕获的 `x` 不在 `f` 内定义，`f` 同样不能作为一等公民使用：

<!-- compile.error -error-->

```cangjie
func h(){
    var x = 1

    func g() { x }  // captured a mutable variable

    func f() {
        g()         // invoked g
    }
    return f        // Error
}
```

示例 6.2：`g` 捕获了 `var` 声明的变量 `x`，`f` 调用了 `g`。但 `g` 捕获的 `x` 在 `f` 内定义，`f` 没有捕获其他 `var` 声明的变量。因此，`f` 仍作为一等公民使用：

<!-- compile -->

```cangjie
func h(){
    func f() {
        var x = 1
        func g() { x } // captured a mutable variable

        g()
    }
    return f // OK
}
```

示例 7：静态成员变量和全局变量的访问，不属于变量捕获，因此访问了 `var` 修饰的全局变量、静态成员变量的函数或 lambda 仍可作为一等公民使用。

<!-- compile -->

```cangjie
class C {
    static public var a: Int32 = 0
    static public func foo() {
        a++ // OK
        return a
    }
}

var globalV1 = 0

func countGlobalV1() {
    globalV1++
    C.a = 99
    let g = C.foo // OK
}

func g(){
    let f = countGlobalV1 // OK
    f()
}
```


---

<!-- Content from source_zh_cn/function/function_call_desugar.md -->
# 函数调用语法糖

## 尾随 lambda

尾随 lambda 可以使函数的调用看起来像是语言内置的语法一样，增加语言的可扩展性。

当函数最后一个形参是函数类型，并且函数调用对应的实参是 lambda 时，可以使用尾随 lambda 语法，将 lambda 放在函数调用的尾部，圆括号外面。

例如，下例中定义了一个 `myIf` 函数，它的第一个参数是 `Bool` 类型，第二个参数是函数类型。当第一个参数的值为 `true` 时，返回第二个参数调用后的值，否则返回 `0`。调用 `myIf` 时可以像普通函数一样调用，也可以使用尾随 lambda 的方式调用。

<!-- compile -->

```cangjie
func myIf(a: Bool, fn: () -> Int64) {
    if(a) {
        fn()
    } else {
        0
    }
}

func test() {
    myIf(true, { => 100 }) // General function call

    myIf(true) {        // Trailing closure call
        100
    }
}
```

当函数调用有且只有一个 lambda 实参时，还可以省略 `()`，只写 lambda。

示例：

<!-- compile -->

```cangjie
func f(fn: (Int64) -> Int64) { fn(1) }

func test() {
    f { i => i * i }
}
```

## Flow 表达式

流操作符包括两种：表示数据流向的中缀操作符 `|>` （称为 `pipeline`）和表示函数组合的中缀操作符 `~>` （称为 `composition`）。

### Pipeline 表达式

当需要对输入数据做一系列的处理时，可以使用 `pipeline` 表达式来简化描述。`pipeline` 表达式的语法形式如下：`e1 |> e2`。等价于如下形式的语法糖：`let v = e1; e2(v)` 。

其中 `e2` 是函数类型的表达式，`e1` 的类型是 `e2` 的参数类型的子类型。

示例：

<!-- compile -->

```cangjie
func inc(x: Array<Int64>): Array<Int64> { // Increasing the value of each element in the array by '1'
    let s = x.size
    var i = 0
    for (e in x where i < s) {
        x[i] = e + 1
        i++
    }
    x
}

func sum(y: Array<Int64>): Int64 { // Get the sum of elements in the array
    var s = 0
    for (j in y) {
        s += j
    }
    s
}

let arr: Array<Int64> = [1, 3, 5]
let res = arr |> inc |> sum // res = 12
```

### Composition 表达式

`composition` 表达式表示两个单参函数的组合。`composition` 表达式语法为 `f ~> g`，等价于 `{ x => g(f(x)) }`。

其中 `f` 和 `g` 均为只有一个参数的函数类型的表达式。

`f` 和 `g` 组合，则要求 `f(x)` 的返回类型是 `g(...)` 的参数类型的子类型。

示例 1：

<!-- compile -->

```cangjie
func f(x: Int64): Float64 {
    Float64(x)
}
func g(x: Float64): Float64 {
    x
}

var fg = f ~> g // The same as { x: Int64 => g(f(x)) }
```

示例 2：

<!-- compile -->

```cangjie
func f(x: Int64): Float64 {
    Float64(x)
}

let lambdaComp = {x: Int64 => x} ~> f // The same as { x: Int64 => f({x: Int64 => x}(x)) }
```

示例 3：

<!-- compile -->

```cangjie
func h1<T>(x: T): T { x }
func h2<T>(x: T): T { x }
var hh = h1<Int64> ~> h2<Int64> // The same as { x: Int64 => h2<Int64>(h1<Int64>(x)) }
```

> **注意：**
>
> 表达式 f ~> g 中，会先对 f 求值，然后对 g 求值，最后才会进行函数的组合。

另外，流操作符不能与无默认值的命名形参函数直接一同使用，这是因为无默认值的命名形参函数必须给出命名实参才可以调用。例如：

<!-- compile.error -->

```cangjie
func f(a!: Int64): Unit {}

var a = 1 |> f  // Error
```

如果需要使用，开发者可以通过 lambda 表达式传入 `f` 函数的命名实参：

<!-- compile -->

```cangjie
func f(a!: Int64): Unit {}

var x = 1 |>  { x: Int64 => f(a: x) } // OK
```

由于相同的原因，当 `f` 的参数有默认值时，直接与流运算符一起使用也是错误的，例如：

<!-- compile.error -->

```cangjie
func f(a!: Int64 = 2): Unit {}

var a = 1 |> f // Error
```

但是当命名形参都存在默认值时，不需要给出命名实参也可以调用该函数，函数仅需要传入非命名形参，那么这种函数是可以同流运算符一起使用的，例如：

<!-- compile -->

```cangjie
func f(a: Int64, b!: Int64 = 2): Unit {}

var a = 1 |> f  // OK
```

当然，如果想要在调用 `f` 时，为参数 `b` 传入其他参数，那么也需要借助 lambda 表达式：

<!-- compile -->

```cangjie
func f(a: Int64, b!: Int64 = 2): Unit {}

var a = 1 |> {x: Int64 => f(x,  b: 3)}  // OK
```

## 变长参数

变长参数是一种特殊的函数调用语法糖。当形参最后一个非命名参数是 `Array` 类型时，实参中对应位置可以直接传入参数序列代替 `Array` 字面量（参数个数可以是 0 个或多个）。示例如下：

<!-- verify -->

```cangjie
func sum(arr: Array<Int64>) {
    var total = 0
    for (x in arr) {
        total += x
    }
    return total
}

main() {
    println(sum())
    println(sum(1, 2, 3))
}
```

程序输出：

```text
0
6
```

需要注意，只有最后一个非命名参数可以作为变长参数，命名参数不能使用这个语法糖。

<!-- compile.error -->

```cangjie
func length(arr!: Array<Int64>) {
    return arr.size
}

main() {
    println(length())        // Error, expected 1 argument, found 0
    println(length(1, 2, 3)) // Error, expected 1 argument, found 3
}
```

变长参数可以出现在全局函数、静态成员函数、实例成员函数、局部函数、构造函数、函数变量、lambda、函数调用操作符重载、索引操作符重载的调用处。不支持其他操作符重载、composition、pipeline 这几种调用方式。示例如下：

<!-- verify -->

```cangjie
class Counter {
    var total = 0
    init(data: Array<Int64>) { total = data.size }
    operator func ()(data: Array<Int64>) { total += data.size }
}

main() {
    let counter = Counter(1, 2)
    println(counter.total)
    counter(3, 4, 5)
    println(counter.total)
}
```

程序输出：

```text
2
5
```

函数重载决议总是会优先考虑不使用变长参数就能匹配的函数，只有在所有函数都不能匹配，才尝试使用变长参数解析。示例如下：

<!-- verify -->

```cangjie
func f<T>(x: T) where T <: ToString {
    println("item: ${x}")
}

func f(arr: Array<Int64>) {
    println("array: ${arr}")
}

main() {
    f()
    f(1)
    f(1, 2)
}
```

程序输出：

```text
array: []
item: 1
array: [1, 2]
```

当编译器无法决议时会报错：

<!-- compile.error -->

```cangjie
func f(arr: Array<Int64>) { arr.size }
func f(first: Int64, arr: Array<Int64>) { first + arr.size }

main() {
    println(f(1, 2, 3)) // Error
}
```


---

<!-- Content from source_zh_cn/function/function_overloading.md -->
# 函数重载

## 函数重载定义

在仓颉编程语言中，如果一个作用域中，一个函数名对应多个函数定义，这种现象称为函数重载。

- 函数名相同，函数参数不同（是指参数个数不同，或者参数个数相同但参数类型不同）的两个函数构成重载。示例如下：

  <!-- compile -->

  ```cangjie
  // Scenario 1

  func f(a: Int64): Unit {}
  func f(a: Float64): Unit {}
  func f(a: Int64, b: Float64): Unit {}
  ```

- 对于两个同名泛型函数 (详见[泛型函数](../generic/generic_function.md#泛型函数)章节），如果重命名一个函数的泛型形参后（使泛型参数顺序相同），其非泛型部分与另一个函数的非泛型部分函数参数不同，则两个函数构成重载，否则这两个泛型函数构成重复定义错误（类型变元的约束不参与判断）。示例如下：

  <!-- compile.error -->

  ```cangjie
  // Scenario 2

  interface I1{}
  interface I2{}

  func f1<X, Y>(a: X, b: Y) {}
  func f1<Y, X>(a: X, b: Y) {} // OK: after rename generic type parameter, it will be 'func f1<X, Y>(a: Y, b: X)'

  func f2<T>(a: T) where T <: I1 {} // Error, not overloading
  func f2<T>(a: T) where T <: I2 {} // Error, not overloading
  ```

- 同一个类内的两个构造函数参数不同，构成重载。示例如下：

  <!-- compile -->

  ```cangjie
  // Scenario 3

  class C {
      var a: Int64
      var b: Float64

      public init(a: Int64, b: Float64) {
          this.a = a
          this.b = b
      }

      public init(a: Int64) {
          b = 0.0
          this.a = a
      }
  }
  ```

- 同一个类内的主构造函数和 `init` 构造函数参数不同，构成重载（认为主构造函数和 `init` 函数具有相同的名字）。示例如下：

  <!-- compile -->

  ```cangjie
  // Scenario 4

  class C {
      C(var a!: Int64, var b!: Float64) {
          this.a = a
          this.b = b
      }

      public init(a: Int64) {
          b = 0.0
          this.a = a
      }
  }
  ```

- 两个函数名相同，参数不同的函数定义在不同的作用域，在两个函数都可见的作用域中构成重载。示例如下：

  <!-- compile -->

  ```cangjie
  // Scenario 5

  func f(a: Int64): Unit {}

  func g() {
      func f(a: Float64): Unit {}
  }
  ```

- 如果子类中存在与父类同名的函数，并且函数的参数类型不同，则构成函数重载。示例如下：

  <!-- compile -->

  ```cangjie
  // Scenario 6
  open class Base {
      public func f(a: Int64): Unit {}
  }

  class Sub <: Base {
      public func f(a: Float64): Unit {}
  }
  ```

只允许函数声明引入的函数重载，但是以下情形不构成重载，不构成重载的两个名字不能定义或声明在同一个作用域内：

- class、interface、struct 类型的静态成员函数和实例成员函数之间不能重载
- enum 类型的 constructor、静态成员函数和实例成员函数之间不能重载

如下示例，两个变量均为函数类型且函数参数类型不同，但由于它们不是函数声明所以不能重载，如下示例将编译报错（重定义错）：

<!-- compile.error -->

```cangjie
main() {
    var f: (Int64) -> Unit
    var f: (Float64) -> Unit
}
```

如下示例，虽然变量 `f` 为函数类型，但由于变量和函数之间不能同名，如下示例将编译报错（重定义错）：

<!-- compile.error -->

```cangjie
main() {
    var f: (Int64) -> Unit
    func f(a: Float64): Unit {} // Error, functions and variables cannot have the same name
}
```

如下示例，静态成员函数 `f` 与实例成员函数 `f` 的参数类型不同，但由于类内静态成员函数和实例成员函数之间不能重载，如下示例将编译报错：

<!-- compile.error -->

```cangjie
class C {
    public static func f(a: Int64): Unit {}
    public func f(a: Float64): Unit {}
}
```

## 函数重载决议

函数调用时，所有可被调用的函数（是指当前作用域可见且能通过类型检查的函数）构成候选集，候选集中有多个函数，究竟选择候选集中哪个函数，需要进行函数重载决议，有如下规则：

- 优先选择作用域级别高的作用域内的函数。在嵌套的表达式或函数中，越是内层作用域级别越高。

  如下示例中在 `inner` 函数体内调用 `g(Sub())` 时，候选集包括 `inner` 函数内定义的函数 `g` 和 `inner` 函数外定义的函数 `g`，函数决议选择作用域级别更高的 `inner` 函数内定义的函数 `g`。

    <!-- compile -->

    ```cangjie
    open class Base {}
    class Sub <: Base {}

    func outer() {
        func g(a: Sub) {
            print("1")
        }

        func inner() {
            func g(a: Base) {
                print("2")
            }

            g(Sub())   // Output: 2
        }
    }
    ```

- 如果作用域级别相对最高的仍有多个函数，则需要选择最匹配的函数（对于函数 f 和 g 以及给定的实参，如果 f 可以被调用时 g 也总是可以被调用的，但反之不然，则称 f 比 g 更匹配）。如果不存在唯一最匹配的函数，则报错。

  如下示例中，两个函数 `g` 定义在同一作用域，选择更匹配的函数 `g(a: Sub): Unit`。

    <!-- compile -->

    ```cangjie
    open class Base {}
    class Sub <: Base {}

    func outer() {
        func g(a: Sub) {
            print("1")
        }
        func g(a: Base) {
            print("2")
        }

        g(Sub())   // Output: 1

    }
    ```

- 子类和父类认为是同一作用域。如下示例中，一个函数 `g` 定义在父类中，另一个函数 `g` 定义在子类中，在调用 `s.g(Sub())` 时，两个函数 `g` 当成同一作用域级别决议，则选择更匹配的父类中定义的函数 `g(a: Sub): Unit`。

    <!-- compile -->

    ```cangjie
    open class Base {
        public func g(a: Sub) {
            print("1")
        }
    }

    class Sub <: Base {
        public func g(a: Base) {
            print("2")
        }
    }

    func outer() {
        let s: Sub = Sub()
        s.g(Sub()) // Output: 1
    }
    ```


---

<!-- Content from source_zh_cn/function/operator_overloading.md -->
# 操作符重载

如果希望在某个类型上支持此类型默认不支持的操作符，可以使用操作符重载实现。

如果需要在某个类型上重载某个操作符，可以通过为类型定义一个函数名为此操作符的函数的方式实现，这样，在该类型的实例使用该操作符时，就会自动调用此操作符函数。

操作符函数定义与普通函数定义相似，区别如下：

- 定义操作符函数时需要在 `func` 关键字前面添加 `operator` 修饰符；
- 操作符函数的参数个数需要匹配对应操作符的要求（详见附录[操作符](../Appendix/operator.md)）；
- 操作符函数只能定义在 class、interface、struct、enum 和 extend 中；
- 操作符函数具有实例成员函数的语义，所以禁止使用 `static` 修饰符；
- 操作符函数不能为泛型函数。

另外，需要注意的是，被重载后的操作符不改变它们固有的优先级和结合性（详见附录[操作符](../Appendix/operator.md)）。

## 操作符重载函数定义和使用

定义操作符函数有两种方式：

1. 对于可以直接包含函数定义的类型 (包括 `struct`、`enum`、`class` 和 `interface` )，可以直接在其内部定义操作符函数的方式实现操作符的重载。
2. 使用 `extend` 的方式为其添加操作符函数，从而实现操作符在这些类型上的重载。对于无法直接包含函数定义的类型（是指除 `struct`、`class`、`enum` 和 `interface` 之外其他的类型）或无法改变其实现的类型，比如第三方定义的 `struct`、`class`、`enum` 和 `interface`，只能采用这种方式（参见[扩展](../extension/extend_overview.md)）。

操作符函数对参数类型的约定如下：

1. 对于一元操作符，操作符函数没有参数，对返回值的类型没有要求。

2. 对于二元操作符，操作符函数只有一个参数，对返回值的类型没有要求。

   如下示例中介绍了一元操作符和二元操作符的定义和使用：

   `-` 实现对一个 `Point` 实例中两个成员变量 `x` 和 `y` 取负值，然后返回一个新的 `Point` 对象，`+` 实现对两个 `Point` 实例中两个成员变量 `x` 和 `y` 分别求和，然后返回一个新的 `Point` 对象。

    <!-- run -overloadOperater -->

    ```cangjie
    open class Point {
        var x: Int64 = 0
        var y: Int64 = 0
        public init (a: Int64, b: Int64) {
            x = a
            y = b
        }

        public operator func -(): Point {
            Point(-x, -y)
        }
        public operator func +(right: Point): Point {
            Point(this.x + right.x, this.y + right.y)
        }
    }
    ```

   接下来，就可以在 `Point` 的实例上直接使用一元 `-` 操作符和二元 `+` 操作符：

    <!-- run -overloadOperater -->

    ```cangjie
    main() {
        let p1 = Point(8, 24)
        let p2 = -p1      // p2 = Point(-8, -24)
        let p3 = p1 + p2  // p3 = Point(0, 0)
    }
    ```

3. 索引操作符（`[]`）分为取值 `let a = arr[i]` 和赋值 `arr[i] = a` 两种形式，它们通过是否存在特殊的命名参数 value 来区分不同的重载。索引操作符重载不要求同时重载两种形式，可以只重载赋值不重载取值，反之亦可。

   索引操作符取值形式 `[]` 内的参数序列对应操作符重载的非命名参数，可以是 1 个或多个，可以是任意类型。不可以有其他命名参数。返回类型可以是任意类型。

    <!-- compile -->

    ```cangjie
    class A {
        operator func [](arg1: Int64, arg2: String): Int64 {
            return 0
        }
    }

    func f() {
        let a = A()
        let b: Int64 = a[1, "2"]
        // b == 0
    }
    ```

   索引操作符赋值形式 `[]` 内的参数序列对应操作符重载的非命名参数，可以是 1 个或多个，可以是任意类型。`=` 右侧的表达式对应操作符重载的命名参数，有且只能有一个命名参数，该命名参数的名称必须是 value, 不能有默认值，value 可以是任意类型。返回类型必须是 Unit 类型。

   需要注意的是，value 只是一种特殊的标记，在索引操作符赋值时并不需要使用命名参数的形式调用。

    <!-- compile -->

    ```cangjie
    class A {
        operator func [](arg1: Int64, arg2: String, value!: Int64): Unit {
            return
        }
    }

    func f() {
        let a = A()
        a[1, "2"] = 0
    }
    ```

   特别的，除 `enum` 外的不可变类型不支持重载索引操作符赋值形式。

4. 函数调用操作符（`()`）重载函数，输入参数和返回值类型可以是任意类型。示例如下：

    <!-- compile -->

    ```cangjie
    open class A {
        public init() {}

        public operator func ()(): Unit {}
    }

    func test1() {
        let a = A() // OK, A() is call the constructor of A
        a()         // OK, a() is to call the operator () overloading function
    }
    ```

   不能使用 `this` 或 `super` 调用 `()` 操作符重载函数。示例如下：

    <!-- compile.error -->

    ```cangjie
    open class A {
        public init() {}
        public init(x: Int64) {
            this() // OK, this() calls the constructor of A
        }

        public operator func ()(): Unit {}

        public func foo() {
            this()  // Error, this() calls the constructor of A.
            super() // Error
        }
    }

    class B <: A {
        public init() {
            super() // OK, super()  calls the constuctor of the super class
        }

        public func goo() {
            super() // Error
        }
    }
    ```

   对于枚举类型，当构造器形式和 `()` 操作符重载函数形式都满足时，优先匹配构造器形式。示例如下：

    <!-- compile -->

    ```cangjie
    enum E {
        Y | X | X(Int64)

        public operator func ()(p: Int64) {}
        public operator func ()(p: Float64) {}
    }

    main() {
        let e = X(1)    // OK, X(1) is to call the constructor X(Int64)
        X(1.0)          // OK, X(1.0) is to call the operator () overloading function
        let e1 = X
        e1(1)           // OK, e1(1) is to call the operator () overloading function
        Y(1)            // OK, Y(1) is to call the operator () overloading function
    }
    ```

## 可以被重载的操作符

下表列出了所有可以被重载的操作符（优先级从高到低）：

| Operator            | Description           |
|:--------------------|:----------------------|
| `()`                | Function call         |
| `[]`                | Indexing              |
| `!`                 | NOT                   |
| `-`                 | Negative              |
| `**`                | Power                 |
| `*`                 | Multiply              |
| `/`                 | Divide                |
| `%`                 | Remainder             |
| `+`                 | Add                   |
| `-`                 | Subtract              |
| `<<`                | Bitwise left shift    |
| `>>`                | Bitwise right shift   |
| `<`                 | Less than             |
| `<=`                | Less than or equal    |
| `>`                 | Greater than          |
| `>=`                | Greater than or equal |
| `==`                | Equal                 |
| `!=`                | Not equal             |
| `&`                 | Bitwise AND           |
| `^`                 | Bitwise XOR           |
| <code>&vert;</code> | Bitwise OR            |

需要注意的是：

> **注意：**
>
> - 一旦在某个类型上重载了除关系操作符（`<`、`<=`、`>`、`>=`、`==` 和 `!=`）之外的其他二元操作符，并且操作符函数的返回类型与左操作数的类型一致或是其子类型，那么此类型支持对应的复合赋值操作符。当操作符函数的返回类型与左操作数的类型不一致且不是其子类型时，在使用对应的复合赋值符号时将报类型不匹配错误。
>   <!-- compile.error -->
>
>   ```cangjie
>   open class MyClass {
>       var x: Int64 = 0
>       public init (a: Int64) {
>           x = a
>       }
>
>       public operator func +(right: MyClass): Int64 { // The above rules are not met
>           this.x + right.x
>       }
>   }
>
>   main() {
>       var a = MyClass(5)
>       var b = MyClass(3)
>       a += b; // Error, type incompatible in this compound assignment expression
>   }
>   ```
>
> - 仓颉编程语言不支持自定义操作符，即不允许定义除上表中所列 `operator` 之外的其他操作符函数。
> - 对于类型 `T`, 如果 `T` 已经默认支持了上述若干可重载操作符，那么通过扩展的方式再次为其实现同签名的操作符函数时将报重定义错误。例如，为数值类型重载其已支持的同签名算术操作符、位操作符或关系操作符等操作符时，为 `Rune` 重载同签名的关系操作符时，为 `Bool` 类型重载同签名的逻辑操作符、判等或不等操作符时，等等这些情况，均会报重定义错误。
>   <!-- compile.error -->
>
>   ```cangjie
>   extend Int64 {
>       public operator func +(x: Int64, y: Int64): Int64 { // Error, invalid number of parameters for operator '+'
>           x + y
>       }
>   }
>   ```


---

<!-- Content from source_zh_cn/function/const_func_and_eval.md -->
# const 函数和常量求值

常量求值允许某些特定形式的表达式在编译时求值，可以减少程序运行时需要的计算。本章主要介绍常量求值的使用方法与规则。

## `const` 上下文与 `const` 表达式

`const` 上下文是指 `const` 变量初始化表达式，这些表达式始终在编译时求值。因此需要对 `const` 上下文中允许的表达式加以限制，避免修改全局状态、I/O 等副作用，确保其可以在编译时求值。

`const` 表达式具备了可以在编译时求值的能力。满足如下规则的表达式是 `const` 表达式：

1. 数值类型、`Bool`、`Unit`、`Rune`、`String` 类型的字面量（不包含插值字符串）。
2. 所有元素都是 `const` 表达式的 `Array` 字面量（不能是 `Array` 类型，可以使用 `VArray` 类型），`tuple` 字面量。
3. `const` 变量，`const` 函数形参，`const` 函数中的局部变量。
4. `const` 函数，包含使用 `const` 声明的函数名、符合 `const` 函数要求的 `lambda`、以及这些函数返回的函数表达式。
5. `const` 函数调用（包含 `const` 构造函数），该函数的表达式必须是 `const` 表达式，所有实参必须都是 `const` 表达式。
6. 所有参数都是 `const` 表达式的 `enum` 构造器调用，和无参数的 `enum` 构造器。
7. 数值类型、`Bool`、`Unit`、`Rune`、`String` 类型的算术表达式、关系表达式、位运算表达式，所有操作数都必须是 `const` 表达式。
8. `if`、`match`、`try`、`throw`、`return`、`is`、`as`。这些表达式内的表达式必须都是 `const` 表达式。
9. `const` 表达式的成员访问（不包含属性的访问），`tuple` 的索引访问。
10. `const init` 和 `const` 函数中的 `this` 和 `super` 表达式。
11. `const` 表达式的 `const` 实例成员函数调用，且所有实参必须都是 `const` 表达式。

> **注意：**
>
> 当前编译器实现暂不支持 `throw` 作为 `const` 表达式使用。

## `const` 函数

`const` 函数是一类特殊的函数，这些函数具备了可以在编译时求值的能力。在 `const` 上下文中调用这种函数时，这些函数会在编译时执行计算。而在其他非 `const` 上下文，`const` 函数会和普通函数一样在运行时执行。

下例是一个计算平面上两点距离的 `const` 函数，`distance` 中使用 `let` 定义了两个局部变量 `dx` 和 `dy`：

<!-- verify -->

```cangjie
struct Point {
    const Point(let x: Float64, let y: Float64) {}
}

const func distance(a: Point, b: Point) {
    let dx = a.x - b.x
    let dy = a.y - b.y
    (dx ** 2 + dy ** 2) ** 0.5
}

main() {
    const a = Point(3.0, 0.0)
    const b = Point(0.0, 4.0)
    const d = distance(a, b)
    println(d)
}
```

编译运行输出：

```text
5.000000
```

需要注意：

1. `const` 函数声明必须使用 `const` 修饰。
2. 全局 `const` 函数和 `static const` 函数中只能访问 `const` 声明的外部变量，包含 `const` 全局变量、`const` 静态成员变量，其他外部变量都不可访问。`const init` 函数和 `const` 实例成员函数除了能访问 `const` 声明的外部变量，还可以访问当前类型的实例成员变量。
3. `const` 函数中的表达式都必须是 `const` 表达式，`const init` 函数除外。
4. `const` 函数中可以使用 `let`、`const` 声明新的局部变量。但不支持 `var`。
5. `const` 函数中的参数类型和返回类型没有特殊规定。如果该函数调用的实参不符合 `const` 表达式要求，那这个函数调用不能作为 `const` 表达式使用，但仍然可以作为普通表达式使用。
6. `const` 函数不一定都会在编译时执行，例如可以在非 `const` 函数中运行时调用。
7. `const` 函数与非 `const` 函数重载规则一致。
8. 数值类型、`Bool`、`Unit`、`Rune`、`String` 类型 和 `enum` 支持定义 `const` 实例成员函数。
9. 对于 `struct` 和 `class`，只有定义了 `const init` 才能定义 `const` 实例成员函数。`class` 中的 `const` 实例成员函数不能是 `open` 的。`struct` 中的 `const` 实例成员函数不能是 `mut` 的。

另外，接口中也可以定义 `const` 函数，但会受到以下规则限制：

1. 接口中的 `const` 函数，实现类型必须也用 `const` 函数才算实现接口。
2. 接口中的非 `const` 函数，实现类型使用 `const` 或非 `const` 函数都算实现接口。
3. 接口中的 `const` 函数与接口的 `static` 函数一样，只有在该接口作为泛型约束的时候，受约束的泛型变元或变量才能使用这些 `const` 函数。

在下面的例子中，在接口 `I` 里定义了两个 `const` 函数，类 `A` 实现了接口 `I`，泛型函数 `g` 的形参类型上界是 `I`。

<!-- verify -->

```cangjie
interface I {
    const func f(): Int64
    const static func f2(): Int64
}

class A <: I {
    public const func f() { 0 }
    public const static func f2() { 1 }
    const init() {}
}

const func g<T>(i: T) where T <: I {
    return i.f() + T.f2()
}

main() {
    println(g(A()))
}
```

编译执行上述代码，输出结果为：

```text
1
```

## `const init`

如果一个 `struct` 或 `class` 定义了 `const` 构造器，那么这个 `struct`/`class` 实例可以用在 `const` 表达式中。

1. 如果当前类型是 `class`，则不能具有 `var` 声明的实例成员变量，否则不允许定义 `const init` 。如果当前类型具有父类，当前的 `const init` 必须调用父类的 `const init`（可以显式调用或者隐式调用无参`const init`），如果父类没有 `const init` 则报错。

    <!-- compile.error -->

    ```cangjie
    public class Foo {
        val a: Int64 = 9 // Error, expected declaration, found 'val'
        let b: String
        const init(b: String) {
            this.b = b
        }
    }
    ```

    <!-- compile.error -->

    ```cangjie
    open public class Boo {
        let boo: String
        const init(b: String) {
            this.boo = b
        }
    }

    public class Foo <: Boo {
        let c: String
        const init(c: String) { //Error, there is no non-parameter constructor in super class, please invoke super call explicitly
            this.c = c
        }
    }
    ```

2. 当前类型的实例成员变量如果有初始值，初始值必须要是 `const` 表达式，否则不允许定义 `const init`。

    <!-- compile.error -->

    ```cangjie
    var a = "4123"

    class Foo {
        let foo: String = a // Error, expected 'const' expression guaranteed to be evaluated at compile time
        const init() {}
    }
    ```

3. `const init` 内可以使用赋值表达式 `=` 对实例成员变量赋值，除此以外不能有其他赋值表达式（如 `+=`, `-=`）。

    <!-- compile.error -->

    ```cangjie
    var a = "4123"

    class Foo {
        let foo: String
        let boo: Int64
        const init() {
            foo = "aa" // OK
            boo += 10 // Error, variable 'boo' is used before initialization
        }
    }
    ```

`const init` 与 `const` 函数的区别是 `const init` 内允许对实例成员变量进行赋值（需要使用赋值表达式）。


---

<!-- Content from source_zh_cn/struct/define_struct.md -->
# 定义 struct 类型

`struct` 类型的定义以关键字 `struct` 开头，后跟 `struct` 的名字，接着是定义在一对花括号中的 `struct` 定义体。`struct` 定义体中可以定义一系列的成员变量、成员属性（参见[属性](../class_and_interface/prop.md)）、静态初始化器、构造函数和成员函数。

<!-- compile -->

```cangjie
struct Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }

    public func area() {
        width * height
    }
}
```

上例中定义了名为 `Rectangle` 的 `struct` 类型，它有两个 `Int64` 类型的成员变量 `width` 和 `height`，一个有两个 `Int64` 类型参数的构造函数（使用关键字 `init` 定义，函数体中通常是对成员变量的初始化），以及一个成员函数 `area`（返回 `width` 和 `height` 的乘积）。

> **注意：**
>
> `struct` 只能定义在源文件的顶层作用域。

## struct 成员变量

`struct` 成员变量分为实例成员变量和静态成员变量（使用 `static` 修饰符修饰），二者访问上的区别在于实例成员变量只能通过 `struct` 实例（说 `a` 是 `T` 类型的实例，指的是 `a` 是一个 `T` 类型的值）访问，静态成员变量只能通过 `struct` 类型名访问。

实例成员变量定义时可以不设置初值（但必须标注类型，如上例中的 `width` 和 `height`），也可以设置初值，例如：

<!-- compile -->

```cangjie
struct Rectangle {
    let width = 10
    let height = 20
}
```

## struct 静态初始化器

`struct` 支持定义静态初始化器，并在静态初始化器中通过赋值表达式来对静态成员变量进行初始化。

静态初始化器以关键字组合 `static init` 开头，后跟无参参数列表和函数体，且不能被访问修饰符修饰。函数体中必须完成对所有未初始化的静态成员变量的初始化，否则编译报错。

<!-- compile -->

```cangjie
struct Rectangle {
    static let degree: Int64
    static init() {
        degree = 180
    }
}
```

一个 `struct` 中最多允许定义一个静态初始化器，否则报重定义错误。

<!-- compile.error -->

```cangjie
struct Rectangle {
    static let degree: Int64
    static init() {
        degree = 180
    }
    static init() { // Error, redefinition with the previous static init function
        degree = 180
    }
}
```

## struct 构造函数

`struct` 支持两类构造函数：普通构造函数和主构造函数。

普通构造函数以关键字 `init` 开头，后跟参数列表和函数体，函数体中必须完成对所有未初始化的实例成员变量的初始化（如果参数名和成员变量名无法区分，可以在成员变量前使用 `this` 加以区分，`this` 表示 `struct` 的当前实例），否则编译报错。

<!-- compile.error -->

```cangjie
struct Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64, height: Int64) { // Error, 'height' is not initialized in the constructor
        this.width = width
    }
}
```

一个 `struct` 中可以定义多个普通构造函数，但它们必须构成重载（参见[函数重载](../function/function_overloading.md)），否则报重定义错误。

<!-- compile.error -->

```cangjie
struct Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64) {
        this.width = width
        this.height = width
    }

    public init(width: Int64, height: Int64) { // OK: overloading with the first init function
        this.width = width
        this.height = height
    }

    public init(height: Int64) { // Error, redefinition with the first init function
        this.width = height
        this.height = height
    }
}
```

除了可以定义若干普通的以 `init` 为名字的构造函数外，`struct` 内还可以定义（最多）一个主构造函数。主构造函数的名字和 `struct` 类型名相同，它的参数列表中可以有两种形式的形参：普通形参和成员变量形参（需要在参数名前加上 `let` 或 `var`），成员变量形参同时扮演定义成员变量和构造函数参数的功能。

使用主构造函数通常可以简化 `struct` 的定义，例如，上述包含一个 `init` 构造函数的 `Rectangle` 可以简化为如下定义：

<!-- compile -->

```cangjie
struct Rectangle {
    public Rectangle(let width: Int64, let height: Int64) {}
}
```

主构造函数的参数列表中也可以定义普通形参，例如：

<!-- compile -->

```cangjie
struct Rectangle {
    public Rectangle(name: String, let width: Int64, let height: Int64) {}
}
```

如果 `struct` 定义中不存在自定义构造函数（包括主构造函数），并且所有实例成员变量都有初始值，则会自动为其生成一个无参构造函数（调用此无参构造函数会创建一个所有实例成员变量的值均等于其初值的对象）；否则，不会自动生成此无参构造函数。例如，对于如下 `struct` 定义，注释中给出了自动生成的无参构造函数：

<!-- compile -->

```cangjie
struct Rectangle {
    let width: Int64 = 10
    let height: Int64 = 10
    /* Auto-generated memberwise constructor:
    public init() {
    }
    */
}
```

## struct 成员函数

`struct` 成员函数分为实例成员函数和静态成员函数（使用 `static` 修饰符修饰），二者的区别在于：实例成员函数只能通过 `struct` 实例访问，静态成员函数只能通过 `struct` 类型名访问；静态成员函数中不能访问实例成员变量，也不能调用实例成员函数，但在实例成员函数中可以访问静态成员变量以及静态成员函数。

下例中，`area` 是实例成员函数，`typeName` 是静态成员函数。

<!-- compile -->

```cangjie
struct Rectangle {
    let width: Int64 = 10
    let height: Int64 = 20

    public func area() {
        this.width * this.height
    }

    public static func typeName(): String {
        "Rectangle"
    }
}
```

实例成员函数中可以通过 `this` 访问实例成员变量，例如：

<!-- compile -->

```cangjie
struct Rectangle {
    let width: Int64 = 1
    let height: Int64 = 1

    public func area() {
        this.width * this.height
    }
}
```

## struct 成员的访问修饰符

`struct` 的成员（包括成员变量、成员属性、构造函数、成员函数、操作符函数（详见[操作符重载](../function/operator_overloading.md)章节））用 4 种访问修饰符修饰：`private`、`internal`、`protected` 和 `public`，缺省的修饰符是 `internal`。

- `private` 表示在 `struct` 定义内可见。
- `internal` 表示仅当前包及子包（包括子包的子包，详见[包](../package/toplevel_access.md)章节）内可见。
- `protected` 表示当前模块（详见[包](../package/toplevel_access.md)章节）可见。
- `public` 表示模块内外均可见。

下面的例子中，`width` 是 `public` 修饰的成员，在类外可以访问，`height` 是缺省访问修饰符的成员，仅在当前包及子包可见，其他包无法访问。

<!-- compile.error -->

```cangjie
package a
public struct Rectangle {
    public var width: Int64
    var height: Int64
    private var area: Int64

    public init(width: Int64, height: Int64, area: Int64) {
        this.width = width
        this.height = height
        this.area = area
    }
}

func samePkgFunc() {
    var r = Rectangle(10, 20, 40)
    r.width = 8               // OK: public 'width' can be accessed here
    r.height = 24             // OK: 'height' has no modifier and can be accessed here
    r.area = 30               // Error, private 'area' can't be accessed here
}
```

<!-- compile.error -->
<!-- cfg="-p b --output-type=staticlib" -->
<!-- cfg="liba.a" -->

```cangjie
package b
import a.*

main() {
    r.width = 8     // OK: public 'width' can be accessed here
    r.height = 24   // Error, no modifier 'height' can't be accessed here
    r.area = 30     // Error, private 'area' can't be accessed here
}
```

## 禁止递归 struct

递归和互递归定义的 `struct` 均是非法的。例如：

<!-- compile.error -->

```cangjie
struct R1 { // Error, 'R1' recursively references itself
    let other: R1
}
struct R2 { // Error, 'R2' and 'R3' are mutually recursive
    let other: R3
}
struct R3 { // Error, 'R2' and 'R3' are mutually recursive
    let other: R2
}
```


---

<!-- Content from source_zh_cn/struct/create_instance.md -->
# 创建 struct 实例

定义了 `struct` 类型后，即可通过调用 `struct` 的构造函数来创建 `struct` 实例。在 `struct` 定义之外，通过 `struct` 类型名调用构造函数创建该类型实例，并可以通过实例访问满足可见性修饰符（如`public`）的实例成员变量和实例成员函数。例如，下例中定义了一个 `Rectangle` 类型的变量 `r`，通过 `r.width` 和 `r.height` 可分别访问 `r` 中 `width` 和 `height` 的值，通过 `r.area()` 可以调用 `r` 的成员函数 `area`。

<!-- compile -->

```cangjie
struct Rectangle {
    public var width: Int64
    public var height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }

    public func area() {
        width * height
    }
}
let r = Rectangle(10, 20)
let width = r.width   // width = 10
let height = r.height // height = 20
let a = r.area()      // a = 200
```

如果希望通过 `struct` 实例去修改成员变量的值，需要将 `struct` 类型的变量定义为可变变量，并且被修改的成员变量也必须是可变成员变量（使用 `var` 定义）。举例如下：

<!-- run -->

```cangjie
struct Rectangle {
    public var width: Int64
    public var height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }

    public func area() {
        width * height
    }
}

main() {
    var r = Rectangle(10, 20) // r.width = 10, r.height = 20
    r.width = 8               // r.width = 8
    r.height = 24             // r.height = 24
    let a = r.area()          // a = 192
}
```

在赋值或传参时，会对 `struct` 实例进行复制（成员变量为引用类型时，仅复制引用而不会复制引用的对象），生成新的实例，对其中一个实例的修改并不会影响另外一个实例。以赋值为例，下面的例子中，将 `r1` 赋值给 `r2` 之后，修改 `r1` 的 `width` 和 `height` 的值，并不会影响 `r2` 的 `width` 和 `height` 值。

<!-- run -->

```cangjie
struct Rectangle {
    public var width: Int64
    public var height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }

    public func area() {
        width * height
    }
}

main() {
    var r1 = Rectangle(10, 20) // r1.width = 10, r1.height = 20
    var r2 = r1                // r2.width = 10, r2.height = 20
    r1.width = 8               // r1.width = 8
    r1.height = 24             // r1.height = 24
    let a1 = r1.area()         // a1 = 192
    let a2 = r2.area()         // a2 = 200
}
```


---

<!-- Content from source_zh_cn/struct/mut.md -->
# mut 函数

struct 类型是值类型，其实例成员函数无法修改实例本身。例如，下例中，成员函数 `g` 中不能修改成员变量 `i` 的值。

<!-- compile.error -->

```cangjie
struct Foo {
    var i = 0

    public func g() {
        i += 1  // Error, the value of a instance member variable cannot be modified in an instance member function
    }
}
```

mut 函数是一种可以修改 `struct` 实例本身的特殊的实例成员函数。在 `mut` 函数内部，`this` 的语义是特殊的，这种 `this` 拥有原地修改字段的能力。

> **注意：**
>
> 只允许在 interface、struct 和 struct 的扩展内定义 `mut` 函数（class 是引用类型，实例成员函数不需要加 `mut` 也可以修改实例成员变量，所以禁止在 class 中定义 `mut` 函数）。

## mut 函数定义

mut 函数与普通的实例成员函数相比，多一个 `mut` 关键字来修饰。

例如，下例中在函数 `g` 之前增加 `mut` 修饰符之后，即可在函数体内修改成员变量 `i` 的值。

<!-- compile -->

```cangjie
struct Foo {
    var i = 0

    public mut func g() {
        i += 1  // OK
    }
}
```

`mut` 只能修饰实例成员函数，不能修饰静态成员函数。

<!-- compile.error -->

```cangjie
struct A {
    public mut func f(): Unit {} // OK
    public mut operator func +(rhs: A): A { // OK
        A()
    }
    public mut static func g(): Unit {} // Error, static member functions cannot be modified with 'mut'
}
```

mut 函数中的 `this` 不能被捕获，也不能作为表达式。`mut` 函数中的 lambda 或嵌套函数不能对 struct 的实例成员变量进行捕获。

示例：

<!-- compile.error -->

```cangjie
struct Foo {
    var i = 0

    public mut func f(): Foo {
        let f1 = { => this } // Error, 'this' in mut functions cannot be captured
        let f2 = { => this.i = 2 } // Error, instance member variables in mut functions cannot be captured
        let f3 = { => this.i } // Error, instance member variables in mut functions cannot be captured
        let f4 = { => i } // Error, instance member variables in mut functions cannot be captured
        this // Error, 'this' in mut functions cannot be used as expressions
    }
}
```

## 接口中的 mut 函数

接口中的实例成员函数，也可以使用 `mut` 修饰。

`struct` 类型在实现 `interface` 的函数时必须保持一样的 `mut` 修饰。`struct` 以外的类型实现 `interface` 的函数时不能使用 `mut` 修饰。

示例：

<!-- compile.error -->

```cangjie
interface I {
    mut func f1(): Unit
    func f2(): Unit
}

struct A <: I {
    public mut func f1(): Unit {} // OK: as in the interface, the 'mut' modifier is used
    public func f2(): Unit {} // OK: as in the interface, the 'mut' modifier is not used
}

struct B <: I {
    public func f1(): Unit {} // Error, 'f1' is modified with 'mut' in interface, but not in struct
    public mut func f2(): Unit {} // Error, 'f2' is not modified with 'mut' in interface, but did in struct
}

class C <: I {
    public func f1(): Unit {} // OK
    public func f2(): Unit {} // OK
}
```

当 `struct` 的实例赋值给 `interface` 类型时是拷贝语义，因此 `interface` 的 `mut` 函数并不能修改 `struct` 实例的值。

示例：

<!-- verify -->

```cangjie
interface I {
    mut func f(): Unit
}
struct Foo <: I {
    public var v = 0
    public mut func f(): Unit {
        v += 1
    }
}
main() {
    var a = Foo()
    var b: I = a  
    b.f()  // Calling 'f' via 'b' cannot modify the value of 'a'
    println(a.v) // 0
}
```

程序输出结果为：

```text
0
```

## mut 函数的使用限制

因为 `struct` 是值类型，所以如果一个变量是 `struct` 类型且使用 `let` 声明，那么不能通过这个变量访问该类型的 `mut` 函数。

示例：

<!-- compile.error -->

```cangjie
interface I {
    mut func f(): Unit
}
struct Foo <: I {
    public var i = 0
    public mut func f(): Unit {
        i += 1
    }
}
main() {
    let a = Foo()
    a.f() // Error, 'a' is of type struct and is declared with 'let', the 'mut' function cannot be accessed via 'a'
    var b = Foo()
    b.f() // OK
    let c: I = Foo()
    c.f() // OK, 变量 c 为接口 I 类型，非 struct 类型，此处允许访问。
}
```

为避免逃逸，如果一个变量的类型是 `struct` 类型，那么这个变量不能将该类型使用 `mut` 修饰的函数作为一等公民来使用，只能调用这些 `mut` 函数。

示例：

<!-- compile.error -->

```cangjie
interface I {
    mut func f(): Unit
}

struct Foo <: I {
    var i = 0

    public mut func f(): Unit {
        i += 1
    }
}

main() {
    var a = Foo()
    var fn = a.f // Error, mut function 'f' of 'a' cannot be used as a first class citizen.
    var b: I = Foo()
    fn = b.f // OK
}
```

为避免逃逸，非 `mut` 的实例成员函数（包括 `lambda` 表达式）不能直接访问所在类型的 `mut` 函数，反之可以。

示例：

<!-- compile.error -->

```cangjie
struct Foo {
    var i = 0

    public mut func f(): Unit {
        i += 1
        g() // OK
    }

    public func g(): Unit {
        f() // Error, mut functions cannot be invoked in non-mut functions
    }
}

interface I {
    mut func f(): Unit {
        g() // OK
    }

    func g(): Unit {
        f() // Error, mut functions cannot be invoked in non-mut functions
    }
}
```


---

<!-- Content from source_zh_cn/enum_and_pattern_match/enum.md -->
# 枚举类型

本节介绍仓颉中的 `enum` 类型。`enum` 类型提供了通过列举一个类型的所有可能取值来定义此类型的方式。

在很多语言中都有 `enum` 类型（或者称枚举类型），但是不同语言中的 `enum` 类型的使用方式和表达能力均有所差异，仓颉中的 `enum` 类型可以理解为函数式编程语言中的代数数据类型（Algebraic Data Types）。

## enum 的定义

定义 `enum` 时需要把它所有可能的取值一一列出，称这些值为 `enum` 的构造器（或者 `constructor`）。

`enum` 类型的定义以关键字 `enum` 开头，接着是 `enum` 的名字，之后是定义在一对花括号中的 `enum` 体，`enum` 体中定义了若干构造器，多个构造器之间使用 `|` 进行分隔（第一个构造器之前的 `|` 是可选的）。构造器可以是有名字的，也可以是没有名字的 `...`。

每个 `enum` 中至少存在一个有名字的构造器。有名字的构造器可以没有参数（即“无参构造器”），也可以携带若干个参数（即“有参构造器”）。如下示例代码定义了一个名为 `RGBColor` 的 `enum` 类型，它有 3 个构造器：`Red`、`Green` 和 `Blue`，分别表示 RGB 色彩模式中的红色、绿色和蓝色。每个构造器有一个 `UInt8` 类型的参数，用来表示每个颜色的亮度级别。

<!-- compile -->

```cangjie
enum RGBColor {
    | Red(UInt8) | Green(UInt8) | Blue(UInt8)
}
```

仓颉支持同一个 `enum` 中定义多个同名构造器，但是要求这些构造器的参数个数不同（认为没有参数的构造器的参数个数等于 `0`），例如：

<!-- compile -->

```cangjie
enum RGBColor {
    | Red | Green | Blue
    | Red(UInt8) | Green(UInt8) | Blue(UInt8)
}
```

每个 `enum` 中最多只有一个没有名字的 `...` 构造器，且 `...` 只能是最后一个构造器。拥有 `...` 构造器的 `enum` 称为 `non-exhaustive enum`。由于没有名字，这个构造器不能被直接匹配，在解构时，需要使用可匹配所有构造器的模式，如通配符模式 `_` 或绑定模式，具体可参见[match 表达式的定义](./match.md#match-表达式的定义) 。例如：

<!-- compile -->

```cangjie
enum T {
    | Red | Green | Blue | ...
}
```

`enum` 支持递归定义，例如，下面的例子中使用 `enum` 定义了一种表达式（即 `Expr`），此表达式只能有 3 种形式：单独的一个数字 `Num`（携带一个 `Int64` 类型的参数）、加法表达式 `Add`（携带两个 `Expr` 类型的参数）、减法表达式 `Sub`（携带两个 `Expr` 类型的参数）。对于 `Add` 和 `Sub` 这两个构造器，其参数中递归地使用到了 `Expr` 自身。

<!-- compile -->

```cangjie
enum Expr {
    | Num(Int64)
    | Add(Expr, Expr)
    | Sub(Expr, Expr)
}
```

另外，在 `enum` 体中还可以定义一系列成员函数、操作符函数（详见[操作符重载](../function/operator_overloading.md)）和成员属性（详见[属性](../class_and_interface/prop.md)），但是要求构造器、成员函数、成员属性之间不能重名。例如，下面的例子在 `RGBColor` 中定义了一个名为 `printType` 的函数，它会输出字符串 `RGBColor`：

<!-- compile -->

```cangjie
enum RGBColor {
    | Red | Green | Blue

    public static func printType() {
        print("RGBColor")
    }
}
```

> **注意：**
>
> `enum` 只能定义在源文件的顶层作用域。

## enum 的使用

定义了 `enum` 类型之后，就可以创建此类型的实例（即 `enum` 值），`enum` 值只能取 `enum` 类型定义中的一个构造器。`enum` 没有构造函数，可以通过 `类型名.构造器`，或者直接使用构造器的方式来构造一个 `enum` 值（对于有参构造器，需要传实参）。

下例中，`RGBColor` 中定义了三个构造器，其中有两个无参构造器（`Red` 和 `Green`）和一个有参构造器（`Blue(UInt8)`），`main` 中定义了三个 `RGBColor` 类型的变量 `r`，`g` 和 `b`，其中，`r` 的值使用 `RGBColor.Red` 进行初始化，`g` 的值直接使用 `Green` 进行初始化，`b` 的值使用 `Blue(100)` 进行初始化：

<!-- compile -->

```cangjie
enum RGBColor {
    | Red | Green | Blue(UInt8)
}

main() {
    let r = RGBColor.Red
    let g = Green
    let b = Blue(100)
}
```

当省略类型名时，`enum` 构造器的名字可能和类型名、变量名、函数名发生冲突。此时必须加上 `enum` 类型名来使用 `enum` 构造器，否则只会选择同名的类型、变量、函数定义。

下面的例子中，只有构造器 `Blue(UInt8)` 可以不带类型名使用，`Red` 和 `Green(UInt8)` 皆会因为名字冲突而不能直接使用，必须加上类型名 `RGBColor`。

<!-- compile -->

```cangjie
let Red = 1

func Green(g: UInt8) {
    return g
}

enum RGBColor {
    | Red | Green(UInt8) | Blue(UInt8)
}

let r1 = Red                 // Will choose 'let Red'
let r2 = RGBColor.Red        // OK: constructed by enum type name

let g1 = Green(100)          // Will choose 'func Green'
let g2 = RGBColor.Green(100) // OK: constructed by enum type name

let b = Blue(100)            // OK: can be uniquely identified as an enum constructor
```

如下的例子中，只有构造器 `Blue` 会因为名称冲突而不能直接使用，必须加上类型名 `RGBColor`。

<!-- compile.error -->

```cangjie
class Blue {}

enum RGBColor {
    | Red | Green(UInt8) | Blue(UInt8)
}

let r = Red                 // OK: constructed by enum type name

let g = Green(100)          // OK: constructed by enum type name

let b = Blue(100)           // Will choose constructor of 'class Blue' and report an error
```


---

<!-- Content from source_zh_cn/enum_and_pattern_match/option_type.md -->
# Option 类型

`Option` 类型使用 `enum` 定义，它包含两个构造器：`Some` 和 `None`。其中，`Some` 会携带一个参数，表示有值；`None` 不带参数，表示无值。当需要表示某个类型可能有值，也可能没有值时，可以选择使用 `Option` 类型。

`Option` 类型被定义为一个泛型 `enum` 类型，定义如下（这里仅需要知道尖括号中的 `T` 是一个类型形参，当 `T` 为不同类型时会得到不同的 `Option` 类型即可。关于泛型的详细介绍，可参见[泛型](../generic/generic_overview.md)）：

<!-- compile -->

```cangjie
enum Option<T> {
    | Some(T)
    | None
}
```

其中，`Some` 构造器的参数类型就是类型形参 `T`，当 `T` 被实例化为不同的类型时，会得到不同的 `Option` 类型，例如：`Option<Int64>`、`Option<String>`等。

`Option` 类型还有一种简单的写法：在类型名前加 `?`。也就是说，对于任意类型 `Ty`，`?Ty` 等价于 `Option<Ty>`。例如，`?Int64` 等价于 `Option<Int64>`，`?String` 等价于 `Option<String>` 等等。

下面的例子展示了如何定义 `Option` 类型的变量：

<!-- compile -->

```cangjie
let a: Option<Int64> = Some(100)
let b: ?Int64 = Some(100)
let c: Option<String> = Some("Hello")
let d: ?String = None
```

另外，虽然 `T` 和 `Option<T>` 是不同的类型，但是当明确知道某个位置需要的是 `Option<T>` 类型的值时，可以直接传一个 `T` 类型的值，编译器会用 `Option<T>` 类型的 `Some` 构造器将 `T` 类型的值封装成 `Option<T>` 类型的值（注意：这里并不是类型转换）。例如，下面的定义是合法的（等价于上例中变量 `a`，`b` 和 `c` 的定义）：

<!-- compile -->

```cangjie
let a: Option<Int64> = 100
let b: ?Int64 = 100
let c: Option<String> = "100"
```

在上下文没有明确的类型要求时，无法使用 `None` 直接构造出想要的类型，此时应使用 `None<T>` 这样的语法来构造 `Option<T>` 类型的数据，例如：

<!-- compile -->

```cangjie
let a = None<Int64> // a: Option<Int64>
let b = None<Bool> // b: Option<Bool>
```

最后，关于 `Option` 的使用，请参见[使用 Option](../error_handle/use_option.md)。


---

<!-- Content from source_zh_cn/enum_and_pattern_match/pattern_overview.md -->
# 模式概述

对于包含匹配值的 `match` 表达式，`case` 之后支持哪些模式决定了 `match` 表达式的表达能力。本节中将依次介绍仓颉支持的模式，包括：常量模式、通配符模式、绑定模式、tuple 模式、类型模式和 enum 模式。

## 常量模式

常量模式可以是整数字面量、浮点数字面量、字符字面量、布尔字面量、字符串字面量（不支持字符串插值）、Unit 字面量。

在包含匹配值的 `match` 表达式（参见[match 表达式](./match.md)）中使用常量模式时，要求常量模式表示的值的类型与待匹配值的类型相同，匹配成功的条件是待匹配的值与常量模式表示的值相等。

下面的例子中，根据 `score` 的值（假设 `score` 只能取 `0` 到 `100` 间被 `10` 整除的值），输出考试成绩的等级：

<!-- verify -->

```cangjie
main() {
    let score = 90
    let level = match (score) {
        case 0 | 10 | 20 | 30 | 40 | 50 => "D"
        case 60 => "C"
        case 70 | 80 => "B"
        case 90 | 100 => "A" // Matched.
        case _ => "Not a valid score"
    }
    println(level)
}
```

编译执行上述代码，输出结果为：

```text
A
```

- 在模式匹配的目标是静态类型为 `Rune` 的值时，`Rune` 字面量和单字符字符串字面量都可用于表示 `Rune` 类型字面量的常量 pattern。

  <!-- verify -->

  ```cangjie
  func translate(n: Rune) {
      match (n) {
          case "A" => 1
          case "B" => 2
          case "C" => 3
          case _ => -1
      }
  }

  main() {
      println(translate(r"C"))
  }
  ```

  编译执行上述代码，输出结果为：

  ```text
  3
  ```

- 在模式匹配的目标是静态类型为 `Byte` 的值时，一个表示 ASCII 字符的字符串字面量可用于表示 `Byte` 类型字面量的常量 pattern。

  <!-- verify -->

  ```cangjie
  func translate(n: Byte) {
      match (n) {
          case "1" => 1
          case "2" => 2
          case "3" => 3
          case _ => -1
      }
  }

  main() {
      println(translate(51)) // UInt32(r'3') == 51
  }
  ```

  编译执行上述代码，输出结果为：

  ```text
  3
  ```

## 通配符模式

通配符模式使用下划线 `_` 表示，可以匹配任意值。通配符模式通常作为最后一个 `case` 中的模式，用来匹配其他 `case` 未覆盖到的情况，如[常量模式](./pattern_overview.md#常量模式)中匹配 `score` 值的示例中，最后一个 `case` 中使用 `_` 来匹配无效的 `score` 值。

## 绑定模式

绑定模式使用 `id` 表示，`id` 是一个合法的标识符。与通配符模式相比，绑定模式同样可以匹配任意值，但绑定模式会将匹配到的值与 `id` 进行绑定，在 `=>` 之后可以通过 `id` 访问其绑定的值。

下面的例子中，最后一个 `case` 中使用了绑定模式。其中，变量 `n` 属于 `id` 标识，用于绑定非 `0` 值：

<!-- verify -->

```cangjie
main() {
    let x = -10
    let y = match (x) {
        case 0 => "zero"
        case n => "x is not zero and x = ${n}" // Matched.
    }
    println(y)
}
```

编译执行上述代码，输出结果为：

```text
x is not zero and x = -10
```

使用 `|` 连接多个模式时不能使用绑定模式，也不可嵌套出现在其他模式中，否则会报错：

<!-- compile.error -->

```cangjie
main() {
    let opt = Some(0)
    match (opt) {
        case x | x => {} // Error, variable cannot be introduced in patterns connected by '|'
        case Some(x) | Some(x) => {} // Error, variable cannot be introduced in patterns connected by '|'
        case x: Int64 | x: String => {} // Error, variable cannot be introduced in patterns connected by '|'
    }
}
```

绑定模式 `id` 相当于新定义了一个名为 `id` 的不可变变量（其作用域从引入处开始到该 `case` 结尾处），因此在 `=>` 之后无法对 `id` 进行修改。例如，下例中最后一个 `case` 中对 `n` 的修改是不允许的。

<!-- compile.error -->

```cangjie
main() {
    let x = -10
    let y = match (x) {
        case 0 => "zero"
        case n => n = n + 0 // Error, 'n' cannot be modified.
                  "x is not zero"
    }
    println(y)
}
```

对于每个 `case` 分支，`=>` 之后变量作用域级别与 `case` 后 `=>` 前引入的变量作用域级别相同，在 `=>` 之后再次引入相同名字会触发重定义错误。例如：

<!-- compile.error -->

```cangjie
main() {
    let x = -10
    let y = match (x) {
        case 0 => "zero"
        case n => let n = 0 // Error, redefinition
                  println(n)
                  "x is not zero"
    }
    println(y)
}
```

> **注意：**
>
> 当模式的 identifier 为 enum 构造器时，该模式会被当成 enum 模式进行匹配，而不是绑定模式（关于 enum 模式，详见 [enum 模式](#enum-模式)章节）。

<!-- verify -->

```cangjie
enum RGBColor {
    | Red | Green | Blue
}

main() {
    let x = Red
    let y = match (x) {
        case Red => "red" // The 'Red' is enum mode here.
        case _ => "not red"
    }
    println(y)
}
```

编译执行上述代码，输出结果为：

```text
red
```

## Tuple 模式

Tuple 模式用于 tuple 值的匹配，它的定义和 tuple 字面量类似：`(p_1, p_2, ..., p_n)`，区别在于这里的 `p_1` 到 `p_n`（`n` 大于等于 `2`）是模式（可以是本章节中介绍的任何模式，多个模式间使用逗号分隔）而不是表达式。

例如，`(1, 2, 3)` 是一个包含三个常量模式的 tuple 模式，`(x, y, _)` 是一个包含两个绑定模式，一个通配符模式的 tuple 模式。

给定一个 tuple 值 `tv` 和一个 tuple 模式 `tp`，当且仅当 `tv` 每个位置处的值均能与 `tp` 中对应位置处的模式相匹配，才称 `tp` 能匹配 `tv`。例如，`(1, 2, 3)` 仅可以匹配 tuple 值 `(1, 2, 3)`，`(x, y, _)` 可以匹配任何三元 tuple 值。

下面的例子中，展示了 tuple 模式的使用：

<!-- verify -->

```cangjie
main() {
    let tv = ("Alice", 24)
    let s = match (tv) {
        case ("Bob", age) => "Bob is ${age} years old"
        case ("Alice", age) => "Alice is ${age} years old" // Matched, "Alice" is a constant pattern, and 'age' is a variable pattern.
        case (name, 100) => "${name} is 100 years old"
        case (_, _) => "someone"
    }
    println(s)
}
```

编译执行上述代码，输出结果为：

```text
Alice is 24 years old
```

同一个 tuple 模式中不允许引入多个名称相同的绑定模式。例如，下例中最后一个 `case` 中的 `case (x, x)` 是不合法的。

<!-- compile.error -->

```cangjie
main() {
    let tv = ("Alice", 24)
    let s = match (tv) {
        case ("Bob", age) => "Bob is ${age} years old"
        case ("Alice", age) => "Alice is ${age} years old"
        case (name, 100) => "${name} is 100 years old"
        case (x, x) => "someone" // Error, Cannot introduce a variable pattern with the same name, which will be a redefinition error.
    }
    println(s)
}
```

## 类型模式

类型模式用于判断一个值的运行时类型是否是某个类型的子类型。类型模式有两种形式：`_: Type`（嵌套一个通配符模式 `_`）和 `id: Type`（嵌套一个绑定模式 `id`），它们的区别是后者会发生变量绑定，而前者不会。

对于待匹配值 `v` 和类型模式 `id: Type`（或 `_: Type`），首先判断 `v` 的运行时类型是否是 `Type` 的子类型，若成立则视为匹配成功，否则视为匹配失败；如匹配成功，则将 `v` 的类型转换为 `Type` 并与 `id` 进行绑定（对于 `_: Type`，不存在绑定这一操作）。

假设有如下两个类，`Base` 和 `Derived`，并且 `Derived` 是 `Base` 的子类，`Base` 的无参构造函数中将 `a` 的值设置为 `10`，`Derived` 的无参构造函数中将 `a` 的值设置为 `20`：

<!-- verify -mergeCase -->

```cangjie
open class Base {
    var a: Int64
    public init() {
        a = 10
    }
}

class Derived <: Base {
    public init() {
        a = 20
    }
}
```

下面的代码展示了使用类型模式并匹配成功的例子：

<!-- verify -mergeCase -->

```cangjie
func test1() {
    var d = Derived()
    var r = match (d) {
        case b: Base => b.a // Matched.
        case _ => 0
    }
    println("r = ${r}")
}
```

下面的代码展示了使用类型模式但类型模式匹配失败的例子：

<!-- verify -mergeCase -->

```cangjie
func test2() {
    var b = Base()
    var r = match (b) {
        case d: Derived => d.a  // Type pattern match failed.
        case _ => 0             // Matched.
    }
    println("r = ${r}")
}
```

<!-- verify -mergeCase -->

```cangjie
main() {
    test1()
    test2()
}
```

编译执行上述代码，输出结果为（第一行为 test1 的输出结果，第二行则是 test2 的输出结果）：

<!-- verify -mergeCase -->

```text
r = 20
r = 0
```

## enum 模式

enum 模式用于匹配 `enum` 类型的实例，它的定义和 `enum` 的构造器类似：无参构造器 `C` 或有参构造器 `C(p_1, p_2, ..., p_n)`，构造器的类型前缀可以省略，区别在于这里的 `p_1` 到 `p_n`（`n` 大于等于 `1`）是模式。例如，`Some(1)` 是一个包含一个常量模式的 enum 模式，`Some(x)` 是一个包含一个绑定模式的 enum 模式。

给定一个 enum 实例 `ev` 和一个 enum 模式 `ep`，当且仅当 `ev` 的构造器名字和 `ep` 的构造器名字相同，且 `ev` 参数列表中每个位置处的值均能与 `ep` 中对应位置处的模式相匹配，才称 `ep` 能匹配 `ev`。例如，`Some("one")` 仅可以匹配 `Option<String>` 类型的`Some` 构造器 `Option<String>.Some("one")`，`Some(x)` 可以匹配任何 Option 类型的 `Some` 构造器。

下面的例子中，展示了 enum 模式的使用，因为 `x` 的构造器是 `Year`，所以会和第一个 `case` 匹配：

<!-- verify -->

```cangjie
enum TimeUnit {
    | Year(UInt64)
    | Month(UInt64)
}

main() {
    let x = Year(2)
    let s = match (x) {
        case Year(n) => "x has ${n * 12} months" // Matched.
        case TimeUnit.Month(n) => "x has ${n} months"
    }
    println(s)
}
```

编译执行上述代码，输出结果为：

```text
x has 24 months
```

当使用 `|` 连接多个 enum 模式时，每个模式必须独立且不能引入新的变量。这是因为 `|` 表示“或”的关系，而变量的引入需要明确的上下文，不能在多个模式之间共享。下面示例为反例示范，其中第五、六个 `case` 不符合该条规则：

<!-- compile.error -->

```cangjie
enum TimeUnit {
    | Year(UInt64)
    | Month(UInt64)
}

main() {
    let x = Year(2)
    let s = match (x) {
        case Year(5) => "1:OK"
        case Month(m) => "2:OK"
        case Year(0) | Year(1) | Month(_) => "3:OK"
        case Year(_) => "4:OK"
        case Year(2) | Month(m) => "5:invalid" // Error, Variable cannot be introduced in patterns connected by '|'
        case Year(n: UInt64) | Month(n: UInt64) => "6:invalid" // Error, Variable cannot be introduced in patterns connected by '|'
    }
    println(s)
}
```

上述示例中，第二个 `case` 引入了一个新变量 `m`，但没有使用 `|` 连接其他模式，故此是合法的。

使用 `match` 表达式匹配 `enum` 值时，要求 `case` 之后的模式要覆盖待匹配 `enum` 类型中的所有构造器，如果未做到完全覆盖，编译器将报错：

<!-- compile.error -->

```cangjie
enum RGBColor {
    | Red | Green | Blue
}

main() {
    let c = Green
    let cs = match (c) { // Error, Not all constructors of RGBColor are covered.
        case Red => "Red"
        case Green => "Green"
    }
    println(cs)
}
```

可以通过加上 `case Blue` 来实现完全覆盖，也可以在 `match` 表达式的最后通过使用 `case _` 来覆盖其他 `case` 未覆盖的到的情况，如：

<!-- verify -->

```cangjie
enum RGBColor {
    | Red | Green | Blue
}

main() {
    let c = Blue
    let cs = match (c) {
        case Red => "Red"
        case Green => "Green"
        case _ => "Other" // Matched.
    }
    println(cs)
}
```

上述代码的执行结果为：

```text
Other
```

## 模式的嵌套组合

Tuple 模式和 enum 模式可以嵌套任意模式。下面的代码展示了不同模式嵌套组合使用：

<!-- verify -->

```cangjie
enum TimeUnit {
    | Year(UInt64)
    | Month(UInt64)
}

enum Command {
    | SetTimeUnit(TimeUnit)
    | GetTimeUnit
    | Quit
}

main() {
    let command = (SetTimeUnit(Year(2022)), SetTimeUnit(Year(2024)))
    match (command) {
        case (SetTimeUnit(Year(year)), _) => println("Set year ${year}")
        case (_, SetTimeUnit(Month(month))) => println("Set month ${month}")
        case _ => ()
    }
}
```

编译并执行上述代码，输出结果为：

```text
Set year 2022
```


---

<!-- Content from source_zh_cn/enum_and_pattern_match/pattern_refutability.md -->
# 模式的 Refutability

模式可以分为两类：`refutable` 模式和 `irrefutable` 模式。在类型匹配的前提下，当一个模式有可能和待匹配值不匹配时，称此模式为 `refutable` 模式；反之，当一个模式总是可以和待匹配值匹配时，称此模式为 `irrefutable` 模式。

对于上述介绍的各种模式，规定如下：

常量模式是 `refutable` 模式。例如，下例中第一个 case 中的 `1` 和第二个 case 中的 `2` 都有可能和 `x` 的值不相等。

<!-- compile -->

```cangjie
func constPat(x: Int64) {
    match (x) {
        case 1 => "one"
        case 2 => "two"
        case _ => "_"
    }
}
```

通配符模式是 `irrefutable` 模式。例如，下例中无论 `x` 的值是多少，`_` 总能和其匹配。

<!-- compile -->

```cangjie
func wildcardPat(x: Int64) {
    match (x) {
        case _ => "_"
    }
}
```

绑定模式是 `irrefutable` 模式。例如，下例中无论 `x` 的值是多少，绑定模式 `a` 总能和其匹配。

<!-- compile -->

```cangjie
func varPat(x: Int64) {
    match (x) {
        case a => "x = ${a}"
    }
}
```

Tuple 模式是 `irrefutable` 模式，当且仅当其包含的每个模式都是 `irrefutable` 模式。例如，下例中 `(1, 2)` 和 `(a, 2)` 都有可能和 `x` 的值不匹配，所以它们是 `refutable` 模式，而 `(a, b)` 可以匹配任何 `x` 的值，所以它是 `irrefutable` 模式。

<!-- compile -->

```cangjie
func tuplePat(x: (Int64, Int64)) {
    match (x) {
        case (1, 2) => "(1, 2)"
        case (a, 2) => "(${a}, 2)"
        case (a, b) => "(${a}, ${b})"
    }
}
```

类型模式是 `refutable` 模式。例如，下例中（假设 `Base` 是 `Derived` 的父类，并且 `Base` 实现了接口 `I`），`x` 的运行时类型有可能既不是 `Base` 也不是 `Derived`，所以 `a: Derived` 和 `b: Base` 均是 `refutable` 模式。

<!-- compile -->

```cangjie
interface I {}
open class Base <: I {}
class Derived <: Base {}

func typePat(x: I) {
    match (x) {
        case a: Derived => "Derived"
        case b: Base => "Base"
        case _ => "Other"
    }
}
```

enum 模式是 `irrefutable` 模式，当且仅当它对应的 `enum` 类型中只有一个有参构造器，且 enum 模式中包含的其他模式也是 `irrefutable` 模式。例如，对于下例中的 `E1` 和 `E2` 定义，函数 `enumPat1` 中的 `A(1)` 是 `refutable` 模式，`A(a)` 是 `irrefutable` 模式；而函数 `enumPat2` 中的 `B(b)` 和 `C(c)` 均是 `refutable` 模式。

<!-- compile -->

```cangjie
enum E1 {
    A(Int64)
}

enum E2 {
    B(Int64) | C(Int64)
}

func enumPat1(x: E1) {
    match (x) {
        case A(1) => "A(1)"
        case A(a) => "A(${a})"
    }
}

func enumPat2(x: E2) {
    match (x) {
        case B(b) => "B(${b})"
        case C(c) => "C(${c})"
    }
}
```


---

<!-- Content from source_zh_cn/enum_and_pattern_match/match.md -->
# match 表达式

## match 表达式的定义

仓颉支持两种 `match` 表达式，第一种是包含待匹配值的 `match` 表达式，第二种是不含待匹配值的 `match` 表达式。

**含匹配值的 match 表达式**：

<!-- verify -->

```cangjie
main() {
    let x = 0
    match (x) {
        case 1 => let r1 = "x = 1"
                  print(r1)
        case 0 => let r2 = "x = 0" // Matched.
                  print(r2)
        case _ => let r3 = "x != 1 and x != 0"
                  print(r3)
    }
}
```

`match` 表达式以关键字 `match` 开头，后跟要匹配的值，如上例中的 `x`，`x` 可以是任意表达式。接着是定义在一对花括号内的若干 `case` 分支，每个 `case` 分支以关键字 `case` 开头，`case` 之后是一个模式或多个由 `|` 连接的相同种类的模式，上例中的 `1`、`0`、`_` 均为模式，详见[模式概述](../enum_and_pattern_match/pattern_overview.md)章节。后面紧跟 `=>`，`=>` 之后即本条 `case` 分支匹配成功后需要执行的操作，可以是一系列表达式、变量和函数定义。其中，新定义的变量或函数的作用域从其定义处开始到下一个 `case` 之前结束，如上例中的变量定义和 `print` 函数调用。

上例中，因为 `x` 的值等于 `0`，所以会和第二条 `case` 分支匹配（此处使用的是常量模式，匹配的是值是否相等，详见[常量模式](../enum_and_pattern_match/pattern_overview.md#常量模式)章节），最后输出 `x = 0`。

编译并执行上述代码，输出结果为：

```text
x = 0
```

`match` 表达式要求所有匹配必须是穷尽（exhaustive）的，意味着待匹配表达式的所有可能取值都应该被考虑到。当 `match` 表达式非穷尽，或者编译器判断不出是否穷尽时，均会编译报错，换言之，所有 `case` 分支（包含 pattern guard）所覆盖的取值范围的并集，应该包含待匹配表达式的所有可能取值。常用的确保 `match` 表达式穷尽的方式是在最后一个 `case` 分支中使用通配符模式 `_`，因为 `_` 可以匹配任何值。

`match` 表达式的穷尽性保证了一定存在和待匹配值相匹配的 `case` 分支。下面的例子将编译报错，因为所有的 `case` 并没有覆盖 `x` 的所有可能取值：

<!-- compile.error -->

```cangjie
func nonExhaustive(x: Int64) {
    match (x) {
        case 0 => print("x = 0")
        case 1 => print("x = 1")
        case 2 => print("x = 2")
    }
}
```

如果被匹配值的类型包含 `enum` 类型且该 `enum` 为 `non-exhaustive enum`，则其在匹配时需要使用可匹配所有构造器的模式，如通配符模式 `_` 和绑定模式。

<!-- compile -->

```cangjie
enum T {
    | Red | Green | Blue | ...
}
func foo(a: T) {
    match (a) {
        case Red => 0
        case Green => 1
        case Blue => 2
        case _ => -1
    }
}

func bar(a: T) {
    match (a) {
        case Red => 0
        case k => -1 // simple binding pattern
    }
}

func baz(a: T) {
    match (a) {
        case Red => 0
        case k: T => -1 // binding pattern with nested type pattern
    }
}
```

在 `case` 分支的模式之后，可以使用 `pattern guard`（模式守卫）进一步对匹配出来的结果进行判断，此为可选内容。

- `pattern guard` 表示本条 `case` 匹配成功后额外需要满足的条件，其使用 `where cond`（语法格式） 表示，要求表达式 `cond` 的类型为 `Bool`。

`match` 表达式执行时，会依次将 `match` 之后的表达式与每个 `case` 中的模式进行匹配。如果有 `pattern guard`，需要 `where` 之后的表达式的值为 `true`；如果 `case` 中有多个由 `|` 连接的模式，只要待匹配值和其中一个模式匹配则认为匹配成功。一旦匹配成功，将执行 `=>` 之后的代码，然后退出 `match` 表达式的执行，这意味着不会再去匹配它之后的 `case`。如果匹配不成功，会继续与它之后的 `case` 中的模式进行匹配，直到匹配成功。`match` 表达式可以保证一定存在匹配的 `case` 分支。

在下面的例子中，使用到了 `enum` 模式，详见 [enum 模式](../enum_and_pattern_match/pattern_overview.md#enum-模式)章节。当 `RGBColor` 的构造器的参数值大于等于 `0` 时，输出它们的值；当参数值小于 `0` 时，即满足第一个 `case` 的 `where cond`，则认为它们的值等于 `0`：

<!-- verify -->

```cangjie
enum RGBColor {
    | Red(Int16) | Green(Int16) | Blue(Int16)
}
main() {
    let c = RGBColor.Green(-100)
    let cs = match (c) {
        case Red(r) where r < 0 => "Red = 0"
        case Red(r) => "Red = ${r}"
        case Green(g) where g < 0 => "Green = 0" // Matched.
        case Green(g) => "Green = ${g}"
        case Blue(b) where b < 0 => "Blue = 0"
        case Blue(b) => "Blue = ${b}"
    }
    print(cs)
}
```

编译执行上述代码，输出结果为：

```text
Green = 0
```

**没有匹配值的 match 表达式**：

<!-- verify -->

```cangjie
main() {
    let x = -1
    match {
        case x > 0 => print("x > 0")
        case x < 0 => print("x < 0") // Matched.
        case _ => print("x = 0")
    }
}
```

与包含待匹配值的 `match` 表达式相比，关键字 `match` 之后并没有待匹配的表达式，并且 `case` 之后不再是 `pattern`，而是类型为 `Bool` 的表达式（上述代码中的 `x > 0` 和 `x < 0`）或者 `_`（表示 `true`），当然，`case` 中也不再有 `pattern guard`。

无匹配值的 `match` 表达式执行时依次判断 `case` 之后的表达式的值，直到遇到值为 `true` 的 `case` 分支；一旦某个 `case` 之后的表达式值等于 `true`，则执行此 `case` 中 `=>` 之后的代码，然后退出 `match` 表达式的执行（意味着不会再去判断该 `case` 之后的其他 `case`）。

上例中，因为 `x` 的值等于 `-1`，所以第二条 `case` 分支中的表达式（即 `x < 0`）的值等于 `true`，执行 `print("x < 0")`。

编译并执行上述代码，输出结果为：

```text
x < 0
```

## match 表达式的类型

对于 `match` 表达式（无论是否有匹配值）：

- 在上下文有明确的类型要求时，要求每个 `case` 分支中 `=>` 之后的代码块的类型是上下文所要求的类型的子类型；

- 在上下文没有明确的类型要求时，`match` 表达式的类型是每个 `case` 分支中 `=>` 之后的代码块的类型的最小公共父类型；

- 当 `match` 表达式的值没有被使用时，其类型为 `Unit`，不要求各分支的类型有最小公共父类型。

下面分别举例说明。

<!-- compile -->

```cangjie
let x = 2
let s: String = match (x) {
    case 0 => "x = 0"
    case 1 => "x = 1"
    case _ => "x != 0 and x != 1" // Matched.
}
```

上面的例子中，定义变量 `s` 时，显式地标注了其类型为 `String`，属于上下文类型信息明确的情况，因此要求每个 `case` 的 `=>` 之后的代码块的类型均是 `String` 的子类型，显然上例中 `=>` 之后的字符串类型的字面量均满足要求。

再来看一个没有上下文类型信息的例子：

<!-- compile -->

```cangjie
let x = 2
let s = match (x) {
    case 0 => "x = 0"
    case 1 => "x = 1"
    case _ => "x != 0 and x != 1" // Matched.
}
```

上例中，定义变量 `s` 时，未显式标注其类型，因为每个 `case` 的 `=>` 之后的代码块的类型均是 `String`，所以 `match` 表达式的类型是 `String`，进而可确定 `s` 的类型也是 `String`。


---

<!-- Content from source_zh_cn/enum_and_pattern_match/other.md -->
# 其他使用模式的地方

模式除了可以在 `match` 表达式中使用外，还可以使用在变量定义和 `for in` 表达式中，例如，等号左侧是个模式，`for` 关键字和 `in` 关键字之间是个模式。同时， `if` 表达式和 `while` 表达式中的条件也可以使用模式，具体详见 [“let pattern” 的“条件”示例](../basic_programming_concepts/expression.md#涉及-let-pattern-的条件示例)。

但是，并不是所有的模式都能使用在变量定义和 `for in` 表达式中，只有 `irrefutable` 的模式才能在这两处被使用，所以只有通配符模式、绑定模式、`irrefutable` tuple 模式和 `irrefutable` enum 模式是允许的。

1. 变量定义和 `for in` 表达式中使用通配符模式的例子如下：

    <!-- verify -->

    ```cangjie
    main() {
        let _ = 100
        for (_ in 1..5) {
            println("0")
        }
    }
    ```

   上例中，变量定义时使用了通配符模式，表示定义了一个没有名字的变量（当然此后也就没办法对其进行访问），`for in` 表达式中使用了通配符模式，表示不会将 `1..5` 中的元素与某个变量绑定（当然循环体中就无法访问 `1..5` 中元素值）。编译执行上述代码，输出结果为：

    ```text
    0
    0
    0
    0
    ```

2. 变量定义和 `for in` 表达式中使用绑定模式的例子如下：

    <!-- verify -->

    ```cangjie
    main() {
        let x = 100
        println("x = ${x}")
        for (i in 1..5) {
            println(i)
        }
    }
    ```

   上例中，变量定义中的 `x` 以及 `for in` 表达式中的 `i` 都是绑定模式。编译执行上述代码，输出结果为：

    ```text
    x = 100
    1
    2
    3
    4
    ```

3. 变量定义和 `for in` 表达式中使用 `irrefutable` tuple 模式的例子如下：

    <!-- verify -->

    ```cangjie
    main() {
        let (x, y) = (100, 200)
        println("x = ${x}")
        println("y = ${y}")
        for ((i, j) in [(1, 2), (3, 4), (5, 6)]) {
            println("Sum = ${i + j}")
        }
    }

    ```

   上例中，变量定义时使用了 tuple 模式，表示对 `(100, 200)` 进行解构并分别和 `x` 与 `y` 进行绑定，效果上相当于定义了两个变量 `x` 和 `y`。`for in` 表达式中使用了 tuple 模式，表示依次将 `[(1, 2), (3, 4), (5, 6)]` 中的 tuple 类型的元素取出，然后解构并分别和 `i` 与 `j` 进行绑定，循环体中输出 `i + j` 的值。编译执行上述代码，输出结果为：

    ```text
    x = 100
    y = 200
    Sum = 3
    Sum = 7
    Sum = 11
    ```

4. 变量定义和 `for in` 表达式中使用 `irrefutable` enum 模式的例子如下：

    <!-- verify -->

    ```cangjie
    enum RedColor {
        Red(Int64)
    }
    main() {
        let Red(red) = Red(0)
        println("red = ${red}")
        for (Red(r) in [Red(10), Red(20), Red(30)]) {
            println("r = ${r}")
        }
    }
    ```

   上例中，变量定义时使用了 enum 模式，表示对 `Red(0)` 进行解构并将构造器的参数值（即 `0`）与 `red` 进行绑定。`for in` 表达式中使用了 enum 模式，表示依次将 `[Red(10), Red(20), Red(30)]` 中的元素取出，然后解构并将构造器的参数值与 `r` 进行绑定，循环体中输出 `r` 的值。编译执行上述代码，输出结果为：

    ```text
    red = 0
    r = 10
    r = 20
    r = 30
    ```


---

<!-- Content from source_zh_cn/class_and_interface/class.md -->
# 类

`class` 类型是面向对象编程中的经典概念，仓颉中同样支持使用 `class` 来实现面向对象编程。`class` 与 `struct` 的主要区别在于：`class` 是引用类型，`struct` 是值类型，它们在赋值或传参时行为是不同的；`class` 之间可以继承，但 `struct` 之间不能继承。

本节依次介绍如何定义 `class` 类型，如何创建对象，以及 `class` 的继承。

## class 定义

`class` 类型的定义以关键字 `class` 开头，后跟 `class` 的名字，接着是定义在一对花括号中的 `class` 定义体。`class` 定义体中可以定义一系列的成员变量、成员属性（参见[属性](prop.md)）、静态初始化器、构造函数、成员函数和操作符函数（详见[操作符重载](../function/operator_overloading.md)）。

<!-- compile -->

```cangjie
class Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }

    public func area() {
        width * height
    }
}
```

上例中定义了名为 `Rectangle` 的 `class` 类型，它有两个 `Int64` 类型的成员变量 `width` 和 `height`，一个有两个 `Int64` 类型参数的构造函数，以及一个成员函数 `area`（返回 `width` 和 `height` 的乘积）。

> **注意：**
>
> `class` 只能定义在源文件的顶层作用域。

使用 `abstract` 修饰的类为抽象类，与普通类不同的是，在抽象类中除了可以定义普通的函数，还允许声明抽象函数（没有函数体）。抽象类定义时的 `open` 修饰符是可选的，也可以使用 `sealed` 修饰符修饰抽象类。`sealed` 修饰符表示该抽象类只能在本包被继承，详见 [class 的继承小节](#class-的继承)。下例中在抽象类 `AbRectangle` 中定义了抽象函数 `foo`。

<!-- compile -->

```cangjie
abstract class AbRectangle {
    public func foo(): Unit
}
```

> **注意：**
>
> - 抽象类中禁止定义 `private` 的抽象函数；
> - 不能为抽象类创建实例；
> - 抽象类的非抽象子类必须实现父类中的所有抽象函数。

### class 成员变量

`class` 成员变量分为实例成员变量和静态成员变量，静态成员变量使用 `static` 修饰符修饰，没有静态初始化器时必须有初值，只能通过类型名访问，参考如下示例：

<!-- compile -->

```cangjie
class Rectangle {
    let width = 10
    static let height = 20
}

let l = Rectangle.height // l = 20
```

实例成员变量定义时可以不设置初值（但必须标注类型），也可以设置初值，只能通过对象（即类的实例）访问，参考如下示例：

<!-- compile -->

```cangjie
class Rectangle {
    let width = 10
    let height: Int64
    init(h: Int64) {
        height = h
    }
}
let rec = Rectangle(20)
let l = rec.height // l = 20
```

### class 静态初始化器

`class` 支持定义静态初始化器，并在静态初始化器中通过赋值表达式来对静态成员变量进行初始化。

静态初始化器以关键字组合 `static init` 开头，后跟无参参数列表和函数体，且不能被访问修饰符修饰。函数体中必须完成对所有未初始化的静态成员变量的初始化，否则编译报错。

<!-- compile -->

```cangjie
class Rectangle {
    static let degree: Int64
    static init() {
        degree = 180
    }
}
```

一个 `class` 中最多允许定义一个静态初始化器，否则报重定义错误。

<!-- compile.error -->

```cangjie
class Rectangle {
    static let degree: Int64
    static init() {
        degree = 180
    }
    static init() { // Error, redefinition with the previous static init function
        degree = 180
    }
}
```

### class 构造函数

和 `struct` 一样，`class` 中也支持定义普通构造函数和主构造函数。

普通构造函数以关键字 `init` 开头，后跟参数列表和函数体，函数体中必须完成所有未初始化实例成员变量的初始化，否则编译报错。

<!-- compile.error -->

```cangjie
class Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64, height: Int64) { // Error, 'height' is not initialized in the constructor
        this.width = width
    }
}
```

一个类中可以定义多个普通构造函数，但它们必须构成重载（参见[函数重载](../function/function_overloading.md)），否则报重定义错误。

<!-- compile.error -->

```cangjie
class Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64) {
        this.width = width
        this.height = width
    }

    public init(width: Int64, height: Int64) { // OK: overloading with the first init function
        this.width = width
        this.height = height
    }

    public init(height: Int64) { // Error, redefinition with the first init function
        this.width = height
        this.height = height
    }
}
```

除了可以定义若干普通的以 `init` 为名字的构造函数外，`class` 内还可以定义（最多）一个主构造函数。主构造函数的名字和 `class` 类型名相同，它的参数列表中可以有两种形式的形参：普通形参和成员变量形参（需要在参数名前加上 `let` 或 `var`），成员变量形参同时具有定义成员变量和构造函数参数的功能。

使用主构造函数通常可以简化 `class` 的定义，例如，上述包含一个 `init` 构造函数的 `Rectangle` 可以简化为如下定义：

<!-- compile -->

```cangjie
class Rectangle {
    public Rectangle(let width: Int64, let height: Int64) {}
}
```

主构造函数的参数列表中也可以定义普通形参，例如：

<!-- compile -->

```cangjie
class Rectangle {
    public Rectangle(name: String, let width: Int64, let height: Int64) {}
}
```

创建类的实例时调用的构造函数，将根据以下顺序执行类中的表达式：

1. 先初始化主构造函数之外定义的有缺省值的变量；
2. 如果构造函数体内未显式调用父类构造函数或本类其他构造函数，则调用父类的无参构造函数 `super()`，如果父类没有无参构造函数，则报错；
3. 执行构造函数体内的代码。

<!-- verify -->

```cangjie
func foo(x: Int64): Int64 {
    println("I'm foo, got ${x}")
    x
}

open class A {
    init() {
        println("I'm A")
    }
}

class B <: A {
    var x = foo(0)
    init() {
        x = foo(1)
        println("init B finished")
    }
}

main() {
    B()
    0
}
```

上述例子中，调用 `B` 的构造函数时，首先初始化有缺省值的变量 `x`，此时 `foo(0)` 被调用；之后调用父类的无参构造函数，此时 `A` 的构造函数被调用；接下来执行构造函数体内的代码，此时 `foo(1)` 被调用，并打印字符串。因此上例的输出为：

```text
I'm foo, got 0
I'm A
I'm foo, got 1
init B finished
```

如果 `class` 定义中不存在自定义构造函数（包括主构造函数），并且所有实例成员变量都有初始值，则会自动为其生成一个无参构造函数（调用此无参构造函数会创建一个所有实例成员变量的值均等于其初值的对象）；否则，不会自动生成此无参构造函数。例如，对于如下 `class` 定义，编译器会为其自动生成一个无参构造函数：

<!-- compile -->

```cangjie
class Rectangle {
    let width = 10
    let height = 20

    /* Auto-generated parameterless constructor:
    public init() {

    }
    */
}

// Invoke the auto-generated parameterless constructor
let r = Rectangle() // r.width = 10，r.height = 20
```

### class 终结器

`class` 支持定义终结器，当类的实例被垃圾回收时，会触发该函数。终结器的函数名固定为 `~init`，通常用于释放系统资源。如下示例中的 `unsafe`，详见 [unsafe 小节](../FFI/cangjie-c.md)：

<!-- compile -->

```cangjie
class C {
    var p: CString

    init(s: String) {
        p = unsafe { LibC.mallocCString(s) }
        println(s)
    }
    ~init() {
        unsafe { LibC.free(p) }
    }
}
```

使用终结器有些限制条件，需要开发者注意：

1. 终结器没有参数，没有返回类型，没有泛型类型参数，没有任何修饰符，也不可以被显式调用。
2. 带有终结器的类不可被 `open` 修饰，只有非 `open` 的类可以拥有终结器。
3. 一个类最多只能定义一个终结器。
4. 终结器不可以定义在扩展中。
5. 终结器被触发的时机是不确定的。
6. 终结器可能在任意一个线程上执行。
7. 多个终结器的执行顺序是不确定的。
8. 终结器向外抛出未捕获异常属于未定义行为。
9. 终结器中创建线程或者使用线程同步功能属于未定义行为。
10. 终结器执行结束之后，如果这个对象还可以被继续访问，则属于未定义行为。
11. 如果对象在初始化过程中抛出异常，这样未完整初始化的对象的终结器不会执行。
12. 依赖终结器的同步行为属于未定义行为。例如，下例中 `main` 函数通过 `while (Test.t0 != 0)` 等待 `Test` 类中的终结器修改 `t0` 的值，属于未定义行为。

    <!-- run -->

    ```cangjie
    import std.collection.ArrayList
    import std.runtime.gc

    class Test {
        public static var t0 : Int32 = 0
        public init () {
            t0++
        }
        ~init () {
            t0--
        }
    }

    var list: ArrayList<Test> = ArrayList<Test>()

    func foo() : Int32 {
        let o1 = Test()
        list.add(o1)
        if (Test.t0 != 1) {
            return 1
        }
        list.remove(at: 0)
        return 0
    }

    main(): Int64 {
        var i : Int64 = 0
        while (i < 100) {
            if (foo() != 0) {
                print("fail: obj is freed before gc!")
                return 1
            }
            gc(heavy: true) // blocking gc expected
            // wait ~init() to be executed
            while (Test.t0 != 0) {  // error, this is undefined behavior
                continue
            }
            i++
        }
        return 0
    }
    ```

### class 成员函数

`class` 成员函数同样分为实例成员函数和静态成员函数（使用 `static` 修饰符修饰），实例成员函数只能通过对象访问，静态成员函数只能通过 `class` 类型名访问；静态成员函数中不能访问实例成员变量，也不能调用实例成员函数，但在实例成员函数中可以访问静态成员变量以及静态成员函数。

下例中，`area` 是实例成员函数，`typeName` 是静态成员函数。

<!-- compile -->

```cangjie
class Rectangle {
    let width: Int64 = 10
    let height: Int64 = 20

    public func area() {
        this.width * this.height
    }

    public static func typeName(): String {
        "Rectangle"
    }
}
```

根据是否有函数体，实例成员函数又可以分为抽象成员函数和非抽象成员函数。抽象成员函数没有函数体，只能定义在抽象类或接口（详见[接口](interface.md)）中。需要注意的是，抽象实例成员函数默认具有 `open` 的语义，`open` 修饰符是可选的，且必须使用 `public` 或 `protected` 进行修饰。

非抽象函数必须有函数体，在函数体中可以通过 `this` 访问实例成员变量，例如：

<!-- compile -->

```cangjie
class Rectangle {
    let width: Int64 = 10
    let height: Int64 = 20

    public func area() {
        this.width * this.height
    }
}
```

### class 成员的访问修饰符

对于 `class` 的成员（包括成员变量、成员属性、构造函数、成员函数），可以使用的访问修饰符有 4 种访问修饰符修饰：`private`、`internal`、`protected` 和 `public`，缺省的含义是 `internal`。

- `private` 表示在 `class` 定义内可见。
- `internal` 表示仅当前包及子包（包括子包的子包，详见[包](../package/toplevel_access.md)）内可见。
- `protected` 表示当前模块（详见[包](../package/toplevel_access.md)）及当前类的子类可见。
- `public` 表示模块内外均可见。

<!-- compile.error -error-->

```cangjie
package a

public open class Rectangle {
    public var width: Int64
    protected var height: Int64
    private var area: Int64
    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
        this.area = this.width * this.height
    }
    init(width: Int64, height: Int64, multiple: Int64) {
        this.width = width
        this.height = height
        this.area = width * height * multiple
    }
}

func samePkgFunc() {
    var r = Rectangle(10, 20) // OK: constructor 'Rectangle' can be accessed here
    r.width = 8               // OK: public 'width' can be accessed here
    r.height = 24             // OK: protected 'height' can be accessed here
    r.area = 30               // Error, private 'area' cannot be accessed here
}
```

<!-- compile.error -error-->

```cangjie
package b
import a.*

public class Cuboid <: Rectangle {
    private var length: Int64
    public init(width: Int64, height: Int64, length: Int64) {
        super(width, height)
        this.length = length
    }
    public func volume() {
        this.width * this.height * this.length // OK: protected 'height' can be accessed here
    }
}

main() {
    var r = Rectangle(10, 20, 2) // Error, Rectangle has no `public` constructor with three parameters
    var c = Cuboid(20, 20, 20)
    c.width = 8               // OK: public 'width' can be accessed here
    c.height = 24             // Error, protected 'height' cannot be accessed here
    c.area = 30               // Error, private 'area' cannot be accessed here
}
```

## This 类型

在类内部，支持 `This` 类型占位符，代指当前类的类型。它只能被作为实例成员函数的返回类型来使用，当使用子类对象调用在父类中定义的返回 `This` 类型的函数时，该函数调用的类型会被识别为子类类型，而非定义所在的父类类型。

如果实例成员函数没有声明返回类型，并且只存在返回 `This` 类型表达式时，当前函数的返回类型会推断为 `This`。示例如下：

<!-- compile -->

```cangjie
open class C1 {
    func f(): This {  // its type is `() -> C1`
        return this
    }

    func f2() { // its type is `() -> C1`
        return this
    }

    public open func f3(): C1 {
        return this
    }
}
class C2 <: C1 {
    // member function f is inherited from C1, and its type is `() -> C2` now
    public override func f3(): This { // OK
        return this
    }
}

main() {
    var obj1: C2 = C2()
    var obj2: C1 = C2()

    var x = obj1.f()    // During compilation, the type of x is C2
    var y = obj2.f()    // During compilation, the type of y is C1
}
```

## 创建对象

定义了 `class` 类型后，即可通过调用其构造函数来创建对象（通过 `class` 类型名调用构造函数）。例如，下例中通过 `Rectangle(10, 20)` 创建 `Rectangle` 类型的对象并赋值给变量 `r`。创建对象之后，可以通过对象访问（`public` 修饰的）实例成员变量和实例成员函数。例如，下例中通过 `r.width` 和 `r.height` 可分别访问 `r` 中 `width` 和 `height` 的值，通过 `r.area()` 可以调用成员函数 `area`。

<!-- compile -->

```cangjie
class Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }

    public func area() {
        this.width * this.height
    }
}

main() {
    let r = Rectangle(10, 20) // r.width = 10, r.height = 20
    let width = r.width       // width = 10
    let height = r.height     // height = 20
    let a = r.area()          // a = 200
}
```

如果希望通过对象去修改成员变量的值（不鼓励这种方式，最好还是通过成员函数去修改），需要将 `class` 类型中的成员变量定义为可变成员变量（即使用 `var` 定义）。举例如下：

<!-- run -->

```cangjie
class Rectangle {
   public var width: Int64
   public var height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }
    public func area() {
        width * height
    }
}

main() {
    let r = Rectangle(10, 20) // r.width = 10, r.height = 20
    r.width = 8               // r.width = 8
    r.height = 24             // r.height = 24
    let a = r.area()          // a = 192
}
```

不同于 `struct`，对象在赋值或传参时，不会将对象进行复制，多个变量指向的是同一个对象，通过一个变量去修改对象中成员的值，其他变量中对应的成员变量也会被修改。以赋值为例，下面的例子中，将 `r1` 赋值给 `r2` 之后，修改 `r1` 的 `width` 和 `height` 的值，`r2` 的 `width` 和 `height` 值也同样会被修改。

<!-- run -->

```cangjie
class Rectangle {
    var width: Int64
    var height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }
     public func area() {
        this.width * this.height
    }
}
main() {
    var r1 = Rectangle(10, 20) // r1.width = 10, r1.height = 20
    var r2 = r1                // r2.width = 10, r2.height = 20
    r1.width = 8               // r1.width = 8
    r1.height = 24             // r1.height = 24
    let a1 = r1.area()         // a1 = 192
    let a2 = r2.area()         // a2 = 192
}
```

## class 的继承

像大多数支持 `class` 的编程语言一样，仓颉中的 `class` 同样支持继承。如果类 B 继承类 A，则称 A 为父类，B 为子类。子类将继承父类中除 `private` 成员和构造函数以外的所有成员。

抽象类总是可被继承的，故抽象类定义时的 `open` 修饰符是可选的，也可以使用 `sealed` 修饰符修饰抽象类，表示该抽象类只能在本包被继承。但非抽象的类可被继承是有条件的：定义时必须使用修饰符 `open` 修饰。当带 `open` 修饰的实例成员被 class 继承时，该 `open` 的修饰符也会被继承。当非 `open` 修饰的类中存在 `open` 修饰的成员时，编译器会给出告警。

可以在子类定义处通过 `<:` 指定其继承的父类，但要求父类必须是可继承的。例如，下面的例子中，`class` A 使用 `open` 修饰，是可以被类 B 继承的，但是因为类 B 是不可继承的，所以 C 在继承 B 的时候会报错。

<!-- compile.error -->

```cangjie
open class A {
    let a: Int64 = 10
}

class B <: A { // OK: 'B' Inheritance 'A'
    let b: Int64 = 20
}

class C <: B { // Error, 'B' is not inheritable
    let c: Int64 = 30
}
```

`class` 仅支持单继承，因此下面这样一个类继承两个类的代码是不合法的（`&` 是类实现多个接口时的语法，详见[接口](interface.md)）。

<!-- compile.error -->

```cangjie
open class A {
    let a: Int64 = 10
}

open class B {
    let b: Int64 = 20
}

class C <: A & B { // Error, 'C' can only inherit one class
    let c: Int64 = 30
}
```

因为类是单继承的，所以任何类都最多只能有一个直接父类。对于定义时指定了父类的 `class`，它的直接父类就是定义时指定的类，对于定义时未指定父类的 `class`，它的直接父类是 `Object` 类型。`Object` 是所有类的父类（注意，`Object` 没有直接父类，并且 `Object` 中不包含任何成员）。

因为子类是继承自父类的，所以子类的对象天然可以当做父类的对象使用，但是反之不然。例如，下例中 B 是 A 的子类，那么 B 类型的对象可以赋值给 A 类型的变量，但是 A 类型的对象不能赋值给 B 类型的变量。

<!-- compile -->

```cangjie
open class A {
    let a: Int64 = 10
}

class B <: A {
    let b: Int64 = 20
}

let a: A = B() // OK: subclass objects can be assigned to superclass variables
```

<!-- compile.error -->

```cangjie
open class A {
    let a: Int64 = 10
}

class B <: A {
    let b: Int64 = 20
}

let b: B = A() // Error, superclass objects can not be assigned to subclass variables
```

`class` 定义的类型不允许继承类型本身。

<!-- compile.error -->

```cangjie
class A <: A {}  // Error, 'A' inherits itself
```

抽象类可以使用 `sealed` 修饰符，表示被修饰的类定义只能在本定义所在的包内被其他类继承。`sealed` 已经蕴含了 `public`/`open` 的语义，因此定义 sealed abstract class 时若提供 `public`/`open` 修饰符，编译器将会告警。`sealed` 的子类可以不是 `sealed` 类，仍可被 `open`/`sealed` 修饰，或不使用任何继承性修饰符。若 `sealed` 类的子类被 `open` 修饰，则其子类可在包外被继承。`sealed` 的子类可以不被 `public` 修饰。

<!-- compile -->

```cangjie
package A

public sealed abstract class C1 {}   // Warning, redundant modifier, 'sealed' implies 'public'
sealed open abstract class C2 {}     // Warning, redundant modifier, 'sealed' implies 'open'
sealed abstract class C3 {}          // OK, 'public' is optional when 'sealed' is used

class S1 <: C1 {}  // OK
public open class S2 <: C1 {}   // OK
public sealed abstract class S3 <: C1 {}  // OK
open class S4 <: C1 {}   // OK
```

<!-- compile.error -->

```cangjie
package B
import A.*

class SS1 <: S2 {}  // OK
class SS2 <: S3 {}  // Error, S3 is sealed class, cannot be inherited here
sealed class SS3 {} // Error, 'sealed' cannot be used on non-abstract class
```

### 父类构造函数调用

子类的 `init` 构造函数可以使用 `super(args)` 的形式调用父类构造函数，或使用 `this(args)` 的形式调用本类其他构造函数，但两者之间只能调用一个。如果调用，必须在构造函数体内的第一个表达式处，在此之前不能有任何表达式或声明。

<!-- compile -->

```cangjie
open class A {
    A(let a: Int64) {}
}

class B <: A {
    let b: Int64
    init(b: Int64) {
        super(30)
        this.b = b
    }

    init() {
        this(20)
    }
}
```

子类的主构造函数中，可以使用 `super(args)` 的形式调用父类构造函数，但不能使用 `this(args)` 的形式调用本类其他构造函数。

如果子类的构造函数没有显式调用父类构造函数，也没有显式调用其他构造函数，编译器会在该构造函数体的开始处插入直接父类的无参构造函数的调用。如果此时父类没有无参构造函数，则会编译报错。

<!-- compile.error -->

```cangjie
open class A {
    let a: Int64
    init() {
        a = 100
    }
}

open class B <: A {
    let b: Int64
    init(b: Int64) {
        // OK, `super()` added by compiler
        this.b = b
    }
}

open class C <: B {
    let c: Int64
    init(c: Int64) {  // Error, there is no non-parameter constructor in super class
        this.c = c
    }
}
```

### 覆盖和重定义

子类中可以覆盖（override）父类中的同名非抽象实例成员函数，即在子类中为父类中的某个实例成员函数定义新的实现。覆盖时，要求父类中的成员函数使用 `open` 修饰，子类中的同名函数使用 `override` 修饰，其中 `override` 是可选的。例如，下面的例子中，子类 B 中的函数 `f` 覆盖了父类 A 中的函数 `f`。

<!-- verify -->

```cangjie
open class A {
    public open func f(): Unit {
        println("I am superclass")
    }
}

class B <: A {
    public override func f(): Unit {
        println("I am subclass")
    }
}

main() {
    let a: A = A()
    let b: A = B()
    a.f()
    b.f()
}
```

对于被覆盖的函数，调用时将根据变量的运行时类型（由实际赋给该变量的对象决定）确定调用的版本（即所谓的动态派发）。例如，上例中 `a` 的运行时类型是 A，因此 `a.f()` 调用的是父类 A 中的函数 `f`；`b` 的运行时类型是 B（编译时类型是 A），因此 `b.f()` 调用的是子类 B 中的函数 `f`。所以程序会输出：

```text
I am superclass
I am subclass
```

对于静态函数，子类中可以重定义父类中的同名非抽象静态函数，即在子类中为父类中的某个静态函数定义新的实现。重定义时，要求子类中的同名静态函数使用 `redef` 修饰，其中 `redef` 是可选的。例如，下面的例子中，子类 D 中的函数 `foo` 重定义了父类 C 中的函数 `foo`。

<!-- verify -->

```cangjie
open class C {
    public static func foo(): Unit {
        println("I am class C")
    }
}

class D <: C {
    public redef static func foo(): Unit {
        println("I am class D")
    }
}

main() {
    C.foo()
    D.foo()
}
```

对于被重定义的函数，调用时将根据 `class` 的类型决定调用的版本。例如，上例中 `C.foo()` 调用的是父类 C 中的函数 `foo`，`D.foo()` 调用的是子类 D 中的函数 `foo`。

```text
I am class C
I am class D
```

如果抽象函数或 `open` 修饰的函数有命名形参，那么实现函数或 `override` 修饰的函数也需要保持同样的命名形参。

<!-- compile.error -->

```cangjie
open class A {
    public open func f(a!: Int32): Int32 {
        a + 1
    }
}

class B <: A {
    public override func f(a!: Int32): Int32 { // OK
        a + 2
    }
}

class C <: A {
    public override func f(b!: Int32): Int32 { // Error
        b + 3
    }
}

main() {
    B().f(a: 0)
    C().f(b: 0)
}
```

还需要注意的是，当实现或重定义的函数为泛型函数时，子类型函数的类型变元约束需要比父类型中对应函数更宽松或相同。

<!-- compile.error -->

```cangjie
open class A {}
open class B <: A {}
open class C <: B {}

open class Base {
    public open func foo<T>(a: T): Unit where T <: B {}
    public open func bar<T>(a: T): Unit where T <: B {}
    public static func f<T>(a: T): Unit where T <: B {}
    public static func g<T>(): Unit where T <: B {}
}

class D <: Base {
    public override func foo<T>(a: T): Unit where T <: C {} // Error, stricter constraint
    public override func bar<T>(a: T): Unit where T <: C {} // Error, stricter constraint
    public redef static func f<T>(a: T): Unit where T <: C {} // Error, stricter constraint
    public redef static func g<T>(): Unit where T <: C {} // Error, stricter constraint
}

class E <: Base {
    public override func foo<T>(a: T): Unit where T <: A {} // OK: looser constraint
    public override func bar<V>(a: V): Unit where V <: A {} // OK: looser constraint, names of generic parameters do not matter
    public redef static func f<T>(a: T): Unit where T <: A {} // OK: looser constraint
    public redef static func g<T>(): Unit where T <: A {} // OK: looser constraint
}

class F <: Base {
    public override func foo<T>(a: T): Unit where T <: B {} // OK: same constraint
    public override func bar<V>(a: V): Unit where V <: B {} // OK: same constraint
    public redef static func f<T>(a: T): Unit where T <: B {} // OK: same constraint
    public redef static func g<T>(): Unit where T <: B {} // OK: same constraint
}
```


---

<!-- Content from source_zh_cn/class_and_interface/interface.md -->
# 接口

接口用来定义一个抽象类型，它不包含数据，但可以定义类型的行为。一个类型如果声明实现某接口，并且实现了该接口中所有的成员，就被称为实现了该接口。

接口的成员可以包含：

- 成员函数
- 操作符重载函数
- 成员属性

这些成员都是抽象的，要求实现类型必须拥有对应的成员实现。

## 接口定义

一个简单的接口定义如下：

<!-- verify -interface -->

```cangjie
interface I { // 'open' modifier is optional.
    func f(): Unit
}
```

接口使用关键字 `interface` 声明，其后是接口的标识符 `I` 和接口的成员。接口成员可被 `open` 修饰符修饰，并且 `open` 修饰符是可选的。

当接口 `I` 声明了一个成员函数 `f` 之后，要为一个类型实现 `I` 时，就必须在该类型中实现一个对应的 `f` 函数。

因为 `interface` 默认具有 `open` 语义，所以 `interface` 定义时的 `open` 修饰符是可选的。

如下面的代码所示，定义了一个 `class Foo`，使用 `Foo <: I` 的形式声明了 `Foo` 实现 `I` 接口。

在 `Foo` 中必须包含 `I` 声明的所有成员的实现，即需要定义一个相同类型的 `f`，否则会由于没有实现接口而编译报错。

<!-- verify -interface -->

```cangjie
class Foo <: I {
    public func f(): Unit {
        println("Foo")
    }
}

main() {
    let a = Foo()
    let b: I = a
    b.f() // "Foo"
}
```

当某个类型实现了某个接口之后，该类型就会成为该接口的子类型。

对于上面的例子，`Foo` 是 `I` 的子类型，因此任何一个 `Foo` 类型的实例，都可以当作 `I` 类型的实例使用。

在 `main` 中将一个 `Foo` 类型的变量 `a`，赋值给一个 `I` 类型的变量 `b`。然后再调用 `b` 中的函数 `f`，就会打印出 `Foo` 实现的 `f` 版本。程序的输出结果为：

<!-- verify -interface -->

```text
Foo
```

`interface` 也可以使用 `sealed` 修饰符表示只能在 `interface` 定义所在的包内继承、实现或扩展该 `interface`。`sealed` 已经蕴含了 `public`/`open` 的语义，因此定义 `sealed interface` 时若提供 `public`/`open` 修饰符，编译器将会告警。继承 `sealed` 接口的子接口或实现 `sealed` 接口的抽象类仍可被 `sealed` 修饰或不使用 `sealed` 修饰。若 `sealed` 接口的子接口被 `public` 修饰，且不被 `sealed` 修饰，则其子接口可在包外被继承、实现或扩展。继承、实现 sealed 接口的类型可以不被 `public` 修饰。

<!-- compile -->

```cangjie
package A
public interface I1 {}
sealed interface I2 {}         // OK
public sealed interface I3 {}  // Warning, redundant modifier, 'sealed' implies 'public'
sealed open interface I4 {}    // Warning, redundant modifier, 'sealed' implies 'open'

class C1 <: I1 {}
public open class C2 <: I1 {}
sealed abstract class C3 <: I2 {}
extend Int64 <: I2 {}
```

<!-- compile.error -error-->

```cangjie
package B
import A.*

class S1 <: I1 {}  // OK
class S2 <: I2 {}  // Error, I2 is sealed interface, cannot be inherited here.
```

通过接口的这种约束能力，可以对一系列的类型约定共同的功能，达到对功能进行抽象的目的。

例如下面的代码，可以定义一个 Flyable 接口，并且让其他具有 Flyable 属性的类实现它。

<!-- verify -->

```cangjie
interface Flyable {
    func fly(): Unit
}

class Bird <: Flyable {
    public func fly(): Unit {
        println("Bird flying")
    }
}

class Bat <: Flyable {
    public func fly(): Unit {
        println("Bat flying")
    }
}

class Airplane <: Flyable {
    public func fly(): Unit {
        println("Airplane flying")
    }
}

func fly(item: Flyable): Unit {
    item.fly()
}

main() {
    let bird = Bird()
    let bat = Bat()
    let airplane = Airplane()
    fly(bird)
    fly(bat)
    fly(airplane)
}
```

编译并执行上面的代码，会看到如下输出：

```text
Bird flying
Bat flying
Airplane flying
```

接口的成员可以是实例的或者静态的，以上的例子已经展示过实例成员函数的作用，接下来来看看静态成员函数的作用。

静态成员函数和实例成员函数类似，都要求实现类型提供实现。

例如下面的例子，定义了一个 `NamedType` 接口，这个接口含有一个静态成员函数 `typename` 用来获得每个类型的字符串名称。

这样其他类型在实现 `NamedType` 接口时就必须实现 `typename` 函数，之后就可以安全地在 `NamedType` 的子类型上获得类型的名称。

<!-- verify -->

```cangjie
interface NamedType {
    static func typename(): String
}

class A <: NamedType {
    public static func typename(): String {
        "A"
    }
}

class B <: NamedType {
    public static func typename(): String {
        "B"
    }
}

main() {
    println("the type is ${ A.typename() }")
    println("the type is ${ B.typename() }")
}
```

程序输出结果为：

```text
the type is A
the type is B
```

接口中的静态成员函数（或属性）可以没有默认实现，也可以拥有默认实现。

当其没有默认实现时，将无法通过接口类型名对其进行访问。例如下面的代码，直接访问 `NamedType` 的 `typename` 函数会发生编译报错，因为 `NamedType` 不具有 `typename` 函数的实现。

<!-- compile.error -->

```cangjie
interface NamedType {
    static func typename(): String
}
main() {
    NamedType.typename() // Error
}
```

接口中的静态成员函数（或属性）也可以拥有默认实现，当另一个类型继承拥有默认静态函数（或属性）实现的接口时，该类型可以不再实现这个静态成员函数（或属性），该函数（或属性）可以通过接口名和该类型名直接访问。如下用例，`NamedType` 的成员函数 `typename` 拥有默认实现，且在 `A` 中都可以不用再重新实现它，同时，也可以通过接口名和该类型名对其进行直接访问。

<!-- verify -->

```cangjie
interface NamedType {
    static func typename(): String {
        "interface NamedType"
    }
}

class A <: NamedType {}

main() {
    println(NamedType.typename())
    println(A.typename())
}
```

程序输出结果为：

```text
interface NamedType
interface NamedType
```

通常会通过泛型约束，在泛型函数中使用这类静态成员。

例如下面的 `printTypeName` 函数，当约束泛型变元 `T` 是 `NamedType` 的子类型时，需要保证 `T` 的实例化类型中所有的静态成员函数（或属性）都必须拥有实现，以保证可以使用 `T.typename` 的方式访问泛型变元的实现，达到了对静态成员抽象的目的。详见[泛型](../generic/generic_overview.md)。

<!-- compile.error -->

```cangjie
interface NamedType {
    static func typename(): String
}

interface I <: NamedType {
    static func typename(): String {
        f()
    }
    static func f(): String
}

class A <: NamedType {
    public static func typename(): String {
        "A"
    }
}

class B <: NamedType {
    public static func typename(): String {
        "B"
    }
}

func printTypeName<T>() where T <: NamedType {
    println("the type is ${ T.typename() }")
}

main() {
    printTypeName<A>() // OK
    printTypeName<B>() // OK
    printTypeName<I>() // Error, 'I' must implement all static function. Otherwise, an unimplemented 'f' is called, causing problems.
}
```

接口中可以定义泛型实例成员函数或泛型静态成员函数，与非泛型函数一样具有 `open` 语义。

<!-- compile -->

```cangjie
import std.collection.ArrayList
interface M {
    func foo<T>(a: T): T
    static func toString<T>(b: ArrayList<T>): String where T <: ToString
}
class C <: M {
    public func foo<S>(a: S): S { // implements M::foo, names of generic parameters do not matter
        a
    }
    public static func toString<T>(b: ArrayList<T>) where T <: ToString {
        var res = ""
        for (s in b) {
            res += s.toString()
        }
        res
    }
}
```

需要注意的是，接口的成员默认就被 `public` 修饰，不可以声明额外的访问控制修饰符，同时也要求实现类型必须使用 `public` 实现。

<!-- compile.error -->

```cangjie
interface I {
    func f(): Unit
}

open class C <: I {
    protected func f() {} // Compiler Error, f needs to be public semantics
}
```

## 接口继承与接口实现

当想为一个类型实现多个接口，可以在声明处使用 `&` 分隔多个接口，实现的接口之间没有顺序要求。

例如下面的例子，可以让 MyInt 同时实现 Addable 和 Subtractable 两个接口。

<!-- compile -->

```cangjie
interface Addable {
    func add(other: Int64): Int64
}

interface Subtractable {
    func sub(other: Int64): Int64
}

class MyInt <: Addable & Subtractable {
    var value = 0
    public func add(other: Int64): Int64 {
        value + other
    }
    public func sub(other: Int64): Int64 {
        value - other
    }
}
```

接口可以继承一个或多个接口，但不能继承类。与此同时，接口继承的时候可以添加新的接口成员。

例如下面的例子，Calculable 接口继承了 Addable 和 Subtractable 两个接口，并且增加了乘除两种运算符重载。

<!-- compile -myInt -->

```cangjie
interface Addable {
    func add(other: Int64): Int64
}

interface Subtractable {
    func sub(other: Int64): Int64
}

interface Calculable <: Addable & Subtractable {
    func mul(other: Int64): Int64
    func div(other: Int64): Int64
}
```

这样实现类型实现 Calculable 接口时就必须同时实现加减乘除四种运算符重载，不能缺少任何一个成员。

<!-- compile -myInt -->

```cangjie
class MyInt <: Calculable {
    var value = 0
    public func add(other: Int64): Int64 {
        value + other
    }
    public func sub(other: Int64): Int64 {
        value - other
    }
    public func mul(other: Int64): Int64 {
        value * other
    }
    public func div(other: Int64): Int64 {
        value / other
    }
}
```

MyInt 实现 Calculable 的同时，也同时实现了 Calculable 继承的所有接口，因此 MyInt 也实现了 Addable 和 Subtractable，即同时是它们的子类型。

<!-- compile -myInt -->

```cangjie
main() {
    let myInt = MyInt()
    let add: Addable = myInt
    let sub: Subtractable = myInt
    let calc: Calculable = myInt
}
```

对于 `interface` 的继承，子接口如果继承了父接口中有默认实现的函数或属性，则在子接口中不允许仅写此函数或属性的声明（即没有默认实现），它必须要给出新的默认实现。函数定义前的 `override` 修饰符或 `redef` 修饰符是可选的。子接口如果继承了父接口中没有默认实现的函数或属性，则在子接口中允许仅写此函数或属性的声明，当然也允许定义默认实现，并且函数声明或定义前的 `override` 修饰符或 `redef` 修饰符同样是可选的。其中，`redef` 修饰符是针对子类中的同名静态函数的重定义。

<!-- compile.error -->

```cangjie
interface I1 {
   func f(a: Int64) {
        a
   }
   static func g(a: Int64) {
        a
   }
   func f1(a: Int64): Unit
   static func g1(a: Int64): Unit
}

interface I2 <: I1 {
    /*'override' is optional*/ func f(a: Int64) {
       a + 1
    }
    override func f(a: Int32) {} // Error, override function 'f' does not have an overridden function from its supertypes
    static /*'redef' is optional*/ func g(a: Int64) {
       a + 1
    }
    /*'override' is optional*/ func f1(a: Int64): Unit {}
    static /*'redef' is optional*/ func g1(a: Int64): Unit {}
}
```

### 接口实现的要求

仓颉除 Tuple、VArray 和函数外的其他类型都可以实现接口。

一个类型实现接口有三种途径：

1. 在定义类型时就声明实现接口，在以上的内容中已经见过相关例子。
2. 通过扩展实现接口，这种方式详见[扩展](../extension/interface_extension.md)。
3. 由语言内置实现，具体详见《仓颉编程语言库 API》相关文档。

实现类型声明实现接口时，需要实现接口中要求的所有成员，为此需要满足下面一些规则。

1. 对于成员函数和操作符重载函数，要求实现类型提供的函数实现与接口对应的函数名称相同、参数列表相同、返回类型相同。
2. 对于成员属性，要求是否被 `mut` 修饰保持一致，并且属性的类型相同。

所以大部分情况都如同上面的例子，需要让实现类型中包含与接口要求的一样的成员的实现。

但有个地方是个例外，如果接口中的成员函数或操作符重载函数的返回值类型是 class 类型，那么允许实现函数的返回类型是其子类型。

例如下面这个例子，`I` 中的 `f` 返回类型是一个 `class` 类型 `Base`，因此 `C` 中实现的 `f` 返回类型可以是 `Base` 的子类型 `Sub`。

<!-- compile -->

```cangjie
open class Base {}
class Sub <: Base {}

interface I {
    func f(): Base
}

class C <: I {
    public func f(): Sub {
        Sub()
    }
}
```

除此以外，接口的成员还可以提供默认实现。例如下面的代码中，`SayHi` 中的 `say` 拥有默认实现，因此 `A` 实现 `SayHi` 时可以继承 `say` 的实现，而 `B` 也可以选择提供自己的 `say` 实现。

<!-- compile -->

```cangjie
interface SayHi {
    func say() {
        "hi"
    }
}

class A <: SayHi {}

class B <: SayHi {
    public func say() {
        "hi, B"
    }
}
```

特别地，如果一个类型在实现多个接口时，多个接口中包含同一个成员的默认实现，这时会发生多重继承的冲突，语言无法选择最适合的实现，因此这时接口中的默认实现也会失效，需要实现类型提供自己的实现。

例如下面的例子，`SayHi` 和 `SayHello` 中都包含了 `say` 的实现，`Foo` 在实现这两个接口时就必须提供自己的实现，否则会出现编译错误。

<!-- compile -->

```cangjie
interface SayHi {
    func say() {
        "hi"
    }
}

interface SayHello {
    func say() {
        "hello"
    }
}

class Foo <: SayHi & SayHello {
    public func say() {
        "Foo"
    }
}
```

struct、enum 和 class 在实现接口时，函数或属性定义前的 `override` 修饰符（或 `redef` 修饰符）是可选的，无论接口中的函数或属性是否存在默认实现。

<!-- compile -->

```cangjie
interface I {
    func foo(): Int64 {
        return 0
    }
}
enum E <: I{
    elem
    public override func foo(): Int64 {
        return 1
    }
}
struct S <: I {
    public override func foo(): Int64 {
        return 1
    }
}
```

## Any 类型

Any 类型是一个内置的接口，它的定义如下：

<!-- compile -->

```cangjie
interface Any {}
```

仓颉中所有接口都默认继承它，所有非接口类型都默认实现它，因此所有类型都可以作为 Any 类型的子类型使用。

如下面的代码，可以将一系列不同类型的变量赋值给 Any 类型的变量。

<!-- compile -->

```cangjie
main() {
    var any: Any = 1
    any = 2.0
    any = "hello, world!"
}
```


---

<!-- Content from source_zh_cn/class_and_interface/prop.md -->
# 属性

属性（Properties）提供了一个 getter 和一个可选的 setter 来间接获取和设置值。

使用属性的时候与普通变量无异，只需要对数据操作，对内部的实现无感知，可以更便利地实现访问控制、数据监控、跟踪调试、数据绑定等机制。

属性在使用时可以作为表达式或被赋值。此处以类和接口为例进行说明，但属性不仅限于类和接口。

以下是一个简单的例子，b 是一个典型的属性，封装了外部对 a 的访问：

<!-- verify -->

```cangjie
class Foo {
    private var a = 0

    public mut prop b: Int64 {
        get() {
            println("get")
            a
        }
        set(value) {
            println("set")
            a = value
        }
    }
}

main() {
    var x = Foo()
    let y = x.b + 1 // get
    x.b = y // set
}
```

此处 Foo 提供了一个名为 b 的属性，针对 getter/setter 这两个功能，仓颉提供了 get 和 set 两种语法来定义。当一个类型为 Foo 的变量 x 在访问 b 时，会调用 b 的 get 操作返回类型为 Int64 的值，因此可以用来与 1 相加；而当 x 在对 b 进行赋值时，会调用 b 的 set 操作，将 y 的值传给 set 的 value，最终将 value 的值赋值给 a。

通过属性 b，外部对 Foo 的成员变量 a 完全不感知，但却可以通过 b 做到同样地访问和修改操作，实现了有效的封装性。所以程序的输出如下：

```text
get
set
```

## 属性定义

属性可以在 interface、class、struct、enum、extend 中定义。

一个典型的属性语法结构如下：

<!-- compile -->

```cangjie
class Foo {
    public prop a: Int64 {
        get() { 0 }
    }
    public mut prop b: Int64 {
        get() { 0 }
        set(v) {}
    }
}
```

其中使用 prop 声明的 a 和 b 都是属性，a 和 b 的类型都是 `Int64`。a 是无 `mut` 修饰符的属性，这类属性有且仅有定义 getter（对应取值）实现。b 是使用 `mut` 修饰的属性，这类属性必须分别定义 getter（对应取值）和 setter（对应赋值）的实现。

> **注意：**
>
> 对于数值、元组、函数、`Bool`、`Unit`、`Nothing`、`String`、`Range` 和 `enum` 类型，在它们的扩展和声明中不能声明 mut 修饰的属性，也不能实现有 mut 属性的接口。

属性的 getter 和 setter 分别对应两个不同的函数。

1. getter 函数类型是 `() -> T`，T 是该属性的类型，当使用该属性作为表达式时会执行 getter 函数。
2. setter 函数类型是 `(T) -> Unit`，T 是该属性的类型，形参名需要显式指定，当对该属性赋值时会执行 setter 函数。

getter 和 setter 的实现中可以和函数体一样包含声明和表达式，与函数体的规则一样，详见[函数体](../function/define_functions.md#函数体)章节。

setter 中的参数对应的是赋值时传入的值。

<!-- compile -->

```cangjie
class Foo {
    private var j = 0
    public mut prop i: Int64 {
        get() {
            j
        }
        set(v) {
            j = v
        }
    }
}
```

需要注意的是，在属性的 getter 和 setter 中访问属性自身属于递归调用，与函数调用一样可能会出现死循环的情况。

### 修饰符

可以在 `prop` 前面声明需要的修饰符。

<!-- compile -->

```cangjie
class Foo {
    public prop a: Int64 {
        get() {
            0
        }
    }
    private prop b: Int64 {
        get() {
            0
        }
    }
}
```

和成员函数一样，成员属性也支持 `open`、`override`、`redef` 修饰，所以也可以在子类型中覆盖/重定义父类型属性的实现。

子类型覆盖父类型的属性时，如果父类型属性带有 `mut` 修饰符，则子类型属性也需要带有 `mut` 修饰符，同时也必须保持一样的类型。

如下代码所示，A 中定义了 x 和 y 两个属性，B 中可以分别对 x 和 y 进行 `override`/`redef`：

<!-- compile -->

```cangjie
open class A {
    private var valueX = 0
    private static var valueY = 0

    public open prop x: Int64 {
        get() { valueX }
    }

    public static mut prop y: Int64 {
        get() { valueY }
        set(v) {
            valueY = v
        }
    }
}
class B <: A {
    private var valueX2 = 0
    private static var valueY2 = 0

    public override prop x: Int64 {
        get() { valueX2 }
    }

    public redef static mut prop y: Int64 {
        get() { valueY2 }
        set(v) {
            valueY2 = v
        }
    }
}
```

### 抽象属性

类似于抽象函数，在 `interface` 和抽象类中也可以声明抽象属性，这些抽象属性没有实现。

<!-- compile -->

```cangjie
interface I {
    prop a: Int64
}

abstract class C {
    public prop a: Int64
}
```

当实现类型实现 `interface` 或者非抽象子类继承抽象类时，必须要实现这些抽象属性。

与覆盖的规则一样，实现类型或子类在实现这些属性时，如果父类型属性带有 `mut` 修饰符，则子类型属性也需要带有 `mut` 修饰符，同时也必须保持一样的类型。

<!-- compile -->

```cangjie
interface I {
    prop a: Int64
    mut prop b: Int64
}
class C <: I {
    private var value = 0

    public prop a: Int64 {
        get() { value }
    }

    public mut prop b: Int64 {
        get() { value }
        set(v) {
            value = v
        }
    }
}
```

通过抽象属性，可以让接口和抽象类对一些数据操作能以更加易用的方式进行约定，相比函数的方式要更加直观。

如下代码所示，如果要对一个 size 值的获取和设置进行约定，使用属性的方式 (I1) 相比使用函数的方式 (I2) 代码更少，也更加符合对数据操作的意图。

<!-- verify -->

```cangjie
interface I1 {
    mut prop size: Int64
}

interface I2 {
    func getSize(): Int64
    func setSize(value: Int64): Unit
}

class C <: I1 & I2 {
    private var mySize = 0

    public mut prop size: Int64 {
        get() {
            mySize
        }
        set(value) {
            mySize = value
        }
    }

    public func getSize() {
        mySize
    }

    public func setSize(value: Int64) {
        mySize = value
    }
}

main() {
    let a: I1 = C()
    a.size = 5
    println(a.size)

    let b: I2 = C()
    b.setSize(5)
    println(b.getSize())
}
```

```text
5
5
```

## 属性使用

属性分为实例成员属性和静态成员属性。成员属性的使用和成员变量的使用方式一样，详见[成员变量](./class.md#class-成员变量)章节。

<!-- verify -->

```cangjie
class A {
    public prop x: Int64 {
        get() {
            123
        }
    }
    public static prop y: Int64 {
        get() {
            321
        }
    }
}

main() {
    var a = A()
    println(a.x) // 123
    println(A.y) // 321
}
```

结果为：

```text
123
321
```

无 `mut` 修饰符的属性类似 `let` 声明的变量，不能被赋值。

<!-- compile.error -->

```cangjie
class A {
    private let value = 0
    public prop i: Int64 {
        get() {
            value
        }
    }
}

main() {
    var x = A()
    println(x.i) // OK
    x.i = 1 // Error
}
```

带有 `mut` 修饰符的属性类似 `var` 声明的变量，可以取值也可以被赋值。

<!-- verify -->

```cangjie
class A {
    private var value: Int64 = 0
    public mut prop i: Int64 {
        get() {
            value
        }
        set(v) {
            value = v
        }
    }
}

main() {
    var x = A()
    println(x.i) // OK
    x.i = 1 // OK
}
```

```text
0
```


---

<!-- Content from source_zh_cn/class_and_interface/subtype.md -->
# 子类型关系

与其他面向对象语言一样，仓颉语言提供子类型关系和子类型多态。举例说明（不限于下述用例）：

- 假设函数的形参是类型 `T`，则函数调用时传入的参数的实际类型既可以是 `T` 也可以是 `T` 的子类型（严格地说，`T` 的子类型已经包括 `T` 自身，下同）。
- 假设赋值表达式 `=` 左侧的变量的类型是 `T`，则 `=` 右侧的表达式的实际类型既可以是 `T` 也可以是 `T` 的子类型。
- 假设函数定义中用户标注的返回类型是 `T`，则函数体的类型（以及函数体内所有 `return` 表达式的类型）既可以是 `T` 也可以是 `T` 的子类型。

下文将说明两个类型为子类型关系的几种情况。

## 继承 class 带来的子类型关系

继承 class 后，子类即为父类的子类型。如下代码中， `Sub` 即为 `Super` 的子类型。

<!-- compile -->

```cangjie
open class Super {}
class Sub <: Super {}
```

## 实现接口带来的子类型关系

实现接口（含扩展实现）后，实现接口的类型即为接口的子类型。如下代码中，`I3` 是 `I1` 和 `I2` 的子类型， `C` 是 `I1` 的子类型， `Int64` 是 `I2` 的子类型：

<!-- compile -->

```cangjie
interface I1 {}
interface I2 {}

interface I3 <: I1 & I2 {}

class C <: I1 {}

extend Int64 <: I2 {}
```

## 元组类型的子类型关系

仓颉语言中的元组类型也有子类型关系。直观的，如果一个元组 `t1` 的每个元素的类型都是另一个元组 `t2` 的对应位置元素类型的子类型，那么元组 `t1` 的类型也是元组 `t2` 的类型的子类型。例如下面的代码中，由于 `C2 <: C1` 和 `C4 <: C3`，因此也有 `(C2, C4) <: (C1, C3)` 以及 `(C4, C2) <: (C3, C1)`。

<!-- compile -->

```cangjie
open class C1 {}
class C2 <: C1 {}

open class C3 {}
class C4 <: C3 {}

let t1: (C1, C3) = (C2(), C4()) // OK
let t2: (C3, C1) = (C4(), C2()) // OK
```

## 函数类型的子类型关系

仓颉语言中，函数是一等公民，而函数类型亦有子类型关系：给定两个函数类型 `(U1) -> S2` 和 `(U2) -> S1`，如果存在 `(U1) -> S2` 是 `(U2) -> S1`的子类型，当且仅当 `U2` 是 `U1` 的子类型，且 `S2` 是 `S1` 的子类型（注意顺序）。例如下面的代码定义了两个函数 `f : (U1) -> S2` 和 `g : (U2) -> S1`，且 `f` 的类型是 `g` 的类型的子类型。由于 `f` 的类型是 `g` 的子类型，所以代码中使用到 `g` 的地方都可以换为 `f`。

<!-- compile -->

```cangjie
open class U1 {}
class U2 <: U1 {}

open class S1 {}
class S2 <: S1 {}


func f(a: U1): S2 { S2() }
func g(a: U2): S1 { S1() }

func call1() {
    g(U2()) // OK
    f(U2()) // OK
}

func h(lam: (U2) -> S1): S1 {
    lam(U2())
}

func call2() {
    h(g) // OK
    h(f) // OK
}
```

对于上面的规则，`S2 <: S1` 部分很好理解：函数调用产生的结果数据会被后续程序使用，函数 `g` 可以产生 `S1` 类型的结果数据，函数 `f` 可以产生 `S2` 类型的结果，而 `g` 产生的结果数据应当能被 `f` 产生的结果数据替代，因此要求 `S2 <: S1`。

对于 `U2 <: U1` 的部分，可以这样理解：在函数调用产生结果前，它本身应当能够被调用，函数调用的实参类型固定不变，同时形参类型要求更宽松时，依然可以被调用，而形参类型要求更严格时可能无法被调用——例如给定上述代码中的定义 `g(U2())` 可以被换为 `f(U2())`，正是因为实参类型 `U2` 的要求更严格于形参类型 `U1`。

## 永远成立的子类型关系

仓颉语言中，有些预设的子类型关系是永远成立的：

- 一个类型 `T` 永远是自身的子类型，即 `T <: T`。
- `Nothing` 类型永远是其他任意类型 `T` 的子类型，即 `Nothing <: T`。
- 任意类型 `T` 都是 `Any` 类型的子类型，即 `T <: Any`。
- 任意 `class` 定义的类型都是 `Object` 的子类型，即如果有 `class C {}`，则 `C <: Object`。

## 传递性带来的子类型关系

子类型关系具有传递性。如下代码中，虽然只描述了 `I2 <: I1`、`C <: I2` 以及 `Bool <: I2`，但根据子类型的传递性，也隐式存在 `C <: I1` 以及 `Bool <: I1` 这两个子类型关系。

<!-- compile -->

```cangjie
interface I1 {}
interface I2 <: I1 {}

class C <: I2 {}

extend Bool <: I2 {}
```

## 泛型类型的子类型关系

泛型类型间也有子类型关系，详见[泛型类型的子类型关系](../generic/generic_subtype.md)。


---

<!-- Content from source_zh_cn/class_and_interface/typecast.md -->
# 类型转换

仓颉不支持不同类型之间的隐式转换（子类型天然是父类型，所以子类型到父类型的转换不是隐式类型转换），类型转换必须显式地进行。下面将依次介绍数值类型之间的转换，`Rune` 到 `UInt32` 和整数类型到 `Rune` 的转换，以及 `is` 和 `as` 操作符。

## 数值类型之间的转换

对于数值类型（包括：`Int8`，`Int16`，`Int32`，`Int64`，`IntNative`，`UInt8`，`UInt16`，`UInt32`，`UInt64`，`UIntNative`，`Float16`，`Float32`，`Float64`），仓颉支持使用 `T(e)` 的方式得到一个值等于 `e`，类型为 `T` 的值。其中，表达式 `e` 的类型和 `T` 可以是上述任意数值类型。

下面的例子展示了数值类型之间的类型转换：

<!-- verify -->

```cangjie
main() {
    let a: Int8 = 10
    let b: Int16 = 20
    let r1 = Int16(a)
    println("The type of r1 is 'Int16', and r1 = ${r1}")
    let r2 = Int8(b)
    println("The type of r2 is 'Int8', and r2 = ${r2}")

    let c: Float32 = 1.0
    let d: Float64 = 1.123456789
    let r3 = Float64(c)
    println("The type of r3 is 'Float64', and r3 = ${r3}")
    let r4 = Float32(d)
    println("The type of r4 is 'Float32', and r4 = ${r4}")

    let e: Int64 = 1024
    let f: Float64 = 1024.1024
    let r5 = Float64(e)
    println("The type of r5 is 'Float64', and r5 = ${r5}")
    let r6 = Int64(f)
    println("The type of r6 is 'Int64', and r6 = ${r6}")
}
```

上述代码的执行结果为：

```text
The type of r1 is 'Int16', and r1 = 10
The type of r2 is 'Int8', and r2 = 20
The type of r3 is 'Float64', and r3 = 1.000000
The type of r4 is 'Float32', and r4 = 1.123457
The type of r5 is 'Float64', and r5 = 1024.000000
The type of r6 is 'Int64', and r6 = 1024
```

> **注意：**
>
> 类型转换时可能发生溢出，若溢出可提前在编译器检测出来，则编译器会直接给出报错，否则根据默认的溢出策略将抛出异常。

## `Rune` 到 `UInt32` 和整数类型到 `Rune` 的转换

`Rune` 到 `UInt32` 的转换使用 `UInt32(e)` 的方式，其中 `e` 是一个 `Rune` 类型的表达式，`UInt32(e)` 的结果是 `e` 的 Unicode scalar value 对应的 `UInt32` 类型的整数值。

整数类型到 `Rune` 的转换使用 `Rune(num)` 的方式，其中 `num` 的类型可以是任意的整数类型，且仅当 `num` 的值落在 `[0x0000, 0xD7FF]` 或 `[0xE000, 0x10FFFF]` （即 Unicode scalar value）中时，返回对应的 Unicode scalar value 表示的字符，否则，编译报错（编译时可确定 `num` 的值）或运行时抛异常。

下面的例子展示了 `Rune` 和 `UInt32` 之间的类型转换：

<!-- verify -->

```cangjie
main() {
    let x: Rune = 'a'
    let y: UInt32 = 65
    let r1 = UInt32(x)
    let r2 = Rune(y)
    println("The type of r1 is 'UInt32', and r1 = ${r1}")
    println("The type of r2 is 'Rune', and r2 = ${r2}")
}
```

上述代码的执行结果为：

```text
The type of r1 is 'UInt32', and r1 = 97
The type of r2 is 'Rune', and r2 = A
```

## `is` 和 `as` 操作符

仓颉支持使用 `is` 操作符来判断某个表达式的类型是否是指定的类型（或其子类型）。具体而言，对于表达式 `e is T`（`e` 可以是任意表达式，`T` 可以是任何类型），当 `e` 的运行时类型是 `T` 的子类型时，`e is T` 的值为 `true`，否则 `e is T` 的值为 `false`。

下面的例子展示了 `is` 操作符的使用：

<!-- verify -->

```cangjie
open class Base {
    var name: String = "Alice"
}
class Derived <: Base {
    var age: UInt8 = 18
}

main() {
    let a = 1 is Int64
    println("Is the type of 1 'Int64'? ${a}")
    let b = 1 is String
    println("Is the type of 1 'String'? ${b}")

    let b1: Base = Base()
    let b2: Base = Derived()
    var x = b1 is Base
    println("Is the type of b1 'Base'? ${x}")
    x = b1 is Derived
    println("Is the type of b1 'Derived'? ${x}")
    x = b2 is Base
    println("Is the type of b2 'Base'? ${x}")
    x = b2 is Derived
    println("Is the type of b2 'Derived'? ${x}")
}
```

上述代码的执行结果为：

```text
Is the type of 1 'Int64'? true
Is the type of 1 'String'? false
Is the type of b1 'Base'? true
Is the type of b1 'Derived'? false
Is the type of b2 'Base'? true
Is the type of b2 'Derived'? true
```

`as` 操作符可以用于将某个表达式的类型转换为指定的类型。因为类型转换有可能会失败，所以 `as` 操作返回的是一个 `Option` 类型。具体而言，对于表达式 `e as T`（`e` 可以是任意表达式，`T` 可以是任何类型），当 `e` 的运行时类型是 `T` 的子类型时，`e as T` 的值为 `Option<T>.Some(e)`，否则 `e as T` 的值为 `Option<T>.None`。

下面的例子展示了 `as` 操作符的使用（注释中标明了 `as` 操作的结果）：

<!-- compile -->

```cangjie
open class Base {
    var name: String = "Alice"
}
class Derived <: Base {
    var age: UInt8 = 18
}

let a = 1 as Int64     // a = Option<Int64>.Some(1)
let b = 1 as String    // b = Option<String>.None

let b1: Base = Base()
let b2: Base = Derived()
let d: Derived = Derived()
let r1 = b1 as Base    // r1 = Option<Base>.Some(b1)
let r2 = b1 as Derived // r2 = Option<Derived>.None
let r3 = b2 as Base    // r3 = Option<Base>.Some(b2)
let r4 = b2 as Derived // r4 = Option<Derived>.Some(b2)
let r5 = d as Base     // r5 = Option<Base>.Some(d)
let r6 = d as Derived  // r6 = Option<Derived>.Some(d)
```


---

<!-- Content from source_zh_cn/generic/generic_overview.md -->
# 泛型概述

在仓颉编程语言中，泛型指的是参数化类型，参数化类型是一个在声明时未知并且需要在使用时指定的类型。类型声明与函数声明可以是泛型的。最为常见的例子就是 `Array<T>`、`Set<T>` 等容器类型。

在仓颉中，function、class、interface、struct 与 enum 的声明都可以声明类型形参，也就是说它们都可以是泛型的。

为了方便讨论，定义如下几个常用的术语：

- 类型形参：一个类型或者函数声明可能有一个或者多个需要在使用处被指定的类型，这些类型就被称为类型形参。在声明形参时，需要给定一个标识符，以便在声明体中引用。
- 类型变元：在声明类型形参后，当通过标识符来引用这些类型时，这些标识符被称为类型变元。
- 类型实参：当在使用泛型声明的类型或函数时指定了泛型参数，这些参数被称为类型实参。
- 类型构造器：一个需要零个、一个或者多个类型作为实参的类型称为类型构造器。

类型形参在声明时一般在类型名称的声明或者函数名称的声明后，使用尖括号 `<...>` 括起来。例如一个泛型的列表可声明为：

<!-- compile -->

```cangjie
class List<T> {
    var elem: Option<T> = None
    var tail: Option<List<T>> = None
}

func sumInt(a: List<Int64>) {  }
```

其中 `List<T>` 中的 `T` 被称为类型形参。对于 `elem: Option<T>` 中对 `T` 的引用称为类型变元，同理 `tail: Option<List<T>>` 中的 `T` 也称为类型变元。函数 `sumInt` 的参数中 `List<Int64>` 的 `Int64` 被称为 `List` 的类型实参。 `List` 就是类型构造器，`List<Int64>` 通过 `Int64` 类型实参构造出了一个类型 `Int64` 的列表类型。


---

<!-- Content from source_zh_cn/generic/generic_function.md -->
# 泛型函数

如果一个函数声明了一个或多个类型形参，则将其称为泛型函数。语法上，类型形参紧跟在函数名后，并用 `<>` 括起，如果有多个类型形参，则用 `,` 分离。

## 全局泛型函数

在声明全局泛型函数时，只需要在函数名后使用尖括号声明类型形参，然后就可以在函数形参、返回类型及函数体中对这一类型形参进行引用。例如 `id` 函数定义为：

<!-- compile -->

```cangjie
func id<T>(a: T): T {
    return a
}
```

其中， `(a: T)` 是函数声明的形参，它使用到了 `id` 函数声明的类型形参 `T`，并且在 `id` 函数的返回类型使用。

再比如另一个复杂的例子，定义如下一个泛型函数 `composition`，该函数声明了 3 个类型形参，分别是 `T1, T2, T3`，其功能是把两个函数 `f: (T1) -> T2, g: (T2) -> T3` 复合成类型为 `(T1) -> T3` 的函数。

<!-- verify -composition -->

```cangjie
func composition<T1, T2, T3>(f: (T1) -> T2, g: (T2) -> T3): (T1) -> T3 {
    return {x: T1 => g(f(x))}
}
```

因为可以被用来复合的函数是任意类型，例如可以是 `(Int32) -> Bool, (Bool) -> Int64` 的复合，也可以是 `(Int64) -> Rune, (Rune) -> Int8` 的复合，所以才需要使用泛型函数。

<!-- verify -composition -->

```cangjie
func times2(a: Int64): Int64 {
    return a * 2
}

func plus10(a: Int64): Int64 {
    return a + 10
}

func times2plus10(a: Int64) {
    return composition<Int64, Int64, Int64>(times2, plus10)(a)
}

main() {
  println(times2plus10(9))
}
```

这里，复合两个 `(Int64) -> Int64` 的函数，将 9 先乘以 2，再加 10，结果会是 28。

<!-- verify -composition -->

```text
28
```

## 局部泛型函数

局部函数也可以是泛型函数。例如泛型函数 `id` 可以嵌套定义在其他函数中：

<!-- verify -->

```cangjie
func foo(a: Int64) {
    func id<T>(a: T): T { a }

    func double(a: Int64): Int64 { a + a }

    return (id<Int64> ~> double)(a) == (double ~> id<Int64>)(a)
}

main() {
    println(foo(1))
}
```

这里由于 `id` 的单位元性质，函数 `id<Int64> ~> double` 和 `double ~> id<Int64>` 是等价的，结果是 `true`。

```text
true
```

## 泛型成员函数

class、struct 与 enum 的成员函数可以是泛型的。例如：

<!-- verify -->

```cangjie
class A {
    func foo<T>(a: T): Unit where T <: ToString {
        println("${a}")
    }
}

struct B {
    func bar<T>(a: T): Unit where T <: ToString {
        println("${a}")
    }
}

enum C {
    | X | Y

    func coo<T>(a: T): Unit where T <: ToString {
        println("${a}")
    }
}

main() {
    var a = A()
    var b = B()
    var c = C.X
    a.foo<Int64>(10)
    b.bar<String>("abc")
    c.coo<Bool>(false)
}
```

程序输出的结果为：

```text
10
abc
false
```

在为类型使用 extend 声明进行扩展时，扩展中的函数也可以是泛型的，例如可以为 `Int64` 类型增加一个泛型成员函数：

<!-- verify -->

```cangjie
extend Int64 {
    func printIntAndArg<T>(a: T) where T <: ToString {
        println(this)
        println("${a}")
    }
}

main() {
    var a: Int64 = 12
    a.printIntAndArg<String>("twelve")
}
```

程序输出的结果将为：

```text
12
twelve
```

## 静态泛型函数

interface、class、struct、enum 与 extend 中可以定义静态泛型函数，例如下例 `ToPair` class 中从 `ArrayList` 中返回一个元组：

<!-- run -->

```cangjie
import std.collection.ArrayList

class ToPair {
    public static func fromArray<T>(l: ArrayList<T>): (T, T) {
        return (l[0], l[1])
    }
}

main() {
    var res: ArrayList<Int64> = ArrayList([1,2,3,4])
    var a: (Int64, Int64) = ToPair.fromArray<Int64>(res)
}
```


---

<!-- Content from source_zh_cn/generic/generic_interface.md -->
# 泛型接口

泛型可以用来定义泛型接口，以标准库中定义的 `Iterable` 为例，它的成员函数 `iterator` 需要返回一个 `Iterator` 类型，这一类型是一个容器的遍历器。 `Iterator` 是一个泛型接口，`Iterator` 内部有一个从容器类型中返回下一个元素的 `next` 成员函数，`next` 成员函数返回的类型是一个需要在使用时指定的类型，所以 `Iterator` 需要声明泛型参数。

<!-- compile -->

```cangjie
public interface Iterable<E> {
    func iterator(): Iterator<E>
}

public interface Iterator<E> <: Iterable<E> {
    func next(): Option<E>
}

public interface Collection<T> <: Iterable<T> {
     prop size: Int64
     func isEmpty(): Bool
}
```


---

<!-- Content from source_zh_cn/generic/generic_class.md -->
# 泛型类

[泛型接口](./generic_interface.md)中介绍了泛型接口的定义和使用，本节介绍泛型类的定义和使用。如 `Map` 的键值对就是使用泛型类来定义的。

`Map` 类型中的键值对 `Node` 类型就可以使用泛型类来定义：

<!-- compile -->

```cangjie
open class Node<K, V> where K <: Hashable & Equatable<K> {
    var key: Option<K> = Option<K>.None
    var value: Option<V> = Option<V>.None

    init() {}

    init(key: K, value: V) {
        this.key = Option<K>.Some(key)
        this.value = Option<V>.Some(value)
    }
}
```

由于键与值的类型有可能不相同，且可以为任意满足条件的类型，所以 `Node` 需要两个类型形参 `K` 与 `V` ，`K <: Hashable, K <: Equatable<K>` 是对于键类型的约束，意为 `K` 要实现 `Hashable` 与 `Equatable<K>` 接口，也就是 `K` 需要满足的条件。对于泛型约束，详见[泛型约束](./generic_constraint.md)章节。

由于泛型类的静态成员变量的内存是共享的，因此，静态成员变量或属性的类型声明和表达式中不能引用类型参数或包含未实例化泛型类型表达式。另外，静态变量或属性初始化表达式中不能调用泛型类的静态成员函数或属性。

<!-- compile.error -->

```cangjie
class A<T> {}
class B<T> {
    static func foo() {1}
    static var err1: A<T> = A<T>() // Error, static member cannot depend on generic parameter 'Generics-T'
    static prop err2: A<T> { // Error, static member cannot depend on generic parameter 'Generics-T'
        get() {
            A<T>() // Error, static member cannot depend on generic parameter 'Generics-T'
        }
    }
    static var vfoo = foo() // Error, it's equal to 'static var vfoo = B<T>.foo()', implicit reference to generic 'T'.
    static var ok: Int64 = 1
}

main() {
    B<Int32>.ok = 2
    println(B<Int64>.ok) // 2
}
```


---

<!-- Content from source_zh_cn/generic/generic_struct.md -->
# 泛型结构体

struct 类型的泛型与 class 是类似的，下面可以使用 struct 定义一个类似于二元元组的类型：

<!-- verify -->

```cangjie
struct Pair<T, U> {
    let x: T
    let y: U
    public init(a: T, b: U) {
        x = a
        y = b
    }
    public func first(): T {
        return x
    }
    public func second(): U {
        return y
    }
}

main() {
    var a: Pair<String, Int64> = Pair<String, Int64>("hello", 0)
    println(a.first())
    println(a.second())
}
```

程序输出的结果为：

```text
hello
0
```

在 `Pair` 中提供了 `first` 与 `second` 两个函数来取得元组的第一个与第二个元素。


---

<!-- Content from source_zh_cn/generic/generic_enum.md -->
# 泛型枚举

在仓颉编程语言的泛型 enum 类型设计中，`Option` 类型是一个典型的示例，关于 `Option` 详细描述请参见 [Option 类型](../enum_and_pattern_match/option_type.md)章节。 `Option` 类型用于表示在某一类型上的值可能是个空的值。这样，`Option` 就可以用来表示在某种类型上计算的失败。这里是何种类型上的失败是不确定的，所以很明显，`Option` 是一个泛型类型，需要声明类型形参。

```cangjie
package std.core // `Option` is defined in std.core.

public enum Option<T> {
      Some(T)
    | None

    public func getOrThrow(): T {
        match (this) {
            case Some(v) => v
            case None => throw NoneValueException()
        }
    }
    // ...
}
```

可以看到，`Option<T>` 分成两种情况，一种是 `Some(T)`，用来表示一个有值的返回结果，另一种是 `None` 用来表示一个空的结果。其中的 `getOrThrow` 函数会是将 `Some(T)` 内部的值返回出来的函数，返回的结果就是 `T` 类型，而如果参数是 None，那么直接抛出异常。

例如，如果想定义一个安全的除法，因为在除法上的计算是可能失败的。如果除数为 0，那么返回 `None` ，否则返回一个用 `Some` 包装过的结果：

<!-- compile -->

```cangjie
func safeDiv(a: Int64, b: Int64): Option<Int64> {
    var res: Option<Int64> = match (b) {
                case 0 => None
                case _ => Some(a/b)
            }
    return res
}
```

这样，在除数为 0 时，程序运行的过程中不会因除以 0 而抛出算术运算异常。


---

<!-- Content from source_zh_cn/generic/generic_subtype.md -->
# 泛型类型的子类型关系

实例化后的泛型类型间也有子类型关系。例如：

<!-- compile -->

```cangjie
interface I<X, Y> { }

class C<Z> <: I<Z, Z> { }
```

根据 `class C<Z> <: I<Z, Z> { }`，便知 `C<Bool> <: I<Bool, Bool>` 以及 `C<D> <: I<D, D>` 等。这可以解读为“对于所有的不含类型变元的 `Z` 类型，都有 `C<Z> <: I<Z, Z>` 成立”。

但是对于下列代码：

<!-- compile -->

```cangjie
open class C { }
class D <: C { }

interface I<X> { }
```

`I<D> <: I<C>` 是不成立的（即使 `D <: C` 成立），这是因为在仓颉语言中，用户定义的类型构造器在其类型参数处是**不型变**的。

型变的具体定义为：如果 `A` 和 `B` 是（实例化后的）类型，`T` 是类型构造器，设有一个类型参数 `X`（例如 `interface T<X>`），那么

- 如果 `T(A) <: T(B)` 当且仅当 `A = B`，则 `T` 是**不型变**的。
- 如果 `T(A) <: T(B)` 当且仅当  `A <: B` ，则 `T` 在 `X` 处是**协变**的。
- 如果 `T(A) <: T(B)` 当且仅当 `B <: A` ，则 `T` 在 `X` 处是**逆变**的。

因为现阶段的仓颉中，所有用户自定义的泛型类型在其所有的类型变元处都是不变的，所以给定 `interface I<X>` 和类型 `A`、`B`，只有 `A = B`，才能得到 `I<A> <: I<B>`；反过来，如果知道了 `I<A> <: I<B>`，也可推出 `A = B`（内建类型除外：内建的元组类型对其每个元素类型来说，都是协变的；内建的函数类型在其入参类型处是逆变的，在其返回类型处是协变的。）

> **注意：**
>
> `class` 以外的类型实现接口，该类型和该接口之间的子类型关系不能作为协变和逆变的依据。

不型变限制了一些语言的表达能力，但也避免了一些安全问题，例如“协变数组运行时抛异常”的问题。


---

<!-- Content from source_zh_cn/generic/typealias.md -->
# 类型别名

当某个类型的名字比较复杂或者在特定场景中不够直观时，可以选择使用类型别名的方式为此类型设置一个别名。

```cangjie
type I64 = Int64
```

类型别名的定义以关键字 `type` 开头，接着是类型的别名（如上例中的 `I64`），然后是等号 `=`，最后是原类型（即被取别名的类型，如上例中的 `Int64`）。

只能在源文件顶层定义类型别名，并且原类型必须在别名定义处可见。例如，下例中 `Int64` 的别名定义在 `main` 中将报错，`LongNameClassB` 类型在为其定义别名时不可见，同样报错。

<!-- compile.error  -->

```cangjie
main() {
    type I64 = Int64 // Error, type aliases can only be defined at the top level of the source file
}

class LongNameClassA { }
type B = LongNameClassB // Error, type 'LongNameClassB' is not defined
```

一个（或多个）类型别名定义中禁止出现（直接或间接的）循环引用。

<!-- compile.error  -->

```cangjie
type A = (Int64, A) // Error, 'A' refered itself
type B = (Int64, C) // Error, 'B' and 'C' are circularly refered
type C = (B, Int64)
```

类型别名并不会定义一个新的类型，它仅仅是为原类型定义了另外一个名字，它有如下几种使用场景：

1. 作为类型使用，例如：

    <!-- compile -->

    ```cangjie
    type A = B
    class B {}
    var a: A = B() // Use typealias A as type B
    ```

2. 当类型别名实际指向的类型为 class、struct 时，可以作为构造器名称使用：

    <!-- compile -->

    ```cangjie
    type A = B
    class B {}
    func foo() { A() }  // Use type alias A as constructor of B
    ```

3. 当类型别名实际指向的类型为 class、interface、struct 时，可以作为访问内部静态成员变量或函数的类型名：

    <!-- compile -->

    ```cangjie
    type A = B
    class B {
        static var b : Int32 = 0
        static func foo() {}
    }
    func foo() {
        A.foo() // Use A to access static method in class B
        A.b
    }
    ```

4. 当类型别名实际指向的类型为 enum 时，可以作为 enum 声明的构造器的类型名：

    <!-- compile -->

    ```cangjie
    enum TimeUnit {
        Day | Month | Year
    }
    type Time = TimeUnit
    var a = Time.Day  
    var b = Time.Month   // Use type alias Time to access constructors in TimeUnit
    ```

需要注意的是，当前用户自定义的类型别名暂不支持在类型转换表达式中使用，参考如下示例：

<!-- compile.error  -->

```cangjie
type MyInt = Int32
MyInt(0)  // Error, no matching function for operator '()' function call
```

## 泛型别名

类型别名也是可以声明类型形参的，但是不能对其形参使用 `where` 声明约束，对于泛型变元的约束会在后面给出解释。

当一个泛型类型的名称过长时，可以使用类型别名来为其声明一个更短的别名。例如，有一个类型为 `RecordData` ，可以把他用类型别名简写为 `RD` ：

<!-- compile -->

```cangjie
struct RecordData<T> {
    var a: T
    public init(x: T) {
        a = x
    }
}

type RD<T> = RecordData<T>

main(): Int64 {
    var struct1: RD<Int32> = RecordData<Int32>(2)
    return 1
}
```

在使用时就可以用 `RD<Int32>` 来代指 `RecordData<Int32>` 类型。


---

<!-- Content from source_zh_cn/generic/generic_constraint.md -->
# 泛型约束

泛型约束的作用是在 function、class、interface、struct、enum 声明时明确泛型形参所具备的操作与能力。只有声明了这些约束才能调用相应的成员函数。在很多场景下泛型形参是需要加以约束的，以 `id` 函数为例：

<!-- compile -->

```cangjie
func id<T>(a: T) {
    return a
}
```

开发者唯一能做的事情就是将函数形参 `a` 这个值返回，而不能进行 `a + 1`，`println("${a}")` 等操作，因为它可能是一个任意的类型，比如 `(Bool) -> Bool`，这样就无法与整数相加，同样因为是函数类型，也不能通过 `println` 函数来输出在命令行上。而如果这一泛型形参上有了约束，那么就可以做更多操作了。

约束大致分为接口约束与 class 类型约束。在函数或类型的声明体之前，可以使用 `where` 关键字来声明泛型约束。对于声明的泛型形参 `T1, T2`，可以使用 `where T1 <: Interface, T2 <: Class` 这样的方式来声明泛型约束。如果同一个类型变元的多个约束，可以使用 `&` 连接，例如，`where T1 <: Interface1 & Interface2`。

仓颉中的 `println` 函数能接受类型为字符串的参数。如果需要把一个泛型类型的变量转为字符串后打印在命令行上，可以对这个泛型类型变元加以约束，这个约束是 `core` 中定义的 `ToString` 接口，显然它是一个接口约束：

```cangjie
package std.core // `ToString` is defined in core.

public interface ToString {
    func toString(): String
}
```

这样就可以利用这个约束，定义一个名为 `genericPrint` 的函数：

<!-- verify -->

```cangjie
func genericPrint<T>(a: T) where T <: ToString {
    println(a)
}

main() {
    genericPrint<Int64>(10)
}
```

结果为：

```text
10
```

如果 genericPrint 函数的类型实参没有实现 ToString 接口，那么编译器会报错。例如传入一个函数做为参数时：

<!-- compile.error -->

```cangjie
func genericPrint<T>(a: T) where T <: ToString {
    println(a)
}

main() {
    genericPrint<(Int64) -> Int64>({ i => 0 })
}
```

如果对上面的文件进行编译，那么编译器会抛出泛型类型参数不满足约束的错误。因为 `genericPrint` 函数的泛型的类型实参不满足约束 `(Int64) -> Int64 <: ToString`。

除了上述通过接口来表示约束，还可以使用 class 类型来约束一个泛型类型变元。例如：当要声明一个动物园类型 `Zoo<T>`，但是需要这里声明的类型形参 `T` 受到约束，这个约束就是 `T` 需要是动物类型 `Animal` 的子类型， `Animal` 类型中声明了 `run` 成员函数。这里声明两个子类型 `Dog` 与 `Fox` 都实现了 `run` 成员函数，这样在 `Zoo<T>` 的类型中，就可以对于 `animals` 数组列表中存放的动物实例调用 `run` 成员函数：

<!-- verify -->

```cangjie
import std.collection.ArrayList

abstract class Animal {
    public func run(): String
}

class Dog <: Animal {
    public func run(): String {
        return "dog run"
    }
}

class Fox <: Animal {
    public func run(): String {
        return "fox run"
    }
}

class Zoo<T> where T <: Animal {
    var animals: ArrayList<Animal> = ArrayList<Animal>()
    public func addAnimal(a: T) {
        animals.add(a)
    }

    public func allAnimalRuns() {
        for(a in animals) {
            println(a.run())
        }
    }
}

main() {
    var zoo: Zoo<Animal> = Zoo<Animal>()
    zoo.addAnimal(Dog())
    zoo.addAnimal(Fox())
    zoo.allAnimalRuns()
}
```

程序的输出为：

```text
dog run
fox run
```

> **注意：**
>
> 泛型变元的约束只能是具体的 class 类型或 interface，且变元如果存在多个 class 类型的上界时，它们必须在同一继承链路上。


---

<!-- Content from source_zh_cn/extension/extend_overview.md -->
# 扩展概述

扩展可以为在当前 `package` 中可见的类型（除函数、元组、接口）添加新功能。

当不能破坏被扩展类型的封装性，但希望添加额外的功能时，可以使用扩展。

可以添加的功能包括：

- 添加成员函数
- 添加操作符重载函数
- 添加成员属性
- 实现接口

上述具体添加的功能方式可参考如下示例，具体使用语法请参考后续介绍：

<!-- compile -->

```cangjie
interface Foo {
    func printValue(a: Int64): Unit
}

class Boo {
    var boo: Int64 =2
}

extend Boo {
    public prop x: Int64 { // 添加成员属性
        get() {
            123
        }
    }

    func newMember(): Unit {
        println("This is a member function of a new extension.") // 添加成员函数
    }

    public operator func -() {
        println("Overload the operator addition function.") // 添加操作符重载函数
        -x
    }
}

// 接口扩展，实现接口
extend<T> Array<T> <: Foo {
    public func printValue(a: Int64) {
        println("The is ${a}.")
    }
}
```

扩展虽然可以添加额外的功能，但不能变更被扩展类型的封装性，因此扩展不支持以下功能：

1. 扩展不能增加成员变量。
2. 扩展的函数和属性必须拥有实现。
3. 扩展的函数和属性不能使用 `open`、`override`、 `redef`修饰。
4. 扩展不能访问被扩展类型中 `private` 修饰的成员。

根据扩展有没有实现新的接口，扩展可以分为 **直接扩展** 和 **接口扩展** 两种用法。直接扩展即不包含额外接口的扩展；接口扩展即包含接口的扩展，接口扩展可以用来为现有的类型添加新功能并实现接口，增强抽象灵活性。


---

<!-- Content from source_zh_cn/extension/direct_extension.md -->
# 直接扩展

一个简单的扩展语法结构示例如下：

<!-- verify -printSize -->

```cangjie
extend String {
    public func printSize() {
        println("the size is ${this.size}")
    }
}
```

如上例所示，扩展使用 `extend` 关键字声明，其后跟着被扩展的类型 `String` 和扩展的功能。

当为 `String` 扩展了 `printSize` 函数之后，就能在当前 `package` 内对 `String` 的实例访问该函数，就像是 `String` 本身具备该函数。

<!-- verify -printSize -->

```cangjie
main() {
    let a = "123"
    a.printSize() // the size is 3
}
```

编译执行上述代码，输出结果为：

<!-- verify -printSize -->

```text
the size is 3
```

被扩展类型是泛型类型时，有两种扩展语法可以对泛型类型扩展功能。

一种是针对特定泛型实例化类型进行扩展，关键字 `extend` 后允许带一个任意实例化完全的泛型类型。为这些类型增加的功能只有在类型完全匹配时才能使用，且泛型类型的类型实参必须符合泛型类型定义处的约束要求。

例如下面所示的 `Foo<T>`：

<!-- compile.error -->

```cangjie
class Foo<T> where T <: ToString {}

extend Foo<Int64> {} // OK

class Bar {}
extend Foo<Bar> {} // Error, generics type arguments do not match the constraint of 'Class-Foo<Generics-T>'
```

另一种是在 `extend` 后面引入泛型形参的泛型扩展。泛型扩展可以用来扩展未实例化或未完全实例化的泛型类型。在 `extend` 后声明的泛型形参必须被直接或间接使用在被扩展的泛型类型上。为这些类型增加的功能只有在类型和约束完全匹配时才能使用。

例如下面所示的 `MyList<T>`：

<!-- compile.error -->

```cangjie
class MyList<T> {
    public let data: Array<T> = Array<T>()
}

extend<T> MyList<T> {}          // OK
extend<R> MyList<R> {}          // OK
extend<T, R> MyList<(T, R)> {}  // OK
extend MyList {}                // Error, generic type should be used with type argument
extend<T, R> MyList<T> {}       // Error, type parameter 'R' must be used in extended type
extend<T, R> MyList<T, R> {}    // Error, type argument's number does not match type parameter's number
```

对于泛型类型的扩展，可以在其中声明额外的泛型约束，来实现一些有限情况下才能使用的函数。

例如可以定义一个叫 Pair 的类型，这个类型可以方便地存储两个元素（类似于 Tuple）。希望 Pair 类型可以容纳任何类型，因此两个泛型变元不应该有任何约束，这样才能保证 Pair 能容纳所有类型。但同时又希望当两个元素可以判等的时候，让 Pair 也可以判等，这时就可以用扩展来实现这个功能。

如下面的代码所示，使用扩展语法，约束了 T1 和 T2 在支持 equals 的情况下，Pair 也可以实现 equals 函数。

<!-- verify -->

```cangjie
class Pair<T1, T2> {
    var first: T1
    var second: T2
    public init(a: T1, b: T2) {
        first = a
        second = b
    }
}

interface Eq<T> {
    func equals(other: T): Bool
}

extend<T1, T2> Pair<T1, T2> where T1 <: Eq<T1>, T2 <: Eq<T2> {
    public func equals(other: Pair<T1, T2>) {
        first.equals(other.first) && second.equals(other.second)
    }
}

class Foo <: Eq<Foo> {
    public func equals(other: Foo): Bool {
        true
    }
}

main() {
    let a = Pair(Foo(), Foo())
    let b = Pair(Foo(), Foo())
    println(a.equals(b)) // true
}
```

编译执行上述代码，输出结果为：

```text
true
```


---

<!-- Content from source_zh_cn/extension/interface_extension.md -->
# 接口扩展

例如下面的例子，类型 `Array` 本身没有实现接口 `PrintSizeable`，但可以通过扩展的方式为 `Array` 增加额外的成员函数 `printSize`，并实现 `PrintSizeable`。

<!-- verify -PrintSizeable -->

```cangjie
interface PrintSizeable {
    func printSize(): Unit
}

extend<T> Array<T> <: PrintSizeable {
    public func printSize() {
        println("The size is ${this.size}")
    }
}
```

当使用扩展为 `Array` 实现 `PrintSizeable` 之后，就相当于在 `Array` 定义时实现接口 `PrintSizeable`。

因此可以将 `Array` 作为 `PrintSizeable` 的实现类型来使用，代码如下所示。

<!-- verify -PrintSizeable -->

```cangjie
main() {
    let a: PrintSizeable = Array<Int64>()
    a.printSize() // 0
}
```

编译执行上述代码，输出结果为：

<!-- verify -PrintSizeable -->

```text
The size is 0
```

可以在同一个扩展内同时实现多个接口，多个接口之间使用 `&` 分开，接口的顺序没有先后关系。

如下面代码所示，可以在扩展中为 `Foo` 同时实现 `I1`、`I2`、`I3`。

<!-- compile -->

```cangjie
interface I1 {
    func f1(): Unit
}

interface I2 {
    func f2(): Unit
}

interface I3 {
    func f3(): Unit
}

class Foo {}

extend Foo <: I1 & I2 & I3 {
    public func f1(): Unit {}
    public func f2(): Unit {}
    public func f3(): Unit {}
}
```

也可以在接口扩展中声明额外的泛型约束，来实现一些特定约束下才能满足的接口。

例如可以让上面的 `Pair` 类型实现 `Eq` 接口，这样 `Pair` 自己也能成为一个符合 `Eq` 约束的类型，如下代码所示。

<!-- verify -->

```cangjie
class Pair<T1, T2> {
    var first: T1
    var second: T2
    public init(a: T1, b: T2) {
        first = a
        second = b
    }
}

interface Eq<T> {
    func equals(other: T): Bool
}

extend<T1, T2> Pair<T1, T2> <: Eq<Pair<T1, T2>> where T1 <: Eq<T1>, T2 <: Eq<T2> {
    public func equals(other: Pair<T1, T2>) {
        first.equals(other.first) && second.equals(other.second)
    }
}

class Foo <: Eq<Foo> {
    public func equals(other: Foo): Bool {
        true
    }
}

main() {
    let a = Pair(Foo(), Foo())
    let b = Pair(Foo(), Foo())
    println(a.equals(b)) // true
}
```

编译执行上述代码，输出结果为：

```text
true
```

如果被扩展的类型已经包含接口要求的函数或属性，那么在扩展中不需要并且也不能重新实现这些函数或属性。

例如下面的例子，定义了一个新接口 `Sizeable`，目的是获取某个类型的 `size`，而已经知道 `Array` 中包含了这个函数，因此就可以通过扩展让 `Array` 实现 `Sizeable`，而不需要添加额外的函数。

<!-- verify -->

```cangjie
interface Sizeable {
    prop size: Int64
}

extend<T> Array<T> <: Sizeable {}

main() {
    let a: Sizeable = Array<Int64>()
    println(a.size)
}
```

编译执行上述代码，输出结果为：

```text
0
```

当多个接口扩展实现的接口存在继承关系时，扩展将按照“先检查实现父接口的扩展，再检查子接口的扩展”的顺序进行检查。

例如，接口 `I1` 存在一个子接口 `I2`，且 `I1` 中包含一个默认实现，类型 `A` 的两个扩展分别实现了父子接口，根据以上检查顺序，实现 `I1` 的扩展将会优先检查，然后再检查实现 `I2` 的扩展。

<!-- verify -->

```cangjie
interface I1 {
    func foo(): Unit { println("I1 foo") }
}
interface I2 <: I1 {
    func foo(): Unit { println("I2 foo") }
}

class A {}

extend A <: I1 {} // first check
extend A <: I2 {} // second check

main() {
    A().foo()
}
```

编译执行上述代码，输出结果为：

```text
I2 foo
```

以上例子中，当检查实现 `I1` 的扩展时，会从 `I1` 中继承 `foo` 函数。在检查实现 `I2` 的扩展时，由于 `A` 中已存在一个继承的，且签名相同的默认实现 `foo` ，此时 `foo` 将被覆盖。因此，调用 `A` 的 `foo` 函数时，最终指向 `I2`（子接口）中的实现。

如果同一类型的两个接口扩展实现的接口存在继承冲突，导致无法确定检查顺序时，将会报错。

<!-- compile.error -->

```cangjie
interface I1 {}
interface I2 <: I1 {}
interface I3 {}
interface I4 <: I3 {}

class A {}
extend A <: I1 & I4 {} // error: unable to decide which extension happens first
extend A <: I2 & I3 {} // error: unable to decide which extension happens first
```

如果同一类型的两个接口扩展实现的接口不存在继承关系，将会被同时检查。

<!-- compile.error -->

```cangjie
interface I1 {
    func foo() {}
}
interface I2 {
    func foo() {}
}

class A {}
extend A <: I1 {} // Error, multiple default implementations, need to re-implement 'foo' in 'A'
extend A <: I2 {} // Error, multiple default implementations, need to re-implement 'foo' in 'A'
```

> **注意：**
>
> 当类 A 有个泛型基类 `B<T1,...,Tn>`，`B<T1,...,Tn>` 扩展了一个接口 `I<R1,...,Rn>`，`I<R1,...,Rn>` 带有默认实现的实例或者静态函数（比如 foo），该函数没有在 `B<T1,...,Tn>` 及其扩展中被重写，且类 A 没有直接实现接口 `I<R1,...,Rn>` 时，通过类 A 的实例调用函数 foo 时会产生非预期行为。

<!-- compile -->

```cangjie
interface I<N> {
    func foo(n: N): N {n}
}

open class B<T> {}

extend<T> B<T> <: I<T> {}

class A <: B<Int64>{}

main() {
    A().foo(0) // this call triggers unexpected behaviour
}
```


---

<!-- Content from source_zh_cn/extension/access_rules.md -->
# 访问规则

## 扩展的修饰符

扩展本身不能使用修饰符修饰。

例如，下面的例子中对 A 的直接扩展前使用了 `public` 修饰，将编译报错。

<!-- compile.error -->

```cangjie
public class A {}

public extend A {}  // Error, expected no modifier before extend
```

扩展成员可使用的修饰符有：`static`、`public`、`protected`、`internal`、`private`、`mut`。

- 使用 `private` 修饰的成员只能在本扩展内使用，外部不可见。
- 使用 `internal` 修饰的成员可以在当前包及子包（包括子包的子包）内使用，这是默认行为。
- 使用 `protected` 修饰的成员在本模块内可以被访问（受导出规则限制）。当被扩展类型是 class 时，该 class 的子类定义体也能访问。
- 使用 `static` 修饰的成员，只能通过类型名访问，不能通过实例对象访问。
- 对 `struct` 类型的扩展可以定义 `mut` 函数。

<!-- compile -->

```cangjie
package p1

public open class A {}

extend A {
    public func f1() {}
    protected func f2() {}
    private func f3() {}
    static func f4() {}
}

main() {
    A.f4()
    var a = A()
    a.f1()
    a.f2()
}
```

扩展内的成员定义不支持使用 `open`、`override`、`redef` 修饰。

<!-- compile.error -->

```cangjie
class Foo {
    public open func f() {}
    static func h() {}
}

extend Foo {
    public override func f() {} // Error
    public open func g() {} // Error
    redef static func h() {} // Error
}
```

## 扩展的孤儿规则

为一个其他 `package` 的类型实现另一个 `package` 的接口，可能造成理解上的困扰。

为了防止一个类型被意外实现不合适的接口，仓颉不允许定义孤儿扩展，即既不与接口（包含接口继承链上的所有接口）定义在同一个包中，也不与被扩展类型定义在同一个包中的接口扩展。

如下代码所示，不能在 `package c` 中，为 `package a` 里的 `Foo` 实现 `package b` 里的 `Bar`。

只能在 `package a` 或者在 `package b` 中为 `Foo` 实现 `Bar`。

<!-- compile.error -->

```cangjie
// package a
public class Foo {}

// package b
public interface Bar {}

// package c
import a.Foo
import b.Bar

extend Foo <: Bar {} // Error
```

## 扩展的访问和遮盖

扩展的实例成员与类型定义处一样可以使用 `this`，`this` 的功能保持一致。同样也可以省略 `this` 访问成员。扩展的实例成员不能使用 `super`。

<!-- compile -->

```cangjie
class A {
    var v = 0
}

extend A {
    func f() {
        print(this.v) // OK
        print(v) // OK
    }
}
```

扩展不能访问被扩展类型中 `private` 修饰的成员。

<!-- compile.error -->

```cangjie
class A {
    private var v1 = 0
    protected var v2 = 0
}

extend A {
    func f() {
        print(v1) // Error
        print(v2) // OK
    }
}
```

扩展不能遮盖被扩展类型的任何成员。

<!-- compile.error -->

```cangjie
class A {
    func f() {}
}

extend A {
    func f() {} // Error
}
```

扩展也不允许遮盖其他扩展增加的任何成员。

<!-- compile.error -->

```cangjie
class A {}

extend A {
    func f() {}
}

extend A {
    func f() {} // Error
}
```

在同一个包内，对同一类型可以扩展多次，并且在扩展中可以直接调用被扩展类型的其他扩展中非 `private` 修饰的函数。

<!-- compile.error -->

```cangjie
class Foo {}

extend Foo { // OK
    private func f() {}
    func g() {}
}

extend Foo { // OK
    func h() {
        g() // OK
        f() // Error
    }
}
```

扩展泛型类型时，可以使用额外的泛型约束。泛型类型的任意两个扩展之间的可见性规则如下：

- 如果两个扩展的约束相同，则两个扩展相互可见，即两个扩展内可以直接使用对方内的函数或属性；
- 如果两个扩展的约束不同，且两个扩展的约束有包含关系，约束更宽松的扩展对约束更严格的扩展可见，反之，不可见；
- 当两个扩展的约束不同时，且两个约束不存在包含关系，则两个扩展均互相不可见。

示例：假设对同一个类型 `E<X>` 的两个扩展分别为扩展 `1` 和扩展 `2` ，`X` 的约束在扩展 `1` 中比扩展 `2` 中更严格，那么扩展 `1` 中的函数和属性对扩展 `2` 均不可见，反之，扩展 `2` 中的函数和属性对扩展 `1` 可见。

<!-- compile.error -->

```cangjie
open class A {}
class B <: A {}
class E<X> {}

interface I1 {
    func f1(): Unit
}
interface I2 {
    func f2(): Unit
}

extend<X> E<X> <: I1 where X <: B {  // extension 1
    public func f1(): Unit {
        f2() // OK
    }
}

extend<X> E<X> <: I2 where X <: A   { // extension 2
    public func f2(): Unit {
        f1() // Error
    }
}
```

## 扩展的导入导出

扩展也是可以被导入和导出的，但是扩展本身不能使用可见性修饰符修饰，扩展的导出有一套特殊的规则。

对于直接扩展，当扩展与被扩展的类型在同一个包中，扩展是否导出，由被扩展类型与泛型约束（如果有）的访问修饰符同时决定，当所有的泛型约束都是导出类型（修饰符与导出规则，详见[顶层声明的可见性](../package/toplevel_access.md)章节）时，该扩展将被导出。当扩展与被扩展类型不在同一个包中时，该扩展不会导出。

如以下代码所示，`Foo` 是导出的，`f1` 函数所在的扩展由于不导出泛型约束，故该扩展不会被导出；`f2` 和 `f3` 函数所在的扩展的泛型约束均被导出，故该扩展被导出；`f4` 函数所在的扩展包含多个泛型约束，且泛型约束中 `I1` 未被导出，故该扩展不会被导出；`f5` 函数所在的扩展包含多个泛型约束，所有的泛型约束均是导出的，故该扩展会被导出。

```cangjie
// package a.b
package a.b

private interface I1 {}
internal interface I2 {}
protected interface I3 {}

extend Int64 <: I1 & I2 & I3 {}

public class Foo<T> {}
// The extension will not be exported
extend<T> Foo<T> where T <: I1 {
    public func f1() {}
}
// The extension will be exported, and only packages that import both Foo and I2 will be able to access it.
extend<T> Foo<T> where T <: I2 {
    public func f2() {}
}
// The extension will be exported, and only packages that import both Foo and I3 will be able to access it.
extend<T> Foo<T> where T <: I3 {
    public func f3() {}
}
// The extension will not be exported. The I1 with the lowest access level determines the export.
extend<T> Foo<T> where T <: I1 & I2 & I3 {
    public func f4() {}
}
// The extension is exported. Only the package that imports Foo, I2, and I3 can access the extension.
extend<T> Foo<T> where T <: I2 & I3 {
    public func f5() {}
}

// package a.c
package a.c
import a.b.*

main() {
    Foo<Int64>().f1() // Cannot access.
    Foo<Int64>().f2() // Cannot access. Visible only for sub-pkg.
    Foo<Int64>().f3() // OK.
    Foo<Int64>().f4() // Cannot access.
    Foo<Int64>().f5() // Cannot access. Visible only for sub-pkg.
}

// package a.b.d
package a.b.d
import a.b.*

main() {
    Foo<Int64>().f1() // Cannot access.
    Foo<Int64>().f2() // OK.
    Foo<Int64>().f3() // OK.
    Foo<Int64>().f4() // Cannot access.
    Foo<Int64>().f5() // OK.
}
```

对于接口扩展则分为两种情况：

1. 当接口扩展与被扩展类型在相同的 `package` 时，扩展会与被扩展类型以及泛型约束（如果有）一起被导出，不受接口类型的访问级别影响，包外不需要导入接口类型也能访问该扩展的成员。
2. 当接口扩展与被扩展类型在不同的 `package` 时，接口扩展是否导出由接口类型以及泛型约束（如果有）里用到的类型中最小的访问级别决定。其他 `package` 必须导入被扩展类型、相应的接口以及约束用到的类型（如果有），才能访问对应接口包含的扩展成员。

如下代码所示，在包 `a` 中，虽然接口访问修饰符为 `private`，但 `Foo` 的扩展仍然会被导出。

```cangjie
// package a
package a

private interface I0 {}

public class Foo<T> {}

// The extension is exported.
extend<T> Foo<T> <: I0 {}
```

当在其他包中为 `Foo` 类型扩展时，扩展是否导出由实现接口和泛型约束的访问修饰符决定。实现接口至少存在一个导出的接口，且所有的泛型约束均可导出时，该扩展将被导出。

```cangjie
// package b
package b

import a.Foo

private interface I1 {}
internal interface I2 {}
protected interface I3 {}
public interface I4 {}

// The extension will not be exported because I1 is not visible outside the file.
extend<T> Foo<T> <: I1 {}

// The extension is exported.
extend<T> Foo<T> <: I2 {}

// The extension is exported.
extend<T> Foo<T> <: I3 {}

// The extension is exported
extend<T> Foo<T> <: I1 & I2 & I3 {}

// The extension will not be exported. The I1 with the lowest access level determines the export.
extend<T> Foo<T> <: I4 where T <: I1 & I2 & I3 {}

// The extension is exported.
extend<T> Foo<T> <: I4 where T <: I2 & I3 {}

// The extension is exported.
extend<T> Foo<T> <: I4 & I3 where T <: I2 {}
```

特别的，接口扩展导出的成员仅限于接口中包含的成员。

<!-- compile.error -access_rules3 -->
<!-- cfg="-p a --output-type=staticlib" -->

```cangjie
// package a
package a

public class Foo {}
```

<!-- compile.error -access_rules3 -->
<!-- cfg="-p b --output-type=staticlib" -->

```cangjie
// package b
package b

import a.Foo

public interface I1 {
    func f1(): Unit
}

public interface I2 {
    func f2(): Unit
}

extend Foo <: I1 & I2 {
    public func f1(): Unit {}
    public func f2(): Unit {}
    public func f3(): Unit {} // f3 will not be exported
}
```

<!-- compile.error -access_rules3 -->
<!-- cfg="-p c --output-type=staticlib" -->
<!-- cfg="liba.a libb.a" -->

```cangjie
// package c
package c

import a.Foo
import b.I1

main() {
    let x: Foo = Foo()
    x.f1() // OK, because f1 is a member of I1.
    x.f2() // error, I2 is not imported
    x.f3() // error, f3 not found
}
```

与扩展的导出类似，扩展的导入也不需要显式地用 `import` 导入，扩展的导入只需要导入被扩展的类型、接口和泛型约束，就可以导入可访问的所有扩展。

如下面的代码所示，在 `package b` 中，只需要导入 `Foo` 就可以使用 `Foo` 对应的扩展中的函数 `f`。

而对于接口扩展，需要同时导入被扩展的类型、扩展的接口和泛型约束（如果有）才能使用。因此在 `package c` 中，需要同时导入 `Foo` 和 `I` 才能使用对应扩展中的函数 `g`。

<!-- compile -->

```cangjie
// package a
package a
public class Foo {}
extend Foo {
    public func f() {}
}
```

```cangjie
// package b
package b
import a.Foo

public interface I {
    func g(): Unit
}
extend Foo <: I {
    public func g() {
        this.f() // OK
    }
}
```

```cangjie
// package c
package c
import a.Foo
import b.I

func test() {
    let a = Foo()
    a.f() // OK
    a.g() // OK
}
```


---

<!-- Content from source_zh_cn/collections/collection_overview.md -->
# 基础 Collection 类型概述

本章介绍仓颉语言中常用的几种基础 Collection 类型，包括 Array、ArrayList、HashSet 和 HashMap。

可以在不同的场景中选择适合对应业务的类型：

- Array：不需要增加和删除元素，但需要修改元素
- ArrayList：需要频繁对元素增删查改
- HashSet：希望每个元素都是唯一的
- HashMap：希望存储一系列的映射关系

下表是这些类型的基础特性：

| 类型名称        | 元素可变 | 增删元素 | 元素唯一性 | 有序序列 |
| --------------- | -------- | -------- | ---------- | -------------- |
| `Array<T>`      | Y        | N        | N          | Y              |
| `ArrayList<T>`     | Y        | Y        | N          | Y              |
| `HashSet<T>`    | N       | Y        | Y          | N              |
| `HashMap<K, V>` | K: N, V: Y | Y        | K: Y, V: N | N              |


---

<!-- Content from source_zh_cn/collections/collection_arraylist.md -->
# ArrayList

使用 ArrayList 类型需要导入 collection 包：

<!-- run -->

```cangjie
import std.collection.*
```

仓颉使用 `ArrayList<T>` 表示 ArrayList 类型，T 表示 ArrayList 的元素类型，T 可以是任意类型。

ArrayList 具备非常好的扩容能力，适合于需要频繁增加和删除元素的场景。

相比 Array，ArrayList 既可以原地修改元素，也可以原地增加和删除元素。

ArrayList 的可变性是一个非常有用的特征，可以让同一个 ArrayList 实例的所有引用都共享同样的元素，并且对它们统一进行修改。

```cangjie
var a: ArrayList<Int64> = ... // ArrayList whose element type is Int64
var b: ArrayList<String> = ... // ArrayList whose element type is String
```

元素类型不相同的 ArrayList 是不相同的类型，所以它们之间不可以互相赋值。

因此以下例子是不合法的。

```cangjie
b = a // Type mismatch
```

仓颉中可以使用构造函数的方式构造一个指定的 ArrayList。

<!-- run -->

```cangjie
let a = ArrayList<String>() // Created an empty ArrayList whose element type is String
let b = ArrayList<String>(100) // Created an ArrayList whose element type is String, and allocate a space of 100
let c = ArrayList<Int64>([0, 1, 2]) // Created an ArrayList whose element type is Int64, containing elements 0, 1, 2
let d = ArrayList<Int64>(c) // Use another Collection to initialize an ArrayList
let e = ArrayList<String>(2, {x: Int64 => x.toString()}) // Created an ArrayList whose element type is String and size is 2. All elements are initialized by specified rule function
```

## 访问 ArrayList 成员

当需要对 ArrayList 的所有元素进行访问时，可以使用 for-in 循环遍历 ArrayList 的所有元素。

<!-- verify -->

```cangjie
import std.collection.ArrayList

main() {
    let list = ArrayList<Int64>([0, 1, 2])
    for (i in list) {
        println("The element is ${i}")
    }
}
```

编译并执行上面的代码，会输出：

```text
The element is 0
The element is 1
The element is 2
```

当需要知道某个 ArrayList 包含的元素个数时，可以使用 size 属性获得对应信息。

<!-- verify -->

```cangjie
import std.collection.ArrayList

main() {
    let list = ArrayList<Int64>([0, 1, 2])
    if (list.size == 0) {
        println("This is an empty arraylist")
    } else {
        println("The size of arraylist is ${list.size}")
    }
}
```

编译并执行上面的代码，会输出：

```text
The size of arraylist is 3
```

当想访问单个指定位置的元素时，可以使用下标语法访问（下标的类型必须是 Int64）。非空 ArrayList 的第一个元素总是从位置 0 开始的。可以从 0 开始访问 ArrayList 的任意一个元素，直到最后一个位置（ArrayList 的 size - 1）。使用负数或大于等于 size 的索引会触发运行时异常。

```cangjie
let a = list[0] // a == 0
let b = list[1] // b == 1
let c = list[-1] // Runtime exceptions
```

ArrayList 也支持下标中使用 Range 的语法，详见 [Array](../basic_data_type/array.md#array) 章节。

## 修改 ArrayList

可以使用下标语法对某个位置的元素进行修改。

<!-- run -->

```cangjie
let list = ArrayList<Int64>([0, 1, 2])
list[0] = 3
```

ArrayList 是引用类型，ArrayList 在作为表达式使用时不会拷贝副本，同一个 ArrayList 实例的所有引用都会共享同样的数据。

因此对 ArrayList 元素的修改会影响到该实例的所有引用。

<!-- run -->

```cangjie
let list1 = ArrayList<Int64>([0, 1, 2])
let list2 = list1
list2[0] = 3
// list1 contains elements 3, 1, 2
// list2 contains elements 3, 1, 2
```

如果需要将单个元素添加到 ArrayList 的末尾，请使用 add 函数。如果希望同时添加多个元素到末尾，可以使用 `add(all!: Collection<T>)` 函数，这个函数可以接受其他相同元素类型的 Collection 类型，如 Array。Collection 类型详见[基础 Collection 类型概述](collection_overview.md)。

<!-- run -->

```cangjie
import std.collection.ArrayList

main() {
    let list = ArrayList<Int64>()
    list.add(0) // list contains element 0
    list.add(1) // list contains elements 0, 1
    let li = [2, 3]
    list.add(all: li) // list contains elements 0, 1, 2, 3
}
```

可以通过 `add(T, at!: Int64)` 和 `add(all!: Collection<T>, at!: Int64)` 函数将指定的单个元素或相同元素类型的 Collection 值插入到指定索引的位置。该索引处的元素和后面的元素会被挪后以腾出空间。

<!-- run -->

```cangjie
let list = ArrayList<Int64>([0, 1, 2]) // list contains elements 0, 1, 2
list.add(4, at: 1) // list contains elements 0, 4, 1, 2
```

从 ArrayList 中删除元素，可以使用 remove 函数，需要指定删除的索引。该索引处后面的元素会前移以填充空间。

<!-- run -->

```cangjie
let list = ArrayList<String>(["a", "b", "c", "d"]) // list contains the elements "a", "b", "c", "d"
list.remove(at: 1) // Delete the element at subscript 1, now the list contains elements "a", "c", "d"
```

## 增加 ArrayList 的大小

每个 ArrayList 都需要特定数量的内存来保存其内容。当向 ArrayList 添加元素并且该 ArrayList 开始超出其保留容量时，该 ArrayList 会分配更大的内存区域并将其所有元素复制到新内存中。这种增长策略意味着触发重新分配内存的添加操作具有性能成本，但随着 ArrayList 的保留内存变大，它们发生的频率会越来越低。

如果知道大约需要添加多少个元素，可以在添加之前预备足够的内存以避免中间重新分配，这样可以提升性能表现。

<!-- run -->

```cangjie
import std.collection.ArrayList

main() {
    let list = ArrayList<Int64>(100) // Allocate space at once
    for (i in 0..100) {
        list.add(i) // Does not trigger reallocation of space
    }
    list.reserve(100) // Prepare more space
    for (i in 0..100) {
        list.add(i) // Does not trigger reallocation of space
    }
}
```


---

<!-- Content from source_zh_cn/collections/collection_hashset.md -->
# HashSet

使用 HashSet 类型需要导入 collection 包：

<!-- run -->

```cangjie
import std.collection.*
```

可以使用 HashSet 类型来构造只拥有不重复元素的 Collection。

仓颉使用 `HashSet<T>` 表示 HashSet 类型，T 表示 HashSet 的元素类型，T 必须是实现了 Hashable 和 `Equatable<T>` 接口的类型，例如数值或 String。

```cangjie
var a: HashSet<Int64> = ... // HashSet whose element type is Int64
var b: HashSet<String> = ... // HashSet whose element type is String
```

元素类型不相同的 HashSet 是不相同的类型，所以它们之间不可以互相赋值。

因此以下例子是不合法的。

```cangjie
b = a // Type mismatch
```

仓颉中可以使用构造函数的方式构造一个指定的 HashSet。

<!-- run -->

```cangjie
let a = HashSet<String>() // Created an empty HashSet whose element type is String
let b = HashSet<String>(100) // Created a HashSet whose capacity is 100
let c = HashSet<Int64>([0, 1, 2]) // Created a HashSet whose element type is Int64, containing elements 0, 1, 2
let d = HashSet<Int64>(c) // Use another Collection to initialize a HashSet
let e = HashSet<Int64>(10, {x: Int64 => (x * x)}) // Created a HashSet whose element type is Int64 and size is 10. All elements are initialized by specified rule function
```

## 访问 HashSet 成员

当需要对 HashSet 的所有元素进行访问时，可以使用 for-in 循环遍历 HashSet 的所有元素。

需要注意的是，HashSet 并不保证按插入元素的顺序排列，因此遍历的顺序和插入的顺序可能不同。

<!-- verify -->

```cangjie
import std.collection.*

main() {
    let mySet = HashSet<Int64>([0, 1, 2])
    for (i in mySet) {
        println("The element is ${i}")
    }
}
```

编译并执行上面的代码，有可能会输出：

```text
The element is 0
The element is 1
The element is 2
```

当需要知道某个 HashSet 包含的元素个数时，可以使用 size 属性获得对应信息。

<!-- verify -->

```cangjie
import std.collection.*

main() {
    let mySet = HashSet<Int64>([0, 1, 2])
    if (mySet.size == 0) {
        println("This is an empty hashset")
    } else {
        println("The size of hashset is ${mySet.size}")
    }
}
```

编译并执行上面的代码，会输出：

```text
The size of hashset is 3
```

当想判断某个元素是否被包含在某个 HashSet 中时，可以使用 contains 函数。如果该元素存在会返回 true，否则返回 false。

<!-- run -->

```cangjie
let mySet = HashSet<Int64>([0, 1, 2])
let a = mySet.contains(0) // a == true
let b = mySet.contains(-1) // b == false
```

## 修改 HashSet

HashSet 是一种可变的引用类型，HashSet 类型提供了添加元素、删除元素的功能。

HashSet 的可变性是一个非常有用的特征，可以让同一个 HashSet 实例的所有引用都共享同样的元素，并且对它们统一进行修改。

如果需要将单个元素添加到 HashSet 里，请使用 add 函数。如果希望同时添加多个元素，可以使用 `add(all!: Collection<T>)` 函数，这个函数可以接受另一个相同元素类型的 Collection 类型（例如 Array）。当元素不存在时，add 函数会执行添加的操作，当 HashSet 中存在相同元素时，add 函数将不会有效果。

<!-- run -->

```cangjie
let mySet = HashSet<Int64>()
mySet.add(0) // mySet contains elements 0
mySet.add(0) // mySet contains elements 0
mySet.add(1) // mySet contains elements 0, 1
let li = [2, 3]
mySet.add(all: li) // mySet contains elements 0, 1, 2, 3
```

HashSet 是引用类型，HashSet 在作为表达式使用时不会拷贝副本，同一个 HashSet 实例的所有引用都会共享同样的数据。

因此对 HashSet 元素的修改会影响到该实例的所有引用。

<!-- run -->

```cangjie
let set1 = HashSet<Int64>([0, 1, 2])
let set2 = set1
set2.add(3)
// set1 contains elements 0, 1, 2, 3
// set2 contains elements 0, 1, 2, 3
```

从 HashSet 中删除元素，可以使用 remove 函数，需要指定删除的元素。

<!-- run -->

```cangjie
let mySet = HashSet<Int64>([0, 1, 2, 3])
mySet.remove(1) // mySet contains elements 0, 2, 3
```


---

<!-- Content from source_zh_cn/collections/collection_hashmap.md -->
# HashMap

使用 HashMap 类型需要导入 collection 包：

<!-- run -->

```cangjie
import std.collection.*
```

可以使用 HashMap 类型来构造元素为键值对的 Collection。

HashMap 是一种哈希表，提供对其包含的元素的快速访问。表中的每个元素都使用其键作为标识，可以使用键来访问相应的值。

仓颉使用 `HashMap<K, V>` 表示 HashMap 类型，K 表示 HashMap 的键类型，K 必须是实现了 Hashable 和 `Equatable<K>` 接口的类型，例如数值或 String。V 表示 HashMap 的值类型，V 可以是任意类型。

```cangjie
var a: HashMap<Int64, Int64> = ... // HashMap whose key type is Int64 and value type is Int64
var b: HashMap<String, Int64> = ... // HashMap whose key type is String and value type is Int64
```

元素类型不相同的 HashMap 是不相同的类型，所以它们之间不可以互相赋值。

因此以下例子是不合法的。

```cangjie
b = a // Type mismatch
```

仓颉中可以使用构造函数的方式构造一个指定的 HashMap。

<!-- run -->

```cangjie
let a = HashMap<String, Int64>() // Created an empty HashMap whose key type is String and value type is Int64
let b = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)]) // whose key type is String and value type is Int64, containing elements ("a", 0), ("b", 1), ("c", 2)
let c = HashMap<String, Int64>(b) // Use another Collection to initialize a HashMap
let d = HashMap<String, Int64>(10) // Created a HashMap whose key type is String and value type is Int64 and capacity is 10
let e = HashMap<Int64, Int64>(10, {x: Int64 => (x, x * x)}) // Created a HashMap whose key and value type is Int64 and size is 10. All elements are initialized by specified rule function
```

## 访问 HashMap 成员

当需要对 HashMap 的所有元素进行访问时，可以使用 for-in 循环遍历 HashMap 的所有元素。

需要注意的是，HashMap 并不保证按插入元素的顺序排列，因此遍历的顺序和插入的顺序可能不同。

<!-- verify -->

```cangjie
import std.collection.HashMap

main() {
    let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
    for ((k, v) in map) {
        println("The key is ${k}, the value is ${v}")
    }
}
```

编译并执行上面的代码，有可能会输出：

```text
The key is a, the value is 0
The key is b, the value is 1
The key is c, the value is 2
```

当需要知道某个 HashMap 包含的元素个数时，可以使用 size 属性获得对应信息。

<!-- verify -->

```cangjie
import std.collection.HashMap

main() {
    let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
    if (map.size == 0) {
        println("This is an empty hashmap")
    } else {
        println("The size of hashmap is ${map.size}")
    }
}
```

编译并执行上面的代码，会输出：

```text
The size of hashmap is 3
```

当想判断 HashMap 中是否包含某个键时，可以使用 contains 函数。如果该键存在会返回 true，否则返回 false。

<!-- run -->

```cangjie
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
let a = map.contains("a") // a == true
let b = map.contains("d") // b == false
```

当想访问指定键对应的元素时，可以使用下标语法访问（下标的类型必须是键类型）。使用不存在的键作为索引会触发运行时异常。

```cangjie
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
let a = map["a"] // a == 0
let b = map["b"] // b == 1
let c = map["d"] // Runtime exceptions
```

## 修改 HashMap

HashMap 是一种可变的引用类型，HashMap 类型提供了修改元素、添加元素、删除元素的功能。

HashMap 的可变性是一个非常有用的特征，可以让同一个 HashMap 实例的所有引用都共享同样的元素，并且对它们统一进行修改。

可以使用下标语法对某个键对应的值进行修改。

<!-- run -->

```cangjie
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
map["a"] = 3
```

HashMap 是引用类型，HashMap 在作为表达式使用时不会拷贝副本，同一个 HashMap 实例的所有引用都会共享同样的数据。

因此对 HashMap 元素的修改会影响到该实例的所有引用。

<!-- run -->

```cangjie
let map1 = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
let map2 = map1
map2["a"] = 3
// map1 contains the elements ("a", 3), ("b", 1), ("c", 2)
// map2 contains the elements ("a", 3), ("b", 1), ("c", 2)
```

如果需要将单个键值对添加到 HashMap 里，请使用 add 函数。如果希望同时添加多个键值对，可以使用 `add(all!: Collection<(K, V)>)` 函数。当键不存在时，add 函数会执行添加的操作，当键存在时，add 函数会将新的值覆盖旧的值。

<!-- run -->

```cangjie
let map = HashMap<String, Int64>()
map.add("a", 0) // map contains the element ("a", 0)
map.add("b", 1) // map contains the elements ("a", 0), ("b", 1)
let map2 = HashMap<String, Int64>([("c", 2), ("d", 3)])
map.add(all: map2) // map contains the elements ("a", 0), ("b", 1), ("c", 2), ("d", 3)
```

除了使用 add 函数以外，也可以使用赋值的方式直接将新的键值对添加到 HashMap。

<!-- run -->

```cangjie
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
map["d"] = 3 // map contains the elements ("a", 0), ("b", 1), ("c", 2), ("d", 3)
```

从 HashMap 中删除元素，可以使用 remove 函数，需要指定删除的键。

<!-- run -->

```cangjie
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2), ("d", 3)])
map.remove("d") // map contains the elements ("a", 0), ("b", 1), ("c", 2)
```


---

<!-- Content from source_zh_cn/collections/collection_iterable_collections.md -->
# Iterable 和 Collections

前面已经了解过 Range、Array、ArrayList，它们都可以使用 for-in 进行遍历操作。对于开发者自定义的类型，也能实现类似的遍历操作。

Range、Array、ArrayList 都是通过 Iterable 来支持 for-in 语法的。

Iterable 是如下形式（只展示了核心代码）的一个内置 interface。

```cangjie
interface Iterable<T> {
    func iterator(): Iterator<T>
    ...
}
```

iterator 函数要求返回的 Iterator 类型是如下形式（只展示了核心代码）的另一个内置 interface。

```cangjie
interface Iterator<T> <: Iterable<T> {
    mut func next(): Option<T>
    ...
}
```

可以使用 for-in 语法来遍历任何一个实现了 Iterable 接口类型的实例。

假设有这样一段 for-in 代码，如下所示。

<!-- run -->

```cangjie
let list = [1, 2, 3]
for (i in list) {
    println(i)
}
```

它等价于如下形式的 while 代码。

<!-- run -->

```cangjie
let list = [1, 2, 3]
var it = list.iterator()
while (true) {
    match (it.next()) {
        case Some(i) => println(i)
        case None => break
    }
}
```

另外一种常见的遍历 Iterable 类型的方法是在 while 表达式的条件中使用模式匹配，比如上面 while 代码的另一种等价写法是：

<!-- run -->

```cangjie
let list = [1, 2, 3]
var it = list.iterator()
while (let Some(i) <- it.next()) {
    println(i)
}
```

Array、ArrayList、HashSet、HashMap 类型都实现了 Iterable，因此可以将其用在 for-in 或者 while 中。


---

<!-- Content from source_zh_cn/package/package_overview.md -->
# 包的概述

随着项目规模的不断扩大，仅在一个超大文件中管理源代码会变得十分困难。这时可以将源代码根据功能进行分组，并将不同功能的代码分开管理，每组独立管理的代码会生成一个输出文件。在使用时，通过导入对应的输出文件使用相应的功能，或者通过不同功能的交互与组合实现更加复杂的特性，使得项目管理更加高效。

在仓颉编程语言中，包是**编译的最小单元**，每个包可以单独输出 AST 文件、静态库文件、动态库文件等产物。每个包有自己的名字空间，在同一个包内不允许有同名的顶层定义或声明（函数重载除外）。一个包中可以包含多个源文件。

模块是若干包的集合，是第三方开发者**发布的最小单元**。一个模块的程序入口只能在其根目录下，它的顶层最多只能有一个作为程序入口的 `main` ，该 `main` 没有参数或参数类型为 `Array<String>`，返回类型为整数类型或 `Unit` 类型。


---

<!-- Content from source_zh_cn/package/package_name.md -->
# 包的声明

在仓颉编程语言中，包声明以关键字 `package` 开头，后接 root 包至当前包由 `.` 分隔路径上所有包的包名。包名必须是合法的普通标识符（不含原始标识符）。例如：

```cangjie
package pkg1      // root 包 pkg1
package pkg1.sub1 // root 包 pkg1 的子包 sub1
```

> **注意：**
>
> 当前 Windows 平台版本，包名暂不支持使用 Unicode 字符，包名必须是一个仅含 ASCII 字符的合法的普通标识符。

包声明必须在源文件的非空非注释的首行，且同一个包中的不同源文件的包声明必须保持一致。

<!-- compile.error -->
<!-- cfg="-p test --output-type=staticlib" -->

```cangjie
// file 1
// Comments are accepted
package test
// declarations...

// file 2
let a = 1 // Error, package declaration must appear first in a file
package test
// declarations...
```

仓颉的包名需反映当前源文件相对于项目源码根目录 `src` 的路径，并将其中的路径分隔符替换为小数点。例如包的源代码位于 `src/directory_0/directory_1` 下，root 包名为 `pkg` 则其源代码中的包声明应为 `package pkg.directory_0.directory_1`。

需要注意的是：

- 包所在的文件夹名必须与包名一致。
- 源码根目录默认名为 `src`。
- 源码根目录下的包可以没有包声明，此时编译器将默认为其指定包名 `default`。

假设源代码目录结构如下：

```text
// The directory structure is as follows:
src
`-- directory_0
    |-- directory_1
    |    |-- a.cj
    |    `-- b.cj
    `-- c.cj
`-- main.cj
```

则 `a.cj`、`b.cj`、`c.cj`、`main.cj` 中的包声明可以为:

```cangjie
// a.cj
// in file a.cj, the declared package name must correspond to relative path directory_0/directory_1.

package default.directory_0.directory_1
```

```cangjie
// b.cj
// in file b.cj, the declared package name must correspond to relative path directory_0/directory_1.

package default.directory_0.directory_1
```

```cangjie
// c.cj
// in file c.cj, the declared package name must correspond to relative path directory_0.

package default.directory_0
```

```cangjie
// main.cj
// file main.cj is in the module root directory and may omit package declaration.

main(): Int64 {
    return 0
}
```

另外，包声明不能引起命名冲突：子包不能和当前包的顶层声明同名。

以下是一些错误示例：

```cangjie
// a.cj
package a
public class B { // Error, 'B' is conflicted with sub-package 'a.B'
    public static func f() {}
}
```

<!-- compile.error -->
<!-- cfg="-p a/B --output-type=staticlib" -->

```cangjie
// b.cj
package a.B
public func f {}
```

<!-- compile.error -->
<!-- cfg="liba.a liba.B.a" -->

```cangjie
// main.cj
import a.B // ambiguous use of 'a.B'

main() {
    a.B.f()
}
```


---

<!-- Content from source_zh_cn/package/toplevel_access.md -->
# 顶层声明的可见性

仓颉编程语言中，可以使用访问修饰符来控制对类型、变量、函数等顶层声明的可见性。仓颉语言有 4 种访问修饰符：`private`、`internal`、`protected`、`public`，在修饰顶层元素时不同访问修饰符的语义如下：

- `private` 表示仅当前文件内可见。不同的文件无法访问这类成员。
- `internal` 表示仅当前包及子包（包括子包的子包）内可见。同一个包内可以不导入就访问这类成员，当前包的子包（包括子包的子包）内可以通过导入来访问这类成员。
- `protected` 表示仅当前模块内可见。同一个包的文件可以不导入就访问这类成员，不同包但是在同一个模块内的其他包可以通过导入访问这些成员，不同模块的包无法访问这些成员。
- `public` 表示模块内外均可见。同一个包的文件可以不导入就访问这类成员，其他包可以通过导入访问这些成员。

| 修饰符         | 文件 | 包及子包 | 模块 | 所有包 |
|-------------|------|----------|------|--------|
| `private`   | Y    | N        | N    | N      |
| `internal`  | Y    | Y        | N    | N      |
| `protected` | Y    | Y        | Y    | N      |
| `public`    | Y    | Y        | Y    | Y      |

不同顶层声明支持的访问修饰符和默认修饰符（默认修饰符是指在省略情况下的修饰符语义，这些默认修饰符也允许显式写出）规定如下：

- `package` 支持使用 `internal`、`protected`、`public`，默认修饰符为 `public`。
- `import` 支持使用全部访问修饰符，默认修饰符为 `private`。
- 其他顶层声明支持使用全部访问修饰符，默认修饰符为 `internal`。

<!-- compile -->

```cangjie
package a

private func f1() { 1 }   // f1 仅在当前文件内可见
func f2() { 2 }           // f2 仅当前包及子包内可见
protected func f3() { 3 } // f3 仅当前模块内可见
public func f4() { 4 }    // f4 当前模块内外均可见
```

仓颉的访问级别排序为 `public > protected > internal > private`。一个声明的访问修饰符不得高于该声明中用到的类型的访问修饰符的级别，参考如下示例：

- 函数声明中的参数与返回值

    <!-- compile.error -->

    ```cangjie
    // a.cj
    package a
    class C {}
    public func f1(a1: C) // Error, public declaration f1 cannot use internal type C.
    {
        return 0
    }
    public func f2(a1: Int8): C // Error, public declaration f2 cannot use internal type C.
    {
        return C()
    }
    public func f3 (a1: Int8) // Error, public declaration f3 cannot use internal type C.
    {
        return C()
    }
    ```

- 变量声明

    <!-- compile.error -->

    ```cangjie
    // a.cj
    package a
    class C {}
    public let v1: C = C() // Error, public declaration v1 cannot use internal type C.
    public let v2 = C() // Error, public declaration v2 cannot use internal type C.
    ```

- 泛型类型的类型实参

    <!-- compile.error -->

    ```cangjie
    // a.cj
    package a
    public class C1<T> {}
    class C2 {}
    public let v1 = C1<C2>() // Error, public declaration v1 cannot use internal type C2.
    ```

- `where` 约束中的类型上界

    <!-- compile.error -->

    ```cangjie
    // a.cj
    package a
    interface I {}
    public class B<T> where T <: I {}  // Error, public declaration B cannot use internal type I.
    ```

值得注意的是：

- `public` 修饰的声明在其初始化表达式或者函数体里面可以使用本包可见的任意类型，包括被 `public` 修饰的类型和不被 `public` 修饰的类型。

    <!-- compile -->

    ```cangjie
    // a.cj
    package a
    class C1 {}
    func f1(a1: C1)
    {
      return 0
    }
    public func f2(a1: Int8) // OK.
    {
      var v1 = C1()
      return 0
    }
    public let v1 = f1(C1()) // OK.
    public class C2 // OK.
    {
      var v2 = C1()
    }
    ```

- `public` 修饰的顶层声明能使用匿名函数，或者任意顶层函数，包括被 `public` 修饰的类型和不被 `public` 修饰的顶层函数。

    <!-- compile -toplevel-->

    ```cangjie
    public var t1: () -> Unit = { => } // OK.
    func f1(): Unit {}
    public let t2 = f1 // OK.

    public func f2() // OK.
    {
      return f1
    }
    ```

- 内置类型诸如 `Rune` 和 `Int64` 等默认的修饰符是 `public`。

    <!-- compile -toplevel-->

    ```cangjie
    var num = 5
    public var t3 = num // OK.
    ```


---

<!-- Content from source_zh_cn/package/import.md -->
# 包的导入

## 使用 `import` 语句导入其他包中的声明或定义

在仓颉编程语言中，可以通过 `import fullPackageName.itemName` 的语法导入其他包中的一个顶层声明或定义，`fullPackageName` 为完整路径包名，`itemName` 为声明的名字。导入语句在源文件中的位置必须在包声明之后，其他声明或定义之前。例如：

```cangjie
package a
import std.math.*
import package1.foo
import {package1.foo, package2.bar}
```

如果要导入的多个 `itemName` 同属于一个 `fullPackageName`，可以使用 `import fullPackageName.{itemName[, itemName]*}` 语法，例如：

```cangjie
import package1.{foo, bar, fuzz}
```

这等价于：

```cangjie
import package1.foo
import package1.bar
import package1.fuzz
```

除了通过 `import fullPackagename.itemName` 语法导入一个特定的顶层声明或定义外，还可以使用 `import packageName.*` 语法将 `packageName` 包中所有可见的顶层声明或定义全部导入。例如：

```cangjie
import package1.*
import {package1.*, package2.*}
```

需要注意：

- 导入的成员的作用域级别低于当前包声明的成员。
- 当已导出的包的模块名或者包名被篡改，使其与导出时指定的模块名或包名不一致，在导入时会报错。
- 只允许导入当前文件可见的顶层声明或定义，导入不可见的声明或定义将会在导入处报错。
- 禁止通过 `import` 导入当前源文件所在包的声明或定义。
- 禁止包间的循环依赖导入，如果包之间存在循环依赖，编译器会报错。

示例如下：

```cangjie
// pkga/a.cj
package pkga    // Error, packages pkga pkgb are in circular dependencies.
import pkgb.*

class C {}
public struct R {}

// pkgb/b.cj
package pkgb

import pkga.*

// pkgc/c1.cj
package pkgc

import pkga.C // Error, 'C' is not accessible in package 'pkga'.
import pkga.R // OK, R is an external top-level declaration of package pkga.
import pkgc.f1 // Error, package 'pkgc' should not import itself.

public func f1() {}

// pkgc/c2.cj
package pkgc

func f2() {
    /* OK, the imported declaration is visible to all source files of the same package
     * and accessing import declaration by its name is supported.
     */
    R()

    // OK, accessing imported declaration by fully qualified name is supported.
    pkga.R()

    // OK, the declaration of current package can be accessed directly.
    f1()

    // OK, accessing declaration of current package by fully qualified name is supported.
    pkgc.f1()
}
```

在仓颉编程语言中，导入的声明或定义如果和当前包中的顶层声明或定义重名且不构成函数重载，则导入的声明和定义会被遮盖；导入的声明或定义如果和当前包中的顶层声明或定义重名且构成函数重载，函数调用时将会根据函数重载的规则进行函数决议。

```cangjie
// pkga/a.cj
package pkga

public struct R {}            // R1
public func f(a: Int32) {}    // f1
public func f(a: Bool) {} // f2

// pkgb/b.cj
package pkgb
import pkga.*

func f(a: Int32) {}         // f3
struct R {}                 // R2

func bar() {
    R()     // OK, R2 shadows R1.
    f(1)    // OK, invoke f3 in current package.
    f(true) // OK, invoke f2 in the imported package
}
```

## 隐式导入 core 包

诸如 `String`、`Range` 等类型能直接使用，并不是因为这些类型是内置类型，而是因为编译器会自动为源码隐式的导入 `core` 包中所有的 `public` 修饰的声明。

## 使用 `import as` 对导入的名字重命名

不同包的名字空间是分隔的，因此在不同的包之间可能存在同名的顶层声明。在导入不同包的同名顶层声明时，支持使用 `import packageName.name as newName` 的方式进行重命名来避免冲突。没有名字冲突的情况下仍然可以通过 `import as` 来重命名导入的内容。`import as` 具有如下规则：

- 使用 `import as` 对导入的声明进行重命名后，当前包只能使用重命名后的新名字，原名无法使用。
- 如果重命名后的名字与当前包顶层作用域的其他名字存在冲突，且这些名字对应的声明均为函数类型，则参与函数重载，否则报重定义的错误。
- 支持 `import pkg as newPkgName` 的形式对包名进行重命名，以解决不同模块中同名包的命名冲突问题。
    <!-- compile.error -import3-->
    <!-- cfg="-p p1 --output-type=staticlib" -->

    ```cangjie
    // a.cj
    package p1
    public func f1() {}
    ```

    <!-- compile.error -import3-->
    <!-- cfg="-p p2 --output-type=staticlib" -->

    ```cangjie
    // d.cj
    package p2
    public func f3() {}
    ```

    <!-- compile.error -import3-->
    <!-- cfg="-p p1 --output-type=staticlib" -->

    ```cangjie
    // b.cj
    package p1
    public func f2() {}
    ```

    <!-- compile.error -import3-->
    <!-- cfg="-p pkgc --output-type=staticlib" -->

    ```cangjie
    // c.cj
    package pkgc
    public func f1() {}
    ```

    <!-- compile.error -import3-->
    <!-- cfg="libp1.a libpkgc.a libp1.a" -->

    ```cangjie
    // main.cj
    import p1 as A
    import p1 as B
    import p2.f3 as f  // OK
    import pkgc.f1 as a
    import pkgc.f1 as b // OK

    func f(a: Int32) {}

    main() {
        A.f1()  // OK, package name conflict is resolved by renaming package name.
        B.f2()  // OK, package name conflict is resolved by renaming package name.
        p1.f1() // Error, the original package name cannot be used.
        a()     // OK.
        b()     // OK.
        pkgc.f1()    // Error, the original name cannot be used.
    }
    ```

- 如果没有对导入的存在冲突的名字进行重命名，在 `import` 语句处不报错；在使用处，会因为无法导入唯一的名字而报错。这种情况可以通过 `import as` 定义别名或者 `import fullPackageName` 导入包作为命名空间。

    ```cangjie
    // a.cj
    package p1
    public class C {}

    // b.cj
    package p2
    public class C {}

    // main1.cj
    package pkga
    import p1.C
    import p2.C

    main() {
        let _ = C() // Error
    }

    // main2.cj
    package pkgb
    import p1.C as C1
    import p2.C as C2

    main() {
        let _ = C1() // OK
        let _ = C2() // OK
    }

    // main3.cj
    package pkgc
    import p1
    import p2

    main() {
        let _ = p1.C() // OK
        let _ = p2.C() // OK
    }
    ```

## 重导出一个导入的名字

在功能繁多的大型项目的开发过程中，这样的场景是非常常见的：包 `p2` 大量地使用从包 `p1` 中导入的声明，当包 `p3` 导入包 `p2` 并使用其中的功能时，`p1` 中的声明同样需要对包 `p3` 可见。如果要求包 `p3` 自行导入 `p2` 中使用到的 `p1` 中的声明，这个过程将过于繁琐。因此希望能够在 `p2` 被导入时一并导入 `p2` 使用到的 `p1` 中的声明。

在仓颉编程语言中，`import` 可以被 `private`、`internal`、`protected`、`public` 访问修饰符修饰。其中，被 `public`、`protected` 或者 `internal` 修饰的 `import` 可以把导入的成员重导出（如果这些导入的成员没有因为名称冲突或者被遮盖导致在本包中不可用）。其他包可以根据可见性直接导入并使用本包中用重导出的内容，无需从原包中导入这些内容。

- `private import` 表示导入的内容仅当前文件内可访问，`private` 是 `import` 的默认修饰符，不写访问修饰符的 `import` 等价于 `private import`。
- `internal import` 表示导入的内容在当前包及其子包（包括子包的子包）均可访问。非当前包访问需要显式 `import`。
- `protected import` 表示导入的内容在当前 module 内都可访问。非当前包访问需要显式 `import`。
- `public import` 表示导入的内容外部都可访问。非当前包访问需要显式 `import`。

在下面的例子中，`b` 是 `a` 的子包，在 `a` 中通过 `public import` 重导出了 `b` 中定义的函数 `f`。

```cangjie
package a
public import a.b.f

public let x = 0
```

```cangjie
internal package a.b

public func f() { 0 }
```

```cangjie
import a.f  // OK
let _ = f() // OK
```

需要注意的是，包不可以被重导出：如果被 `import` 导入的是包，那么该 `import` 不允许被 `public`、`protected` 或者 `internal` 修饰。

<!-- compile.error -->

```cangjie
public import a.b // Error, cannot re-export package
```


---

<!-- Content from source_zh_cn/package/entry.md -->
# 程序入口

仓颉程序入口为 `main`，源文件根目录下的包的顶层最多只能有一个 `main`。

如果模块采用生成可执行文件的编译方式，编译器只在源文件根目录下的顶层查找 `main`。如果没有找到，编译器将会报错；如果找到 `main`，编译器会进一步对其参数和返回值类型进行检查。需要注意的是，`main` 不可被访问修饰符修饰，当一个包被导入时，包中定义的 `main` 不会被导入。

作为程序入口的 `main` 可以没有参数或参数类型为 `Array<String>`，返回值类型为 `Unit` 或整数类型。

没有参数的 `main`：

<!-- run -->

```cangjie
// main.cj
main(): Int64 { // OK.
    return 0
}
```

参数类型为 `Array<String>` 的 `main`：

<!-- run -->

```cangjie
// main.cj
main(args: Array<String>): Unit { // OK.
    for (arg in args) {
        println(arg)
    }
}
```

使用 `cjc main.cj` 编译完成后，通过命令行执行：`./main Hello, World`，将会得到如下输出：

```text
Hello,
World
```

以下是一些错误示例：

<!-- compile.error  -->

```cangjie
// main.cj
main(): String { // Error, return type of 'main' is not 'Integer' or 'Unit'.
    return ""
}
```

<!-- compile.error  -->

```cangjie
// main.cj
main(args: Array<Int8>): Int64 { // Error, 'main' cannot be defined with parameter whose type is not Array<String>.
    return 0
}
```

<!-- compile.error  -->

```cangjie
// main.cj
// Error, multiple 'main's are found in source files.
main(args: Array<String>): Int32 {
    return 0
}

main(): Int8 {
    return 0
}
```


---

<!-- Content from source_zh_cn/error_handle/exception_overview.md -->
# 定义异常

异常是一类特殊的可以被程序员捕获并处理的错误，是程序执行时出现的一系列不正常行为的统称。例如，数组越界、除零错误、计算溢出、非法输入等。为了保证系统的正确性和健壮性，很多软件系统中都包含大量的代码用于错误检测和错误处理。

异常不属于程序的正常功能，一旦发生异常，要求程序必须立即处理，即将程序的控制权从正常功能的执行处转移至处理异常的部分。仓颉编程语言提供了异常处理机制，用于处理程序运行时可能出现的各种异常情况。

在仓颉语言中，异常类包括 `Error` 和 `Exception`：

- `Error` 类描述仓颉语言运行时，系统内部错误和资源耗尽错误。应用程序不应该抛出这种类型错误，如果出现内部错误，只能通知给用户，尽量安全终止程序。
- `Exception` 类描述的是程序运行时的逻辑错误或者 IO 错误导致的异常，例如数组越界或者试图打开一个不存在的文件等，这类异常需要在程序中捕获处理。

开发者不可以通过继承仓颉语言内置的 Error 或其子类来自定义异常，但是可以继承内置的 Exception 或其子类来自定义异常，例如：

<!-- compile -->

```cangjie
open class FatherException <: Exception {
    public init() {
        super("This is FatherException.")
    }
    public init(message: String) {
        super(message)
    }
    public open override func getClassName(): String {
        "FatherException"
    }
}

class ChildException <: FatherException {
    public init() {
        super("This is ChildException.")
    }
    public open override func getClassName(): String {
        "ChildException"
    }
}
```

下表展示了 `Exception` 的主要函数及其说明：

| 函数种类 | 函数及说明                                                                     |
| :------- |:--------------------------------------------------------------------------|
| 构造函数 | `init()` 默认构造函数。                                                          |
| 构造函数 | `init(message: String)`  可以设置异常消息的构造函数。                                   |
| 成员属性 | `open prop message: String`  返回发生异常的详细信息。该消息在异常类构造函数中初始化，默认为空字符串。          |
| 成员函数 | `open func toString(): String`  返回异常类型名以及异常的详细信息，其中，异常的详细信息会默认调用 message。 |
| 成员函数 | `func getClassName(): String`  返回用户定义的类名，子类需要重写该方法以返回子类的名称。               |
| 成员函数 | `func printStackTrace(): Unit` 打印堆栈信息至标准错误流。                              |

下表展示了 `Error` 的主要函数及其说明：

| 函数种类 | 函数及说明                                                   |
| :------- | :----------------------------------------------------------- |
| 成员属性 | `open prop message: String`  返回发生错误的详细信息。该消息在错误发生时，内部初始化，默认为空字符串。 |
| 成员函数 | `open func toString(): String`  返回错误类型名以及错误的详细信息，其中，错误的详细信息会默认调用 message。 |
| 成员函数 | `func printStackTrace(): Unit` 打印堆栈信息至标准错误流。    |


---

<!-- Content from source_zh_cn/error_handle/handle.md -->
# throw 和处理异常

上文介绍了如何自定义异常，接下来学习如何抛出和处理异常。

- 由于异常是 `class` 类型，只需要按 class 对象的构建方式去创建异常即可。如表达式 `FatherException()` 即创建了一个类型为 `FatherException` 的异常。
- 仓颉语言提供 `throw` 关键字，用于抛出异常。用 `throw` 来抛出异常时，`throw` 之后的表达式必须是 `Exception` 的子类型（同为异常的 `Error` 不可以手动 `throw` ），如 `throw ArithmeticException("I am an Exception!")` （被执行到时）会抛出一个算术运算异常。
- `throw` 关键字抛出的异常需要被捕获处理。若异常没有被捕获，则由系统调用默认的异常处理函数。

异常处理由 `try` 表达式完成，可分为：

- 不涉及资源自动管理的普通 try 表达式。
- 会进行资源自动管理 try-with-resources 表达式。

## 普通 try 表达式

普通 try 表达式包括三个部分：try 块，catch 块和 finally 块。

- try 块，以关键字 `try` 开始，后面紧跟一个由表达式与声明组成的块（用一对花括号括起来，定义了新的局部作用域，可以包含任意表达式和声明，后简称“块”），try 后面的块内可以抛出异常，并被紧随的 catch 块所捕获并处理（如果不存在 catch 块或未被捕获，则在执行完 finally 块后，该异常继续被抛出）。

- catch 块，一个普通 try 表达式可以包含零个或多个 catch 块（当没有 catch 块时必须有 finally 块）。每个 catch 块以关键字 `catch` 开头，后跟一条 `catchPattern` 和一个块，`catchPattern` 通过模式匹配的方式匹配待捕获的异常。一旦匹配成功，则交由其后跟随的块进行处理，并且忽略它后面的其他 catch 块。当某个 catch 块可捕获的异常类型均可被定义在它前面的某个 catch 块所捕获时，会在此 catch 块处报“catch 块不可达”的 warning。

- finally 块，以关键字 `finally` 开始，后面紧跟一个块。原则上，finally 块中主要实现一些“善后”的工作，如释放资源等，且要尽量避免在 finally 块中再抛异常。并且无论异常是否发生（即无论 try 块中是否抛出异常），finally 块内的内容都会被执行（若异常未被处理，执行完 finally 块后，继续向外抛出异常）。一个 try 表达式在包含 catch 块时可以不包含 finally 块，否则必须包含 finally 块。

`try` 后面紧跟的块以及每个 `catch` 块的作用域互相独立。

下面是一个只有 try 块和 catch 块的简单示例：

<!-- verify -->

```cangjie
main() {
    try {
        throw NegativeArraySizeException("I am an Exception!")
    } catch (e: NegativeArraySizeException) {
        println(e)
        println("NegativeArraySizeException is caught!")
    }
    println("This will also be printed!")
}
```

执行结果为：

```text
NegativeArraySizeException: I am an Exception!
NegativeArraySizeException is caught!
This will also be printed!
```

`catchPattern` 中引入的变量作用域级别与 `catch` 后面的块中变量作用域级别相同，在 catch 块中再次引入相同名字会触发重定义错误。例如：

<!-- compile.error -->

```cangjie
main() {
    try {
        throw NegativeArraySizeException("I am an Exception!")
    } catch (e: NegativeArraySizeException) {
        println(e)
        let e = 0 // Error, redefinition
        println(e)
        println("NegativeArraySizeException is caught!")
    }
    println("This will also be printed!")
}
```

下面是带有 finally 块的 try 表达式的简单示例：

<!-- verify -->

```cangjie
main() {
    try {
        throw NegativeArraySizeException("NegativeArraySizeException")
    } catch (e: NegativeArraySizeException) {
        println("Exception info: ${e}.")
    } finally {
        println("The finally block is executed.")
    }
}
```

执行结果为：

```text
Exception info: NegativeArraySizeException: NegativeArraySizeException.
The finally block is executed.
```

try 表达式可以出现在任何允许使用表达式的地方。try 表达式的类型的确定方式，与 `if`、`match` 表达式等多分支语法结构的类型的确定方式相似，为 finally 分支除外的所有分支的类型的最小公共父类型。例如下面代码中的 try 表达式和变量 `x` 的类型均为 E 和 D 的最小公共父类型 D；finally 分支中的 `C()` 并不参与公共父类型的计算（若参与，则最小公共父类型会变为 `C`）。

另外，当 `try` 表达式的值没有被使用时，其类型为 `Unit`，不要求各分支的类型有最小公共父类型。

<!-- compile -->

```cangjie
open class C { }
open class D <: C { }
class E <: D { }
main () {
    let x = try {
        E()
    } catch (e: Exception) {
        D()
    } finally {
        C()
    }
    0
}
```

## try-with-resources 表达式

try-with-resources 表达式主要是为了自动释放非内存资源。不同于普通 try 表达式，try-with-resources 表达式中的 catch 块和 finally 块均是可选的，并且 try 关键字其后的块之间可以插入一个或者多个 `ResourceSpecification` 用来申请一系列的资源（`ResourceSpecification` 并不会影响整个 try 表达式的类型）。这里所讲的资源对应到语言层面即指对象，因此 `ResourceSpecification` 其实就是实例化一系列的对象（多个实例化之间使用“,”分隔）。使用 try-with-resources 表达式的例子如下所示：

<!-- compile -->

```cangjie
class Worker <: Resource {
    var hasTools: Bool = false
    let name: String

    public init(name: String) {
        this.name = name
    }
    public func getTools() {
        println("${name} picks up tools from the warehouse.")
        hasTools = true
    }

    public func work() {
        if (hasTools) {
            println("${name} does some work with tools.")
        } else {
            println("${name} doesn't have tools, does nothing.")
        }
    }

    public func isClosed(): Bool {
        if (hasTools) {
            println("${name} hasn't returned the tool.")
            false
        } else {
            println("${name} has no tools")
            true
        }
    }
    public func close(): Unit {
        println("${name} returns the tools to the warehouse.")
        hasTools = false
    }
}

main() {
    try (r = Worker("Tom")) {
        r.getTools()
        r.work()
    }
    try (r = Worker("Bob")) {
        r.work()
    }
    try (r = Worker("Jack")) {
        r.getTools()
        throw Exception("Jack left, because of an emergency.")
    }
}
```

程序输出结果为：

```text
Tom picks up tools from the warehouse.
Tom does some work with tools.
Tom hasn't returned the tool.
Tom returns the tools to the warehouse.
Bob doesn't have tools, does nothing.
Bob has no tools
Jack picks up tools from the warehouse.
Jack hasn't returned the tool.
Jack returns the tools to the warehouse.
An exception has occurred:
Exception: Jack left, because of an emergency.
         at test.main()(xxx/xx.cj:xx)
```

`try` 关键字和 `{}` 之间引入的名字，其作用域与 `{}` 中引入的变量作用域级别相同，在 `{}` 中再次引入相同名字会触发重定义错误。

<!-- compile.error -->

```cangjie
class R <: Resource {
    public func isClosed(): Bool {
        true
    }
    public func close(): Unit {
        print("R is closed")
    }
}

main() {
    try (r = R()) {
        println("Get the resource")
        let r = 0 // Error, redefinition
        println(r)
    }
}
```

try-with-resources 表达式中的 `ResourceSpecification` 的类型必须实现 Resource 接口：

<!-- run -->

```cangjie
interface Resource {
    func isClosed(): Bool  // 离开 try-with-resources 作用域时，判断是否需要调用 close 函数释放资源
    func close(): Unit  // 在 isClosed 返回 false 的场景下释放资源。
}
```

需要说明的是，try-with-resources 表达式中一般没有必要再包含 catch 块和 finally 块，也不建议开发者再手动释放资源（逻辑冗余）。但是，如果需要显式地捕获 try 块或资源申请和释放过程中可能抛出的异常并处理，仍可在 try-with-resources 表达式中包含 catch 块和 finally 块：

<!-- verify -->

```cangjie
class R <: Resource {
    public func isClosed(): Bool {
        true
    }
    public func close(): Unit {
        print("R is closed")
    }
}

main() {
    try (r = R()) {
        println("Get the resource")
    } catch (e: Exception) {
        println("Exception happened when executing the try-with-resources expression")
    } finally {
        println("End of the try-with-resources expression")
    }
}
```

程序输出结果如下：

```text
Get the resource
End of the try-with-resources expression
```

try-with-resources 表达式的类型是 `Unit`。

## CatchPattern 进阶介绍

大多数时候，只想捕获某一类型和其子类型的异常，这时候使用 CatchPattern 的**类型模式**来处理；但有时也需要所有异常做统一处理（如此处不该出现异常，出现了就统一报错），这时可以使用 CatchPattern 的**通配符模式**来处理。

类型模式在语法上有两种格式：

- `Identifier: ExceptionClass`。此格式可以捕获类型为 `ExceptionClass` 及其子类的异常，并将捕获到的异常实例转换成 `ExceptionClass`，然后与 `Identifier` 定义的变量进行绑定，接着就可以在 catch 块中通过 Identifier 定义的变量访问捕获到的异常实例。
- `Identifier: ExceptionClass_1 | ExceptionClass_2 | ... | ExceptionClass_n`。此格式可以通过连接符 `|` 将多个异常类进行拼接，连接符 `|` 表示“或”的关系：可以捕获类型为 `ExceptionClass_1` 及其子类的异常，或者捕获类型为 `ExceptionClass_2` 及其子类的异常，依次类推，或捕获类型为 `ExceptionClass_n` 及其子类的异常（假设 n 大于 1）。当待捕获异常的类型属于上述“或”关系中的任一类型或其子类型时，此异常将被捕获。但是由于无法静态地确定被捕获异常的类型，所以被捕获异常的类型会被转换成由 `|` 连接的所有类型的最小公共父类，并将异常实例与 `Identifier` 定义的变量进行绑定。因此在此类模式下，catch 块内只能通过 `Identifier` 定义的变量访问 `ExceptionClass_i（1 <= i <= n）` 的最小公共父类中的成员变量和成员函数。当然，也可以使用通配符代替类型模式中的 `Identifier`，差别仅在于通配符不会进行绑定操作。

示例如下：

<!-- verify -->

```cangjie
main(): Int64 {
    try {
        throw IllegalArgumentException("This is an Exception!")
    } catch (e: OverflowException) {
        println(e.message)
        println("OverflowException is caught!")
    } catch (e: IllegalArgumentException | NegativeArraySizeException) {
        println(e.message)
        println("IllegalArgumentException or NegativeArraySizeException is caught!")
    } finally {
        println("finally is executed!")
    }
    return 0
}
```

执行结果：

```text
This is an Exception!
IllegalArgumentException or NegativeArraySizeException is caught!
finally is executed!
```

关于“被捕获异常的类型是由 `|` 连接的所有类型的最小公共父类”的示例：

<!-- verify -->

```cangjie
open class Father <: Exception {
    var father: Int32 = 0
}

class ChildOne <: Father {
    var childOne: Int32 = 1
}

class ChildTwo <: Father {
    var childTwo: Int32 = 2
}

main() {
    try {
        throw ChildOne()
    } catch (e: ChildTwo | ChildOne) {
        println("${e is Father}")
    }
}
```

执行结果：

```text
true
```

**通配符模式**的语法是 `_`，它可以捕获同级 try 块内抛出的任意类型的异常，等价于类型模式中的 `e: Exception`，即捕获 Exception 子类所定义的异常。示例如下：

<!-- compile -->

```cangjie
// Catch with wildcardPattern.
try {
    throw OverflowException()
} catch (_) {
    println("catch an exception!")
}
```


---

<!-- Content from source_zh_cn/error_handle/common_runtime_exceptions.md -->
# 常见运行时异常

在仓颉语言中内置了最常见的异常类，开发人员可以直接使用。

| 异常                              | 描述                                              |
| :-------------------------------- | :------------------------------------------------ |
| `ConcurrentModificationException` | 并发修改产生的异常                                |
| `IllegalArgumentException`        | 传递不合法或不正确参数时抛出的异常                |
| `NegativeArraySizeException`      | 创建大小为负的数组时抛出的异常                    |
| `NoneValueException`              | 值不存在时产生的异常，如 Map 中不存在要查找的 key |
| `OverflowException`               | 算术运算溢出异常                                  |


---

<!-- Content from source_zh_cn/error_handle/use_option.md -->
# 使用 Option

在 [Option 类型](../enum_and_pattern_match/option_type.md)中介绍了 Option 类型的定义，因为 Option 类型可以同时表示有值和无值两种状态，而无值在某些情况下也可以理解为一种错误，所以 Option 类型也可以用作错误处理。

例如，在下例中，如果函数 `getOrThrow` 的参数值等于 `Some(v)` 则将 `v` 的值返回，如果参数值等于 `None` 则抛出异常。

<!-- compile -->

```cangjie
func getOrThrow(a: ?Int64) {
    match (a) {
        case Some(v) => v
        case None => throw NoneValueException()
    }
}
```

因为 `Option` 是一种非常常用的类型，所以仓颉为其提供了多种解构方式，以方便 `Option` 类型的使用，具体包括：模式匹配、`getOrThrow` 函数、`coalescing` 操作符（`??`），以及问号操作符（`?`）。下面将对这些方式逐一介绍。

- 模式匹配：因为 Option 类型是一种 enum 类型，所以可以使用上文提到的 enum 的模式匹配来实现对 `Option` 值的解构。例如，下例中函数 `getString` 接受一个 `?Int64` 类型的参数，当参数是 `Some` 值时，返回其中数值的字符串表示，当参数是 `None` 值时，返回字符串 `"none"`。

    <!-- verify -->

    ```cangjie
    func getString(p: ?Int64): String{
        match (p) {
            case Some(x) => "${x}"
            case None => "none"
        }
    }
    main() {
        let a = Some(1)
        let b: ?Int64 = None
        let r1 = getString(a)
        let r2 = getString(b)
        println(r1)
        println(r2)
    }
    ```

   上述代码的执行结果为：

    ```text
    1
    none
    ```

- `coalescing` 操作符（`??`）：对于 `?T` 类型的表达式 `e1`，如果希望 `e1` 的值等于 `None` 时同样返回一个 `T` 类型的值 `e2`，可以使用 `??` 操作符。对于表达式 `e1 ?? e2`，当 `e1` 的值等于 `Some(v)` 时返回 `v` 的值，否则返回 `e2` 的值。举例如下：

    <!-- verify -->

    ```cangjie
    main() {
        let a = Some(1)
        let b: ?Int64 = None
        let r1: Int64 = a ?? 0
        let r2: Int64 = b ?? 0
        println(r1)
        println(r2)
    }
    ```

   上述代码的执行结果为：

    ```text
    1
    0
    ```

- 问号操作符（`?`）：`?` 需要和 `.` 或 `()` 或 `[]` 或 `{}`（特指尾随 lambda 调用的场景）一起使用，用以实现 `Option` 类型对 `.`，`()`，`[]` 和 `{}` 的支持。以 `.` 为例（`()`，`[]` 和 `{}`同理），对于 `?T1` 类型的表达式 `e`，当 `e` 的值等于 `Some(v)` 时，`e?.b` 的值等于 `Option<T2>.Some(v.b)`，否则 `e?.b` 的值等于 `Option<T2>.None`，其中 `T2` 是 `v.b` 的类型。举例如下：

    <!-- compile -->

    ```cangjie
    struct R {
        public var a: Int64
        public init(a: Int64) {
            this.a = a
        }
    }

    let r = R(100)
    let x = Some(r)
    let y = Option<R>.None
    let r1 = x?.a   // r1 = Option<Int64>.Some(100)
    let r2 = y?.a   // r2 = Option<Int64>.None
    ```

   问号操作符（`?`）支持多层访问，以 `a?.b.c?.d` 为例（`()`，`[]` 和 `{}`同理）。表达式 `a` 的类型需要是某个 `Option<T1>` 且 `T1` 包含实例成员 `b`，`b` 的类型中包含实例成员变量 `c` 且 `c` 的类型是某个 `Option<T2>`，`T2` 包含实例成员 `d`；表达式 `a?.b.c?.d` 的类型为 `Option<T3>`，其中 `T3` 是 `T2` 的实例成员 `d` 的类型；当 `a` 的值等于 `Some(va)` 且 `va.b.c` 的值等于 `Some(vc)` 时，`a?.b.c?.d` 的值等于 `Option<T3>.Some(vc.d)`；当 `a` 的值等于 `Some(va)` 且 `va.b.c` 的值等于 `None` 时，`a?.b.c?.d` 的值等于 `Option<T3>.None`（`d` 不会被求值）；当 `a` 的值等于 `None` 时，`a?.b.c?.d` 的值等于 `Option<T3>.None`（`b`，`c` 和 `d` 都不会被求值）。

    <!-- compile -->

    ```cangjie
    struct A {
        let b: B = B()
    }

    struct B {
        let c: Option<C> = C()
        let c1: Option<C> = Option<C>.None
    }

    struct C {
        let d: Int64 = 100
    }

    let a = Some(A())
    let a1 = a?.b.c?.d // a1 = Option<Int64>.Some(100)
    let a2 = a?.b.c1?.d // a2 = Option<Int64>.None
    ```

- `getOrThrow` 函数：对于 `?T` 类型的表达式 `e`，可以通过调用 `getOrThrow` 函数实现解构。当 `e` 的值等于 `Some(v)` 时，`getOrThrow()` 返回 `v` 的值，否则抛出异常。举例如下：

    <!-- verify -->

    ```cangjie
    main() {
        let a = Some(1)
        let b: ?Int64 = None
        let r1 = a.getOrThrow()
        println(r1)
        try {
            let r2 = b.getOrThrow()
        } catch (e: NoneValueException) {
            println("b is None")
        }
    }
    ```

   上述代码的执行结果为：

    ```text
    1
    b is None
    ```


---

<!-- Content from source_zh_cn/concurrency/concurrency_overview.md -->
# 并发概述

并发编程是现代编程语言中不可或缺的特性，仓颉编程语言提供*抢占式的线程模型*作为并发编程机制。线程可以细分为两种不同概念，**语言线程**和 **native 线程**。

- 语言线程是编程语言中并发模型的基本执行单位。仓颉编程语言希望给开发者提供一个友好、高效、统一的并发编程界面，让开发者无需关心操作系统线程、用户态线程等差异，因此提供**仓颉线程**的概念。开发者在大多数情况下只需面向仓颉线程编写并发代码。
- native 线程指语言实现中所使用到的线程（一般是操作系统线程），它们作为语言线程的具体实现载体。不同编程语言会以不同的方式实现语言线程。例如，一些编程语言直接通过操作系统调用来创建线程，这意味着每个语言线程对应一个 native 线程，这种实现方案一般被称之为 `1:1` 线程模型。此外，另有一些编程语言提供特殊的线程实现，它们允许多个语言线程在多个 native 线程上切换执行，这种也被称为 `M:N` 线程模型，即 M 个语言线程在 N 个 native 线程上调度执行，其中 M 和 N 不一定相等。当前，仓颉语言的实现同样采用 `M:N` 线程模型；因此，仓颉线程本质上是一种用户态的轻量级线程，支持抢占且相比操作系统线程更轻量化。

仓颉线程本质上是用户态的轻量级线程，每个仓颉线程都受到底层 native 线程的调度执行，并且多个仓颉线程可以由一个 native 线程执行。每个 native 线程会不断地选择一个就绪的仓颉线程完成执行，如果仓颉线程在执行过程中发生阻塞（例如等待互斥锁的释放），那么 native 线程会将当前的仓颉线程挂起，并继续选择下一个就绪的仓颉线程。发生阻塞的仓颉线程在重新就绪后会继续被 native 线程调度执行。

在大多数情况下，开发者只需要面向仓颉线程进行并发编程而不需要考虑这些细节。但在进行跨语言编程时，开发者需要谨慎调用可能发生阻塞的 foreign 函数，例如 IO 相关的操作系统调用等。例如，下列示例代码中的新线程会调用 foreign 函数 `socket_read`。在程序运行过程中，某一 native 线程将调度并执行该仓颉线程，在进入到 foreign 函数中后，系统调用会直接阻塞当前 native 线程直到函数执行完成。native 线程在阻塞期间将无法调度其他仓颉线程来执行，这会降低程序执行的吞吐量。

```cangjie
foreign socket_read(sock: Int64): CPointer<Int8>

let fut = spawn {
    let sock: Int64 = ...
    let ptr = socket_read(sock)
}
```

> **注意：**
>
> 本文档在没有歧义的情况下将直接以**线程**简化对**仓颉线程**的指代。


---

<!-- Content from source_zh_cn/concurrency/create_thread.md -->
# 创建线程

当开发者希望并发执行某一段代码时，只需创建一个仓颉线程即可。要创建一个新的仓颉线程，可以使用关键字 `spawn` 并传递一个无形参的 `lambda` 表达式，该 `lambda` 表达式即为在新线程中执行的代码。

下方示例代码中，主线程和新线程均会尝试打印一些文本：

<!-- run -->

```cangjie
main(): Int64 {
    spawn { =>
        println("New thread before sleeping")
        sleep(100 * Duration.millisecond) // sleep for 100ms.
        println("New thread after sleeping")
    }

    println("Main thread")

    return 0
}
```

在上面的例子中，新线程会在主线程结束时一起停止，无论这个新线程是否已完成运行。上方示例的输出每次可能略有不同，有可能会输出类似如下的内容：

```text
New thread before sleeping
Main thread

```

`sleep()` 函数会让当前线程睡眠指定的时长，之后再恢复执行，其时间由指定的 Duration 类型决定。`sleep()` 详细介绍请参见[线程睡眠指定时长](./sleep.md)章节。


---

<!-- Content from source_zh_cn/concurrency/use_thread.md -->
# 访问线程

## 使用 `Future<T>` 等待线程结束并获取返回值

在上面的例子中，新创建的线程会由于主线程结束而提前结束，在缺乏顺序保证的情况下，甚至可能会出现新创建的线程还来不及得到执行就退出了。可以通过 `spawn` 表达式的返回值，来等待线程执行结束。

`spawn` 表达式的返回类型是 `Future<T>`，其中 `T` 是类型变元，其类型与 lambda 表达式的返回类型一致。当调用 `Future<T>` 的 `get()` 成员函数时，它将等待它的线程执行完成。

`Future<T>` 的原型声明如下：

```cangjie
public class Future<T> {
    // Blocking the current thread, waiting for the result of the thread corresponding to the current Future object.
    // If an exception occurs in the corresponding thread, the method will throw the exception.
    public func get(): T

    // Blocking the current thread, waiting for the result of the thread corresponding to the current Future object.
    // If the corresponding thread has not completed execution within Duration, the method will throws TimeoutException.
    // If `timeout` <= Duration.Zero, its behavior is the same as `get()`.
    public func get(timeout: Duration): T

    // Non-blocking method that immediately returns Option<T>.None if thread has not finished execution.
    // Returns the computed result otherwise.
    // If an exception occurs in the corresponding thread, the method will throw the exception.
    public func tryGet(): Option<T>
}
```

下方示例代码演示了如何使用 `Future<T>` 在 `main` 中等待新创建的线程执行完成：

<!-- run -->

```cangjie
main(): Int64 {
    let fut: Future<Unit> = spawn { =>
        println("New thread before sleeping")
        sleep(100 * Duration.millisecond) // sleep for 100ms.
        println("New thread after sleeping")
    }

    println("Main thread")

    fut.get() // wait for the thread to finish.
    return 0
}
```

调用 `Future<T>` 实例的 `get()` 会阻塞当前运行的线程，直到 `Future<T>` 实例所代表的线程运行结束。因此，上方示例有可能会输出类似如下内容：

```text
New thread before sleeping
Main thread
New thread after sleeping
```

主线程在完成打印后会因为调用 `get()` 而等待新创建的线程执行结束。但主线程和新线程的打印顺序具有不确定性。

如果将 `fut.get()` 移动到主线程的打印之前，如下所示：

<!-- verify -->

```cangjie
main(): Int64 {
    let fut: Future<Unit> = spawn { =>
        println("New thread before sleeping")
        sleep(100 * Duration.millisecond) // sleep for 100ms.
        println("New thread after sleeping")
    }

    fut.get() // wait for the thread to finish.

    println("Main thread")
    return 0
}
```

主线程将等待新创建的线程执行完成，然后再执行打印，因此程序的输出将变得确定，如下所示：

```text
New thread before sleeping
New thread after sleeping
Main thread
```

可见，`get()` 的调用位置会影响线程是否能同时运行。

`Future<T>` 除了可以用于阻塞等待线程执行结束以外，还可以获取线程执行的结果。如下是它提供的具体成员函数：

- `get(): T`：阻塞等待线程执行结束，并返回执行结果，如果该线程已经结束，则直接返回执行结果。

    示例代码如下：

    <!-- verify -->

    ```cangjie
    main(): Int64 {
        let fut: Future<Int64> = spawn {
            sleep(Duration.second) // sleep for 1s.
            return 1
        }

        try {
            // wait for the thread to finish, and get the result.
            let res: Int64 = fut.get()
            println("result = ${res}")
        } catch (_) {
            println("oops")
        }
        return 0
    }
    ```

    输出结果如下：

    ```text
    result = 1
    ```

- `get(timeout: Duration): T`：阻塞等待该 `Future<T>` 所代表的线程执行结束，并返回执行结果，当到达超时时间 timeout 时，如果该线程还没有执行结束，将会抛出异常 TimeoutException。如果 `timeout <= Duration.Zero`, 其行为与 `get()` 相同。

    示例代码如下：

    <!-- verify -->

    ```cangjie
    main(): Int64 {
        let fut = spawn {
            sleep(Duration.second) // sleep for 1s.
            return 1
        }

        // wait for the thread to finish, but only for 1ms.
        try {
            let res = fut.get(Duration.millisecond * 1)
            println("result: ${res}")
        } catch (_: TimeoutException) {
            println("oops")
        }
        return 0
    }

    ```

    输出结果如下：

    ```text
    oops
    ```

## 访问线程属性

每个 `Future<T>` 对象都有一个对应的仓颉线程，以 `Thread` 对象为表示。`Thread` 类主要被用于访问线程的属性信息，例如线程标识等。需要注意的是，`Thread` 无法直接被实例化构造对象，仅能从 `Future<T>` 的 `thread` 成员属性获取对应的 `Thread` 对象，或是通过 `Thread` 的静态成员属性 `currentThread` 得到当前正在执行线程对应的 `Thread` 对象。

`Thread` 类的部分方法定义如下（完整的方法描述可参考《仓颉编程语言库 API》）。

```cangjie
class Thread {
    // Get the currently running thread
    static prop currentThread: Thread

    // Get the unique identifier (represented as an integer) of the thread object
    prop id: Int64

    // Check whether the thread has any cancellation request
    prop hasPendingCancellation: Bool
}
```

下列示例代码在创建新线程后分别通过两种方式获取线程标识。由于主线程和新线程获取的是同一个 `Thread` 对象，所以他们能够打印出相同的线程标识。

<!-- run -->

```cangjie
main(): Unit {
    let fut = spawn {
        println("Current thread id: ${Thread.currentThread.id}")
    }
    println("New thread id: ${fut.thread.id}")
    fut.get()
}
```

输出结果如下（其中线程 id 会变化，也可能为其他值）:

```text
New thread id: 1
Current thread id: 1
```


---

<!-- Content from source_zh_cn/concurrency/terminal_thread.md -->
# 终止线程

可以通过 `Future<T>` 的 `cancel()` 方法向对应的线程发送终止请求，该方法不会停止线程执行。开发者需要使用 `Thread` 的 `hasPendingCancellation` 属性来检查线程是否存在终止请求。

一般而言，如果线程存在终止请求，那么开发者可以实施相应的线程终止逻辑。因此，如何终止线程都交由开发者自行处理，如果开发者忽略终止请求，那么线程继续执行直到正常结束。

示例代码如下：

<!-- verify -->

```cangjie
import std.sync.SyncCounter

main(): Unit {
    let syncCounter = SyncCounter(1)
    let fut = spawn {
        syncCounter.waitUntilZero()  // block until the syncCounter becomes zero
        if (Thread.currentThread.hasPendingCancellation) {  // Check cancellation request
            println("cancelled")
            return
        }
        println("hello")
    }
    fut.cancel()    // Send cancellation request
    syncCounter.dec()
    fut.get() // Join thread
}
```

输出结果如下：

```text
cancelled
```


---

<!-- Content from source_zh_cn/concurrency/sync.md -->
# 同步机制

在并发编程中，如果缺少同步机制来保护多个线程共享的变量，很容易会出现数据竞争问题（data race）。

仓颉编程语言提供三种常见的同步机制来确保数据的线程安全：原子操作、互斥锁和条件变量。

## 原子操作 Atomic

仓颉提供整数类型、`Bool` 类型和引用类型的原子操作。

其中整数类型包括： `Int8`、`Int16`、`Int32`、`Int64`、`UInt8`、`UInt16`、`UInt32`、`UInt64`。

整数类型的原子操作支持基本的读写、交换以及算术运算操作：

| 操作             | 功能                                              |
| ---------------- | ------------------------------------------------- |
| `load`           | 读取                                              |
| `store`          | 写入                                              |
| `swap`           | 交换，返回交换前的值                               |
| `compareAndSwap` | 比较再交换，交换成功返回 `true`，否则返回 `false` |
| `fetchAdd`       | 加法，返回执行加操作之前的值                      |
| `fetchSub`       | 减法，返回执行减操作之前的值                      |
| `fetchAnd`       | 与，返回执行与操作之前的值                        |
| `fetchOr`        | 或，返回执行或操作之前的值                        |
| `fetchXor`       | 异或，返回执行异或操作之前的值                    |

需要注意的是：

1. 交换操作和算术操作的返回值是修改前的值。
2. compareAndSwap 是判断当前原子变量的值是否等于 old 值，如果等于，则使用 new 值替换；否则不替换。

以 `Int8` 类型为例，对应的原子操作类型声明如下：

```cangjie
class AtomicInt8 {
    public func load(): Int8
    public func store(val: Int8): Unit
    public func swap(val: Int8): Int8
    public func compareAndSwap(old: Int8, new: Int8): Bool
    public func fetchAdd(val: Int8): Int8
    public func fetchSub(val: Int8): Int8
    public func fetchAnd(val: Int8): Int8
    public func fetchOr(val: Int8): Int8
    public func fetchXor(val: Int8): Int8
}
```

上述每一种原子类型的方法都有一个对应的方法可以接收内存排序参数，目前内存排序参数仅支持顺序一致性。

类似的，其他整数类型对应的原子操作类型有：

```cangjie
class AtomicInt16 {...}
class AtomicInt32 {...}
class AtomicInt64 {...}
class AtomicUInt8 {...}
class AtomicUInt16 {...}
class AtomicUInt32 {...}
class AtomicUInt64 {...}
```

下方示例演示了如何在多线程程序中，使用原子操作实现计数：

<!-- verify -->

```cangjie
import std.sync.AtomicInt64
import std.collection.ArrayList

let count = AtomicInt64(0)

main(): Int64 {
    let list = ArrayList<Future<Int64>>()

    // create 1000 threads.
    for (_ in 0..1000) {
        let fut = spawn {
            sleep(Duration.millisecond) // sleep for 1ms.
            count.fetchAdd(1)
        }
        list.add(fut)
    }

    // Wait for all threads finished.
    for (f in list) {
        f.get()
    }

    let val = count.load()
    println("count = ${val}")
    return 0
}
```

输出结果应为：

```text
count = 1000
```

以下是使用整数类型原子操作的一些其他正确示例：

<!-- compile -->

```cangjie
var obj: AtomicInt32 = AtomicInt32(1)
var x = obj.load() // x: 1, the type is Int32
x = obj.swap(2) // x: 1
x = obj.load() // x: 2
var y = obj.compareAndSwap(2, 3) // y: true, the type is Bool.
y = obj.compareAndSwap(2, 3) // y: false, the value in obj is no longer 2 but 3. Therefore, the CAS operation fails.
x = obj.fetchAdd(1) // x: 3
x = obj.load() // x: 4
```

`Bool` 类型和引用类型的原子操作只提供读写和交换操作：

| 操作             | 功能                                              |
| ---------------- | ------------------------------------------------- |
| `load`           | 读取                                              |
| `store`          | 写入                                              |
| `swap`           | 交换，返回交换前的值                              |
| `compareAndSwap` | 比较再交换，交换成功返回 `true`，否则返回 `false` |

> **注意：**
>
> 引用类型原子操作只对引用类型有效。

原子引用类型是 `AtomicReference`，以下是使用 `Bool` 类型、引用类型原子操作的一些正确示例：

<!-- verify -->

```cangjie
import std.sync.{AtomicBool, AtomicReference}

class A {}

main() {
    var obj = AtomicBool(true)
    var x1 = obj.load() // x1: true, the type is Bool
    println(x1)
    var t1 = A()
    var obj2 = AtomicReference(t1)
    var x2 = obj2.load() // x2 and t1 are the same object
    var y1 = obj2.compareAndSwap(x2, t1) // x2 and t1 are the same object, y1: true
    println(y1)
    var t2 = A()
    var y2 = obj2.compareAndSwap(t2, A()) // x and t1 are not the same object, CAS fails, y2: false
    println(y2)
    y2 = obj2.compareAndSwap(t1, A()) // CAS successes, y2: true
    println(y2)
}
```

编译执行上述代码，输出结果为：

```text
true
true
false
true
```

## 可重入互斥锁 Mutex

可重入互斥锁的作用是对临界区加以保护，使得任意时刻最多只有一个线程能够执行临界区的代码。当一个线程试图获取一个已被其他线程持有的锁时，该线程会被阻塞，直到锁被释放，该线程才会被唤醒，可重入是指线程获取该锁后可再次获得该锁。

使用可重入互斥锁时，必须牢记两条规则：

1. 在访问共享数据之前，必须尝试获取锁；
2. 处理完共享数据后，必须释放锁，以便其他线程可以获得锁。

`Mutex` 提供的主要成员函数如下：

```cangjie
public class Mutex <: UniqueLock {
    // Create a Mutex.
    public init()

    // Locks the mutex, blocks if the mutex is not available.
    public func lock(): Unit

    // Unlocks the mutex. If there are other threads blocking on this
    // lock, then wake up one of them.
    public func unlock(): Unit

    // Tries to lock the mutex, returns false if the mutex is not
    // available, otherwise returns true.
    public func tryLock(): Bool

    // Generate a Condition instance for the mutex.
    public func condition(): Condition
}
```

下方示例演示了如何使用 `Mutex` 来保护对全局共享变量 `count` 的访问，对 `count` 的操作即属于临界区：

<!-- verify -->

```cangjie
import std.sync.Mutex
import std.collection.ArrayList

var count: Int64 = 0
let mtx = Mutex()

main(): Int64 {
    let list = ArrayList<Future<Unit>>()

    // create 1000 threads.
    for (i in 0..1000) {
        let fut = spawn {
            sleep(Duration.millisecond) // sleep for 1ms.
            mtx.lock()
            count++
            mtx.unlock()
        }
        list.add(fut)
    }

    // Wait for all threads finished.
    for (f in list) {
        f.get()
    }

    println("count = ${count}")
    return 0
}
```

输出结果应为：

```text
count = 1000
```

下方示例演示了如何使用 `tryLock`：

<!-- run -->

```cangjie
import std.sync.Mutex


main(): Int64 {
    let mtx: Mutex = Mutex()
    var future: Future<Unit> = spawn {
        mtx.lock()
        println("get the lock, do something")
        sleep(Duration.millisecond * 10)
        mtx.unlock()
    }
    try {
        future.get(Duration.millisecond * 10)
    } catch (e: TimeoutException) {
        if (mtx.tryLock()) {
            println("tryLock success, do something")
            mtx.unlock()
            return 0
        }
        println("tryLock failed, do nothing")
        return 0
    }
    return 0
}
```

一种可能的输出结果如下：

```text
get the lock, do something
```

以下是互斥锁的一些错误示例：

错误示例 1：线程操作临界区后没有解锁，导致其他线程无法获得锁而阻塞。

<!-- compile.error -->
<!-- cfg="libcangjie-std-sync" -->

```cangjie
import std.sync.Mutex

var sum: Int64 = 0
let mutex = Mutex()

main() {
    let foo = spawn { =>
        mutex.lock()
        sum = sum + 1
    }
    let bar = spawn { =>
        mutex.lock()
        sum = sum + 1
    }
    foo.get()
    println("${sum}")
    bar.get() // Because the thread is not unlocked, other threads waiting to obtain the current mutex will be blocked.
}
```

错误示例 2：在本线程没有持有锁的情况下调用 `unlock` 将会抛出异常。

<!-- compile.error -->
<!-- cfg="libcangjie-std-sync" -->

```cangjie
import std.sync.Mutex

var sum: Int64 = 0
let mutex = Mutex()

main() {
    let foo = spawn { =>
        sum = sum + 1
        mutex.unlock() // Error, Unlock without obtaining the lock and throw an exception: IllegalSynchronizationStateException.
    }
    foo.get()
}
```

错误示例 3：`tryLock()` 并不保证获取到锁，可能会造成不在锁的保护下操作临界区和在没有持有锁的情况下调用 `unlock` 抛出异常等行为。

<!-- compile.error -->
<!-- cfg="libcangjie-std-sync" -->

```cangjie
import std.sync.Mutex

var sum: Int64 = 0
let mutex = Mutex()

main() {
    for (i in 0..100) {
        spawn { =>
            mutex.tryLock() // Error, `tryLock()` just trying to acquire a lock, there is no guarantee that the lock will be acquired, and this can lead to abnormal behavior.
            sum = sum + 1
            mutex.unlock()
        }
    }
}
```

另外，`Mutex` 在设计上是一个可重入锁，也就是说：在某个线程已经持有一个 `Mutex` 锁的情况下，再次尝试获取同一个 `Mutex` 锁，永远可以立即获得该 `Mutex` 锁。

> **注意：**
>
> 虽然 `Mutex` 是一个可重入锁，但是调用 `unlock()` 的次数必须和调用 `lock()` 的次数相同，才能成功释放该锁。

下方示例代码演示了 `Mutex` 可重入的特性：

<!-- verify -->

```cangjie
import std.sync.Mutex

var count: Int64 = 0
let mtx = Mutex()

func foo() {
    mtx.lock()
    count += 10
    bar()
    mtx.unlock()
}

func bar() {
    mtx.lock()
    count += 100
    mtx.unlock()
}

main(): Int64 {
    let fut = spawn {
        sleep(Duration.millisecond) // sleep for 1ms.
        foo()
    }

    foo()

    fut.get()

    println("count = ${count}")
    return 0
}
```

输出结果应为：

```text
count = 220
```

在上方示例中，无论是主线程还是新创建的线程，如果在 `foo()` 中已经获得了锁，那么继续调用 `bar()` 的话，在 `bar()` 函数中由于是对同一个 `Mutex` 进行加锁，因此也是能立即获得该锁的，不会出现死锁。

## Condition

`Condition` 是与某个互斥锁绑定的条件变量（也就是等待队列），`Condition` 实例由互斥锁创建，一个互斥锁可以创建多个 `Condition` 实例。`Condition` 可以使线程阻塞并等待来自另一个线程的信号以恢复执行。这是一种利用共享变量进行线程同步的机制，主要提供如下方法：

```cangjie
public class Mutex <: UniqueLock {
    // ...
    // Generate a Condition instance for the mutex.
    public func condition(): Condition
}

public interface Condition {
    // Wait for a signal, blocking the current thread.
    func wait(): Unit
    func wait(timeout!: Duration): Bool

    // Wait for a signal and predicate, blocking the current thread.
    func waitUntil(predicate: ()->Bool): Unit
    func waitUntil(predicate: ()->Bool, timeout!: Duration): Bool

    // Wake up one thread of those waiting on the monitor, if any.
    func notify(): Unit

    // Wake up all threads waiting on the monitor, if any.
    func notifyAll(): Unit
}
```

调用 `Condition` 接口的 `wait`、`notify` 或 `notifyAll` 方法前，需要确保当前线程已经持有绑定的锁。`wait` 方法包含如下动作：

1. 添加当前线程到对应锁的等待队列中；
2. 阻塞当前线程，同时完全释放该锁，并记录锁的重入次数；
3. 等待某个其他线程使用同一个 `Condition` 实例的 `notify` 或 `notifyAll` 方法向该线程发出信号；
4. 当前线程被唤醒后，会自动尝试重新获取锁，且持有锁的重入状态与第 2 步记录的重入次数相同；但是如果尝试获取锁失败，则当前线程会阻塞在该锁上。

`wait` 方法接受一个可选参数 `timeout`。需要注意的是，业界很多常用的常规操作系统不保证调度的实时性，因此无法保证一个线程会被阻塞“精确的 N 纳秒”——可能会观察到与系统相关的不精确情况。此外，当前语言规范明确允许实现产生虚假唤醒——在这种情况下，`wait` 返回值是由实现决定的——可能为 `true` 或 `false`。因此鼓励开发者始终将 `wait` 包在一个循环中：

```cangjie
synchronized (obj) {
  while (<condition is not true>) {
    obj.wait()
  }
}
```

以下是使用 `Condition` 的一个正确示例：

<!-- verify -->

```cangjie
import std.sync.Mutex

let mtx = Mutex()
let condition = synchronized(mtx) {
    mtx.condition()
}
var flag: Bool = true

main(): Int64 {
    let fut = spawn {
        mtx.lock()
        while (flag) {
            println("New thread: before wait")
            condition.wait()
            println("New thread: after wait")
        }
        mtx.unlock()
    }

    // Sleep for 10ms, to make sure the new thread can be executed.
    sleep(10 * Duration.millisecond)

    mtx.lock()
    println("Main thread: set flag")
    flag = false
    mtx.unlock()

    mtx.lock()
    println("Main thread: notify")
    condition.notifyAll()
    mtx.unlock()

    // wait for the new thread finished.
    fut.get()
    return 0
}
```

输出结果应为：

```text
New thread: before wait
Main thread: set flag
Main thread: notify
New thread: after wait
```

`Condition` 对象执行 `wait` 时，必须在锁的保护下进行，否则 `wait` 中释放锁的操作会抛出异常。

以下是使用条件变量的一些错误示例：

<!-- run.error -->

```cangjie
import std.sync.Mutex

let m1 = Mutex()
let c1 = synchronized(m1) {
    m1.condition()
}
let m2 = Mutex()
var flag: Bool = true
var count: Int64 = 0

func foo1() {
    spawn {
        m2.lock()
        while (flag) {
            c1.wait() // Error：The lock used together with the condition variable must be the same lock and in the locked state. Otherwise, the unlock operation in `wait` throws an exception.
        }
        count = count + 1
        m2.unlock()
    }
    m1.lock()
    flag = false
    c1.notifyAll()
    m1.unlock()
}

func foo2() {
    spawn {
        while (flag) {
            c1.wait() // Error：The `wait` of a conditional variable must be called with a lock held.
        }
        count = count + 1
    }
    m1.lock()
    flag = false
    c1.notifyAll()
    m1.unlock()
}

main() {
    foo1()
    foo2()
    c1.wait()
}
```

有时在复杂的线程间同步的场景下需要对同一个锁对象生成多个 `Condition` 实例，以下示例实现了一个长度固定的有界 `FIFO` 队列。当队列为空，`get()` 会被阻塞；当队列已满，`put()` 会被阻塞。

<!-- compile -->

```cangjie
import std.sync.{Mutex, Condition}

class BoundedQueue {
    // Create a Mutex, two Conditions.
    let m: Mutex = Mutex()
    var notFull: Condition
    var notEmpty: Condition

    var count: Int64 // Object count in buffer.
    var head: Int64  // Write index.
    var tail: Int64  // Read index.

    // Queue's length is 100.
    let items: Array<Object> = Array<Object>(100, {i => Object()})

    init() {
        count = 0
        head = 0
        tail = 0

        synchronized(m) {
          notFull  = m.condition()
          notEmpty = m.condition()
        }
    }

    // Insert an object, if the queue is full, block the current thread.
    public func put(x: Object) {
        // Acquire the mutex.
        synchronized(m) {
          while (count == 100) {
            // If the queue is full, wait for the "queue notFull" event.
            notFull.wait()
          }
          items[head] = x
          head++
          if (head == 100) {
            head = 0
          }
          count++

          // An object has been inserted and the current queue is no longer
          // empty, so wake up the thread previously blocked on get()
          // because the queue was empty.
          notEmpty.notify()
        } // Release the mutex.
    }

    // Pop an object, if the queue is empty, block the current thread.
    public func get(): Object {
        // Acquire the mutex.
        synchronized(m) {
          while (count == 0) {
            // If the queue is empty, wait for the "queue notEmpty" event.
            notEmpty.wait()
          }
          let x: Object = items[tail]
          tail++
          if (tail == 100) {
            tail = 0
          }
          count--

          // An object has been popped and the current queue is no longer
          // full, so wake up the thread previously blocked on put()
          // because the queue was full.
          notFull.notify()

          return x
        } // Release the mutex.
    }
}
```

## synchronized 关键字

`Lock` 提供了一种便利灵活的加锁的方式，同时因为它的灵活性，也可能引起忘记解锁，或者在持有锁的情况下抛出异常不能自动释放持有的锁的问题。因此，仓颉编程语言提供一个 `synchronized` 关键字，搭配 `Lock` 一起使用，可以在其后跟随的作用域内自动进行加锁解锁操作，用来解决类似的问题。

下方示例代码演示了如何使用 `synchronized` 关键字来保护共享数据：

<!-- verify -->

```cangjie
import std.sync.Mutex
import std.collection.ArrayList

var count: Int64 = 0
let mtx = Mutex()

main(): Int64 {
    let list = ArrayList<Future<Unit>>()

    // create 1000 threads.
    for (i in 0..1000) {
        let fut = spawn {
            sleep(Duration.millisecond) // sleep for 1ms.
            // Use synchronized(mtx), instead of mtx.lock() and mtx.unlock().
            synchronized(mtx) {
                count++
            }
        }
        list.add(fut)
    }

    // Wait for all threads finished.
    for (f in list) {
        f.get()
    }

    println("count = ${count}")
    return 0
}
```

输出结果应为：

```text
count = 1000
```

通过在 `synchronized` 后面加上一个 `Lock` 实例，对其后面修饰的代码块进行保护，可以使得任意时刻最多只有一个线程可以执行被保护的代码：

1. 一个线程在进入 `synchronized` 修饰的代码块之前，会自动获取 `Lock` 实例对应的锁，如果无法获取锁，则当前线程被阻塞；
2. 一个线程在退出 `synchronized` 修饰的代码块之前，会自动释放该 `Lock` 实例的锁。

对于控制转移表达式（如 `break`、`continue`、`return`、`throw`），在导致程序的执行跳出 `synchronized` 代码块时，也符合上面第 2 条的说明，也就说也会自动释放 `synchronized` 表达式对应的锁。

下方示例演示了在 `synchronized` 代码块中出现 `break` 语句的情况：

<!-- verify -->

```cangjie
import std.sync.Mutex
import std.collection.ArrayList

var count: Int64 = 0
var mtx: Mutex = Mutex()

main(): Int64 {
    let list = ArrayList<Future<Unit>>()
    for (i in 0..10) {
        let fut = spawn {
            while (true) {
                synchronized(mtx) {
                    count = count + 1
                    break
                    println("in thread")
                }
            }
        }
        list.add(fut)
    }

    // Wait for all threads finished.
    for (f in list) {
        f.get()
    }

    synchronized(mtx) {
        println("in main, count = ${count}")
    }
    return 0
}
```

输出结果应为：

```text
in main, count = 10
```

实际上 `in thread` 这行不会被打印，因为 `break` 语句实际上会让程序执行跳出 `while` 循环（在跳出 `while` 循环之前，先跳出 `synchronized` 代码块）。

## 线程局部变量 ThreadLocal

使用 core 包中的 `ThreadLocal` 可以创建并使用线程局部变量，每一个线程都有它独立的一个存储空间来保存这些线程局部变量。因此，在每个线程可以安全地访问他们各自的线程局部变量，而不受其他线程的影响。

```cangjie
public class ThreadLocal<T> {
    /* 构造一个携带空值的仓颉线程局部变量 */
    public init()

    /* 获得仓颉线程局部变量的值 */
    public func get(): Option<T> // 如果值不存在，则返回 Option<T>.None。返回值 Option<T> - 仓颉线程局部变量的值

    /* 通过 value 设置仓颉线程局部变量的值 */
    public func set(value: Option<T>): Unit // 如果传入 Option<T>.None，该局部变量的值将被删除，在线程后续操作中将无法获取。参数 value - 需要设置的局部变量的值。
}
```

下方示例代码演示了如何通过 `ThreadLocal`类来创建并使用各自线程的局部变量：

<!-- run -->

```cangjie

main(): Int64 {
    let tl = ThreadLocal<Int64>()
    let fut1 = spawn {
        tl.set(123)
        println("tl in spawn1 = ${tl.get().getOrThrow()}")
    }
    let fut2 = spawn {
        tl.set(456)
        println("tl in spawn2 = ${tl.get().getOrThrow()}")
    }
    fut1.get()
    fut2.get()
    0
}
```

可能的输出结果如下：

```text
tl in spawn1 = 123
tl in spawn2 = 456
```

或者

```text
tl in spawn2 = 456
tl in spawn1 = 123
```


---

<!-- Content from source_zh_cn/concurrency/sleep.md -->
# 线程睡眠指定时长 sleep

`sleep` 函数会阻塞当前运行的线程，该线程会主动睡眠一段时间，之后再恢复执行，其参数类型为 Duration 类型。函数原型为：

```cangjie
func sleep(dur: Duration): Unit // Sleep for at least `dur`.
```

> **注意：**
>
> 如果 `dur` <= Duration.Zero, 那么当前线程只会让出执行资源，并不会进入睡眠。

以下是使用 `sleep` 的示例：

<!-- verify -->

```cangjie
main(): Int64 {
    println("Hello")
    sleep(Duration.second)  // sleep for 1s.
    println("World")
    return 0
}
```

输出结果如下：

```text
Hello
World
```


---

<!-- Content from source_zh_cn/Basic_IO/basic_IO_overview.md -->
# I/O 流概述

本章介绍基本的 I/O 概念和文件操作。

仓颉编程语言将与应用程序外部载体交互的操作称为 I/O 操作。I 对应输入（Input），O 对应输出（Output）。

仓颉编程语言所有的 I/O 机制都是基于数据流进行输入输出，这些数据流表示了字节数据的序列。数据流是一串连续的数据集合，它就像承载数据的管道，在管道的一端输入数据，在管道的另一端就可以输出数据。

仓颉编程语言将输入输出抽象为流（Stream）。

- 将数据从外存中读取到内存中的称为输入流（InputStream），输入端可以一段一段地向管道中写入数据，这些数据段会按先后顺序形成一个长的数据流。
- 将数据从内存写入外存中的称为输出流（OutputStream），输出端也可以一段一段地从管道中读出数据，每次可以读取其中的任意长度的数据（不需要跟输入端匹配），但只能读取先输入的数据，再读取后输入的数据。

有了这一层抽象，仓颉编程语言就可以使用统一的接口来实现与外部数据的交互。

仓颉编程语言将标准输入输出、文件操作、网络数据流、字符串流、加密流、压缩流等等形式的操作，统一用 Stream 描述。

Stream 主要面向处理原始二进制数据，Stream 中最小的数据单元是 `Byte`。

仓颉编程语言将 Stream 定义成了 `interface`，它让不同的 Stream 可以用装饰器模式进行组合，极大地提升了可扩展性。

## 输入流

程序从输入流读取数据源（数据源包括外界的键盘、文件、网络等），即输入流是将数据源读入到程序的通信通道。

仓颉编程语言用 `InputStream` 接口类型来表示输入流，它提供了 `read` 函数，这个函数会将可读的数据写入到 `buffer` 中，返回值表示了该次读取的字节总数。

InputStream 接口定义：

<!-- run -->

```cangjie
interface InputStream {
    func read(buffer: Array<Byte>): Int64
}
```

当拥有一个输入流的时候，就可以像下面的代码那样去读取字节数据，读取的数据会被写到 `read` 的入参数组中。

输入流读取示例：

```cangjie
import std.io.InputStream

main() {
    let input: InputStream = ...
    let buf = Array<Byte>(256, repeat: 0)
    while (input.read(buf) > 0) {
        println(buf)
    }
}
```

## 输出流

程序向输出流写入数据。输出流是将程序中的数据输出到外界（显示器、打印机、文件、网络等）的通信通道。

仓颉编程语言用 `OutputStream` 接口类型来表示输出流，它提供了 `write` 函数，这个函数会将 `buffer` 中的数据写入到绑定的流中。

特别的，有一些输出流的 `write` 不会立即写到外存中，而是有一定的缓冲策略，只有当符合条件或主动调用 `flush` 时才会真实写入，目的是提高性能。

为了统一处理这些 `flush` 操作，在 `OutputStream` 中有一个 `flush` 的默认实现，它有助于抹平 API 调用的差异性。

OutputStream 接口定义：

```cangjie
interface OutputStream {
    func write(buffer: Array<Byte>): Unit

    func flush(): Unit {
        // 空实现
    }
}
```

当拥有一个输出流时，可以写入字节数据。

输出流写入示例：

```cangjie
import std.io.OutputStream

main() {
    let output: OutputStream = ...
    let buf = Array<Byte>(256, repeat: 111)
    output.write(buf)
    output.flush()
}
```

## 数据流分类

按照数据流职责上的差异，可以将 Stream 简单分成两类：

- 节点流：直接提供数据源，节点流的构造方式通常是依赖某种直接的外部资源（如文件、网络等）。
- 处理流：只能代理其他数据流进行处理，处理流的构造方式通常是依赖其他的流。


---

<!-- Content from source_zh_cn/Basic_IO/basic_IO_source_stream.md -->
# I/O 节点流

节点流是指直接提供数据源的流，节点流的构造方式通常是依赖某种直接的外部资源（如文件、网络等）。

仓颉编程语言中常见的节点流包含标准流（StdIn、StdOut、StdErr）、文件流（File）、网络流（Socket）等。

本章介绍标准流和文件流。

## 标准流

标准流包含标准输入流（stdin）、标准输出流（stdout）和标准错误输出流（stderr）。

标准流是程序与外部数据交互的标准接口。程序运行的时候从输入流读取数据，作为程序的输入，程序运行过程中输出的信息被传送到输出流，类似的，错误信息被传送到错误流。

在仓颉编程语言中可以使用 `Console` 类型来分别访问它们。

使用 `Console` 类型需要导入 `console` 包：

导入 console 包示例：

<!-- run -->

```cangjie
import std.console.*
```

`Console` 对三个标准流都进行了易用性封装，提供了更方便的基于 `String` 的扩展操作，并且对于很多常见类型都提供了丰富的重载来优化性能。

其中最重要的是 `Console` 提供了并发安全的保证，可以在任意线程中安全地通过 `Console` 提供的接口来读写内容。

默认情况下标准输入流来源于键盘输入的信息，例如在命令行界面中输入的文本。

当需要从标准输入流中获取数据时，可以通过 `stdIn` 来读取，例如通过 `readln` 函数来获取命令行的输入。

标准输入流读取示例：

<!-- run -->

```cangjie
import std.console.Console

main() {
    let txt = Console.stdIn.readln()
    println(txt ?? "")
}
```

运行上面的代码，在命令行上输入一些文字，然后换行结束，即可看到输入的内容。

输出流分为标准输出流和标准错误流，默认情况下，它们都会输出到屏幕，例如在命令行界面中看到的文本。

当需要往标准输出流中写入数据时，可以通过 `stdOut`/`stdErr` 来写入，例如通过 `write` 函数来向命令打印内容。

使用 `stdOut` 和直接使用 `print` 函数的差别是，`stdOut` 是并发安全的，并且由于 `stdOut` 使用了缓存技术，在输入内容较多时拥有更好的性能表现。

需要注意的是，写完数据后需要对 `stdOut` 调用 `flush` 才能保证内容被写到标准流中。

标准输出流写入示例：

<!-- run -->

```cangjie
import std.console.Console

main() {
    for (i in 0..1000) {
        Console.stdOut.writeln("hello, world!")
    }
    Console.stdOut.flush()
}
```

## 文件流

仓颉编程语言提供了 `fs` 包来支持通用文件系统任务。不同的操作系统对于文件系统提供的接口有所不同。仓颉编程语言抽象出以下一些共通的功能，通过统一的功能接口，屏蔽不同操作系统之间的差异，来简化使用。

常规操作任务包括：创建文件/目录、读写文件、重命名或移动文件/目录、删除文件/目录、复制文件/目录、获取文件/目录元数据、检查文件/目录是否存在。具体 API 可以查阅库文档。

使用文件系统相关的功能需要导入 `fs` 包：

导入 fs 包示例：

<!-- run -->

```cangjie
import std.fs.*
```

本章会着重介绍 `File` 相关的使用，对于 `Path` 和 `Directory` 的使用可以查阅对应的 API 文档。

`File` 类型在仓颉编程语言中同时提供了常规文件操作和文件流两类功能。

### 常规文件操作

对于常规的文件操作，可以使用一系列静态函数来完成快捷的操作。

例如如果要检查某个路径对应的文件是否存在，可以使用 `exists` 函数。当 `exists` 函数返回 `true` 时表示文件存在，反之不存在。

exists 函数使用示例：

<!-- run -->

```cangjie
import std.fs.exists

main() {
    let exist = exists("./tempFile.txt")
    println("exist: ${exist}")
}
```

移动文件、拷贝文件和删除文件也非常简单，`File` 同样提供了对应的静态函数 `move`、`copy`、`delete`。

move、copy、delete 函数使用示例：

<!-- compile -->

```cangjie
import std.fs.{copy, rename, remove}

main() {
    copy("./tempFile.txt", to: "./tempFile2.txt", overwrite: false)
    rename("./tempFile2.txt",  to: "./tempFile3.txt", overwrite: false)
    remove("./tempFile3.txt")
}
```

如果需要直接将文件的所有数据读出来，或者一次性将数据写入文件里，可以使用 `File` 提供的 `readFrom`、`writeTo` 函数直接读写文件。在数据量较少的情况下它们既简单易用又能提供较好的性能表现，无需手动处理数据流。

readFrom、writeTo 函数使用示例：

<!-- compile -->

```cangjie
import std.fs.File

main() {
    let bytes = File.readFrom("./tempFile.txt") // 一次性读取了所有的数据
    File.writeTo("./otherFile.txt", bytes) // 把数据一次性写入另一个文件中
}
```

### 文件流操作

除了上述的常规文件操作之外，`File` 类型也被设计为一种数据流类型，因此 `File` 类型本身实现了 `IOStream` 接口。当创建了一个 `File` 的实例，可以把这个实例当成数据流来使用。

File 类定义：

```cangjie
public class File <: Resource & IOStream & Seekable {
    ...
}
```

`File` 提供了两种构造方式，一种是通过方便的静态函数 `create` 直接创建新文件的实例，另一种是通过构造函数传入完整的打开文件模式来构造新实例。

其中 `create` 创建的文件是只写的，不能对实例进行读操作，否则会抛出运行时异常。

File 构造示例：

<!-- compile -->

```cangjie
// 创建
internal import std.fs.*
internal import std.io.*

main() {
    let file = File.create("./tempFile.txt")
    file.write("hello, world!".toArray())

    // 打开
    let file2 = File("./tempFile.txt", Read)
    let bytes = readToEnd(file2) // 读取所有数据
    println(bytes)
}
```

当需要更精细的打开模式时，可以使用构造函数传入一个 `OpenMode` 值。`OpenMode` 是一个 `enum` 类型，它提供了丰富的文件打开模式，包含 `Read`、`Write`、`Append` 和 `ReadWrite` 模式。

File 打开模式使用示例：

```cangjie
// 使用指定选项打开模式
let file = File("./tempFile.txt", Write)
```

因为打开 `File` 的实例会占用宝贵的系统资源，所以使用完 `File` 的实例之后需要注意及时关闭 `File`，以释放系统资源。

`File` 实现了 `Resource` 接口，在大多数时候都可以使用 try-with-resource 语法来简化使用。

try-with-resource 语法使用示例：

```cangjie
try (file2 = File("./tempFile.txt", Read)) {
    ...
    // 结束使用后自动释放文件
}
```


---

<!-- Content from source_zh_cn/Basic_IO/basic_IO_process_stream.md -->
# I/O 处理流

处理流是指代理其他数据流进行处理的流。

仓颉编程语言中常见的处理流包含 `BufferedInputStream`、`BufferedOutputStream`、`StringReader`、`StringWriter`、`ChainedInputStream` 等。

本章介绍缓冲流和字符串流。

## 缓冲流

由于涉及磁盘的 I/O 操作相比内存的 I/O 操作要慢很多，所以对于高频次且小数据量的读写操作来说，不带缓冲的数据流效率很低，每次读取和写入数据都会带来大量的 I/O 耗时。而带缓冲的数据流，可以多次读写数据，但不触发磁盘 I/O 操作，只是先放到内存里。等凑够了缓冲区大小的时候再一次性操作磁盘，这种方式可以显著减少磁盘操作次数，从而提升性能表现。

仓颉编程语言标准库提供了 `BufferedInputStream` 和 `BufferedOutputStream` 这两个类型用来提供缓冲功能。

使用 `BufferedInputStream` 和 `BufferedOutputStream` 类型需要导入 `io` 包。

导入 io 包示例：

<!-- run -->

```cangjie
import std.io.*
```

`BufferedInputStream` 的作用是为另一个输入流添加缓冲的功能。本质上 `BufferedInputStream` 是通过一个内部缓冲数组实现的。

当通过 `BufferedInputStream` 来读取流的数据时，`BufferedInputStream` 会一次性读取整个缓冲区大小的数据，再使用 `read` 函数就可以分多次读取更小规模的数据；当缓冲区中的数据被读完之后，输入流就会再次填充缓冲区；如此反复，直到读完数据流的所有数据。

如果构造一个 `BufferedInputStream`，只需要在构造函数中传入另一个输入流。如果需要指定缓冲区的大小，也可以额外传入 `capacity` 参数进行指定。

BufferedInputStream 构造示例：

<!-- run -->

```cangjie
import std.io.{ByteBuffer, BufferedInputStream}

main(): Unit {
    let arr1 = "0123456789".toArray()
    let byteBuffer = ByteBuffer()
    byteBuffer.write(arr1)
    let bufferedInputStream = BufferedInputStream(byteBuffer)
    let arr2 = Array<Byte>(20, repeat: 0)

    /* 读取流中数据，返回读取到的数据的长度 */
    let readLen = bufferedInputStream.read(arr2)
    println(String.fromUtf8(arr2[..readLen])) // 0123456789
}
```

`BufferedOutputStream` 的作用是为另一个输出流添加缓冲的功能。BufferedOutputStream 也是通过一个内部缓冲数组实现的。

当通过 `BufferedOutputStream` 来向输出流写入数据时，`write` 的数据会先写入内部缓冲数组中；当缓冲区中的数据被填满之后，`BufferedOutputStream` 会将缓冲区的数据一次性写入输出流中，然后清空缓冲区再次被写入；如此反复，直到写完所有的数据。

需要注意的是，由于没写够缓冲区时不会触发输出流的写入操作，所以当往 `BufferedOutputStream` 写完所有的数据后，需要额外调用 `flush` 函数来最终完成写入。

如果构造一个 `BufferedOutputStream`，只需要在构造函数中传入另一个输出流。如果需要指定缓冲区的大小，也可以额外传入 `capacity` 参数指定。

BufferedOutputStream 构造示例：

<!-- run -->

```cangjie
import std.io.{ByteBuffer, BufferedOutputStream, readToEnd}

main(): Unit {
    let arr1 = "01234".toArray()
    let byteBuffer = ByteBuffer()
    byteBuffer.write(arr1)
    let bufferedOutputStream = BufferedOutputStream(byteBuffer)
    let arr2 = "56789".toArray()

    /* 向流中写入数据，此时数据在外部流的缓冲区中 */
    bufferedOutputStream.write(arr2)

    /* 调用 flush 函数，真正将数据写入内部流中 */
    bufferedOutputStream.flush()
    println(String.fromUtf8(readToEnd(byteBuffer))) // 0123456789
}
```

## 字符串流

由于仓颉编程语言的输入流和输出流是基于字节数据来抽象的（拥有更好的性能），在部分以字符串为主的场景中使用起来不太友好，例如往文件里写入大量的文本内容时，需要将文本内容转换成字节数据，再写入文件。

为了提供友好的字符串操作能力，仓颉编程语言提供了 `StringReader` 和 `StringWriter` 来添加字符串处理能力。

使用 `StringReader` 和 `StringWriter` 类型需要导入 `io` 包：

导入 io 包示例：

<!-- run -->

```cangjie
import std.io.*
```

`StringReader` 提供了按行读、按筛选条件读的能力，相比将字节数据读出来再手动转换成字符串，具有更好的性能表现和易用性。

如果构造 `StringReader`，传入另一个输入流即可。

StringReader 使用示例：

<!-- run -->

```cangjie
import std.io.{ByteBuffer, StringReader}

main(): Unit {
    let arr1 = "012\n346789".toArray()
    let byteBuffer = ByteBuffer()
    byteBuffer.write(arr1)
    let stringReader = StringReader(byteBuffer)

    /* 读取一行数据 */
    let line = stringReader.readln()
    println(line ?? "error") // 012
}
```

`StringWriter` 提供了直接写字符串、按行直接写字符串的能力，相比将字节数据手动转换成字符串再写入，具有更好的性能表现和易用性。

如果构造 `StringWriter`，传入另一个输出流即可。

StringWriter 使用示例：

<!-- run -->

```cangjie
import std.io.{ByteBuffer, StringWriter, readToEnd}

main(): Unit {
    let byteBuffer = ByteBuffer()
    let stringWriter = StringWriter(byteBuffer)

    /* 写入字符串 */
    stringWriter.write("number")

    /* 写入字符串并自动转行 */
    stringWriter.writeln(" is:")

    /* 写入数字 */
    stringWriter.write(100.0f32)

    stringWriter.flush()

    println(String.fromUtf8(readToEnd(byteBuffer))) // number is:\n100.000000
}
```


---

<!-- Content from source_zh_cn/Net/net_overview.md -->
# 网络编程概述

网络通信是两个设备通过计算机网络进行数据交换的过程。通过编写软件达成网络通信的行为即为网络编程。

仓颉为开发者提供了基础的网络编程功能，在仓颉标准库中，开发者可使用 std 模块下的 socket 包来实现传输层网络通信。

在传输层协议中，分为不可靠传输和可靠传输两种，仓颉将其抽象为 DatagramSocket 和 StreamSocket。其中不可靠传输协议常见的是 UDP，可靠传输协议常见的是 TCP，仓颉分别将其抽象为 UdpSocket 和 TcpSocket。另外，仓颉也实现了对传输层 Unix Domain 协议的支持，并支持其通过可靠和不可靠传输两种方式进行通信。

而在应用层协议中，较为常见的是 HTTP 协议，常用于开发 Web 应用程序等。当前 HTTP 协议已有多个版本，仓颉目前支持 HTTP/1.0、HTTP/1.1、HTTP/2.0。

另外，WebSocket 作为一种提升 Web 服务端与客户端间的通信效率的应用层协议，仓颉将其抽象为 WebSocket 对象，并支持从 HTTP 协议升级至 WebSocket 协议。

需要注意的是，仓颉的网络编程是阻塞式的。但被阻塞的是仓颉线程，阻塞中的仓颉线程会将系统线程让渡出去，因此并不会真正阻塞一个系统线程。


---

<!-- Content from source_zh_cn/Net/net_socket.md -->
# Socket 编程

仓颉的 Socket 编程指的是基于传输层协议实现网络传输数据包的功能。

在可靠传输场景下，仓颉分别启动客户端套接字和服务端套接字。客户端套接字必须指定将要连接的远端地址，可选择性地绑定本端地址，在连接成功后，才可以收发报文。而服务端套接字必须绑定本端地址，在绑定成功后，才可以收发报文。

在不可靠传输场景下，套接字无需区分客户端和服务端，仓颉分别启动两个套接字进行数据传输。套接字必须绑定本端地址，绑定成功后，才可以收发报文。并且，套接字也可选择性地指定远端连接地址，指定后将仅接受指定的远端地址的报文，同时在 send 时无需指定远端地址，报文将发送至成功连接的地址。

## TCP 编程

TCP 作为一种常见的可靠传输协议，以 TCP 类型套接字举例，仓颉在可靠传输场景下的可参考的编程模型如下：

1. 创建服务端套接字，并指定本端绑定地址。
2. 执行绑定。
3. 执行 accept 动作，将阻塞等待，直到获取到一个客户端套接字连接。
4. 同步创建客户端套接字，并指定远端的待连接的地址。
5. 执行连接。
6. 连接成功后，服务端会在 accept 接口返回一个新的套接字，此时服务端可以通过此套接字进行读写操作，即收发报文。客户端则可以直接进行读写操作。

TCP 服务端和客户端程序示例如下：

<!-- verify -->

```cangjie
import std.time.*
import std.sync.*
import std.net.*

var SERVER_PORT: UInt16 = 0

func runTcpServer() {
    try (serverSocket = TcpServerSocket(bindAt: SERVER_PORT)) {
        serverSocket.bind()
        SERVER_PORT = (serverSocket.localAddress as IPSocketAddress)?.port ?? 0

        try (client = serverSocket.accept()) {
            let buf = Array<Byte>(10, repeat: 0)
            let count = client.read(buf)

            // 服务端读取到的数据为: [1, 2, 3, 0, 0, 0, 0, 0, 0, 0]
            println("Server read ${count} bytes: ${buf}")
        }
    }
}

main(): Int64 {
    let future = spawn {
        runTcpServer()
    }
    sleep(Duration.millisecond * 500)

    try (socket = TcpSocket("127.0.0.1", SERVER_PORT)) {
        socket.connect()
        socket.write([1, 2, 3])
    }

    future.get()

    return 0
}
```

编译执行上述代码，将打印：

```text
Server read 3 bytes: [1, 2, 3, 0, 0, 0, 0, 0, 0, 0]
```

## UDP 编程

UDP 作为一种常见的不可靠传输协议，以 UDP 类型套接字举例，仓颉在不可靠传输场景下的可参考的编程模型如下：

1. 创建套接字，并指定本端绑定地址。
2. 执行绑定。
3. 指定远端地址进行报文发送。
4. 不连接远端地址场景下，可以收取来自不同远端地址的报文，并返回远端地址信息。

UDP 收发报文程序示例如下：

<!-- verify -->

```cangjie
import std.time.*
import std.sync.*
import std.net.*

let SERVER_PORT: UInt16 = 8080

func runUpdServer() {
    try (serverSocket = UdpSocket(bindAt: SERVER_PORT)) {
        serverSocket.bind()

        let buf = Array<Byte>(3, repeat: 0)
        let (clientAddr, count) = serverSocket.receiveFrom(buf)
        let sender = (clientAddr as IPSocketAddress)?.address.toString() ?? ""

        // Server receive 3 bytes: [1, 2, 3] from 127.0.0.1
        println("Server receive ${count} bytes: ${buf} from ${sender}")
    }
}

main(): Int64 {
    let future = spawn {
        runUpdServer()
    }
    sleep(Duration.second)

    try (udpSocket = UdpSocket(bindAt: 0)) {
        udpSocket.sendTimeout = Duration.second * 2
        udpSocket.bind()
        udpSocket.sendTo(
            IPSocketAddress("127.0.0.1", SERVER_PORT),
            [1, 2, 3]
        )
    }

    future.get()

    return 0
}
```

编译执行上述代码，将打印：

```text
Server receive 3 bytes: [1, 2, 3] from 127.0.0.1
```


---

<!-- Content from source_zh_cn/Net/net_http.md -->
# HTTP 编程

HTTP 作为一种通用的应用层协议，通过请求-响应的机制实现数据传输，客户端发送请求，服务端返回响应。请求和响应的格式是固定的，由报文头和报文体组成。

常用的请求类型为 GET 和 POST，GET 请求只有报文头，用于向服务器请求应用层数据，POST 请求带有报文体，以一个空行与报文头进行分隔，用于向服务器提供应用层数据。

请求-响应的报文头字段内容较多，此处不再一一赘述，仓颉支持 HTTP 1.0/1.1/2.0 等协议版本，开发者可以基于协议 RFC 9110、9112、9113、9218、7541 以及仓颉所提供的 HttpRequestBuilder 和 HttpResponseBuilder 类构造请求及响应报文。

以下示例展示了如何使用仓颉进行客户端和服务端编程，实现的功能是客户端发送请求头为 GET /hello 的请求，服务端返回响应，响应体为 \"Hello Cangjie!\"，代码如下:

> **说明：**
>
> net、log 等库已从仓颉 SDK 移到 stdx 模块，使用前需要下载软件包，并在 cjpm.toml 中配置。

<!-- verify -->

```cangjie
import stdx.net.http.*
import std.time.*
import std.sync.*
import stdx.log.*

// 1. 构建 Server 实例
let server = ServerBuilder()
    .addr("127.0.0.1")
    .port(0)
    .build()

func startServer(): Unit {
    // 2. 注册请求处理逻辑
    server.distributor.register("/hello", {httpContext =>
        httpContext.responseBuilder.body("Hello Cangjie!")
    })
    server.logger.level = LogLevel.OFF
    // 3. 启动服务
    server.serve()
}

func startClient(): Unit {
    // 1. 构建 client 实例
    let client = ClientBuilder().build()
    // 2. 发送 request
    let response = client.get("http://127.0.0.1:${server.port}/hello")
    // 3. 读取response body
    let buffer = Array<Byte>(32, repeat: 0)
    let length = response.body.read(buffer)
    println(String.fromUtf8(buffer[..length]))
    // 4. 关闭连接
    client.close()
}

main () {
    spawn {
        startServer()
    }
    sleep(Duration.second)
    startClient()
}
```

编译执行上述代码，将打印：

```text
Hello Cangjie!
```


---

<!-- Content from source_zh_cn/Net/net_websocket.md -->
# WebSocket 编程

在网络编程中，WebSocket 是一种常用的应用层协议。与 HTTP 一样，它也基于 TCP 协议之上，并且常用于 web 服务端应用开发。

不同于 HTTP 的是， WebSocket 只需要客户端和服务端进行一次握手，即可创建长久的连接，并且进行双向的数据传输。即基于 WebSocket 实现的服务端可以主动传输数据给客户端，从而实现实时通讯。

WebSocket 是一个独立的协议，它与 HTTP 的关联在于，它的握手被 HTTP 服务端解释为一个升级请求。因此，仓颉将 WebSocket 包含在 http 包中。

仓颉将 WebSocket 协议通信机制抽象为 WebSocket 类，提供方法将一个 http/1.1 或 http/2.0 服务端句柄升级到 WebSocket 协议实例，通过返回的 WebSocket 实例进行 WebSocket 通信，例如数据报文的读写。

在仓颉中，WebSocket 所传输的数据基本单元称为帧，帧分为两类，一类为传输控制信息的帧，即 Close Frame 用于关闭连接， Ping Frame 用于实现 Keep-Alive ， Pong Frame 是 Ping Frame 的响应类型，另一类是传输应用数据的帧，应用数据帧支持分段传输。

仓颉的帧由三个属性构成，其中 fin 和 frameType 共同说明了帧是否分段和帧的类型，payload 为帧的载荷，除此之外开发者无需关心其他属性即可进行报文传输。

如下示例展示了 WebSocket 的握手以及消息收发过程：创建 HTTP 客户端和服务端，分别发起 WebSocket 升级（或握手），握手成功后开始帧的读写。

> **说明：**
>
> net、encoding、log 等库已从仓颉 SDK 移到 stdx 模块，使用前需要下载软件包，并在 cjpm.toml 中配置。

<!-- verify -->

```cangjie
import stdx.net.http.*
import stdx.encoding.url.*
import std.time.*
import std.sync.*
import std.collection.*
import stdx.log.*

let server = ServerBuilder()
                        .addr("127.0.0.1")
                        .port(0)
                        .build()

// client：
main() {
    // 1 启动服务器
    spawn { startServer() }
    sleep(Duration.millisecond * 200)

    let client = ClientBuilder().build()
    let u = URL.parse("ws://127.0.0.1:${server.port}/webSocket")

    let subProtocol = ArrayList<String>(["foo1", "bar1"])
    let headers = HttpHeaders()
    headers.add("test", "echo")

    // 2 完成 WebSocket 握手，获取 WebSocket 实例
    let websocket: WebSocket
    let respHeaders: HttpHeaders
    (websocket, respHeaders) = WebSocket.upgradeFromClient(client, u, subProtocols: subProtocol, headers: headers)
    client.close()

    println("subProtocol: ${websocket.subProtocol}")      // fool1
    println(respHeaders.getFirst("rsp") ?? "") // echo

    // 3 消息收发
    // 发送 hello
    websocket.write(TextWebFrame, "hello".toArray())
    // 收
    let data = ArrayList<UInt8>()
    var frame = websocket.read()
    while(true) {
        match(frame.frameType) {
            case ContinuationWebFrame =>
                data.add(all: frame.payload)
                if (frame.fin) {
                    break
                }
            case TextWebFrame | BinaryWebFrame =>
                if (!data.isEmpty()) {
                    throw Exception("invalid frame")
                }
                data.add(all: frame.payload)
                if (frame.fin) {
                    break
                }
            case CloseWebFrame =>
                websocket.write(CloseWebFrame, frame.payload)
                break
            case PingWebFrame =>
                websocket.writePongFrame(frame.payload)
            case _ => ()
        }
        frame = websocket.read()
    }
    println("data size: ${data.size}")      // 4097
    println("last item: ${String.fromUtf8(data.toArray()[4096])}")        // a


    // 4 关闭 websocket，
    // 收发 CloseFrame
    websocket.writeCloseFrame(status: 1000)
    let websocketFrame = websocket.read()
    println("close frame type: ${websocketFrame.frameType}")      // CloseWebFrame
    println("close frame payload: ${websocketFrame.payload}")     // 3, 232
    // 关闭底层连接
    websocket.closeConn()

    server.close()
}

func startServer() {
    // 1 注册 handler
    server.distributor.register("/webSocket", handler1)
    server.logger.level = LogLevel.OFF
    server.serve()
}

// server:
func handler1(ctx: HttpContext): Unit {
    // 2 完成 websocket 握手，获取 websocket 实例
    let websocketServer = WebSocket.upgradeFromServer(ctx, subProtocols: ArrayList<String>(["foo", "bar", "foo1"]),
        userFunc: {request: HttpRequest =>
            let value = request.headers.getFirst("test") ?? ""
            let headers = HttpHeaders()
            headers.add("rsp", value)
            headers
        })
    // 3 消息收发
    // 收 hello
    let data = ArrayList<UInt8>()
    var frame = websocketServer.read()
    while(true) {
        match(frame.frameType) {
            case ContinuationWebFrame =>
                data.add(all: frame.payload)
                if (frame.fin) {
                    break
                }
            case TextWebFrame | BinaryWebFrame =>
                if (!data.isEmpty()) {
                    throw Exception("invalid frame")
                }
                data.add(all: frame.payload)
                if (frame.fin) {
                    break
                }
            case CloseWebFrame =>
                websocketServer.write(CloseWebFrame, frame.payload)
                break
            case PingWebFrame =>
                websocketServer.writePongFrame(frame.payload)
            case _ => ()
        }
        frame = websocketServer.read()
    }
    println("data: ${String.fromUtf8(data.toArray())}")    // hello
    // 发 4097 个 a
    websocketServer.write(TextWebFrame, Array<UInt8>(4097, repeat: 97))

    // 4 关闭 websocket，
    // 收发 CloseFrame
    let websocketFrame = websocketServer.read()
    println("close frame type: ${websocketFrame.frameType}")   // CloseWebFrame
    println("close frame payload: ${websocketFrame.payload}")     // 3, 232
    websocketServer.write(CloseWebFrame, websocketFrame.payload)
    // 关闭底层连接
    websocketServer.closeConn()
}
```

该示例运行结果如下：

```text
subProtocol: foo1
echo
data: hello
data size: 4097
last item: a
close frame type: CloseWebFrame
close frame payload: [3, 232]
close frame type: CloseWebFrame
close frame payload: [3, 232]
```


---

<!-- Content from source_zh_cn/Macro/macro_introduction.md -->
# 宏的简介

宏可以理解为一种特殊的函数。一般的函数在输入的值上进行计算，然后输出一个新的值，而宏的输入和输出都是程序本身。在输入一段程序后，输出一段新的程序，这段输出的程序随后用于编译和执行。为了把宏的调用和函数调用区分开来，在调用宏时需使用 `@` 加上宏的名称。

如下示例代码希望实现在调试过程中打印某个表达式的值，同时打印出表达式本身。

```cangjie
let x = 3
let y = 2
@dprint(x)        // 打印 "x = 3"
@dprint(x + y)    // 打印 "x + y = 5"
```

显然，`dprint` 不能被写为常规的函数，因为函数只能获得输入表达式的值，不能获得输入表达式本身。但是，可以将 `dprint` 实现为一个宏来获取输入表达式的程序片段。一个基本的实现如下：

<!-- verify -macro12 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define

import std.ast.*

public macro dprint(input: Tokens): Tokens {
    let inputStr = input.toString()
    let result = quote(
        print($(inputStr) + " = ")
        println($(input)))
    return result
}
```

在解释每行代码之前，先测试这个宏可以达到预期的效果。首先，在当前目录下创建一个 `define` 文件夹，并在 `define` 文件夹中创建 `dprint.cj` 文件，将以上内容复制到 `dprint.cj` 文件中。另外在当前目录下创建 `main.cj`，包含以下测试代码：

<!-- verify -macro12 -->

```cangjie
import define.*

main() {
    let x = 3
    let y = 2
    @dprint(x)
    @dprint(x + y)
}
```

请注意，得到的目录结构如下：

```text
// Directory layout.
src
|-- define
|     `-- dprint.cj
`-- main.cj
```

在当前目录（`src`）下，运行编译命令：

```bash
cjc define/*.cj --compile-macro
cjc main.cj -o main
```

然后运行 `./main`，可以看到如下输出：

<!-- verify -macro12 -->

```text
x = 3
x + y = 5
```

依次查看代码的每个部分：

- 第 1 行：`macro package define`

  宏必须声明在独立的包中（不能和其他 public 函数一起），含有宏的包使用 `macro package` 来声明。这里声明了一个名为 `define` 的宏包。

- 第 2 行：`import std.ast.*`

  实现宏需要的数据类型，例如 `Tokens` 和后面会讲到的语法节点类型，位于仓颉标准库的 `ast` 包中，因此任何宏的实现都需要首先引入 `ast` 包。

- 第 3 行：`public macro dprint(input: Tokens): Tokens`

  在这里声明一个名为 `dprint` 的宏。由于这个宏是一个非属性宏（之后会解释这个概念），它接受一个类型为 `Tokens` 的参数。该输入代表传给宏的程序片段。宏的返回值也是一个程序片段。

- 第 4 行：`let inputStr = input.toString()`

  在宏的实现中，首先将输入的程序片段转化为字符串。在前面的测试案例中，`inputStr` 成为 `"x"` 或 `"x + y"`

- 第 5-7 行：`let result = quote(...)`

  这里 [`quote` 表达式](./Tokens_types_and_quote_expressions.md#quote-表达式和插值)是用于构造 [`Tokens`](./Tokens_types_and_quote_expressions.md#tokens-类型) 的一种表达式，它将括号内的程序片段转换为 `Tokens`。在 `quote` 的输入中，可以使用插值 `$(...)` 来将括号内的表达式转换为 `Tokens`，然后插入到 `quote` 构建的 `Tokens` 中。对于以上代码，`$(inputStr)` 中插入了 `inputStr` 字符串的值（包含字符串两端的引号），`$(input)` 中插入了 `input`，即输入的程序片段。因此，如果输入的表达式是 `x + y`，那么形成的`Tokens`为：

  ```cangjie
  print("x + y" + " = ")
  println(x + y)
  ```

- 第 8 行：`return result`

  最后，将构造出来的代码片段返回，这两行代码片段将被编译，运行时将输出 `x + y = 5`。

回顾 `dprint` 宏的定义，`dprint` 使用 `Tokens` 作为入参，并使用 `quote` 和插值构造了另一个 `Tokens` 作为返回值。为了使用宏，需要详细了解 `Tokens`、`quote` 和插值的概念，下面将分别介绍它们。


---

<!-- Content from source_zh_cn/Macro/Tokens_types_and_quote_expressions.md -->
# Tokens 相关类型和 quote 表达式

## Token 类型

宏操作的基本类型是 `Tokens`，代表一个程序片段。`Tokens` 由若干个 `Token` 组成，每个 `Token` 可以理解为用户可操作的词法单元。一个 `Token` 可能是一个标识符（例如变量名等）、字面量（例如整数、浮点数、字符串）、关键字或运算符。每个 `Token` 包含它的类型、内容和位置信息。

`Token` 的类型取值为 enum `TokenKind` 中的元素。`TokenKind` 的可用值详见《仓颉编程语言库 API》文档。通过提供 `TokenKind` 和 `Token` 的值（`TokenKind` 对应的标识符或字面量），可以直接构造任何 `Token`。具体的构造函数如下：

```cangjie
Token(k: TokenKind)
Token(k: TokenKind, v: String)
```

下面给出一些`Token`构造的例子：

<!-- compile -->

```cangjie
import std.ast.*

let tk1 = Token(TokenKind.ADD)   // '+' 运算符
let tk2 = Token(TokenKind.FUNC)   // func 关键字
let tk3 = Token(TokenKind.IDENTIFIER, "x")   // x 标识符
let tk4 = Token(TokenKind.INTEGER_LITERAL, "3")  // 整数字面量
let tk5 = Token(TokenKind.STRING_LITERAL, "xyz")  // 字符串字面量
```

## Tokens 类型

一个 `Tokens` 代表由多个 `Token` 组成的序列。可以通过 `Token` 数组直接构造 `Tokens`。下面是 3 种基本的构造 `Tokens` 实例的方式：

```cangjie
Tokens()   // 构造空列表
Tokens(tks: Array<Token>)
Tokens(tks: ArrayList<Token>)
```

此外，`Tokens` 类型支持以下功能：

- `size`：返回 `Tokens` 中包含 `Token` 的数量
- `get(index: Int64)`：获取指定下标的 `Token` 元素
- `[]`：获取指定下标的 `Token` 元素
- `+`：拼接两个 `Tokens`，或者直接拼接 `Tokens` 和 `Token`
- `dump()`：打印包含的所有 `Token`，供调试使用
- `toString()`：打印 `Tokens` 对应的程序片段

在下面的案例中，使用构造函数直接构造 `Token` 和 `Tokens`，然后打印详细的调试信息：

<!-- run -->

```cangjie
import std.ast.*

let tks = Tokens([
    Token(TokenKind.INTEGER_LITERAL, "1"),
    Token(TokenKind.ADD),
    Token(TokenKind.INTEGER_LITERAL, "2")
])
main() {
    println(tks)
    tks.dump()
}
```

预期输出如下（具体的位置信息可能不同）：

```text
1 + 2
description: integer_literal, token_id: 140, token_literal_value: 1, fileID: 1, line: 4, column: 5
description: add, token_id: 12, token_literal_value: +, fileID: 1, line: 5, column: 5
description: integer_literal, token_id: 140, token_literal_value: 2, fileID: 1, line: 6, column: 5
```

在 dump 信息中，包含了每个 `Token` 的类型（`description`）和值（`token_literal_value`），最后打印每个 `Token` 的位置信息。

## quote 表达式和插值

在大多数情况下，直接构造和拼接 `Tokens` 会比较繁琐。因此，仓颉语言提供了 `quote` 表达式来从代码模板构造 `Tokens`。之所以说是代码模板，因为在 `quote` 中可以使用 `$(...)` 来插入上下文中的表达式。插入的表达式的类型需要支持被转换为 `Tokens`（具体来说，实现了 `ToTokens` 接口）。在标准库中，以下类型实现了 `ToTokens` 接口：

- 所有的节点类型（节点将在[语法节点](./sytax_node.md)中讨论）
- `Token` 和 `Tokens` 类型
- 所有基础数据类型：整数、浮点数、`Bool`、`Rune` 和 `String`
- `Array<T>` 和 `ArrayList<T>`，这里对 `T` 的类型有限制，并根据 `T` 的类型不同，输出不同的分隔符，详细请见《仓颉编程语言库 API》文档。

下面的例子展示 `Array` 和基础数据类型的插值：

<!-- verify -->

```cangjie
import std.ast.*

let intList: Array<Int64> = [1, 2, 3, 4, 5]
let float: Float64 = 1.0
let str: String = "Hello"
let tokens = quote(
    arr = $(intList)
    x = $(float)
    s = $(str)
)

main() {
    println(tokens)
}
```

输出结果是：

```text

arr =[1, 2, 3, 4, 5]
x = 1.0
s = "Hello"

```

更多插值的用法可以参考  [使用 quote 插值语法节点](./sytax_node.md#使用-quote-插值语法节点)。

特别地，当 `quote` 表达式包含某些特殊 `Token` 时，需要进行转义：

- `quote` 表达式中不允许出现不匹配的小括号，但是通过 `\` 转义的小括号，不计入小括号的匹配规则。
- 当 `$` 表示一个普通 `Token`，而非用于代码插值时，需要通过 `\` 进行转义。
- 除以上情况外，`quote` 表达式中出现 `\` 会编译报错。

> **注意：**
>
> `#` 符号仅能用于构造多行原始字符串字面量，不支持单独使用。

下面是一些 `quote` 表达式内包含这些特殊 `Token` 的例子：

<!-- compile.error -->

```cangjie
import std.ast.*

let tks1 = quote((x))       // ok
let tks2 = quote(\()        // ok
let tks3 = quote( ( \) ) )  // ok
let tks4 = quote())         // error: unmatched delimiter: ')'
let tks5 = quote( ( \) )    // error: unclosed delimiter: '('
let tks6 = quote(\$(1))     // ok
let tks7 = quote(\x)        // error: unknown start of token: \
let tks8 = quote(#)         // error: expected '#' or '"' in raw string
```


---

<!-- Content from source_zh_cn/Macro/sytax_node.md -->
# 语法节点

在仓颉语言的编译过程中，首先通过词法分析将代码转换成 `Tokens`，然后对 `Tokens` 进行语法解析，得到一个语法树。每个语法树的节点可能是一个表达式、声明、类型、模式等。仓颉标准库 `std.ast` 包提供了每种节点对应的类，它们之间具有适当的继承关系。其中，主要的抽象类如下：

- `Node`：所有语法节点的父类
- `TypeNode`：所有类型节点的父类
- `Expr`：所有表达式节点的父类
- `Decl`：所有声明节点的父类
- `Pattern`：所有模式节点的父类

具体节点的类型众多，具体细节请参见《仓颉编程语言库 API》。在下面的案例中，主要使用以下节点：

- `BinaryExpr`：二元运算表达式
- `FuncDecl`：函数的声明

## 节点的解析

通过标准库 `std.ast` 包，基本上每种节点都可以从 `Tokens` 解析。有两种解析 `Tokens` 并构造语法节点的方法。

### 使用解析函数来解析 Tokens

以下函数用于从 `Tokens` 解析并构造任意的语法节点：

- `parseExpr(input: Tokens): Expr`：将输入的 `Tokens` 解析为表达式节点。
- `parseExprFragment(input: Tokens, startFrom!: Int64 = 0): (Expr, Int64)`：将输入 `Tokens` 的一个片段解析为表达式节点，片段从 `startFrom` 索引开始，解析可能只消耗从索引 `startFrom` 开始的片段的一部分，并返回第一个未被消耗的 `Token` 的索引（如果消耗了整个片段，返回值为 `input.size`）。
- `parseDecl(input: Tokens, astKind!: String = "")`：将输入的 `Tokens` 解析为声明节点，`astKind` 为额外的设置，具体请参见《仓颉编程语言库 API》文档。
- `parseDeclFragment(input: Tokens, startFrom!: Int64 = 0): (Decl, Int64)`：将输入 `Tokens` 的一个片段解析为声明节点，`startFrom` 参数和返回索引的含义和 `parseExpr` 相同。
- `parseType(input: Tokens): TypeNode`：将输入的 `Tokens` 解析为类型节点。
- `parseTypeFragment(input: Tokens, startFrom!: Int64 = 0): (TypeNode, Int64)`：将输入 `Tokens` 的一个片段解析为类型节点，`startFrom` 参数和返回索引的含义和 `parseExpr` 相同。
- `parsePattern(input: Tokens): Pattern`：将输入的 `Tokens` 解析为模式节点。
- `parsePatternFragment(input: Tokens, startFrom!: Int64 = 0): (Pattern, Int64)`：将输入 `Tokens` 的一个片段解析为模式节点，`startFrom` 参数和返回索引的含义和 `parseExpr` 相同。

如果解析失败将抛出异常。这种解析方式适用于类型未知的代码片段，如果需要获取具体的子类型节点，需要将解析结果手动转换成具体的子类型。

这些函数的使用如下例所示：

<!-- verify -->

```cangjie
let tks1 = quote(a + b)
let tks2 = quote(u + v, x + y)
let tks3 = quote(
    func f1(x: Int64) { return x + 1 }
)
let tks4 = quote(
    func f2(x: Int64) { return x + 2 }
    func f3(x: Int64) { return x + 3 }
)

let binExpr1 = parseExpr(tks1)
let (binExpr2, mid) = parseExprFragment(tks2)
let (binExpr3, _) = parseExprFragment(tks2, startFrom: mid + 1) // 跳过逗号
println("binExpr1 = ${binExpr1.toTokens()}")
println("binExpr2 = ${binExpr2.toTokens()}, binExpr3 = ${binExpr3.toTokens()}")
let funcDecl1 = parseDecl(tks3)
let (funcDecl2, mid2) = parseDeclFragment(tks4)
let (funcDecl3, _) = parseDeclFragment(tks4, startFrom: mid2)
println("${funcDecl1.toTokens()}")
println("${funcDecl2.toTokens()}")
println("${funcDecl3.toTokens()}")
```

输出结果是：

```text
binExpr1 = a + b
binExpr2 = u + v, binExpr3 = x + y
func f1(x: Int64) {
    return x + 1
}

func f2(x: Int64) {
    return x + 2
}

func f3(x: Int64) {
    return x + 3
}
```

### 使用语法节点的构造函数来解析 Tokens

大多数语法节点都支持 `init(input: Tokens)` 构造函数，将输入的 `Tokens` 解析为相应类型的节点，例如：

<!-- run -->

```cangjie
import std.ast.*

let binExpr = BinaryExpr(quote(a + b))
let funcDecl = FuncDecl(quote(func f1(x: Int64) { return x + 1 }))
```

如果解析失败将抛出异常。这种解析方式适用于类型已知的代码片段，解析后不需要再手动转换成具体的子类型。

## 节点的组成部分

从 `Tokens` 解析出节点之后，可以查看节点的组成部分。作为例子，仅列出 `BinaryExpr` 和 `FuncDecl` 的组成部分，关于其他节点的更详细的解释请参见《仓颉编程语言库 API》文档。

- `BinaryExpr` 节点：
    - `leftExpr: Expr`：运算符左侧的表达式
    - `op: Token`：运算符
    - `rightExpr: Expr`：运算符右侧的表达式
- `FuncDecl` 节点（部分）：
    - `identifier: Token`：函数名
    - `funcParams: ArrayList<FuncParam>`：参数列表
    - `declType: TypeNode`：返回值类型
    - `block: Block`：函数体
- `FuncParam`节点（部分）：
    - `identifier: Token`：参数名
    - `paramType: TypeNode`：参数类型
- `Block`节点（部分）：
    - `nodes: ArrayList<Node>`：块中的表达式和声明

每个组成部分都是 `public mut prop`，因此可以被查看和更新。通过一些例子展示更新的结果。

### BinaryExpr 案例

<!-- verify -->

```cangjie
let binExpr = BinaryExpr(quote(x * y))
binExpr.leftExpr = BinaryExpr(quote(a + b))
println(binExpr.toTokens())

binExpr.op = Token(TokenKind.ADD)
println(binExpr.toTokens())
```

输出结果是：

```text
(a + b) * y
a + b + y
```

首先，通过解析，获得 `binExpr` 为节点 `x * y`，图示如下：

```text
    *
  /   \
 x     y
```

第二步，将左侧的节点（即 `x`）替换为 `a + b`，因此，获得的语法树如下：

```text
      *
    /   \
   +     y
  / \
 a   b
```

当输出这个语法树的时候，必须在 `a + b` 周围添加括号，得到 `(a + b) * y`（如果输出`a + b * y`，含义为先做乘法，再做加法，与语法树的含义不同）。`ast` 库具备在输出语法树时自动添加括号的功能。

第三步，将语法树根部的运算符从 `*` 替换为 `+`，因此得到语法树如下：

```text
      +
    /   \
   +     y
  / \
 a   b
```

这个语法树可以输出为 `a + b + y`，因为加法本身就是左结合的，不需要在左侧添加括号。

### FuncDecl 案例

<!-- verify -->

```cangjie
let funcDecl = FuncDecl(quote(func f1(x: Int64) { x + 1 }))
funcDecl.identifier = Token(TokenKind.IDENTIFIER, "foo")
println("Number of parameters: ${funcDecl.funcParams.size}")
funcDecl.funcParams[0].identifier = Token(TokenKind.IDENTIFIER, "a")
println("Number of nodes in body: ${funcDecl.block.nodes.size}")
let binExpr = (funcDecl.block.nodes[0] as BinaryExpr).getOrThrow()
binExpr.leftExpr = parseExpr(quote(a))
println(funcDecl.toTokens())
```

在这个案例中，首先通过解析构造出了一个 `FuncDecl` 节点，然后分别修改了该节点的函数名、参数名，以及函数体中表达式的一部分。输出结果是：

```text
Number of parameters: 1
Number of nodes in body: 1
func foo(a: Int64) {
    a + 1
}
```

## 使用 quote 插值语法节点

任何语法节点都可以在 `quote` 语句中插值，部分语法节点的 `ArrayList` 列表也可以被插值（主要对应实际情况中会出现这类节点列表的情况）。插值直接通过 `$(node)` 表达即可，其中 `node` 是任意节点类型的实例。

下面，通过一些案例展示节点的插值。

<!-- verify -->

```cangjie
var binExpr = BinaryExpr(quote(1 + 2))
let a = quote($(binExpr))
let b = quote($binExpr)
let c = quote($(binExpr.leftExpr))
let d = quote($binExpr.leftExpr)
println("a: ${a.toTokens()}")
println("b: ${b.toTokens()}")
println("c: ${c.toTokens()}")
println("d: ${d.toTokens()}")
```

输出结果是：

```text
a: 1 + 2
b: 1 + 2
c: 1
d: 1 + 2.leftExpr
```

一般来说，插值运算符后面的表达式使用小括号限定作用域，例如 `$(binExpr)`。但是当后面只跟单个标识符的时候，小括号可省略，即可写为 `$binExpr`。因此，在案例中 `a` 和 `b` 都在 `quote` 中插入了 `binExpr`节点，结果为 `1 + 2`。然而，如果插值运算符后面的表达式更复杂，不加小括号可能造成作用域出错。例如，表达式 `binExpr.leftExpr` 求值为 `1 + 2` 的左表达式，即 `1`，因此 `c` 正确赋值为 `1`。但 `d` 中的插值被解释为 `($binExpr).leftExpr`，因此结果是 `1 + 2.leftExpr`。为了明确插值的作用域，推荐在插值运算符中使用小括号。

下面的案例展示节点列表（`ArrayList`）的插值。

<!-- verify -->

```cangjie
var incrs = ArrayList<Node>()
for (i in 1..=5) {
    incrs.add(parseExpr(quote(x += $(i))))
}
var foo = quote(
    func foo(n: Int64) {
        let x = n
        $(incrs)
        x
    })
println(foo)
```

输出结果是：

```text
func foo(n: Int64) {
    let x = n
    x += 1
    x += 2
    x += 3
    x += 4
    x += 5
    x
}
```

在这个案例中，创建了一个节点列表 `incrs`，包含表达式 `x += 1`，...，`x += 5`。对 `incrs` 的插值将节点依次列出，在每个节点后换行。这适用于插入需要依次执行的表达式和声明的情况。

下面的案例展示在某些情况下，需要在插值周围添加括号，以保证正确性。

<!-- verify -->

```cangjie
var binExpr1 = BinaryExpr(quote(x + y))
var binExpr2 = BinaryExpr(quote($(binExpr1) * z))       // 错误：得到 x + y * z
println("binExpr2: ${binExpr2.toTokens()}")
println("binExpr2.leftExpr: ${binExpr2.leftExpr.toTokens()}")
println("binExpr2.rightExpr: ${binExpr2.rightExpr.toTokens()}")
var binExpr3 = BinaryExpr(quote(($(binExpr1)) * z))     // 正确：得到 (x + y) * z
println("binExpr3: ${binExpr3.toTokens()}")
```

输出结果是：

```text
binExpr2: x + y * z
binExpr2.leftExpr: x
binExpr2.rightExpr: y * z
binExpr3: (x + y) * z
```

首先，构建表达式 `x + y`，然后将该表达式插入到模板 `$(binExpr1) * z` 中。这里的意图是得到一个先计算 `x + y` 再乘 `z` 的表达式，但是，插值的结果是 `x + y * z`，即先计算 `y * z` 再加 `x`。这是因为插值不会自动添加括号以保证被插入的表达式的原子性（这和前一节介绍的 `leftExpr` 的替换不同）。因此，需要在 `$(binExpr1)` 周围添加小括号，保证得到正确的结果。


---

<!-- Content from source_zh_cn/Macro/implementation_of_macros.md -->
# 宏的实现

本章节介绍仓颉宏的定义和使用，仓颉宏可以分为[非属性宏](./implementation_of_macros.md#非属性宏)和[属性宏](./implementation_of_macros.md#属性宏)。同时本章节还会介绍宏出现嵌套时的行为。

## 非属性宏

非属性宏只接受被转换的代码，不接受其他参数（属性），其定义格式如下：

```cangjie
import std.ast.*

public macro MacroName(args: Tokens): Tokens {
    ... // Macro body
}
```

宏的调用格式如下：

```cangjie
@MacroName(...)
```

宏调用使用 `()` 括起来。括号里面可以是任意合法 `Tokens`，也可以是空。

当宏作用于声明时，一般可以省略括号。参考如下示例：

```cangjie
@MacroName func name() {}        // Before a FuncDecl
@MacroName struct name {}        // Before a StructDecl
@MacroName class name {}         // Before a ClassDecl
@MacroName var a = 1             // Before a VarDecl
@MacroName enum e {}             // Before a Enum
@MacroName interface i {}        // Before a InterfaceDecl
@MacroName extend e <: i {}      // Before a ExtendDecl
@MacroName mut prop i: Int64 {}  // Before a PropDecl
@MacroName @AnotherMacro(input)  // Before a macro call
```

对于括号里 `Tokens` 的合法性有以下特殊说明：

- 输入的内容必须是由合法的 `Token` 组成的序列，类似 "#"、" \` "、"\\" 等符号单独使用都不是合法的仓颉 `Token`，不支持其作为输入值。

- 输入的内容中，若存在不匹配的小括号则必须使用转义符号 "\\" 对其进行转义。

- 输入的内容中，若希望 "@" 作为输入的 `Token` 则必须使用转义符号 "\\" 对其进行转义。

对于输入的特殊说明，可以参考如下示例：

```cangjie
// Illegal input Tokens
@MacroName(#)    // Not a whole Token
@MacroName(`)    // Not a whole Token
@MacroName(()    // ( and ) not match
@MacroName(\[)   // Escape for unsupported symbol

// Legal input Tokens
@MacroName(#"abc"#)
@MacroName(`class`)
@MacroName([)
@MacroName([])
@MacroName(\()
@MacroName(\@)
```

宏展开过程作用于仓颉语法树，宏展开后，编译器会继续进行后续的编译过程。因此，需要注意以下规则：

- 宏展开后的代码依然是合法的仓颉代码，并且宏展开后的代码不允许出现包的声明与导入语句，否则可能引发编译问题。
- 当宏用于声明时，如果省略括号，宏的输入必须是语法合法的声明。

下面是几个宏应用的典型示例。

- 示例 1

  宏定义文件 `macro_definition.cj`

  <!-- verify -macro6 -->
  <!-- cfg="--compile-macro" -->

  ```cangjie
  macro package macro_definition

  import std.ast.*

  public macro testDef(input: Tokens): Tokens {
      println("I'm in macro body")
      return input
  }
  ```

  宏调用文件 `macro_call.cj`

  <!-- verify -macro6 -->

  ```cangjie
  package macro_calling

  import macro_definition.*

  main(): Int64 {
      println("I'm in function body")
      let a: Int64 = @testDef(1 + 2)
      println("a = ${a}")
      return 0
  }
  ```

  上述代码的编译过程可以参考[宏的编译和使用](./compiling_error_reporting_and_debugging.md#宏的编译和使用)。

  在用例中添加了打印信息，其中宏定义中的 `I'm in macro body` 将在编译 `macro_call.cj` 的期间输出。同时，宏调用点被展开，如编译如下代码：

  ```cangjie
  let a: Int64 = @testDef(1 + 2)
  ```

  编译器将宏返回的 `Tokens` 更新到调用点的语法树上，得到如下代码：

  ```cangjie
  let a: Int64 = 1 + 2
  ```

  也就是说，可执行程序中的代码实际变为了：

  ```cangjie
  main(): Int64 {
      println("I'm in function body")
      let a: Int64 = 1 + 2
      println("a = ${a}")
      return 0
  }
  ```

  `a` 经过计算得到的值为 3，在打印 `a` 的值时插值为 3。至此，上述程序的运行结果为：

  <!-- verify -macro6 -->

  ```text
  I'm in function body
  a = 3
  ```

下面看一个更有意义的用宏处理函数的例子，这个宏 ModifyFunc 宏的作用是给 myFunc 增加 id 参数，并在 `counter++` 前后插入一段代码。

- 示例 2

  宏定义文件 `macro_definition.cj`

  <!-- verify -macro7 -->
  <!-- cfg="--compile-macro" -->

  ```cangjie
  // file macro_definition.cj
  macro package macro_definition

  import std.ast.*

  public macro ModifyFunc(input: Tokens): Tokens {
      println("I'm in macro body")
      let funcDecl = FuncDecl(input)
      return quote(
          func $(funcDecl.identifier)(id: Int64) {
              println("start ${id}")
              $(funcDecl.block.nodes)
              println("end")
          })
  }
  ```

  宏调用文件 `macro_call.cj`

  <!-- verify -macro7 -->

  ```cangjie
  package macro_calling

  import macro_definition.*

  var counter = 0

  @ModifyFunc
  func myFunc() {
      counter++
  }

  func exModifyFunc() {
      println("I'm in function body")
      myFunc(123)
      println("myFunc called: ${counter} times")
      return 0
  }

  main(): Int64 {
      exModifyFunc()
  }
  ```

  同样的，上述两段代码分别位于不同文件中，先编译宏定义文件 `macro_definition.cj`，再编译宏调用 `macro_call.cj` 生成可执行文件。

  这个例子中，ModifyFunc 宏的输入是一个函数声明，因此可以省略括号：

  ```cangjie
  @ModifyFunc
  func myFunc() {
      counter++
  }
  ```

  经过宏展开后，得到如下代码：

  ```cangjie
  func myFunc(id: Int64) {
      println("start ${id}")
      counter++
      println("end")
  }
  ```

  myFunc 会在 main 中调用，它接受的实参也是在 main 中定义的，从而形成了一段合法的仓颉程序。运行时打印如下：

  <!-- verify -macro7 -->

  ```text
  I'm in function body
  start 123
  end
  myFunc called: 1 times
  ```

## 属性宏

和非属性宏相比，属性宏的定义会增加一个 Tokens 类型的输入，这个增加的入参可以让开发者输入额外的信息。比如开发者可能希望在不同的调用场景下使用不同的宏展开策略，则可以通过这个属性入参进行标记位设置。同时，这个属性入参也可以传入任意 Tokens，这些 Tokens 可以与被宏修饰的代码进行组合拼接等。下面是一个简单的例子：

```cangjie
// Macro definition with attribute
public macro Foo(attrTokens: Tokens, inputTokens: Tokens): Tokens {
    return attrTokens + inputTokens  // Concatenate attrTokens and inputTokens.
}
```

如上面的宏定义，属性宏的入参数量为 2，入参类型为 `Tokens`，在宏定义内，可以对 `attrTokens` 和 `inputTokens` 进行一系列的组合、拼接等变换操作，最后返回新的 `Tokens`。

带属性的宏与不带属性的宏的调用类似，属性宏调用时新增的入参 attrTokens 通过 [] 传入，其调用形式为：

```cangjie
// attribute macro with parentheses
var a: Int64 = @Foo[1+](2+3)

// attribute macro without parentheses
@Foo[public]
struct Data {
    var count: Int64 = 100
}
```

- 宏 Foo 调用，当参数是 `2+3` 时，与 `[]` 内的属性 `1+` 进行拼接，经过宏展开后，得到 `var a: Int64 = 1+2+3` 。
- 宏 Foo 调用，当参数是 struct Data 时，与 `[]` 内的属性 `public` 进行拼接，经过宏展开后，得到

  ```cangjie
  public struct Data {
      var count: Int64 = 100
  }
  ```

关于属性宏，需要注意以下几点：

- 带属性的宏，与不带属性的宏相比，能修饰的 AST 是相同的，可以理解为带属性的宏对可传入参数做了增强。

- 属性宏小括号内的参数合法性规则与非属性宏的参数合法性规则一致。

- 属性宏中括号内的参数（属性）的合法性规则有如下特殊说明：

    - 输入的内容必须是由合法的 `Token` 组成的序列，类似 "#"、" \` "、"\\" 等符号单独使用都不是合法的仓颉 `Token`，不支持其作为输入值。

    - 输入的内容中，若存在不匹配的中括号则必须使用转义符号 "\\" 对其进行转义。

    - 输入的内容中，若希望 "@" 作为输入的 `Token` 则必须使用转义符号 "\\" 对其进行转义。

    ```cangjie
    // Illegal attribute Tokens
    @MacroName[#]()    // Not a whole Token
    @MacroName[`]()    // Not a whole Token
    @MacroName[@]()    // Not escape for @
    @MacroName[[]()    // [ and ] not match
    @MacroName[\(]()   // Escape for unsupported symbol

    // Legal attribute Tokens
    @MacroName[#"abc"#]()
    @MacroName[`class`]()
    @MacroName[(]()
    @MacroName[()]()
    @MacroName[\[]()
    @MacroName[\@]()
    ```

- 宏的定义和调用的类型要保持一致：如果宏定义有两个入参，即为属性宏定义，调用时必须加上 `[]`，且内容可以为空；如果宏定义有一个入参，即为非属性宏定义，调用时不能使用 `[]`。

## 嵌套宏

仓颉语言不支持宏定义的嵌套；有条件地支持在宏定义和宏调用中嵌套宏调用。

### 宏定义中嵌套宏调用

下面是一个宏定义中包含其他宏调用的例子。

宏包 `pkg1` 中定义 `getIdent` 宏：

<!-- compile -macro8 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package pkg1

import std.ast.*

public macro getIdent(attr:Tokens, input:Tokens):Tokens {
    return quote(
        let decl = (parseDecl(input) as VarDecl).getOrThrow()
        let name = decl.identifier.value
        let size = name.size - 1
        let $(attr) = Token(TokenKind.IDENTIFIER, name[0..size])
    )
}
```

宏包 `pkg2` 中定义 `Prop` 宏，其中嵌套了 `getIdent` 宏的调用：

<!-- compile -macro8 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package pkg2

import std.ast.*
import pkg1.*

public macro Prop(input:Tokens):Tokens {
    let v = parseDecl(input)
    @getIdent[ident](input)
    return quote(
        $(input)
        public prop $(ident): $(decl.declType) {
            get() {
                this.$(v.identifier)
            }
        }
    )
}
```

宏调用包 `pkg3`  中调用 `Prop` 宏：

<!-- compile -macro8 -->

```cangjie
package pkg3

import pkg2.*
class A {
    @Prop
    private let a_: Int64 = 1
}

main() {
    let b = A()
    println("${b.a}")
}
```

注意，按照宏定义必须比宏调用点先编译的约束，上述 3 个文件的编译顺序必须是：pkg1 -> pkg2 -> pkg3。pkg2 中的 `Prop` 宏定义：

```cangjie
public macro Prop(input:Tokens):Tokens {
    let v = parseDecl(input)
    @getIdent[ident](input)
    return quote(
        $(input)
        public prop $(ident): $(decl.declType) {
            get() {
                this.$(v.identifier)
            }
        }
    )
}
```

会先被展开成如下代码，再进行编译。

```cangjie
public macro Prop(input: Tokens): Tokens {
    let v = parseDecl(input)

    let decl = (parseDecl(input) as VarDecl).getOrThrow()
    let name = decl.identifier.value
    let size = name.size - 1
    let ident = Token(TokenKind.IDENTIFIER, name[0 .. size])

    return quote(
        $(input)
        public prop $(ident): $(decl.declType) {
            get() {
                this.$(v.identifier)
            }
        }
    )
}
```

### 宏调用中嵌套宏调用

嵌套宏的常见场景，是宏修饰的代码块中，出现了宏调用。一个具体的例子如下：

`pkg1` 包中定义 `Foo` 和 `Bar` 宏：

<!-- run -macro9 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package pkg1

import std.ast.*

public macro Foo(input: Tokens): Tokens {
    return input
}

public macro Bar(input: Tokens): Tokens {
    return input
}
```

`pkg2` 包中定义 `addToMul` 宏：

<!-- run -macro9 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package pkg2

import std.ast.*

public macro addToMul(inputTokens: Tokens): Tokens {
    var expr: BinaryExpr = match (parseExpr(inputTokens) as BinaryExpr) {
        case Some(v) => v
        case None => throw Exception()
    }
    var op0: Expr = expr.leftExpr
    var op1: Expr = expr.rightExpr
    return quote(($(op0)) * ($(op1)))
}
```

`pkg3` 包中使用上面定义的三个宏：

<!-- run -macro9 -->

```cangjie
package pkg3

import pkg1.*
import pkg2.*
@Foo
struct Data {
    let a = 2
    let b = @addToMul(2+3)

    @Bar
    public func getA() {
        return a
    }

    public func getB() {
        return b
    }
}

main(): Int64 {
    let data = Data()
    var a = data.getA() // a = 2
    var b = data.getB() // b = 6
    println("a: ${a}, b: ${b}")
    return 0
}
```

如上代码所示，宏 `Foo` 修饰了 `struct Data`，而在 `struct Data` 内，出现了宏调用 `addToMul` 和 `Bar`。这种嵌套场景下，代码变换的规则是：将嵌套内层的宏（`addToMul` 和 `Bar`）展开后，再去展开外层的宏（`Foo`）。允许出现多层宏嵌套，代码变换的规则总是由内向外去依次展开宏。

嵌套宏可以出现在带括号和不带括号的宏调用中，二者可以组合，但开发者需要保证没有歧义，且明确宏的展开顺序：

```cangjie
var a = @foo(@foo1(2 * 3)+@foo2(1 + 3))  // foo1, foo2 have to be defined.

@Foo1 // Foo2 expands first, then Foo1 expands.
@Foo2[attr: struct] // Attribute macro can be used in nested macro.
struct Data{
    @Foo3 @Foo4[123] var a = @bar1(@bar2(2 + 3) + 3)  // bar2, bar1, Foo4, Foo3 expands in order.
    public func getA() {
        return @foo(a + 2)
    }
}
```

### 嵌套宏之间的消息传递

这里指的是宏调用的嵌套。

内层宏可以调用库函数 `assertParentContext` 来保证内层宏调用一定嵌套在特定的外层宏调用中。如果内层宏调用这个函数时没有嵌套在给定的外层宏调用中，该函数将抛出一个错误。库函数 `InsideParentContext` 同样用于检查内层宏调用是否嵌套在特定的外层宏调用中，该函数返回一个布尔值。下面是一个简单的例子。

宏定义如下：

```cangjie
public macro Outer(input: Tokens): Tokens {
    return input
}

public macro Inner(input: Tokens): Tokens {
    assertParentContext("Outer")
    return input
}
```

宏调用如下：

```cangjie
@Outer var a = 0
@Inner var b = 0 // Error, The macro call 'Inner' should with the surround code contains a call 'Outer'.
```

如上代码所示，`Inner` 宏在定义时使用了 `assertParentContext` 函数用于检查其在调用阶段是否位于 `Outer` 宏中，在代码示例的宏调用场景下，由于 `Outer` 和 `Inner` 在调用时不存在这样的嵌套关系，因此编译器将报告一个错误。

内层宏也可以通过发送键/值对的方式与外层宏通信。当内层宏执行时，通过调用标准库函数 `setItem` 向外层宏发送信息；随后，当外层宏执行时，调用标准库函数 `getChildMessages` 接收每一个内层宏发送的信息（一组键/值对映射）。下面是一个简单的例子。

宏定义如下：

<!-- run -macro10 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define

import std.ast.*

public macro Outer(input: Tokens): Tokens {
    let messages = getChildMessages("Inner")

    let getTotalFunc = quote(public func getCnt() {
                       )
    for (m in messages) {
        let identName = m.getString("identifierName")
        // let value = m.getString("key")            // 接收多组消息
        getTotalFunc.append(Token(TokenKind.IDENTIFIER, identName))
        getTotalFunc.append(quote(+))
    }
    getTotalFunc.append(quote(0))
    getTotalFunc.append(quote(}))
    let funcDecl = parseDecl(getTotalFunc)

    let decl = (parseDecl(input) as ClassDecl).getOrThrow()
    decl.body.decls.add(funcDecl)
    return decl.toTokens()

}

public macro Inner(input: Tokens): Tokens {
    assertParentContext("Outer")
    let decl = parseDecl(input)
    setItem("identifierName", decl.identifier.value)
    // setItem("key", "value")                      // 可以通过不同的key值传递多组消息
    return input
}
```

宏调用如下：

<!-- run -macro11 -->
<!-- cfg="--compile-macro" -->

```cangjie
import define.*

@Outer
class Demo {
    @Inner var state = 1
    @Inner var cnt = 42
}

main(): Int64 {
    let d = Demo()
    println("${d.getCnt()}")
    return 0
}
```

在上面的代码中，`Outer` 接收两个 `Inner` 宏发送来的变量名，自动为类添加如下内容：

```cangjie
public func getCnt() {
    state + cnt + 0
}
```

具体流程为：内层宏 `Inner` 通过 `setItem` 向外层宏发送信息；`Outer` 宏通过 `getChildMessages` 函数接收到 `Inner` 发送的一组信息对象（`Outer` 中可以调用多次 `Inner`）；最后通过该信息对象的 `getString` 函数接收对应的值。


---

<!-- Content from source_zh_cn/Macro/compiling_error_reporting_and_debugging.md -->
# 编译、报错与调试

## 宏的编译和使用

当前编译器约束宏的定义与宏的调用不允许在同一包里。宏包必须首先被编译，然后再编译宏调用的包。在宏调用的包中，不允许出现宏的定义。由于宏需在包中导出给另一个包使用，因此编译器约束宏定义必须使用 `public` 修饰。

下面介绍一个简单的例子。

源码目录结构如下：

```text
// Directory layout.
root_path
├── macros
│    └── m.cj
├── src
│    └── demo.cj
└─ target
```

宏定义放在 _macros_ 子目录下：

<!-- run -macro0 -->
<!-- cfg="--compile-macro" -->

```cangjie
// macros/m.cj
// In this file, we define the macro Inner, Outer.
macro package define
import std.ast.*

public macro Inner(input: Tokens) {
    return input
}

public macro Outer(input: Tokens) {
    return input
}

```

宏调用放在 _src_ 子目录下：

<!-- run -macro0 -->

```cangjie
// src/demo.cj
import define.*
@Outer
class Demo {
    @Inner var state = 1
    @Inner var cnt = 42
}

main() {
    println("test macro")
}
```

当宏定义文件的编译产物和使用宏的文件不在同一目录下时，需要通过添加 `--import-path` 编译选项来指定宏定义文件编译产物的路径。以下为 Linux 平台的编译命令（具体编译选项会随着 cjc 更新而演进，以最新 cjc 的编译选项为准）：

```shell
# 先编译宏定义文件在指定目录产生默认的动态库文件（允许指定动态库的路径，但不能指定动态库的名字）
cjc macros/m.cj --compile-macro --output-dir ./target

# 编译使用宏的文件，宏替换完成，产生可执行文件
cjc src/demo.cj -o demo --import-path ./target --output-dir ./target

# 运行可执行文件
./target/demo
```

在 Linux 平台上，将生成用于包管理的 `macro_define.cjo` 和实际的动态库文件。

若在 Windows 平台：

```shell
# 当前目录: src

# 先编译宏定义文件在指定目录产生默认的动态库文件（允许指定动态库的路径，但不能指定动态库的名字）
cjc macros/m.cj --compile-macro --output-dir ./target

# 编译使用宏的文件，宏替换完成，产生可执行文件
cjc src/demo.cj -o demo.exe --import-path ./target --output-dir ./target
```

如果宏包还依赖其他动态库，则需要保证宏包在运行态（宏展开依赖宏包内方法的执行）下能够找到这些依赖。在 Linux 下可以通过设置 `LD_LIBRAYR_PATH`（Windows 下设置 `PATH`）环境变量添加所依赖动态库的路径。

> **说明：**
>
> 宏替换过程依赖仓颉 runtime ，宏替换过程中仓颉 runtime 的初始化配置采用宏提供的默认配置，配置参数支持使用仓颉 runtime 运维日志进行查询，其中 cjHeapSize 与 cjStackSize 支持用户修改，其余暂不支持，仓颉 runtime 初始化配置可参见[runtime 初始化可选配置](../Appendix/runtime_env.md#runtime初始化可选配置)章节。

## 并行宏展开

可以在编译宏调用文件时添加 `--parallel-macro-expansion` 选项，启用并行宏展开的能力。编译器会自动分析宏调用之间的依赖关系，无依赖关系的宏调用可以并行执行，如上述例子中的两个 `@Inner` 就可以并行展开，如此可以缩短整体编译时间。

> **注意：**
>
> 如果宏函数依赖一些全局变量，使用并行宏展开会存在风险。

<!-- compile -macro1 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define
import std.ast.*
import std.collection.HashMap

var Counts = HashMap<String, Int64>()

public macro Inner(input: Tokens) {
    for (t in input) {
        if (t.value.size == 0) {
            continue
        }
        // 统计所有有效token value的出现次数
        if (!Counts.contains(t.value)) {
            Counts[t.value] = 0
        }
        Counts[t.value] = Counts[t.value] + 1
    }
    return input
}

public macro B(input: Tokens) {
    return input
}
```

参考上述代码，如果 `@Inner` 的宏调用出现在多处，并且启用了并行宏展开选项，则访问全局变量 `Counts` 就可能存在冲突，导致最后获取的结果不正确。

建议不要在宏函数中使用全局变量，如果必须使用，要么关闭并行宏展开选项，或者可以通过仓颉线程锁对全局变量进行保护。

## diagReport 报错机制

仓颉标准库 `std.ast` 包提供了自定义报错接口 `diagReport`。方便定义宏的用户，在解析传入 Tokens 时，对错误 Tokens 内容进行自定义报错。

自定义报错接口提供同原生编译器报错一样的输出格式，允许用户报 warning 和 error 两类错误提示信息。

`diagReport` 的函数原型如下：

```cangjie
public func diagReport(level: DiagReportLevel, tokens: Tokens, message: String, hint: String): Unit
```

其参数含义如下：

- level: 报错信息等级
- tokens: 报错信息中所引用源码内容对应的 Tokens
- message: 报错的主信息
- hint: 辅助提示信息

参考如下使用示例。

宏定义文件：

<!-- compile.error -macro2 -->
<!-- cfg="--compile-macro" -->

```cangjie
// macro_definition.cj
macro package macro_definition

import std.ast.*

public macro testDef(input: Tokens): Tokens {
    for (i in 0..input.size) {
        if (input[i].kind == IDENTIFIER) {
            diagReport(DiagReportLevel.ERROR, input[i..(i + 1)],
                       "This expression is not allowed to contain identifier",
                       "Here is the illegal identifier")
        }
    }
    return input
}
```

宏调用文件：

<!-- compile.error -macro2 -->

```cangjie
// macro_call.cj
package macro_calling

import std.ast.*
import macro_definition.*

main(): Int64 {
    let a = @testDef(1)
    let b = @testDef(a)
    let c = @testDef(1 + a)
    return 0
}
```

编译宏调用文件过程中，会出现如下报错信息：

```text
error: This expression is not allowed to contain identifier
 ==> call.cj:9:22:
  |
9 |     let b = @testDef(a)
  |                      ^ Here is the illegal identifier
  |

error: This expression is not allowed to contain identifier
  ==> call.cj:10:26:
   |
10 |     let c = @testDef(1 + a)
   |                          ^ Here is the illegal identifier
   |

2 errors generated, 2 errors printed.
```

## 使用 --debug-macro 输出宏展开结果

借助宏在编译期做代码生成时，如果发生错误，处理起来十分棘手，这是开发者经常遇到但一般很难定位的问题。这是因为，开发者写的源码，经过宏的变换后变成了不同的代码片段。编译器抛出的错误信息是基于宏最终生成的代码进行提示的，但这些代码在开发者的源码中没有体现。

为了解决这个问题，仓颉宏提供 debug 模式，在这个模式下，开发者可以从编译器为宏生成的 debug 文件中看到完整的宏展开后的代码，如下所示。

宏定义文件：

<!-- compile -macro3 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define

import std.ast.*

public macro Outer(input: Tokens): Tokens {
    let messages = getChildMessages("Inner")

    let getTotalFunc = quote(public func getCnt() {
                       )
    for (m in messages) {
        let identName = m.getString("identifierName")
        getTotalFunc.append(Token(TokenKind.IDENTIFIER, identName))
        getTotalFunc.append(quote(+))
    }
    getTotalFunc.append(quote(0))
    getTotalFunc.append(quote(}))
    let funcDecl = parseDecl(getTotalFunc)

    let decl = (parseDecl(input) as ClassDecl).getOrThrow()
    decl.body.decls.add(funcDecl)
    return decl.toTokens()

}

public macro Inner(input: Tokens): Tokens {
    assertParentContext("Outer")
    let decl = parseDecl(input)
    setItem("identifierName", decl.identifier.value)
    return input
}
```

宏调用文件 `demo.cj`：

<!-- compile -macro3 -->
<!-- cfg="--debug-macro" -->

```cangjie
import define.*

@Outer
class Demo {
    @Inner var state = 1
    @Inner var cnt = 42
}

main(): Int64 {
    let d = Demo()
    println("${d.getCnt()}")
    return 0
}

```

在编译使用宏的文件时，在选项中，增加 `--debug-macro`，即使用仓颉宏的 _debug_ 模式。

```shell
cjc --debug-macro demo.cj --import-path ./target
```

> **注意：**
>
> 如果使用仓颉的 `CJPM` 包管理工具进行编译，可在配置文件 `cjpm.toml` 中添加 `--debug-macro` 的编译选项来使用宏的 _debug_ 模式。
>
> ```text
> compile-option = "--debug-macro"
> ```

在 _debug_ 模式下，会生成临时文件 _demo.cj.macrocall_，对应宏展开的部分如下：

```cangjie
// demo.cj.macrocall
/* ===== Emitted by MacroCall @Outer in demo.cj:3:1 ===== */
/* 3.1 */class Demo {
/* 3.2 */    var state = 1
/* 3.3 */    var cnt = 42
/* 3.4 */    public func getCnt() {
/* 3.5 */        state + cnt + 0
/* 3.6 */    }
/* 3.7 */}
/* 3.8 */
/* ===== End of the Emit ===== */
```

如果宏展开后的代码有语义错误，则编译器的错误信息会溯源到宏展开后代码的具体行列号。仓颉宏的 _debug_ 模式有以下注意事项：

- 宏的 _debug_ 模式会重排源码的行列号信息，不适用于某些特殊的换行场景。例如：

  ```cangjie
  // before expansion
  @M{} - 2 // macro M return 2

  // after expansion
  // ===== Emmitted my Macro M at line 1 ===
  2
  // ===== End of the Emit =====
  - 2
  ```

  这些因换行符导致语义改变的情形，不应使用 _debug_ 模式。

- 不支持宏调用在宏定义内的调试，会编译报错。

  ```cangjie
  public macro M(input: Tokens) {
      let a = @M2(1+2) // M2 is in macro M, not suitable for debug mode.
      return input + quote($a)
  }
  ```

- 不支持带括号宏的调试。

  ```cangjie
  // main.cj

  main() {
      // For macro with parenthesis, newline introduced by debug will change the semantics
      // of the expression, so it is not suitable for debug mode.
      let t = @M(1+2)
  }
  ```


---

<!-- Content from source_zh_cn/Macro/defining_and_importing_macro_package.md -->
# 宏包定义和导入

仓颉语言中宏的定义需要放在由 `macro package` 声明的包中，被 `macro package` 限定的包仅允许宏定义对外可见，其他声明包内可见。

> **说明：**
>
> 重导出的声明也允许对外可见，关于包管理和重导出的相关概念，请参见[包的导入](../package/import.md)章节。

<!-- compile.error -macro4 -->
<!-- cfg="--compile-macro" -->

```cangjie
// file define.cj
macro package define         // 编译 define.cjo 携带 macro 属性
import std.ast.*

public func A() {}          // Error, 宏包不允许定义外部可见的非宏定义，此处会报错

public macro M(input: Tokens): Tokens { // macro M 外部可见
    return input
}
```

需要特殊说明的是，在宏包中，允许其他宏包和非宏包的声明被重导出。在非宏包中仅允许非宏包的声明被重导出。

参考如下示例：

- 在宏包 A 中定义宏 `M1`

  <!-- compile -macro5 -->
  <!-- cfg="--compile-macro" -->

  ```cangjie
  macro package A
  import std.ast.*

  public macro M1(input: Tokens): Tokens {
      return input
  }
  ```

  编译命令如下：

  ```shell
  cjc A.cj --compile-macro
  ```

- 在非宏包 B 中定义一个 public 函数 `f1`。注意在非 `macro package` 中无法重导出 `macro package` 的符号

  <!-- compile -macro5 -->
  <!-- cfg="--output-type=dylib -o libB.so" -->

  ```cangjie
  package B
  // public import A.* // Error, it is not allowed to re-export a macro package in a package.

  public func f1(input: Int64): Int64 {
      return input
  }
  ```

  编译命令如下，这里选择使用 `--output-type` 选项将 B 包编译成动态库，关于 cjc 编译选项介绍可以参考 "附录 > cjc 编译选项" 章节。

  ```shell
  cjc B.cj --output-type=dylib -o libB.so
  ```

- 在宏包 C 中定义宏 `M2`，依赖了 A 包和 B 包的内容。可以看到 `macro package` 中可以重导出 `macro package` 和非 `macro package` 的符号

  <!-- compile -macro5 -->
  <!-- cfg="--compile-macro -L. -lB" -->

  ```cangjie
  macro package C
  public import A.* // correct: macro package is allowed to re-export in a macro package.
  public import B.* // correct: non-macro package is also allowed to re-export in a macro package.
  import std.ast.*

  public macro M2(input: Tokens): Tokens {
      return @M1(input) + Token(TokenKind.NL) + quote(f1(1))
  }
  ```

  编译命令如下，注意这里需要显式链接 B 包动态库：

  ```cangjie
  cjc C.cj --compile-macro -L. -lB
  ```

- 在 `main.cj` 中使用 `M2` 宏

  <!-- compile -macro5 -->
  <!-- cfg="--compile-macro -L. -lB" -->

  ```cangjie
  import C.*

  main() {
      @M2(let a = 1)
  }
  ```

  编译命令如下：

  ```cangjie
  cjc main.cj -o main -L. -lB
  ```

  `main.cj`中 `M2` 宏展开后的结果如下：

  ```cangjie
  import C.*

  main() {
      let a = 1
      f1(1)
  }
  ```

可以看到 `main.cj` 中出现了来自于 B 包的符号 `f1`。宏的编写者可以在 C 包中重导出 B 包里的符号，这样宏的使用者仅需导入宏包，就可以正确地编译宏展开后的代码。如果在 `main.cj` 中仅使用 `import C.M2` 导入宏符号，则会报 `undeclared identifier 'f1'` 的错误信息。


---

<!-- Content from source_zh_cn/Macro/builtin_compilation_flags.md -->
# 内置编译标记

仓颉语言提供了一些预定义的编译标记，可以通过这些编译标记控制仓颉编译器的编译行为。

## 源码位置

仓颉提供了几个内置编译标记，用于在编译时获取源码的位置。

- `@sourcePackage()` 展开后是一个 `String` 类型的字面量，内容为该标记所在的源码的包名。
- `@sourceFile()` 展开后是一个 `String` 类型的字面量，内容为该标记所在的源码的文件名。
- `@sourceLine()` 展开后是一个 `Int64` 类型的字面量，内容为该标记所在的源码的代码行。

这几个编译标记可以在任意表达式内部使用，只要能符合类型检查规则即可。示例如下：

<!-- run -->

```cangjie
func test1() {
    let s: String = @sourceFile()  // The value of `s` is the current source file name
}

func test2(n!: Int64 = @sourceLine()) { /* at line 5 */
    // The default value of `n` is the source file line number of the definition of `test2`
    println(n) // print 5
}
```

## 条件编译

条件编译使用 `@When` 标记，是一种在程序代码中根据特定条件选择性地编译不同代码段的技术。条件编译的作用主要体现在以下几个方面：

- 平台适应：支持根据当前的编译环境选择性地编译代码，用于实现跨平台的兼容性。
- 功能选择：支持根据不同的需求选择性地编译代码，用于实现功能的灵活配置。
- 调试支持：支持调试模式下编译相关代码，用于提高程序的性能和安全性。例如，在调试模式下编译调试信息或记录日志相关的代码，而在发布版本中将其排除。
- 性能优化：支持根据预定义的条件选择性地编译代码，用于提高程序的性能。

关于条件编译的具体内容，请参见[条件编译](../compile_and_build/conditional_compilation.md)章节，这里不再额外展开。

## @FastNative

为了提升与 `C` 语言互操作的性能，仓颉提供 `@FastNative` 标记用于优化对 `C` 函数的调用。值得注意的是 `@FastNative` 只能用于 `foreign` 声明的函数。

首先编译以下 C 语言程序得到动态库文件 `libcProg.so`，示例如下：

```c
#include <stdio.h>

char* foo()
{
    static char str[] = "this is an example";
    return str;
}
```

仓颉文件 `main.cj`：

```cangjie
@FastNative
foreign func foo(): CPointer<Int32>

@FastNative
foreign func printf(fmt: CPointer<Int32>, ...): Int32

main(): Int32 {
    unsafe{
        let str = foo()
        printf(str)
    }
}
```

具体的编译介绍，详情请参见[附录](../Appendix/compile_options_cjvm.md#cjc-编译选项)。下面为该用例对应的编译命令：

```shell
cjc -L . -lcProg ./main.cj
```

执行上述命令编译 `main.cj` 之后生成一个可执行文件 `main`，其执行结果如下：

```text
this is an example
```

开发者在使用 `@FastNative` 修饰 `foreign` 函数时，应确保对应的 `C` 函数满足以下两点要求：

1. 函数的整体执行时间不宜太长。例如：不允许函数内部存在很大的循环；不允许函数内部产生阻塞行为，例如：调用 `sleep`、`wait` 等函数。
2. 函数内部不能调用仓颉方法。

## @Frozen

`@Frozen` 标记可用于修饰函数和属性。如果确定某个函数、属性在将来的版本更新中不会去修改它的内部实现，那么可以使用 `@Frozen` 对其进行标记，该标记代表开发者对该函数/属性在未来版本演进的一种承诺。被 `@Frozen` 修饰的函数和属性，在后续的升级版本中，签名和函数体都不能发生任何变化。这意味着，前后两个代码版本，在相同编译器、相同编译选项的情况下，该函数或属性的生成产物完全一致。

`@Frozen` 标记可被用于修饰：

- 全局函数
- 类、结构、接口、扩展、枚举中的函数
- 类、接口、扩展中的属性

`@Frozen` 标记不可被用于修饰：

- 除了函数和属性以外的其他类型声明
- 嵌套函数
- 表达式

使用示例如下：

<!-- run -->

```cangjie
@Frozen
public func test(): Unit {}

public class testClass {
    @Frozen
    public func testFunc(): Unit {}

    @Frozen
    public prop testProp: Unit {
        get() {}
    }
}
```

## @Attribute

仓颉语言内部提供 `@Attribute` 标记，开发者通过内置的 `@Attribute` 来对某个声明设置属性值，从而达到标记声明的目的。属性值可以是 `identifier` 或者 `string`，下面是一个简单的例子，这段示例代码为变量 `cnt` 添加了一个 `identifier` 类型的属性 `State`，为变量 `bcnt` 添加了一个 `string` 类型的属性 `"Binding"`。

```cangjie
@Attribute[State] var cnt = 0       // identifier
@Attribute["Binding"] var bcnt = 0  // string
```

同时，标准库 `std.ast` 包提供了 `getAttrs()` 方法用于获取节点的属性，以及 `hasAttr(attrs: String)` 方法用于判断当前节点是否具有某个属性，下面是一个具体的例子。

宏定义如下：

```cangjie
public macro Component(input: Tokens): Tokens {
    var varDecl = parseDecl(input)
    if (varDecl.hasAttr("State")) { // 如果该节点被标记了属性且值为 “State” 返回 true, 否则返回 false
        var attrs = varDecl.getAttrs() // 返回一组 Tokens
        println(attrs[0].value)
    }
    return input
}
```

宏调用如下：

```cangjie
@Component(
    @Attribute[State] var cnt = 0
)
```

## @Deprecated

`@Deprecated` 表示此 API 已废弃，虽然暂时可用，但未来将被移除或更改，建议其他开发者不要调用此 API。例如：

```cangjie
@Deprecated["用boo代替", since: "1.3.4"]
func foo() {}

main() {
    foo()
}
```

编译器编译时将提供告警信息：

```text
warning: function 'foo' is deprecated since 1.3.4. 用boo代替
 ==> file.cj:5:5:
  |
5 |     foo()
  |     ^^^ deprecated
  |
  # note: this warning can be suppressed by setting the compiler option `-Woff deprecated`

1 warning generated, 1 warning printed.
```

@Deprecated 自定义宏可以应用于以下声明：

- 类、接口、结构体、枚举、枚举构造器
- 顶级（全局）函数或变量
- 静态或非静态的成员函数、成员变量、属性、属性设置器
- 运算符函数
- 扩展的成员函数、静态函数、属性或属性设置器
- foreign 函数或声明在 foreign 块内的函数
- 构造函数和主构造函数
- 抽象的函数和属性
- 类型别名（包括关联类型）
- 函数具有默认参数的命名参数
- const 变量和函数
- 宏定义
- 注解类

### @Deprecated 参数

- `message: String` - 描述声明为何废弃、如何迁移等。
- `since!: ?String` - 废弃版本。
- `strict!: Bool` - 默认值为 `false`，在被该标记修饰的 API 的调用处会触发警告。如果设置为 `true`，则会触发编译错误。

```cangjie
@Deprecated["Use Macro2", since: "1990", strict: true]
public macro Macro(input: Tokens): Tokens {
    return input
}
```


---

<!-- Content from source_zh_cn/Macro/pratical_case.md -->
# 实用案例

## 快速幂的计算

通过一个简单的例子展示使用宏进行编译期求值，生成优化代码的应用。在计算幂 `n ^ e` 时，如果 `e` 是一个（比较大的）整数，可以通过重复取平方（而不是迭代相乘）的方式加速计算。这个算法可以直接使用 while 循环实现，例如：

<!-- run -->

```cangjie
func power(n: Int64, e: Int64) {
    var result = 1
    var vn = n
    var ve = e
    while (ve > 0) {
        if (ve % 2 == 1) {
            result *= vn
        }
        ve /= 2
        if (ve > 0) {
            vn *= vn
        }
    }
    result
}
```

然而，这个实现需要每次对 `e` 的值进行分析，在循环和条件判断中多次对 `ve` 进行判断和更新。此外，实现只支持 `n` 的类型为`Int64`的情况，如果要支持其他类型的 `n`，还要处理如何表达 `result = 1` 的问题。如果预先知道 `e` 的具体值，可以将这个代码写的更简单。例如，如果知道 `e` 的值为 10，可以展开整个循环如下：

<!-- run -->

```cangjie
func power_10(n: Int64) {
    var vn = n
    vn *= vn         // vn = n ^ 2
    var result = vn  // result = n ^ 2
    vn *= vn         // vn = n ^ 4
    vn *= vn         // vn = n ^ 8
    result *= vn     // result = n ^ 10
    result
}
```

当然，手动编写这些代码非常繁琐，希望在给定 `e` 的值之后，自动将这些代码生成出来。宏可以做到这一点。使用案例如下：

```cangjie
public func power_10(n: Int64) {
    @power[10](n)
}
```

这个宏展开的代码是（根据 `.macrocall` 文件）：

```cangjie
public func power_10(n: Int64) {
    /* ===== Emitted by MacroCall @power in main.cj:20:5 ===== */
    /* 20.1 */var _power_vn = n
    /* 20.2 */_power_vn *= _power_vn
    /* 20.3 */var _power_result = _power_vn
    /* 20.4 */_power_vn *= _power_vn
    /* 20.5 */_power_vn *= _power_vn
    /* 20.6 */_power_result *= _power_vn
    /* 20.7 */_power_result
/* ===== End of the Emit ===== */
}
```

下面是宏 `@power` 的实现。

<!-- verify -macro13 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define

import std.ast.*
import std.convert.*

public macro power(attrib: Tokens, input: Tokens) {
    let attribExpr = parseExpr(attrib)
    if (let Some(litExpr) <- (attribExpr as LitConstExpr)) {
        let lit = litExpr.literal
        if (lit.kind != TokenKind.INTEGER_LITERAL) {
            diagReport(DiagReportLevel.ERROR, attrib,
                       "Attribute must be integer literal",
                       "Expected integer literal")
        }
        var n = Int64.parse(lit.value)
        var result = quote(var _power_vn = $(input)
        )
        var flag = false
        while (n > 0) {
            if (n % 2 == 1) {
                if (!flag) {
                    result += quote(var _power_result = _power_vn
                    )
                    flag = true
                } else {
                    result += quote(_power_result *= _power_vn
                    )
                }
            }
            n /= 2
            if (n > 0) {
                result += quote(_power_vn *= _power_vn
                )
            }
        }
        result += quote(_power_result)
        return result
    } else {
        diagReport(DiagReportLevel.ERROR, attrib,
                   "Attribute must be integer literal",
                   "Expected integer literal")
    }
    return input
}
```

这段代码的解释如下：

- 首先，确认输入的属性 `attrib` 是一个整数字面量，否则通过 `diagReport` 报错。将这个字面量解析为整数 `n`。
- 设 `result` 为当前积累的输出代码，首先添加 `var _power_vn` 的声明。这里为了避免变量名冲突，使用不易造成冲突的名字 `_power_vn`。
- 下面进入 while 循环，布尔变量 `flag` 表示 `var _power_result` 是否已经被初始化。其余的代码结构和之前展示的 `power` 函数的实现类似，但区别是使用 while 循环和 if 判断在编译时决定生成的代码是什么，而不是在运行时做这些判断。然后生成由 `_power_result *= _power_vn` 和 `_power_vn *= _power_vn` 适当组合的代码。
- 最后添加返回 `_power_result` 的代码，并将这段代码作为宏的输出值返回。

将这段代码放到 `macros/power.cj` 文件中，并在 `main.cj` 添加如下测试：

<!-- verify -macro13 -->
<!-- cfg="--debug-macro" -->

```cangjie
import define.*

public func power_10(n: Int64) {
    @power[10](n)
}

main() {
    let a = 3
    println(power_10(a))
}
```

输出结果为：

<!-- verify -macro13 -->

```text
59049
```

## Memoize 宏

Memoize（记忆化）是动态规划算法的常用手段。它将已经计算过的子问题的结果存储起来，当同一个子问题再次出现时，可以直接查询表来获取结果，从而避免重复的计算，提高算法的效率。

通常 Memoize 的使用需要开发者手动实现存储和提取的功能。通过宏，可以自动化这一过程。宏的效果如下：

```cangjie
@Memoize[true]
func fib(n: Int64): Int64 {
    if (n == 0 || n == 1) {
        return n
    }
    return fib(n - 1) + fib(n - 2)
}

main() {
    let start = DateTime.now()
    let f35 = fib(35)
    let end = DateTime.now()
    println("fib(35): ${f35}")
    println("execution time: ${(end - start).toMicroseconds()} us")
}
```

在以上代码中，`fib` 函数采用简单的递归方式实现。如果没有 `@Memoize[true]` 标注，这个函数的运行时间将随着 `n` 指数增长。例如，如果在前面的代码中去掉 `@Memoize[true]` 这一行，或者把 `true` 改为 `false`，则 `main` 函数的运行结果为：

```text
fib(35): 9227465
execution time: 199500 us
```

恢复 `@Memoize[true]`，运行结果为：

```text
fib(35): 9227465
execution time: 78 us
```

相同的答案和大幅缩短的计算时间表明，`@Memoize` 的使用确实实现了记忆化。

为了理解 `@Memoize` 的原理，展示对以上 `fib` 函数进行宏展开的结果（来自 `.macrocall` 文件，但是为了提高可读性整理了格式）。

<!-- run -->

```cangjie
import std.collection.*

var memoizeFibMap = HashMap<Int64, Int64>()

func fib(n: Int64): Int64 {
    if (memoizeFibMap.contains(n)) {
        return memoizeFibMap.get(n).getOrThrow()
    }

    let memoizeEvalResult = { =>
        if (n == 0 || n == 1) {
            return n
        }

        return fib(n - 1) + fib(n - 2)
    }()
    memoizeFibMap.add(n, memoizeEvalResult)
    return memoizeEvalResult
}
```

上述代码的执行流程如下：

- 首先，定义 `memoizeFibMap` 为一个从 `Int64` 到 `Int64` 的哈希表，这里第一个 `Int64` 对应 `fib` 的唯一参数的类型，第二个 `Int64` 对应 `fib` 返回值的类型。
- 其次，在函数体中，检查入参是否在 `memoizeFibMap` 中，如果是则立即反馈哈希表中存储的值。否则，使用 `fib` 原来的函数体得到计算结果。这里使用了（不带参数的）匿名函数使 `fib` 的函数体不需要任何改变，并且能够处理任何从 `fib` 函数退出的方式（包括中间的 return，返回最后一个表达式等）。
- 最后，把计算结果存储到 `memoizeFibMap` 中，然后将计算结果返回。

有了这样一个“模板”之后，下面宏的实现就不难理解了。完整的代码如下。

<!-- compile -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define

import std.ast.*

public macro Memoize(attrib: Tokens, input: Tokens) {
    if (attrib.size != 1 || attrib[0].kind != TokenKind.BOOL_LITERAL) {
        diagReport(DiagReportLevel.ERROR, attrib,
                   "Attribute must be a boolean literal (true or false)",
                   "Expected boolean literal (true or false) here")
    }

    let memoized = (attrib[0].value == "true")
    if (!memoized) {
        return input
    }

    let fd = FuncDecl(input)
    if (fd.funcParams.size != 1) {
        diagReport(DiagReportLevel.ERROR, fd.lParen + fd.funcParams.toTokens() + fd.rParen,
                   "Input function to memoize should take exactly one argument",
                   "Expect only one argument here")
    }

    let memoMap = Token(TokenKind.IDENTIFIER, "_memoize_" + fd.identifier.value + "_map")
    let arg1 = fd.funcParams[0]

    return quote(
        var $(memoMap) = HashMap<$(arg1.paramType), $(fd.declType)>()

        func $(fd.identifier)($(arg1)): $(fd.declType) {
            if ($(memoMap).contains($(arg1.identifier))) {
                return $(memoMap).get($(arg1.identifier)).getOrThrow()
            }

            let memoizeEvalResult = { => $(fd.block.nodes) }()
            $(memoMap).add($(arg1.identifier), memoizeEvalResult)
            return memoizeEvalResult
        }
    )
}
```

首先，对属性和输入做合法性检查。属性必须是布尔字面量，如果为 `false` 则直接返回输入。否则，检查输入必须能够解析为函数声明（`FuncDecl`），并且必须包含正好一个参数。下面，产生哈希表的变量，取不容易造成冲突的变量名。最后，通过 `quote`模板生成返回的代码，其中用到哈希表的变量名，以及唯一参数的名称、类型和输入函数的返回类型。

## 一个 dprint 宏的扩展

本节一开始使用了一个打印表达式的宏作为案例，但这个宏一次只能接受一个表达式。希望扩展这个宏，使其能够接受多个表达式，由逗号分开。下面展示如何使用 `parseExprFragment` 来实现这个功能。

宏的实现如下：

<!-- verify -macro15 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define

import std.ast.*

public macro dprint2(input: Tokens) {
    let exprs = ArrayList<Expr>()
    var index: Int64 = 0
    while (true) {
        let (expr, nextIndex) = parseExprFragment(input, startFrom: index)
        exprs.add(expr)
        if (nextIndex == input.size) {
            break
        }
        if (input[nextIndex].kind != TokenKind.COMMA) {
            diagReport(DiagReportLevel.ERROR, input[nextIndex..nextIndex+1],
                       "Input must be a comma-separated list of expressions",
                       "Expected comma")
        }
        index = nextIndex + 1  // 跳过逗号
    }
    let result = quote()
    for (expr in exprs) {
        result.append(quote(
            print($(expr.toTokens().toString()) + " = ")
            println($(expr))
        ))
    }
    return result
}
```

使用案例：

<!-- verify -macro15 -->
<!-- cfg="--debug-macro" -->

```cangjie
import define.*

main() {
    let x = 3
    let y = 2
    @dprint2(x, y, x + y)
}
```

输出结果为：

<!-- verify -macro15 -->

```text
x = 3
y = 2
x + y = 5
```

在宏的实现中，使用 while 循环从索引 0 开始依次解析每个表达式。变量 `index` 保存当前解析的位置。每次调用 `parseExprFragment` 时，从当前位置开始，并返回解析后的位置（以及解析得到的表达式）。如果解析后的位置到达了输入的结尾，则退出循环。否则检查到达的位置是否是一个逗号，如果不是逗号，报错并退出，如果是逗号，跳过这个逗号并开始下一轮的解析。在得到表达式的列表后，依次输出每个表达式。

## 一个简单的 DSL

这个案例展示了如何使用宏实现一个简单的 DSL（Domain Specific Language，领域特定语言）。LINQ（Language Integrated Query，语言集成查询）是微软 .NET 框架的一个组成部分，它提供了一种统一的数据查询语法，允许开发者使用类似 SQL 的查询语句来操作各种数据源。在这里，仅展示一个最简单的 LINQ 语法的支持。

希望支持的语法为：

```text
from <variable> in <list> where <condition> select <expression>
```

其中，`variable` 是一个标识符，`list`、`condition` 和 `expression` 都是表达式。因此，实现宏的策略是先后提取标识符和表达式，同时检查中间的关键字是正确的。最后，生成由提取部分组成的查询结果。

宏的实现如下：

<!-- verify -macro16 -->
<!-- cfg="--compile-macro" -->

```cangjie
macro package define

import std.ast.*

public macro linq(input: Tokens) {
    let syntaxMsg = "Syntax is \"from <attrib> in <table> where <cond> select <expr>\""
    if (input.size == 0 || input[0].value != "from") {
        diagReport(DiagReportLevel.ERROR, input[0..1], syntaxMsg,
                   "Expected keyword \"from\" here.")
    }
    if (input.size <= 1 || input[1].kind != TokenKind.IDENTIFIER) {
        diagReport(DiagReportLevel.ERROR, input[1..2], syntaxMsg,
                   "Expected identifier here.")
    }
    let attribute = input[1]
    if (input.size <= 2 || input[2].value != "in") {
        diagReport(DiagReportLevel.ERROR, input[2..3], syntaxMsg,
                   "Expected keyword \"in\" here.")
    }
    var index: Int64 = 3
    let (table, nextIndex) = parseExprFragment(input, startFrom: index)
    if (nextIndex == input.size || input[nextIndex].value != "where") {
        diagReport(DiagReportLevel.ERROR, input[nextIndex..nextIndex+1], syntaxMsg,
                   "Expected keyword \"where\" here.")
    }
    index = nextIndex + 1  // 跳过where
    let (cond, nextIndex2) = parseExprFragment(input, startFrom: index)
    if (nextIndex2 == input.size || input[nextIndex2].value != "select") {
        diagReport(DiagReportLevel.ERROR, input[nextIndex2..nextIndex2+1], syntaxMsg,
                   "Expected keyword \"select\" here.")
    }
    index = nextIndex2 + 1  // 跳过select
    let (expr, nextIndex3) = parseExprFragment(input, startFrom: index)

    return quote(
        for ($(attribute) in $(table)) {
            if ($(cond)) {
                println($(expr))
            }
        }
    )
}
```

使用案例：

<!-- verify -macro16 -->
<!-- cfg="--debug-macro" -->

```cangjie
import define.*

main() {
    @linq(from x in 1..=10 where x % 2 == 1 select x * x)
}
```

这个例子从 1, 2, ... 10 列表中筛选出奇数，然后返回所有奇数的平方。输出结果为：

<!-- verify -macro16 -->

```text
1
9
25
49
81
```

可以看到，宏的实现的很大部分用于解析并校验输入的 Tokens，这对宏的可用性至关重要。实际的 LINQ 语言（以及大多数 DSL）的语法更加复杂，需要一整套解析的机制，通过识别不同的关键字或连接符来决定下一步解析的内容。


---

<!-- Content from source_zh_cn/reflect_and_annotation/dynamic_feature.md -->
# 动态特性

本章介绍 Cangjie 的动态特性，应用动态特性开发者能够更为优雅的实现一些功能。仓颉的动态特性主要包含反射。

## 仓颉反射基本介绍

反射指程序可以访问、检测和修改它本身状态或行为的一种机制。

反射这一动态特性有以下的优点：

- 提高了程序的灵活性和扩展性。

- 程序能够在运行时获悉各种对象的类型，对其成员进行枚举、调用等操作。

- 允许在运行时创建新类型，无需提前硬编码。

但使用反射调用，其性能通常低于直接调用，因此反射机制主要应用于对灵活性和拓展性要求很高的系统框架上。

## 如何获得 TypeInfo

对于仓颉的反射特性，需要知道 TypeInfo 这一类型，这个核心类型中记录任意类型的类型信息，并且定义了方法用于获取类型信息、设置值等。当然为了便于用户操作仓颉还提供了 ClassTypeInfo、PrimitiveTypeInfo、ParameterInfo 等一系列的信息类型。

可以使用三种静态的 `of` 方法来生成 TypeInfo 信息类。

```cangjie
public class TypeInfo {
    public static func of(a: Any): TypeInfo
    public static func of(a: Object): ClassTypeInfo
    public static func of<T>(): TypeInfo
}
```

当采用入参为 `Any` 和 `Object` 类型的 `of` 函数，输出为该实例的运行时类型信息，采用泛型参数的 `of` 函数则会返回传入参数的静态类型信息。两种方法产生的信息完全相同，但不保证一定对应同一对象。

例如可以用反射来获取一个自定义类型的类型信息。

```cangjie
import std.reflect.*

class Foo {}

main() {
    let a: Foo = Foo()
    let info: TypeInfo = TypeInfo.of(a)
    let info2: TypeInfo = TypeInfo.of<Foo>()
    println(info)
    println(info2)
}
```

编译并执行上面的代码，会输出：

```text
default.Foo
default.Foo
```

此外 TypeInfo 还提供了静态函数 `get`，该接口可通过传入的类型名称获取 TypeInfo。

```cangjie
public class TypeInfo {
    public static func get(qualifiedName: String): TypeInfo
}
```

请注意，传入参数需要符合 `module.package.type` 的完全限定模式规则。对于编译器预导入的类型，包含 core 包中的类型和编译器内置类型，例如 `primitive type`、`Option`、`Iterable` 等，查找的字符串需要直接使用其类型名，不能带包名和模块名前缀。当运行时无法查询到对应类型的实例，则会抛出 `InfoNotFoundException`。

```cangjie
let t1: TypeInfo = TypeInfo.get("Int64")
let t1: TypeInfo = TypeInfo.get("default.Foo")
let t2: TypeInfo = TypeInfo.get("std.socket.TcpSocket")
let t3: TypeInfo = TypeInfo.get("net.http.ServerBuilder")
```

采用这种方式时无法获取一个未实例化的泛型类型。

```cangjie
import std.collection.*
import std.reflect.*

class A<T> {
    A(public let t: T) {}
}

class B<T> {
    B(public let t: T) {}
}

main() {
    let aInfo: TypeInfo = TypeInfo.get("default.A<Int64>")// Error,`default.A<Int64>` is not instantiated，will throw InfoNotFoundException
    let b: B<Int64> = B<Int64>(1)
    let bInfo: TypeInfo = TypeInfo.get("default.B<Int64>")// OK `default.B<Int64>` has been instantiated.
}
```

## 如何使用反射访问成员

在获取到对应的类型信息类即 `TypeInfo` 后，便可以通过其相应接口访问对应类的实例成员以及静态成员。此外 `TypeInfo` 的子类 `ClassTypeInfo` 还提供了接口用于访问类公开的构造函数以及它的成员变量、属性、函数。仓颉的反射被设计为只能访问到类型内 public 的成员，意味着 private 和 protected 修饰的成员在反射中是不可见的。

例如当想要在运行时对类的某一实例成员变量进行获取与修改。

```cangjie
import std.reflect.*

public class Foo {
    public static var param1 = 20
    public var param2 = 10
}

main(): Unit{
    let obj = Foo()
    let info = TypeInfo.of(obj)
    let staticVarInfo = info.getStaticVariable("param1")
    let instanceVarInfo = info.getInstanceVariable("param2")
    println("成员变量初始值")
    print("Foo 的静态成员变量 ${staticVarInfo} = ")
    println((staticVarInfo.getValue() as Int64).getOrThrow())
    print("obj 的实例成员变量 ${instanceVarInfo} = ")
    println((instanceVarInfo.getValue(obj) as Int64).getOrThrow())
    println("更改成员变量")
    staticVarInfo.setValue(8)
    instanceVarInfo.setValue(obj, 25)
    print("Foo 的静态成员变量 ${staticVarInfo} = ")
    println((staticVarInfo.getValue() as Int64).getOrThrow())
    print("obj 的实例成员变量 ${instanceVarInfo} = ")
    println((instanceVarInfo.getValue(obj) as Int64).getOrThrow())
    return
}
```

编译并执行上面的代码，会输出：

```text
成员变量初始值
Foo 的静态成员变量 static param1: Int64 = 20
obj 的实例成员变量 param2: Int64 = 10
更改成员变量
Foo 的静态成员变量 static param1: Int64 = 8
obj 的实例成员变量 param2: Int64 = 25
```

同时也可以通过反射对属性进行检查以及修改。

```cangjie
import std.reflect.*

public class Foo {
    public let _p1: Int64 = 1
    public prop p1: Int64 {
        get() { _p1 }
    }
    public var _p2: Int64 = 2
    public mut prop p2: Int64 {
        get() { _p2 }
        set(v) { _p2 = v }
    }
}

main(): Unit{
    let obj = Foo()
    let info = TypeInfo.of(obj)
    let instanceProps = info.instanceProperties.toArray()
    println("obj的实例成员属性包含${instanceProps}")
    let PropInfo1 = info.getInstanceProperty("p1")
    let PropInfo2 = info.getInstanceProperty("p2")

    println((PropInfo1.getValue(obj) as Int64).getOrThrow())
    println((PropInfo2.getValue(obj) as Int64).getOrThrow())
    if (PropInfo1.isMutable()) {
        PropInfo1.setValue(obj, 10)
    }
    if (PropInfo2.isMutable()) {
        PropInfo2.setValue(obj, 20)
    }
    println((PropInfo1.getValue(obj) as Int64).getOrThrow())
    println((PropInfo2.getValue(obj) as Int64).getOrThrow())
    return
}
```

编译并执行上面的代码，会输出：

```text
obj 的实例成员属性包含[prop p1: Int64, mut prop p2: Int64]
1
2
1
20
```

还可以通过反射机制进行函数调用。

```cangjie
import std.reflect.*

public class Foo {
    public static func f1(v0: Int64, v1: Int64): Int64 {
        return v0 + v1
    }
}

main(): Unit {
    var num = 0
    let intInfo = TypeInfo.of<Int64>()
    let funcInfo = TypeInfo.of<Foo>().getStaticFunction("f1", intInfo, intInfo)
    num = (funcInfo.apply(TypeInfo.of<Foo>(), [1, 1]) as Int64).getOrThrow()
    println(num)
}
```

编译并执行上面的代码，会输出：

```text
2
```


---

<!-- Content from source_zh_cn/reflect_and_annotation/anno.md -->
# 注解

仓颉中提供了一些内置编译标记用来支持一些特殊情况的处理。

## 确保正确使用整数运算溢出策略的内置编译标记

仓颉中提供三种内置编译标记来控制整数溢出的处理策略，即 `@OverflowThrowing`，`@OverflowWrapping` 和 `@OverflowSaturating` ，这些编译标记当前只能标记于函数声明之上，作用于函数内的整数运算和整型转换。它们分别对应以下三种溢出处理策略：

1. 抛出异常（throwing）：当整数运算溢出时，抛出异常。

    <!-- compile -->

    ```cangjie
    @OverflowThrowing
    func add(a: Int8, b: Int8){
        return a + b
    }
    main() {
        add(100,29)
        /* 100 + 29 在数学上等于 129，
        * 在 Int8 的表示范围上发生了上溢出，
        * 程序抛出异常
        */
    }
    ```

    需要注意的是，对于整数溢出行为是 throwing 的场景，若整数溢出可提前在编译期检测出来，则编译器会直接给出报错。

    <!-- compile.error -->

    ```cangjie
    @OverflowThrowing
    main() {
        let res: Int8 = Int8(100) + Int8(29) // Error, arithmetic operation '+' overflow
        // 100 + 29 在数学上等于 129，在 Int8 的表示范围上发生了上溢出，编译器检测出来并报错
        let con: UInt8 = UInt8(-132) // Error, integer type conversion overflow
        /* -132 在 UInt8 的表示范围上发生了下溢出，
        * 程序抛出异常
        */
    }
    ```

2. 高位截断（wrapping）：当整数运算的结果超出用于接收它的内存空间所能表示的数据范围时，则截断超出该内存空间的部分。

    <!-- compile -->

    ```cangjie
    @OverflowWrapping
    main() {
        let res: Int8 = Int8(105) * Int8(4)
        /* 105 * 4 在数学上等于 420，
        * 对应的二进制为 1 1010 0100，
        * 超过了用于接收该结果的 8 位内存空间，
        * 截断后的结果在二进制上表示为 1010 0100，
        * 对应为有符号整数 -92
        */
        let temp: Int16 = Int16(-132)
        let con: UInt8 = UInt8(temp)
        /* -132 对应的二进制为 1111 1111 0111 1100，
        * 超过了用于接收该结果的 8 位内存空间，
        * 截断后的结果在二进制上表示为 0111 1100
        * 对应为有符号整数 124
        */
    }
    ```

3. 饱和（saturating）：当整数运算溢出时，选择对应固定精度的极值作为结果。

    <!-- compile -->

    ```cangjie
    @OverflowSaturating
    main() {
        let res: Int8 = Int8(-100) - Int8(45)
        /* -100 - 45 在数学上等于 -145，
        * 在 Int8 的表示范围上发生了下溢出，
        * 选择 Int8 的最小值 -128 作为结果
        */
        let con: Int8 = Int8(1024)
        /* 1024 在 Int8 的表示范围上发生了上溢出，
        * 选择 Int8 的最大值 127 作为结果
        */
    }
    ```

默认情况下（即未标注该类内置编译标记时），采取抛出异常（`@OverflowThrowing`）的处理策略。

实际情况下需要根据业务场景的需求正确选择溢出策略。例如要在 `Int32` 上实现某种安全运算，使得计算结果和计算过程在数学上相等，就需要使用抛出异常的策略。

【反例】

<!-- compile -->

```cangjie
// 计算结果被高位截断
@OverflowWrapping
func operation(a: Int32, b: Int32): Int32 {
    a + b // No exception will be thrown when overflow occurs
}
```

该错误例子使用了高位截断的溢出策略，比如当传入的参数 `a` 和 `b` 较大导致结果溢出时，会产生高位截断的情况，导致函数返回结果和计算表达式 `a + b` 在数学上不是相等关系。

【正例】

<!-- run -->

```cangjie
// 安全
@OverflowThrowing
func operation(a: Int32, b: Int32): Int32 {
    a + b
}

main(): Int64 {
    try {
        operation(Int32.Max, 1)
    } catch (e: ArithmeticException) {
        println(e.message)
        //Handle error
    }
    0
}
```

该正确例子使用了抛出异常的溢出策略，当传入的参数 `a` 和 `b` 较大导致整数溢出时，`operation` 函数会抛出异常。

下面总结了可能造成整数溢出的数学操作符。

| 操作符  | 溢出 |         操作符          | 溢出 |         操作符         | 溢出 | 操作符  | 溢出 |
|:----:|:--:|:--------------------:|:--:|:-------------------:|:--:|:----:|:--:|
| `+`  | Y  |         `-=`         | Y  |        `<<`         | N  | `<`  | N  |
| `-`  | Y  |         `*=`         | Y  |        `>>`         | N  | `>`  | N  |
| `*`  | Y  |         `/=`         | Y  |         `&`         | N  | `>=` | N  |
| `/`  | Y  |         `%=`         | N  | <code>&vert;</code> | N  | `<=` | N  |
| `%`  | N  |        `<<=`         | N  |         `^`         | N  | `==` | N  |
| `++` | Y  |        `>>=`         | N  |        `**=`        | Y  |      |    |
| `--` | Y  |         `&=`         | N  |         `!`         | N  |      |    |
| `=`  | N  | <code>&vert;=</code> | N  |        `!=`         | N  |      |    |
| `+=` | Y  |         `^=`         | N  |        `**`         | Y  |      |    |

## 测试框架内置编译标记

在测试中使用 mock 时，当 mock 的对象是与静态和顶级声明相关内容时，需要通过测试框架内置编译标记来指示编译器做一些准备工作，才能正常使用 mock。

测试框架内置编译标记 `@EnsurePreparedToMock` 只能在 lambda 表达式上使用，lambda 表达式调用静态和顶级声明作为其最后一个表达式，然后编译器将准备这个声明以供 mock。

例如：

<!-- run -pkg1 -->
<!-- cfg="-p prod --mock=on --output-type=dylib" -->

```cangjie
package prod

public func test(a: String, b: String): String {
    a + b
}
```

<!-- run -pkg1 -->
<!-- cfg="-lprod -L . --test" -->

```cangjie
package test

import prod.*
import std.unittest.mock.*

@Test
public class TestA {
    @TestCase
    func case1(): Unit {
        { =>
            let matcher0 = Matchers.eq("z")
            let matcher1 = Matchers.eq("y")
            let stubCall = @EnsurePreparedToMock { => return(test(matcher0.value(), matcher1.value())) }
            ConfigureMock.stubFunction(stubCall,[matcher0.withDescription(#"eq("z")"#), matcher1.withDescription(#"eq("y")"#)], Option<String>.None, "test", #"test("z", "y")"#, 15)
        }().returns("mocked value")
        println(test("z", "y")) // prints "mocked value"
    }
}
```

上述示例中，`ConfigureMock.stubFunction` 为函数 `test` 注册了一个桩，`returns` 为定义的桩设置返回值。

> **注意：**
>
> 通常，标准库的 mock 接口可用于定义 mock 声明，并且在常规情况下不应直接使用此内置注释。相反，应该使用相应的标准库函数。这些标准库函数在内部使用 `@EnsurePreparedToMock`。

使用 `@EnsurePreparedToMock` 注解的约束：

- 仅当使用测试和 mock 相关编译选项进行编译时才允许使用（使用 `--test`/`--test-only` 和 `--mock=on`/`--mock=runtime-error` 编译选项）。
- 只能应用于具有合适的最后一个表达式的 lambda。
- lambda 的最后一个表达式应该是调用、成员访问或引用表达式，要求是：
    - 顶级函数或变量；
    - 静态函数、属性或字段；
    - foreign 声明​​；
    - 不是局部函数或变量；
    - 非私有声明；
    - 不是 const 表达式或声明；
    - 必须是来自通过 mock 模式构建的包的声明。

## 自定义注解

自定义注解机制用来让反射（详见[反射章节](dynamic_feature.md)）获取标注内容，目的是在类型元数据之外提供更多的有用信息，以支持更复杂的逻辑。

开发者可以通过自定义类型标注 `@Annotation` 方式创建自己的自定义注解。`@Annotation` 只能修饰 `class`，并且不能是 `abstract` 或 `open` 或 `sealed` 修饰的 `class`。当一个 `class` 声明它标注了 `@Annotation`，那么它必须要提供至少一个 `const init` 函数，否则编译器会报错。

下面的例子定义了一个自定义注解 `@Version`，并用其修饰 `A`, `B` 和 `C`。在 `main` 中，通过反射获取到类上的 `@Version` 注解信息，并将其打印出来。

<!-- verify -->

```cangjie
package pkg

import std.reflect.TypeInfo

@Annotation
public class Version {
    let code: String
    const init(code: String) {
        this.code = code
    }
}

@Version["1.0"]
class A {}

@Version["1.1"]
class B {}

main() {
    let objects = [A(), B()]
    for (obj in objects) {
        let annOpt = TypeInfo.of(obj).findAnnotation<Version>()
        if (let Some(ann) <- annOpt) {
            println(ann.code)
        }
    }
}
```

编译并执行上述代码，输出结果为：

```text
1.0
1.1
```

注解信息需要在编译时生成信息并绑定到类型上，自定义注解在使用时必须使用 `const init` 构建出合法的实例。注解声明语法与声明宏语法一致，后面的 `[]` 括号中需要按顺序或命名参数规则传入参数，且参数必须是 const 表达式，详见[常量求值章节](../function/const_func_and_eval.md)。对于拥有无参构造函数的注解类型，声明时允许省略中括号。

下面的例子中定义了一个拥有无参 `const init` 的自定义注解 `@Marked`，使用时 `@Marked` 和 `@Marked[]` 这两种写法均可。

<!-- verify -->

```cangjie
package pkg

import std.reflect.TypeInfo

@Annotation
public class Marked {
    const init() {}
}

@Marked
class A {}

@Marked[]
class B {}

main() {
    if (TypeInfo.of(A()).findAnnotation<Marked>().isSome()) {
        println("A is Marked")
    }
    if (TypeInfo.of(B()).findAnnotation<Marked>().isSome()) {
        println("B is Marked")
    }
}
```

编译并执行上述代码，输出结果为：

```text
A is Marked
B is Marked
```

对于同一个注解目标，同一个注解类不允许声明多次，即不可重复。

<!-- verify.error -->
<!-- cfg="--Marked" -->

```cangjie
@Marked
@Marked // Error
class A {}
```

`Annotation` 不会被继承，因此一个类型的注解元数据只会来自它定义时声明的注解。如果需要父类型的注解元数据信息，需要开发者自己用反射接口查询。

下面的例子中，`A` 被 `@Marked` 注解修饰，`B` 继承 `A`，但是 `B` 没有 `A` 的注解。

<!-- verify -->

```cangjie
package pkg

import std.reflect.TypeInfo

@Annotation
public class Marked {
    const init() {}
}

@Marked
open class A {}

class B <: A {}

main() {
    if (TypeInfo.of(A()).findAnnotation<Marked>().isSome()) {
        println("A is Marked")
    }
    if (TypeInfo.of(B()).findAnnotation<Marked>().isSome()) {
        println("B is Marked")
    }
}
```

编译并执行上述代码，输出结果为：

```text
A is Marked
```

自定义注解可以用在类型声明（`class`、`struct`、`enum`、`interface`）、成员函数/构造函数中的参数、构造函数声明、成员函数声明、成员变量声明、成员属性声明。也可以限制自己可以使用的位置，这样可以减少开发者的误用，这类注解需要在声明 `@Annotation` 时标注 `target` 参数，参数类型为 `Array<AnnotationKind>`。其中，`AnnotationKind` 是标准库中定义的 `enum`。当没有限定 target 的时候，该自定义注解可以用在以上全部位置。当限定 target 时，只能用在声明的列表中。

<!-- compile -->

```cangjie
public enum AnnotationKind {
    | Type
    | Parameter
    | Init
    | MemberProperty
    | MemberFunction
    | MemberVariable
}
```

下面的例子中，自定义注解通过 `target` 限定只能用在成员函数上，用在其他位置会编译报错。

<!--compile.error -->

```cangjie
@Annotation[target: [MemberFunction]]
public class Marked {
    const init() {}
}

class A {
    @Marked // OK, member funciton
    func marked() {}
}

@Marked // Error, type
class B {}
```


---

<!-- Content from source_zh_cn/FFI/cangjie-c.md -->
# 仓颉-C 互操作

为了兼容已有的生态，仓颉支持调用 C 语言的函数，也支持 C 语言调用仓颉的函数。

## 仓颉调用 C 的函数

在仓颉中要调用 C 的函数，需要在仓颉语言中用 `@C` 和 `foreign` 关键字声明这个函数，但 `@C` 在修饰 `foreign` 声明的时候，可以省略。

举个例子，假设要调用 C 的 `rand` 和 `printf` 函数，它的函数签名如下：

```c
// stdlib.h
int rand();

// stdio.h
int printf (const char *fmt, ...);
```

那么在仓颉中调用这两个函数的方式如下：

```cangjie
// declare the function by `foreign` keyword, and omit `@C`
foreign func rand(): Int32
foreign func printf(fmt: CString, ...): Int32

main() {
    // call this function by `unsafe` block
    let r = unsafe { rand() }
    println("random number ${r}")
    unsafe {
        var fmt = LibC.mallocCString("Hello, No.%d\n")
        printf(fmt, 1)
        LibC.free(fmt)
    }
}
```

需要注意的是：

1. `foreign` 修饰函数声明，代表该函数为外部函数。被 `foreign` 修饰的函数只能有函数声明，不能有函数实现。
2. `foreign` 声明的函数，参数和返回类型必须符合 C 和仓颉数据类型之间的映射关系，详情请参见[类型映射](./cangjie-c.md#类型映射)。
3. 由于 C 侧函数很可能产生不安全操作，所以调用 `foreign` 修饰的函数需要被 `unsafe` 块包裹，否则会发生编译错误。
4. `@C` 修饰的 `foreign` 关键字只能用来修饰函数声明，不可用来修饰其他声明，否则会发生编译错误。
5. `@C` 只支持修饰 `foreign` 函数、顶层作用域中的非泛型函数和 `struct` 类型。
6. `foreign` 函数不支持命名参数和参数默认值。`foreign` 函数允许变长参数，使用 `...` 表达，只能用于参数列表的最后。变长参数均需要满足 `CType` 约束，但不必是同一类型。
7. 仓颉（CJNative 后端）虽然提供了栈扩容能力，但是由于 C 侧函数实际使用栈大小仓颉无法感知，所以 ffi 调用进入 C 函数后，仍然存在栈溢出的风险（可能导致程序运行时崩溃或者产生不可预期的行为），需要开发者根据实际情况，修改 `cjStackSize` 的配置。

一些不合法的 `foreign` 声明的示例代码如下：

```cangjie
foreign func rand(): Int32 { // compiler error
    return 0
}
@C
foreign var a: Int32 = 0 // compiler error
@C
foreign class A{} // compiler error
@C
foreign interface B{} // compiler error
```

## CFunc

仓颉中的 `CFunc` 指可以被 C 语言代码调用的函数，共有以下三种形式：

1. `@C` 修饰的 `foreign` 函数
2. `@C` 修饰的仓颉函数
3. 类型为 `CFunc` 的 `lambda` 表达式，与普通的 lambda 表达式不同，`CFunc lambda` 不能捕获变量。

<!-- run -->

```cangjie
// Case 1
foreign func free(ptr: CPointer<Int8>): Unit

// Case 2
@C
func callableInC(ptr: CPointer<Int8>) {
    print("This function is defined in Cangjie.")
}

// Case 3
let f1: CFunc<(CPointer<Int8>) -> Unit> = { ptr =>
    print("This function is defined with CFunc lambda.")
}
```

以上三种形式声明/定义的函数的类型均为 `CFunc<(CPointer<Int8>) -> Unit>`。`CFunc` 对应 C 语言的函数指针类型。这个类型为泛型类型，其泛型参数表示该 `CFunc` 入参和返回值类型，使用方式如下：

<!-- run -->

```cangjie
foreign func atexit(cb: CFunc<() -> Unit>): Int32
```

与 `foreign` 函数一样，其他形式的 `CFunc` 的参数和返回类型必须满足 `CType` 约束，且不支持命名参数和参数默认值。

`CFunc` 在仓颉代码中被调用时，需要处在 `unsafe` 上下文中。

仓颉语言支持将一个 `CPointer<T>` 类型的变量类型转换为一个具体的 `CFunc`，其中 `CPointer` 的泛型参数 `T` 可以是满足 `CType` 约束的任意类型，使用方式如下：

<!-- compile -->

```cangjie
main() {
    var ptr = CPointer<Int8>()
    var f = CFunc<() -> Unit>(ptr)
    unsafe { f() } // core dumped when running, because the pointer is nullptr.
}
```

> **注意：**
>
> 将一个指针强制类型转换为 `CFunc` 并进行函数调用是危险行为，需要用户保证指针指向的是一个切实可用的函数地址，否则将发生运行时错误。

## inout 参数

在仓颉中调用 `CFunc` 时，其实参可以使用 `inout` 关键字修饰，组成引用传值表达式，此时，该参数按引用传递。引用传值表达式的类型为 `CPointer<T>`，其中 `T` 为 `inout` 修饰的表达式的类型。

引用传值表达式具有以下约束：

- 仅可用于对 `CFunc` 的调用处。
- 其修饰对象的类型必须满足 `CType` 约束，但不可以是 `CString`。
- 其修饰对象不可以是用 `let` 定义的，不可以是字面量、入参、其他表达式的值等临时变量。
- 通过仓颉侧引用传值表达式传递到 C 侧的指针，仅保证在函数调用期间有效，即此种场景下 C 侧不应该保存指针以留作后用。

`inout` 修饰的变量，可以是定义在顶层作用域中的变量、局部变量、`struct` 中的成员变量，但不能直接或间接来源于 `class` 的实例成员变量。

下面是一个例子：

```cangjie
foreign func foo1(ptr: CPointer<Int32>): Unit

@C
func foo2(ptr: CPointer<Int32>): Unit {
    let n = unsafe { ptr.read() }
    println("*ptr = ${n}")
}

let foo3: CFunc<(CPointer<Int32>) -> Unit> = { ptr =>
    let n = unsafe { ptr.read() }
    println("*ptr = ${n}")
}

struct Data {
    var n: Int32 = 0
}

class A {
    var data = Data()
}

main() {
    var n: Int32 = 0
    unsafe {
        foo1(inout n)  // OK
        foo2(inout n)  // OK
        foo3(inout n)  // OK
    }
    var data = Data()
    var a = A()
    unsafe {
        foo1(inout data.n)   // OK
        foo1(inout a.data.n) // Error, n is derived indirectly from instance member variables of class A
    }
}
```

> **注意：**
>
> 使用宏扩展特性时，在宏的定义中，暂时不能使用 `inout` 参数特性。

## unsafe

在引入与 C 语言的互操作过程中，同时也引入了 C 的许多不安全因素，因此在仓颉中使用 `unsafe` 关键字，用于对跨 C 调用的不安全行为进行标识。

关于 unsafe 关键字，有以下几点说明：

- `unsafe` 可以修饰函数、表达式，也可以修饰一段作用域。
- 被 `@C` 修饰的函数，被调用处需要在 `unsafe` 上下文中。
- 在调用 `CFunc` 时，使用处需要在 `unsafe` 上下文中。
- `foreign` 函数在仓颉中进行调用，被调用处需要在 `unsafe` 上下文中。
- 当被调用函数被 `unsafe` 修饰时，被调用处需要在 `unsafe` 上下文中。

使用方式如下：

<!-- run -->

```cangjie
foreign func rand(): Int32

@C
func foo(): Unit {
    println("foo")
}

var foo1: CFunc<() -> Unit> = { =>
    println("foo1")
}

main(): Int64 {
    unsafe {
        rand()           // Call foreign func.
        foo()            // Call @C func.
        foo1()           // Call CFunc var.
    }
    0
}
```

需要注意的是，普通 `lambda` 无法传递 `unsafe` 属性，当 `unsafe` 的 `lambda` 逃逸后，可以不在 `unsafe` 上下文中直接调用而未产生任何编译错误。当需要在 `lambda` 中调用 `unsafe` 函数时，建议在 `unsafe` 块中进行调用，参考如下用例：

<!-- run -->

```cangjie
unsafe func A(){}
unsafe func B(){
    var f = { =>
        unsafe { A() } // Avoid calling A() directly without unsafe in a normal lambda.
    }
    return f
}
main() {
    var f = unsafe{ B() }
    f()
    println("Hello World")
}
```

## 调用约定

函数调用约定描述调用者和被调用者双方如何进行函数调用（如参数如何传递、栈由谁清理等），函数调用和被调用双方必须使用相同的调用约定才能正常运行。仓颉编程语言通过 `@CallingConv` 来表示各种调用约定，支持的调用约定如下：

- **CDECL**：`CDECL` 表示 clang 的 C 编译器在不同平台上默认使用的调用约定。
- **STDCALL**：`STDCALL` 表示 Win32 API 使用的调用约定。

通过 C 语言互操作机制调用的 C 函数，未指定调用约定时将采用默认的 `CDECL` 调用约定。如下调用 C 标准库函数 `rand` 示例：

<!-- run -->

```cangjie
@CallingConv[CDECL]   // Can be omitted in default.
foreign func rand(): Int32

main() {
    println(unsafe { rand() })
}
```

`@CallingConv` 只能用于修饰 `foreign` 块、单个 `foreign` 函数和顶层作用域中的 `CFunc` 函数。当 `@CallingConv` 修饰 `foreign` 块时，会为 `foreign` 块中的每个函数分别加上相同的 `@CallingConv` 修饰。

## 使用说明

- 操作系统线程局部变量使用约束

  仓颉和 C 语言互操作时，使用操作系统线程的局部变量存在风险，说明如下：

  1. 线程局部变量包括 C 语言提供的 `thread_local` 定义的变量和使用 `pthread_key_create` 创建的变量。
  2. 仓颉具备仓颉线程调度能力，支持仓颉线程的切换和恢复，仓颉线程被调度到哪个操作系统线程是随机的，从而在仓颉线程上调用其他语言的线程局部变量是有风险的。

  如下示例中，仓颉调用 C 语言的线程局部变量存在风险：

  ```c
  // C language logic using thread_local
  static thread_local int64_t count = 0;
  int64_t getCount() {
      count++;
      return count;
  }
  ```

  ```cangjie
  foreign func getCount(): Int64
  // Cangjie invokes the preceding C language logic
  spawn {
      let r1 = unsafe { getCount() }  // r1 equals 1
      sleep(Duration.second * 10)
      let r2 = unsafe { getCount() }  // r2 may not be equal to 2
  }
  ```

- 线程绑定使用约束

  仓颉调用 C 语言执行互操作逻辑时，仓颉线程调度到哪个操作系统线程是随机的，线程优先级和线程亲和性等与线程绑定的行为不建议使用。

- 同步原语使用说明

  仓颉调用 C 语言执行互操作逻辑时，当前这个仓颉线程会等待互操作逻辑执行结束，不建议在其他语言中出现可能导致长时间等待的阻塞性行为。

- 对进程 fork 场景的支持说明

  仓颉调用 C 语言执行互操作逻辑时，如果在 C 语言中以 `fork()` 方式创建子进程，子进程中不支持执行仓颉逻辑。同一进程中其他操作系统线程不受影响。

- 进程退出时的说明

  仓颉调用 C 语言执行互操作逻辑时，如果在 C 语言中退出进程，进程内共享的资源已经释放，可能导致非法访问等错误。

## 类型映射

### 基础类型

仓颉与 C 语言支持基本数据类型的映射，总体原则是：

1. 仓颉的类型不包含指向托管内存的引用类型；
2. 仓颉的类型和 C 的类型具有同样的内存布局。

比如说，一些基本的类型映射关系如下：

| Cangjie Type |   C Type   |    Size (byte)     |
|:------------:|:----------:|:------------------:|
|    `Unit`    |   `void`   |         0          |
|    `Bool`    |   `bool`   |         1          |
|   `UInt8`    |   `char`   |         1          |
|    `Int8`    |  `int8_t`  |         1          |
|   `UInt8`    | `uint8_t`  |         1          |
|   `Int16`    | `int16_t`  |         2          |
|   `UInt16`   | `uint16_t` |         2          |
|   `Int32`    | `int32_t`  |         4          |
|   `UInt32`   | `uint32_t` |         4          |
|   `Int64`    | `int64_t`  |         8          |
|   `UInt64`   | `uint64_t` |         8          |
| `IntNative`  | `ssize_t`  | platform dependent |
| `UIntNative` |  `size_t`  | platform dependent |
|  `Float32`   |  `float`   |         4          |
|  `Float64`   |  `double`  |         8          |

> **说明：**
>
> `int` 类型、`long` 类型等由于其在不同平台上的不确定性，需要程序员自行指定对应仓颉编程语言类型。在 C 互操作场景中，与 C 语言类似，`Unit` 类型仅可作为 `CFunc` 中的返回类型和 `CPointer` 的泛型参数。

仓颉也支持与 C 语言的结构体和指针类型的映射。

### 结构体

对于结构体类型，仓颉用 `@C` 修饰的 `struct` 来对应。比如说 C 语言里面有这样的一个结构体：

```c
typedef struct {
    long long x;
    long long y;
    long long z;
} Point3D;
```

那么它对应的仓颉类型可以这样定义：

<!-- run -example00-->

```cangjie
@C
struct Point3D {
    var x: Int64 = 0
    var y: Int64 = 0
    var z: Int64 = 0
}
```

如果 C 语言里有这样的一个函数：

```c
Point3D addPoint(Point3D p1, Point3D p2);
```

那么对应的，在仓颉里面可以这样声明这个函数：

<!-- run -example00-->

```cangjie
foreign func addPoint(p1: Point3D, p2: Point3D): Point3D
```

用 `@C` 修饰的 `struct` 必须满足以下限制：

- 成员变量的类型必须满足 `CType` 约束
- 不能实现或者扩展 `interfaces`
- 不能作为 `enum` 的关联值类型
- 不允许被闭包捕获
- 不能具有泛型参数

用 `@C` 修饰的 `struct` 自动满足 `CType` 约束。

### 指针

对于指针类型，仓颉提供 `CPointer<T>` 类型来对应 C 侧的指针类型，其泛型参数 `T` 需要满足 `CType` 约束。比如对于 malloc 函数，在 C 里面的签名为：

```c
void* malloc(size_t size);
```

那么在仓颉中，它可以声明为：

<!-- run -->

```cangjie
foreign func malloc(size: UIntNative): CPointer<Unit>
```

`CPointer` 可以进行读写、偏移计算、判空以及转为指针的整型形式等，详细 API 可以参考《仓颉编程语言库 API》。其中读写和偏移计算为不安全行为，当不合法的指针调用这些函数时，可能发生未定义行为，这些 unsafe 函数需要在 unsafe 块中调用。

`CPointer` 的使用示例如下：

<!-- run -->

```cangjie
foreign func malloc(size: UIntNative): CPointer<Unit>
foreign func free(ptr: CPointer<Unit>): Unit

@C
struct Point3D {
    var x: Int64
    var y: Int64
    var z: Int64

    init(x: Int64, y: Int64, z: Int64) {
        this.x = x
        this.y = y
        this.z = z
    }
}

main() {
    let p1 = CPointer<Point3D>() // create a CPointer with null value
    if (p1.isNull()) {  // check if the pointer is null
        print("p1 is a null pointer")
    }

    let sizeofPoint3D: UIntNative = 24
    var p2 = unsafe { malloc(sizeofPoint3D) }    // malloc a Point3D in heap
    var p3 = unsafe { CPointer<Point3D>(p2) }    // pointer type cast

    unsafe { p3.write(Point3D(1, 2, 3)) } // write data through pointer

    let p4: Point3D = unsafe { p3.read() } // read data through pointer

    let p5: CPointer<Point3D> = unsafe { p3 + 1 } // offset of pointer

    unsafe { free(p2) }
}
```

仓颉语言支持 `CPointer` 之间的强制类型转换，转换前后的 `CPointer` 的泛型参数 `T` 均需要满足 `CType` 的约束，使用方式如下：

<!-- run -->

```cangjie
main() {
    var pInt8 = CPointer<Int8>()
    var pUInt8 = CPointer<UInt8>(pInt8) // CPointer<Int8> convert to CPointer<UInt8>
}
```

仓颉语言支持将一个 `CFunc` 类型的变量类型转换为一个具体的 `CPointer`，其中 `CPointer` 的泛型参数 `T` 可以是满足 `CType` 约束的任意类型，使用方式如下：

<!-- run -->

```cangjie
foreign func rand(): Int32
main() {
    var ptr = CPointer<Int8>(rand)
}
```

> **注意：**
>
> 将一个 `CFunc` 强制类型转换为指针通常是安全的，但是不应该对转换后的指针执行任何的 `read`，`write` 操作，可能会导致运行时错误。

### 数组

仓颉使用 `VArray` 类型与 C 的数组类型映射，`VArray` 可以作为函数参数和 `@C struct` 成员。当 `VArray<T, $N>` 中的元素类型 `T` 满足 `CType` 约束时， `VArray<T, $N>` 类型也满足 `CType` 约束。

**作为函数参数类型：**

当 `VArray` 作为 `CFunc` 的参数时， `CFunc` 的函数签名仅可以是 `CPointer<T>` 类型或 `VArray<T, $N>` 类型。当函数签名中的参数类型为 `VArray<T, $N>` 时，传递的参数仍以 `CPointer<T>` 形式传递。

`VArray` 作为参数的使用示例如下：

```cangjie
foreign func cfoo1(a: CPointer<Int32>): Unit
foreign func cfoo2(a: VArray<Int32, $3>): Unit
```

对应的 C 侧函数定义可以是：

```c
void cfoo1(int *a) { ... }
void cfoo2(int a[3]) { ... }
```

调用 `CFunc` 时，需要通过 `inout` 修饰 `VArray` 类型变量：

```cangjie
var a: VArray<Int32, $3> = [1, 2, 3]
unsafe {
    cfoo1(inout a)
    cfoo2(inout a)
}
```

`VArray` 不允许作为 `CFunc` 的返回值类型。

**作为 @C struct 成员：**

当 `VArray` 作为 `@C struct` 成员时，它的内存布局与 C 侧的结构体排布一致，需要保证仓颉侧声明长度与类型也与 C 完全一致：

```c
struct S {
    int a[2];
    int b[0];
}
```

在仓颉中，可以声明为如下结构体与 C 代码对应：

<!-- run -->

```cangjie
@C
struct S {
    var a = VArray<Int32, $2>(repeat: 0)
    var b = VArray<Int32, $0>(repeat: 0)
}
```

> **注意：**
>
> C 语言中允许结构体的最后一个字段为未指明长度的数组类型，该数组被称为柔性数组（flexible array），仓颉不支持包含柔性数组的结构体的映射。

### 字符串

特别地，对于 C 语言中的字符串类型，仓颉中设计了一个 `CString` 类型来对应。为简化为 C 语言字符串的操作，`CString` 提供了以下成员函数：

- `init(p: CPointer<UInt8>)`  通过 CPointer 构造一个 CString
- `func getChars()` 获取字符串的地址，类型为 `CPointer<UInt8>`
- `func size(): Int64`  计算该字符串的长度
- `func isEmpty(): Bool`  判断该字符串的长度是否为 0，如果字符串的指针为空返回 true
- `func isNotEmpty(): Bool`  判断该字符串的长度是否不为 0，如果字符串的指针为空返回 false
- `func isNull(): Bool`  判断该字符串的指针是否为 null
- `func startsWith(str: CString): Bool`  判断该字符串是否以 str 开头
- `func endsWith(str: CString): Bool`  判断该字符串是否以 str 结尾
- `func equals(rhs: CString): Bool`  判断该字符串是否与 rhs 相等
- `func equalsLower(rhs: CString): Bool`  判断该字符串是否与 rhs 相等，忽略大小写
- `func subCString(start: UInt64): CString`  从 start 开始截取子串，返回的子串存储在新分配的空间中
- `func subCString(start: UInt64, len: UInt64): CString`  从 start 开始截取长度为 len 的子串，返回的子串存储在新分配的空间中
- `func compare(str: CString): Int32`  该字符串与 str 比较，返回结果与 C 语言的 `strcmp(this, str)` 一样
- `func toString(): String`  用该字符串构造一个新的 String 对象
- `func asResource(): CStringResource` 获取 CString 的 Resource 类型

另外，将 `String` 类型转换为 `CString` 类型，可以通过调用 LibC 中的 `mallocCString` 接口，使用完成后需要对 `CString` 进行释放。

`CString` 的使用示例如下：

<!-- run -->

```cangjie
foreign func strlen(s: CString): UIntNative

main() {
    var s1 = unsafe { LibC.mallocCString("hello") }
    var s2 = unsafe { LibC.mallocCString("world") }

    let t1: Int64 = s1.size()
    let t2: Bool = s2.isEmpty()
    let t3: Bool = s1.equals(s2)
    let t4: Bool = s1.startsWith(s2)
    let t5: Int32 = s1.compare(s2)

    let length = unsafe { strlen(s1) }

    unsafe {
        LibC.free(s1)
        LibC.free(s2)
    }
}
```

### sizeOf/alignOf

仓颉还提供了 `sizeOf` 和 `alignOf` 两个函数，用于获取上述 C 互操作类型的内存占用和内存对齐数值（单位：字节），函数声明如下：

```cangjie
public func sizeOf<T>(): UIntNative where T <: CType
public func alignOf<T>(): UIntNative where T <: CType
```

使用示例：

<!-- run -->

```cangjie
@C
struct Data {
    var a: Int64 = 0
    var b: Float32 = 0.0
}

main() {
    println(sizeOf<Data>())
    println(alignOf<Data>())
}
```

在 64 位机器上运行，将输出：

```text
16
8
```

## CType

除类型映射一节提供的与 C 侧类型进行映射的类型外，仓颉还提供了一个 `CType` 接口，接口本身不包含任何方法，它可以作为所有 C 互操作支持的类型的父类型，便于在泛型约束中使用。

需要注意的是：

1. `CType` 接口是仓颉中的一个接口类型，它本身不满足 `CType` 约束；
2. `CType` 接口不允许被继承、扩展；
3. `CType` 接口不会突破子类型的使用限制。

`CType` 的使用示例如下：

<!-- verify -->

```cangjie
func foo<T>(x: T): Unit where T <: CType {
    match (x) {
        case i32: Int32 => println(i32)
        case ptr: CPointer<Int8> => println(ptr.isNull())
        case f: CFunc<() -> Unit> => unsafe { f() }
        case _ => println("match failed")
    }
}

main() {
    var i32: Int32 = 1
    var ptr = CPointer<Int8>()
    var f: CFunc<() -> Unit> = { => println("Hello") }
    var f64 = 1.0
    foo(i32)
    foo(ptr)
    foo(f)
    foo(f64)
}
```

执行结果如下：

```text
1
true
Hello
match failed
```

## C 调用仓颉的函数

仓颉提供 `CFunc` 类型来对应 C 侧的函数指针类型。C 侧的函数指针可以传递到仓颉，仓颉也可以构造出对应 C 的函数指针的变量传递到 C 侧。

假设一个 C 的库 API 如下：

```c
typedef void (*callback)(int);
void set_callback(callback cb);
```

对应的，在仓颉里面这个函数可以声明为：

```cangjie
foreign func set_callback(cb: CFunc<(Int32) -> Unit>): Unit
```

CFunc 类型的变量可以从 C 侧传递过来，也可以在仓颉侧构造出来。在仓颉侧构造 CFunc 类型有两种办法，一个是用 `@C` 修饰的函数，另外一个是标记为 CFunc 类型的闭包。

`@C` 修饰的函数，表明它的函数签名是满足 C 的调用规则的，定义还是写在仓颉这边。`foreign` 修饰的函数定义是在 C 侧的。

> **注意：**
>
> `foreign` 修饰的函数与 `@C` 修饰的函数，这两种 `CFunc` 的命名不建议使用 `CJ_`（不区分大小写）作为前缀，否则可能与标准库及运行时等编译器内部符号出现冲突，导致未定义行为。

示例如下：

```cangjie
@C
func myCallback(s: Int32): Unit {
    println("handle ${s} in callback")
}

main() {
    // the argument is a function qualified by `@C`
    unsafe { set_callback(myCallback) }

    // the argument is a lambda with `CFunc` type
    let f: CFunc<(Int32) -> Unit> = { i => println("handle ${i} in callback") }
    unsafe { set_callback(f) }
}
```

假设 C 函数编译出来的库是 "libmyfunc.so"，那么需要使用 `cjc -L. -lmyfunc test.cj -o test.out` 编译命令，使仓颉编译器去链接这个库。最终就能生成想要的可执行程序。

另外，在编译 C 代码时，请打开 `-fstack-protector-all/-fstack-protector-strong` 栈保护选项，仓颉侧代码默认拥有溢出检查与栈保护功能。在引入 C 代码后，需要同步保证 unsafe 块中的溢出的安全性。

## 编译选项

使用 C 互操作通常需要手动链接 C 的库，仓颉编译器提供了相应的编译选项。

- `--library-path <value>`, `-L <value>`, `-L<value>`：指定要链接的库文件所在的目录。

  `--library-path <value>` 指定的路径会被加入链接器的库文件搜索路径。另外环境变量 `LIBRARY_PATH` 中指定的路径也会被加入链接器的库文件搜索路径中，通过 `--library-path` 指定的路径会比 `LIBRARY_PATH` 中的路径拥有更高的优先级。

- `--library <value>`, `-l <value>`, `-l<value>`：指定要链接的库文件。

  给定的库文件会被直接传给链接器，库文件名的格式应为 `lib[arg].[extension]`。

关于仓颉编译器支持的所有编译选项，详情请参见 "附录 > cjc 编译选项"。

## 示例

这里演示如何使用 C 互操作以及 `write/read` 接口对一个结构体进行赋值和读取值。

C 代码如下：

```c
// draw.c
#include<stdio.h>
#include<stdint.h>

typedef struct {
    int64_t x;
    int64_t y;
} Point;

typedef struct {
    float x;
    float y;
    float z;
} Cube;

void drawPicture(Point* point, Cube* cube) {
    point->x = 1;
    point->y = 2;
    printf("Draw Point finished.\n");

    printf("Before draw cube\n");
    printf("%f\n", cube->x);
    printf("%f\n", cube->y);
    printf("%f\n", cube->z);
    cube->x = 4.4;
    cube->y = 5.5;
    cube->z = 6.6;
    printf("Draw Cube finished.\n");
}
```

仓颉代码如下：

```cangjie
// main.cj
@C
struct Point {
    var x: Int64 = 0
    var y: Int64 = 0
}

@C
struct Cube {
    var x: Float32 = 0.0
    var y: Float32 = 0.0
    var z: Float32 = 0.0

    init(x: Float32, y: Float32, z: Float32) {
        this.x = x
        this.y = y
        this.z = z
    }
}

foreign func drawPicture(point: CPointer<Point>, cube: CPointer<Cube>): Int32

main() {
    let pPoint = unsafe { LibC.malloc<Point>() }
    let pCube = unsafe { LibC.malloc<Cube>() }

    var cube = Cube(1.1, 2.2, 3.3)
    unsafe {
        pCube.write(cube)
        drawPicture(pPoint, pCube)   // in which x, y will be changed

        println(pPoint.read().x)
        println(pPoint.read().y)
        println(pCube.read().x)
        println(pCube.read().y)
        println(pCube.read().z)

        LibC.free(pPoint)
        LibC.free(pCube)
    }
}
```

编译仓颉代码的命令如下（以 CJNative 后端为例）：

```shell
cjc -L . -l draw ./main.cj
```

其中编译命令中 `-L .` 表示链接库时从当前目录查找（假设 `libdraw.so` 存在于当前目录），`-l draw` 表示链接的库的名字，编译成功后默认生成二进制文件 `main`，执行二进制文件的命令如下：

```shell
LD_LIBRARY_PATH=.:$LD_LIBRARY_PATH ./main
```

运行结果如下：

```shell
Draw Point finished.
Before draw cube
1.100000
2.200000
3.300000
Draw Cube finished.
1
2
4.400000
5.500000
6.600000
```


---

<!-- Content from source_zh_cn/compile_and_build/cjc_usage.md -->
# `cjc` 使用

`cjc`是仓颉编程语言的编译命令，其提供了丰富的功能及对应的编译选项，本章将对基本使用方法进行介绍。

`cjc-frontend` （仓颉前端编译器）会随 `cjc` 一起通过 `Cangjie SDK` 提供，`cjc-frontend` 能够将仓颉源码编译至仓颉的中间表示 （`LLVM IR`）。 `cjc-frontend` 仅进行仓颉代码的前端编译，虽然 `cjc-frontend` 和 `cjc` 共享部分编译选项，但编译流程会在前端编译结束时中止。使用 `cjc` 时仓颉编译器会自动进行前端、后端的编译以及链接工作。`cjc-frontend` 仅作为前端编译器的实体体现提供，除编译器开发者外，仓颉代码的编译应优先使用 `cjc` 。

## `cjc` 基本使用方法

本节介绍 `cjc` 的基本使用方法。关于编译选项详情，请查阅 [cjc 编译选项](../Appendix/compile_options.md)章节。

`cjc` 的使用方式如下：

```shell
cjc [option] file...
```

假如有一个名为 `hello.cj` 的仓颉文件：

<!-- run -->

```cangjie
main() {
    println("Hello, World!")
}
```

可以使用以下命令来编译此文件：

```shell
$ cjc hello.cj
```

此时工作目录下会新增可执行文件 `main` ，`cjc` 默认会将给定源代码文件编译成可执行文件，并将可执行文件命名为 `main`。

以上为不给任何编译选项时 `cjc` 的默认行为，可以通过使用编译选项来控制 `cjc` 的行为，例如让 `cjc` 进行整包编译，又或者是指定输出文件的名字。


---

<!-- Content from source_zh_cn/compile_and_build/cjpm_usage.md -->
# `cjpm` 介绍

`CJPM（Cangjie Package Manager）` 是仓颉语言的官方包管理工具，用来管理、维护仓颉项目的模块系统，并且提供更简易统一的编译入口，支持自定义编译命令。通过包管理器自动依赖管理，实现对引入的多版本三方依赖软件进行分析合并，无需开发者担心多版本依赖冲突问题，大大减轻开发者的负担。同时提供基于仓颉语言原生的自定义构建机制，允许开发者在构建的不同阶段增加预处理和后处理流程，实现构建流程可灵活定制，能够满足开发者不同业务场景下的编译构建需求。

## `cjpm` 基本使用方法

通过 `cjpm -h` 即可查看主界面，由几个板块组成，从上到下分别是： 当前命令说明、使用示例（Usage）、支持的可用命令（Available subcommands）、支持的配置项（Available options）、更多提示内容。

```text
Cangjie Package Manager

Usage:
  cjpm [subcommand] [option]

Available subcommands:
  init             Init a new cangjie module
  check            Check the dependencies
  update           Update cjpm.lock
  tree             Display the package dependencies in the source code
  build            Compile the current module
  run              Compile and run an executable product
  test             Unittest a local package or module
  bench            Run benchmarks in a local package or module
  clean            Clean up the target directory
  install          Install a cangjie binary
  uninstall        Uninstall a cangjie binary

Available options:
  -h, --help       help for cjpm
  -v, --version    version for cjpm

Use "cjpm [subcommand] --help" for more information about a command.
```

`cjpm init` 用来初始化一个新的仓颉模块或工作空间。初始化模块时会默认在当前文件夹创建 `cjpm.toml` 文件，并且新建 `src` 源码文件夹，在 `src` 下生成默认的 `main.cj` 文件。自定义参数初始化功能支持可以通过 `cjpm init -h` 查看。

例如：

```text
输入: cjpm init
输出: cjpm init success
```

`cjpm build` 用来构建当前仓颉项目，执行该命令前会先检查依赖项，检查通过后调用 `cjc` 进行构建。支持全量编译、增量编译、交叉编译、并行编译等，更多编译功能支持可以通过 `cjpm build -h` 查看。通过 `cjpm build -V` 命令可以打印所有的编译过程命令。

例如：

```text
输入: cjpm build -V
输出:
compile package module1.package1: cjc --import-path target -p "src/package1" --output-type=staticlib -o target/release/module1/libmodule1.package1.a
compile package module1: cjc --import-path target -L target/release/module1 -lmodule1.package1 -p "src" --output-type=exe --output-dir target/release/bin -o main

cjpm build success
```

## `cjpm.toml` 配置文件说明

配置文件 `cjpm.toml` 用来配置一些基础信息、依赖项、编译选项等内容，`cjpm` 主要通过这个文件进行解析执行。

配置文件代码如下所示：

```text
[package] # 单模块配置字段，与 workspace 字段不能同时存在
  cjc-version = "1.0.0" # 所需 `cjc` 的最低版本要求，必需
  name = "demo" # 模块名及模块 root 包名，必需
  description = "nothing here" # 描述信息，非必需
  version = "1.0.0" # 模块版本信息，必需
  compile-option = "" # 额外编译命令选项，非必需
  override-compile-option = "" # 额外全局编译命令选项，非必需
  link-option = "" # 链接器透传选项，可透传安全编译命令，非必需
  output-type = "executable" # 编译输出产物类型，必需
  src-dir = "" # 指定源码存放路径，非必需
  target-dir = "" # 指定产物存放路径，非必需
  package-configuration = {} # 单包配置选项，非必需

[workspace] # 工作空间管理字段，与 package 字段不能同时存在
  members = [] # 工作空间成员模块列表，必需
  build-members = [] # 工作空间编译模块列表，需要是成员模块列表的子集，非必需
  test-members = [] # 工作空间测试模块列表，需要是编译模块列表的子集，非必需
  compile-option = "" # 应用于所有工作空间成员模块的额外编译命令选项，非必需
  override-compile-option = "" # 应用于所有工作空间成员模块的额外全局编译命令选项，非必需
  link-option = "" # 应用于所有工作空间成员模块的链接器透传选项，非必需
  target-dir = "" # 指定产物存放路径，非必需

[dependencies] # 源码依赖配置项，非必需
  coo = { git = "xxx", branch = "dev" } # 导入 `git` 依赖
  doo = { path = "./pro1" } # 导入源码依赖

[test-dependencies] # 测试阶段的依赖配置项，格式和 dependencies 相同，非必需

[script-dependencies] # 构建脚本的依赖配置项，格式和 dependencies 相同，非必需

[replace] # 依赖替换配置项，格式和 dependencies 相同，非必需

[ffi.c] # 导入 C 语言的库依赖，非必需
  clib1.path = "xxx"

[profile] # 命令剖面配置项，非必需
  build = {} # build 命令配置项
  test = {} # test 命令配置项
  bench = {} # bench 命令配置项
  customized-option = {} # 自定义透传选项

[target.x86_64-unknown-linux-gnu] # 后端和平台隔离配置项，非必需
  compile-option = "value1" # 额外编译命令选项，适用于特定 target 的编译流程和指定该 target 作为交叉编译目标平台的编译流程，非必需
  override-compile-option = "value2" # 额外全局编译命令选项，适用于特定 target 的编译流程和指定该 target 作为交叉编译目标平台的编译流程，非必需
  link-option = "value3" # 链接器透传选项，适用于特定 target 的编译流程和指定该 target 作为交叉编译目标平台的编译流程，非必需

[target.x86_64-w64-mingw32.dependencies] # 适用于对应 target 的源码依赖配置项，非必需

[target.x86_64-w64-mingw32.test-dependencies] # 适用于对应 target 的测试阶段依赖配置项，非必需

[target.x86_64-unknown-linux-gnu.bin-dependencies] # 仓颉二进制库依赖，适用于特定 target 的编译流程和指定该 target 作为交叉编译目标平台的编译流程，非必需
  path-option = ["./test/pro0", "./test/pro1"] # 以文件目录形式配置二进制库依赖
[target.x86_64-unknown-linux-gnu.bin-dependencies.package-option] # 以单文件形式配置二进制库依赖
  "pro0.xoo" = "./test/pro0/pro0.xoo.cjo"
  "pro0.yoo" = "./test/pro0/pro0.yoo.cjo"
  "pro1.zoo" = "./test/pro1/pro1.zoo.cjo"
```


---

<!-- Content from source_zh_cn/compile_and_build/conditional_compilation.md -->
# 条件编译

开发者可以通过预定义或自定义的条件完成条件编译；仓颉目前支持导入和声明的条件编译。

## 导入和声明的条件编译

仓颉支持使用内置编译标记 `@When` 来完成条件编译，编译条件使用 `[]` 括起来，`[]` 内支持输入一组或多组编译条件。`@When` 可以作用于导入节点和除 `package` 外的声明节点。

### 使用方法

以内置 os 编译条件为例，其使用方法如下：

<!-- run -->

```cangjie
@When[os == "Linux"]
class mc{}

main(): Int64 {
    var a = mc()
    return 0
}
```

在上面代码中，开发者在 `Linux` 系统中可以正确编译执行；在`非 Linux` 系统中，则会遇到找不到 `mc` 类定义的编译错误。

值得注意的是：

- 仓颉不支持编译条件嵌套，以下写法均不允许：

    ```cangjie
    @When[os == "Windows"]
    @When[os == "Linux"]    // Error, illegal nested when conditional compilation
    import std.ast.*
    @When[os == "Windows"]
    @When[os == "Linux"]    // Error, illegal nested when conditional compilation
    func A(){}
    ```

- `@When[...]` 作为内置编译标记，在导入前处理，由宏展开生成的代码中含有 `@When[...]` 会编译报错，如：

    ```cangjie
    @M0                     // macro which returns the input
    @When[os == "Linux"]    // Error, unexpected when conditional compilation directive
    func A(){}
    ```

## 内置编译条件变量

仓颉提供的内置条件变量有: `os`、 `backend`、 `arch`、 `cjc_version`、 `debug` 和 `test`。

### os

os 表示目标平台的操作系统。`os` 支持 `==` 和 `!=` 两种操作符。支持的操作系统有：`Windows`、`Linux`、`macOS`。

使用方式如下：

<!-- run -->

```cangjie
@When[os == "Linux"]
func foo() {
    print("Linux, ")
}
@When[os == "Windows"]
func foo() {
    print("Windows, ")
}
@When[os != "Windows"]
func fee() {
    println("NOT Windows")
}
@When[os != "Linux"]
func fee() {
    println("NOT Linux")
}
main() {
    foo()
    fee()
}
```

如果在 `Windows` 环境下编译执行，会得到 `Windows, NOT Linux` 的信息；如果是在 `Linux` 环境下，则会得到 `Linux, NOT Windows` 的信息。

### backend

`backend` 表示目标平台的后端类型，用于支持多种后端条件编译。`backend` 条件支持 `==` 和 `!=` 两种操作符。

当前支持的后端有：`cjnative`。

使用方式如下：

<!-- run -->

```cangjie
@When[backend == "cjnative"]
func foo() {
    print("cjnative backend")
}
@When[backend != "cjnative"]
func foo() {
    print("not cjnative backend")
}
main() {
    foo()
}
```

用 `cjnative` 后端的发布包编译执行，会得到 `cjnative backend` 的信息。

### arch

`arch` 表示目标平台的处理器架构。`arch` 条件支持 `==` 和 `!=` 两种操作符。

支持的处理器架构有：`x86_64`、`aarch64`。

使用方式如下：

<!-- run -->

```cangjie
@When[arch == "aarch64"]
var arch = "aarch64"

@When[arch == "x86_64"]
var arch = "x86_64"

main() {
    println(arch)
}
```

在 `x86_64` 架构的目标平台编译执行，会得到 `x86_64` 的信息；在 `aarch64` 架构的目标平台编译执行，会得到 `aarch64` 的信息。

### cjc_version

`cjc_version` 是仓颉内置的条件，开发者可以根据当前仓颉编译器的版本选择要编译的代码。`cjc_version` 条件支持 `==`、`!=`、`>`、`<`、`>=`、`<=` 六种操作符，格式为 `xx.xx.xx` 支持每个 `xx` 支持 1-2 位数字，计算规则为补位 (补齐 2 位) 比较，例如：`0.18.8 < 0.18.11`， `0.18.8 == 0.18.08`。

使用方式如下：

<!-- run -->

```cangjie
@When[cjc_version == "0.18.6"]
func foo() {
    println("cjc_version equals 0.18.6")
}
@When[cjc_version != "0.18.6"]
func foo() {
    println("cjc_version is NOT equal to 0.18.6")
}
@When[cjc_version > "0.18.6"]
func fnn() {
    println("cjc_version is greater than 0.18.6")
}
@When[cjc_version <= "0.18.6"]
func fnn() {
    println("cjc_version is less than or equal to 0.18.6")
}
@When[cjc_version < "0.18.6"]
func fee() {
    println("cjc_version is less than 0.18.6")
}
@When[cjc_version >= "0.18.6"]
func fee() {
    println("cjc_version is greater than or equal to 0.18.6")
}
main() {
    foo()
    fnn()
    fee()
}
```

根据 `cjc` 的版本，上面代码的执行输出结果会有不同。

### debug

`debug` 表示当前是否启用了调试模式即开启 `-g` 编译选项, 可以用于在编译代码时进行调试和发布版本之间的切换。`debug` 条件仅支持逻辑非运算符（`!`）。

使用方式如下：

<!-- run -->

```cangjie
@When[debug]
func foo() {
    println("debug")
}
@When[!debug]
func foo() {
    println("NOT debug")
}
main() {
    foo()
}
```

启用 `-g` 编译执行会得到 `cjc debug` 的信息，如果没有启用 `-g` 编译执行会得到 `NOT debug` 的信息。

### test

`test` 表示当前是否启用了单元测试选项 `--test`。`test` 条件仅支持逻辑非运算符（`!`）。可以用于区分测试代码与普通代码。
使用方式如下：

<!-- run -->

```cangjie
@When[test]
@Test
class Tests {
    @TestCase
    public func case1(): Unit {
        @Expect("run", foo())
    }
}

func foo() {
    "run"
}

@When[!test]
main () {
    println(foo())
}
```

使用 `--test` 编译执行得到的测试结果，不使用 `--test` 也可正常完成编译运行得到 `run` 的信息。

## 自定义编译条件变量

仓颉允许开发者自定义编译条件变量和取值，自定义的条件变量必须是一个合法的标识符且不允许和内置条件变量同名，其值是一个字符串字面量。自定义条件支持 `==` 和 `!=` 两种运算符。和内置条件变量不同点在于自定义的条件需要开发者在编译时通过 `--cfg` 编译选项或者在配置文件 `cfg.toml` 中定义。

### 配置自定义条件变量

配置自定义条件变量的方式有两种：在编译选项中直接配置键值对或在配置文件配置键值对。

开发者可以使用 `--cfg <value>` 以键值对的形式向编译器传递自定义编译条件变量或者指定配置文件 `cfg.toml` 的搜索路径。

- 选项值需要使用双引号括起来。

- 若选项值中包含 `=` 则会按照键值对的形式直接进行配置（若路径中包含 `=` 则需要通过 `\` 转义），多个键值对可以使用逗号 `,` 分隔。如：

    ```shell
    $ cjc --cfg "feature = lion, platform = dsp" source.cj
    ```

- 允许多次使用 `--cfg` 编译选项配置，例如：

    ```shell
    $ cjc --cfg "feature = lion" --cfg "platform = dsp" source.cj
    ```

- 不允许多次定义同一个条件变量，例如：

    ```shell
    $ cjc --cfg "feature = lion" --cfg "feature = meta" source.cj
    ```

    ```shell
    $ cjc --cfg "feature = lion, feature = meta" source.cj
    ```

    上述两条编译指令都会报错。

- 若选项值中不包含 `=` 或存在通过 `\` 转义的 `=` 则将选项值作为配置文件 `cfg.toml` 的搜索路径传递给编译器，例如：

    ```shell
    $ cjc --cfg "./cfg" source.cj
    ```

    若 `./cfg` 目录下存在 `cfg.toml`，则编译器会在编译时自动获取 `./cfg/cfg.toml` 中配置的自定义编译条件。`cfg.toml` 文件中应采用键值对的方式配置自定义条件变量，每个键值对独占一行，键名是一个合法的仓颉普通标识符，键值是一个双引号括起来的字符串，字符串不支持转义。`cfg.toml` 文件中也支持全行注释和行末注释，例如：

    ```toml
    feature = "lion"
    platform = "dsp"
    # 全行注释
    feature = "meta" # 行末注释
    ```

- 多次使用 `--cfg` 配置 `cfg.toml` 文件的搜索路径时，按照传入的顺序依次搜索`cfg.toml` 文件，若在所有传入的搜索路径下都没有找到 `cfg.toml` 文件，则在默认路径下搜索配置文件 `cfg.toml`。

- 多次使用 `--cfg` 编译选项进行配置时，若某次以键值对的形式直接进行配置，则会忽略配置文件 `cfg.toml` 中的配置。

- 若未使用 `--cfg` 编译选项，编译器会在默认路径（通过 `--package` 或 `-p` 指定的 `package` 目录或 `cjc` 执行目录）下搜索配置文件 `cfg.toml`。

## 多条件编译

仓颉条件编译允许开发者自由组合多个条件编译选项。支持逻辑运算符组合多个条件，支持括号运算符明确优先级。

使用方式如下：

```cangjie
//source.cj
@When[(test || feature == "lion") && !debug]
func fee() {
    println("feature lion")
}
main() {
    fee()
}
```

使用如下编译命令编译运行上段代码：

```shell
$ cjc --cfg="feature=lion" source.cj -o runner.out
```

会得到输出结果如下：

```text
feature lion
```


---

<!-- Content from source_zh_cn/deploy_and_run/runtime_deploy.md -->
# 部署仓颉运行时

为了使仓颉可执行程序能够在不同的操作系统环境中正常运行，仓颉语言提供了一套运行时（`runtime`）环境。该运行时环境为仓颉可执行程序提供了对内存和其他系统资源的访问，例如在运行过程中依赖的仓颉动态库。

安装完整的仓颉工具链包含了仓颉代码编译环境和仓颉运行时的安装（详情请参见[安装仓颉工具链](../first_understanding/install.md)章节）。如果不需要编译代码，仅仅是运行可执行程序，也可以在环境中独立部署运行时。

本节介绍仓颉运行时的部署。

**值得注意的是**，编译时使用[全静态链接](../Appendix/compile_options.md#static)仓颉库，运行时模块已在编译时嵌入到可执行文件中，因此无需在运行环境额外部署运行时，可直接在运行环境中运行编译所得的可执行文件。

## Linux

1. 首先请前往仓颉官方发布渠道，下载适配平台架构的安装包：

    - `cangjie-sdk-linux-x64-x.y.z.tar.gz`：适用于 x86_64 架构 Linux 系统的仓颉工具链。
    - `cangjie-sdk-linux-aarch64-x.y.z.tar.gz`：适用于 aarch64 架构 Linux 系统的仓颉工具链。

2. 请将下载的安装包解压到合适的目录。

    解压完成后，可以在当前工作路径下看到一个名为 `cangjie` 的目录，其中存放了仓颉工具链的全部内容。

    `cangjie` 目录下的 `runtime` 目录，即为运行时库，存放了仓颉 `runtime` 的全部动态库。

3. 请在运行环境执行如下命令完成 `runtime` 的部署（其中 `${CANGJIE_HOME}` 请修改为 `cangjie` 目录所在的路径，`${hw_arch}` 请修改为对应的硬件架构）：

    ```bash
    export LD_LIBRARY_PATH=${CANGJIE_HOME}/runtime/lib/linux_${hw_arch}_llvm:${LD_LIBRARY_PATH}
    ```

## macOS

1. 首先请前往仓颉官方发布渠道，下载适配平台架构的安装包：

    - `cangjie-sdk-mac-x64-x.y.z.tar.gz`：适用于 x86_64 架构 macOS 系统的仓颉工具链。
    - `cangjie-sdk-mac-aarch64-x.y.z.tar.gz`：适用于 aarch64/arm64 架构 macOS 系统的仓颉工具链。

2. 请将下载的安装包解压到合适的目录。

    解压完成后，可以在当前工作路径下看到一个名为 `cangjie` 的目录，其中存放了仓颉工具链的全部内容。

    `cangjie` 目录下的 `runtime` 目录，即为运行时库，存放了仓颉 `runtime` 的全部动态库。

3. 请在运行环境执行如下命令完成 `runtime` 的部署（其中 `${CANGJIE_HOME}` 请修改为 `cangjie` 目录所在的路径，`${hw_arch}` 请修改为对应的硬件架构）：

    ```bash
    export DYLD_LIBRARY_PATH=${CANGJIE_HOME}/runtime/lib/darwin_${hw_arch}_llvm:${DYLD_LIBRARY_PATH}
    ```

## Windows

1. 首先请前往仓颉官方发布渠道，下载适配平台架构的安装包：

    - `cangjie-sdk-windows-x64-x.y.z.zip`：适用于 x86_64 架构 Windows 系统的仓颉工具链。

2. 请将下载的安装包解压到合适的目录。

    解压完成后，可以在当前工作路径下看到一个名为 `cangjie` 的目录，其中存放了仓颉工具链的全部内容。

    `cangjie` 目录下的 `runtime` 目录，即为运行时库，存放了仓颉 `runtime` 的全部动态库。

3. 此处为开发者提供三种环境下部署 `runtime` 的方法，可以根据使用习惯及环境配置，选择一种执行（其中 `${CANGJIE_HOME}` 请修改为 `cangjie` 目录所在的路径，`${hw_arch}` 请修改为对应的硬件架构）：

    - 若使用 Windows 命令提示符（CMD）环境，请执行：

        ```bash
        set "PATH=${CANGJIE_HOME}\runtime\lib\windows_x86_64_llvm;%PATH%;"
        ```

    - 若使用 PowerShell 环境，请执行：

        ```bash
        $env:PATH = "${CANGJIE_HOME}\runtime\lib\windows_x86_64_llvm;" + $env:Path
        ```

    - 若使用 MSYS shell、bash 等环境，请执行：

        ```bash
        export PATH=${CANGJIE_HOME}/runtime/lib/windows_x86_64_llvm
        ```


---

<!-- Content from source_zh_cn/deploy_and_run/run.md -->
# 运行仓颉可执行程序

## 直接运行

### Linux / macOS

1. 首先请查阅[部署仓颉运行时](./runtime_deploy_cjnative.md)章节完成运行时库的部署。

2. 将编译得到的可执行文件 `main` 拷贝至运行环境中，执行可执行文件即可。

    ```bash
    ./main
    ```

    **值得注意的是**，使用 `cjpm` 编译得到的可执行文件 `main` 在 `target/release/bin` 目录下。

### Windows

1. 首先请查阅[部署仓颉运行时](./runtime_deploy_cjnative.md)章节，完成运行时库的部署。

2. 将编译得到的可执行文件 `main.exe` 拷贝至运行环境中，执行可执行文件即可。

    ```bash
    .\main.exe
    ```

    **值得注意的是**，使用 `cjpm` 编译得到的可执行文件 `main.exe` 在 `target\release\bin` 目录下。

## 使用 cjpm 运行

开发者常用 `cjpm` 来管理、编译、运行仓颉项目。

开发者可以根据[安装仓颉工具链](../first_understanding/install.md)章节，在运行环境上安装完整的仓颉工具链。 安装完成后，将整个仓颉项目拷贝至运行环境，使用 `cjpm run` 命令运行仓颉项目即可。


---

<!-- Content from source_zh_cn/Appendix/compile_options.md -->
# `cjc` 编译选项

本章介绍常用的 `cjc` 编译选项。若某一选项同时适用于 `cjc-frontend`，则该选项会有 <sup>[frontend]</sup> 上标；若该选项在 `cjc-frontend` 下行为与 `cjc` 不同，选项会有额外说明。

- 两个横杠开头的选项为长选项，如 `--xxxx`。
  如果长选项有可选参数，那么选项和参数之间需要用等号连接，如 `--xxxx=<value>`。
  如果长选项有必选参数，那么选项和参数之间既可以用空格隔开，也可以用等号连接，如 `--xxxx <value>` 与 `--xxxx=<value>` 等价。

- 一个横杠开头的选项为短选项，如 `-x`。
  对于短选项，如果其后有参数，选项和参数之间可以用空格隔开，也可以不隔开，如 `-x <value>` 与 `-x<value>` 等价。

## 基本选项

### `--output-type=[exe|staticlib|dylib]` <sup>[frontend]</sup>

指定输出文件的类型。`exe` 模式下会生成可执行文件，`staticlib` 模式下会生成静态库文件（ `.a` 文件），`dylib` 模式下会生成动态库文件（Linux 平台为 `.so` 文件、Windows 平台为 `.dll` 文件，macOS 平台为 `.dylib` 文件）。

`cjc` 默认为 `exe` 模式。

除了可以将 `.cj` 文件编译成一个可执行文件以外，也可以将其编译成一个静态或者是动态的链接库，例如使用：

```shell
$ cjc tool.cj --output-type=dylib
```

可以将 `tool.cj` 编译成一个动态链接库，在 Linux 平台上，`cjc` 会生成一个名为 `libtool.so` 的动态链接库文件。

**值得注意的是**，若编译可执行程序时链接了仓颉的动态库文件，必须同时指定 `--dy-std` 与 `--dy-libs` 选项，详情请见 [`--dy-std` 选项说明](#--dy-std)。

<sup>[frontend]</sup> 在 `cjc-frontend` 中，编译流程仅进行至 `LLVM IR`，因此输出总是 `.bc` 文件，但不同的 `--output-type` 类型仍会影响前端编译的策略。

### `--package`, `-p` <sup>[frontend]</sup>

编译包，使用此选项时需要指定一个目录作为输入，目录中的源码文件需要属于同一个包。

假设有文件 `log/printer.cj`：

```cangjie
package log

public func printLog(message: String) {
    println("[Log]: ${message}")
}
```

与文件 `main.cj`:

```cangjie
import log.*

main() {
    printLog("Everything is great")
}
```

可以使用

```shell
$ cjc -p log --output-type=staticlib
```

来编译 `log` 包，`cjc` 会在当前目录下生成一个 `liblog.a` 文件。

可以使用 `liblog.a` 文件来编译 `main.cj` ，编译命令如下：

```shell
$ cjc main.cj liblog.a
```

`cjc` 会将 `main.cj` 与 `liblog.a` 一同编译成一个可执行文件 `main` 。

### `--module-name <value>` <sup>[frontend]</sup>

指定要编译的模块的名称。

假设有文件 `my_module/src/log/printer.cj`：

```cangjie
package log

public func printLog(message: String) {
    println("[Log]: ${message}")
}
```

与文件 `main.cj`:

```cangjie
import my_module.log.*

main() {
    printLog("Everything is great")
}
```

可以使用

```shell
$ cjc -p my_module/src/log --module-name my_module --output-type=staticlib -o my_module/liblog.a
```

来编译 `log` 包并指定其模块名为 `my_module`，`cjc` 会在 `my_module` 目录下生成一个 `my_module/liblog.a` 文件。

然后可以使用 `liblog.a` 文件来编译导入了 `log` 包的 `main.cj` ，编译命令如下：

```shell
$ cjc main.cj my_module/liblog.a
```

`cjc` 会将 `main.cj` 与 `liblog.a` 一同编译成一个可执行文件 `main` 。

### `--output <value>`, `-o <value>`, `-o<value>` <sup>[frontend]</sup>

指定输出文件的路径，编译器的输出将被写入指定文件。

例如，以下命令会将输出的可执行文件名称指定为 `a.out`。

```shell
cjc main.cj -o a.out
```

### `--library <value>`, `-l <value>`, `-l<value>`

指定要链接的库文件。

给定的库文件会被直接传给链接器，此编译选项一般需要和 `--library-path <value>` 配合使用。

文件名的格式应为 `lib[arg].[extension]`。当需要链接库 `a` 时，可以使用选项 `-l a`，库文件搜索目录下的 `liba.a`、`liba.so`（或链接 Windows 目标程序时会搜索 `liba.dll`）等文件会被链接器搜索到并根据需要被链接至最终输出中。

### `--library-path <value>`, `-L <value>`, `-L<value>`

指定要链接的库文件所在的目录。

使用 `--library <value>` 选项时，通常也需要使用此选项来指定要链接的库文件所在的目录。

`--library-path <value>` 指定的路径会被加入链接器的库文件搜索路径。此外，环境变量 `LIBRARY_PATH` 中指定的路径也会被加入链接器的库文件搜索路径中，通过 `--library-path` 指定的路径会比 `LIBRARY_PATH` 中的路径拥有更高的优先级。

假设有从以下 C 语言源文件通过 C 语言编译器编译得到的动态库文件 `libcProg.so`，

```c
#include <stdio.h>

void printHello() {
    printf("Hello World\n");
}
```

仓颉文件 `main.cj`：

```cangjie
foreign func printHello(): Unit

main(): Int64 {
  unsafe {
    printHello()
  }
  return 0
}
```

可以使用

```shell
cjc main.cj -L . -l cProg
```

来编译 `main.cj` 并指定要链接的 `cProg` 库，这里 `cjc` 会输出一个可执行文件 `main`。

执行 `main` 会有如下输出：

```shell
$ LD_LIBRARY_PATH=.:$LD_LIBRARY_PATH ./main
Hello World
```

**值得注意的是**，由于使用了动态库文件，这里需要将库文件所在目录加入 `$LD_LIBRARY_PATH` 以保证 `main` 能够在执行时进行动态链接。

### `-g` <sup>[frontend]</sup>

生成带有调试信息的可执行文件或库文件。

> **注意：**
>
> `-g` 只能配合 `-O0` 使用，如果使用更高的优化级别可能会导致调试功能出现异常。

### `--trimpath <value>` <sup>[frontend]</sup>

移除调试信息中源文件路径信息的前缀。

编译仓颉代码时，`cjc` 会保存源文件（`.cj` 文件）的绝对路径信息以在运行时提供调试与异常信息。

使用此选项可以将指定的路径前缀从源文件路径信息中移除，`cjc` 的输出文件中的源文件路径信息不会包含用户指定的部分。

可以多次使用 `--trimpath` 指定多个不同的路径前缀；对于每个源文件路径，编译器会将第一个匹配到的前缀从路径中移除。

### `--coverage` <sup>[frontend]</sup>

生成支持统计代码覆盖率的可执行程序。编译器会为每一个编译单元生成一个后缀名为 `gcno` 的代码信息文件。在执行程序后，每一个编译单元都会生成一个后缀名为 `gcda` 的执行统计文件。根据这两个文件，配合使用 `cjcov` 工具可以生成本次执行下的代码覆盖率报表。

> **注意：**
>
> `--coverage` 只能配合 `-O0` 使用，如果使用更高的优化级别，编译器将告警并强制使用 `-O0`。`--coverage` 用于编译生成可执行程序，如果用于生成静态库或者动态库，那么在最终使用该库时可能出现链接错误。

### `--int-overflow=[throwing|wrapping|saturating]` <sup>[frontend]</sup>

指定固定精度整数运算的溢出策略，默认为 `throwing`。

- `throwing` 策略下，整数运算溢出时会抛出异常。
- `wrapping` 策略下，整数运算溢出时会回转至对应固定精度整数的另一端。
- `saturating` 策略下，整数运算溢出时会选择对应固定精度的极值作为结果。

### `--diagnostic-format=[default|noColor|json]` <sup>[frontend]</sup>

> **注意：**
>
> Windows 版本暂不支持输出带颜色渲染的错误信息。

指定错误信息的输出格式，默认为 `default` 。

- `default` 错误信息默认格式输出（带颜色）
- `noColor` 错误信息默认格式输出（无颜色）
- `json` 错误信息`json`格式输出

### `--verbose`, `-V` <sup>[frontend]</sup>

`cjc` 会打印出编译器版本信息、工具链依赖的相关信息以及编译过程中执行的命令。

### `--help`, `-h` <sup>[frontend]</sup>

打印可用的编译选项。

使用此选项时，编译器仅会打印编译选项相关信息，不会对任何输入文件进行编译。

### `--version`, `-v` <sup>[frontend]</sup>

打印编译器版本信息。

使用此选项时，编译器仅会打印版本信息，不会对任何输入文件进行编译。

### `--save-temps <value>`

保留编译过程中生成的中间文件并保存至 `<value>` 路径下。

编译器会保留编译过程中生成的 `.bc`、`.o` 等中间文件。

### `--import-path <value>` <sup>[frontend]</sup>

指定导入模块的 AST 文件的搜索路径。

假设已有以下目录结构，`libs/myModule` 目录中包含 `myModule` 模块的库文件和 `log` 包的 AST 导出文件：

```text
.
├── libs
|   └── myModule
|       ├── log.cjo
|       └── libmyModule.a
└── main.cj
```

且有如下 `main.cj` 文件：

```cangjie
import myModule.log.printLog

main() {
    printLog("Everything is great")
}
```

可以通过使用 `--import-path ./libs` 来将 `./libs` 加入导入模块的 AST 文件搜索路径，`cjc` 会使用 `./libs/myModule/log.cjo` 文件来对 `main.cj` 文件进行语义检查与编译。

`--import-path` 提供与 `CANGJIE_PATH` 环境变量相同的功能，但通过 `--import-path` 设置的路径拥有更高的优先级。

### `--scan-dependency` <sup>[frontend]</sup>

通过 `--scan-dependency` 指令可以获得指定包源码或者一个包的 `cjo` 文件对于其他包的直接依赖以及其他信息，以 `json` 格式输出。

```cangjie
// this file is placed under directory pkgA
macro package pkgA
import pkgB.*
import std.io.*
import pkgB.subB.*
```

```shell
cjc --scan-dependency --package pkgA
```

或

```shell
cjc --scan-dependency pkgA.cjo
```

```json
{
  "package": "pkgA",
  "isMacro": true,
  "dependencies": [
    {
      "package": "pkgB",
      "isStd": false,
      "imports": [
        {
          "file": "pkgA/pkgA.cj",
          "begin": {
            "line": 2,
            "column": 1
          },
          "end": {
            "line": 2,
            "column": 14
          }
        }
      ]
    },
    {
      "package": "pkgB.subB",
      "isStd": false,
      "imports": [
        {
          "file": "pkgA/pkgA.cj",
          "begin": {
            "line": 4,
            "column": 1
          },
          "end": {
            "line": 4,
            "column": 19
          }
        }
      ]
    },
    {
      "package": "std.io",
      "isStd": true,
      "imports": [
        {
          "file": "pkgA/pkgA.cj",
          "begin": {
            "line": 3,
            "column": 1
          },
          "end": {
            "line": 3,
            "column": 16
          }
        }
      ]
    }
  ]
}
```

### `--no-sub-pkg` <sup>[frontend]</sup>

表明当前编译包没有子包。

开启该选项后，编译器可以进一步缩减 code size 大小。

### `--warn-off`, `-Woff <value>` <sup>[frontend]</sup>

关闭编译期出现的全部或部分警告。

`<value>` 可以为 `all` 或者一个设定好的警告组别。当参数为 `all` 时，对于编译过程中生成的所有警告，编译器都不会打印；当参数为其他设定好的组别时，编译器将不会打印编译过程中生成的该组别警告。

在打印每个警告时，会有一行 `#note` 提示该警告属于什么组别并如何关闭它，可以通过 `--help` 打印所有可用的编译选项参数，来查阅具体的组别名称。

### `--warn-on`, `-Won <value>` <sup>[frontend]</sup>

开启编译期出现的全部或部分警告。

`--warn-on` 的 `<value>` 与 `--warn-off` 的 `<value>` 取值范围相同，`--warn-on` 通常与 `--warn-off` 组合使用；比如，可以通过设定 `-Woff all -Won <value>` 来仅允许组别为 `<value>` 的警告被打印。

**特别要注意的是**，`--warn-on` 与 `--warn-off` 在使用上顺序敏感；针对同一组别，后设定的选项会覆盖之前选项的设定，比如，调换上例中两个编译选项的位置，使其变为 `-Won <value> -Woff all`，其效果将变为关闭所有警告。

### `--error-count-limit <value>` <sup>[frontend]</sup>

限制编译器打印错误个数的上限。

参数 `<value>` 可以为 `all` 或一个非负整数。当参数为 `all` 时，编译器会打印编译过程中生成的所有错误；当参数为非负整数 `N` 时，编译器最多会打印 `N` 个错误。此选项默认值为 8。

### `--output-dir <value>` <sup>[frontend]</sup>

控制编译器生成的中间文件与最终文件的保存目录。

控制编译器生成的中间文件的保存目录，例如 `.cjo` 文件。当指定 `--output-dir <path1>` 时也指定了 `--output <path2>`，则中间文件会被保存至 `<path1>`，最终输出会被保存至 `<path1>/<path2>` 。

> **注意：**
>
> 同时指定此选项与 `--output` 选项时，`--output` 选项的参数必须是一个相对路径。

### `--static`

静态链接仓颉库。

此选项仅在编译可执行文件时生效。

**值得注意的是：**

`--static` 选项仅适用于 Linux 平台，在其他平台不生效。

### `--static-std`

静态链接仓颉库的 std 模块。

此选项仅在编译动态链接库或可执行文件时生效。

当编译可执行程序时（即指定了 `--output-type=exe` 时），`cjc` 默认静态链接仓颉库的 std 模块。

### <span id="--dy-std">`--dy-std`

动态链接仓颉库的 std 模块。

此选项仅在编译动态链接库或可执行文件时生效。

当编译动态库时（即指定了 `--output-type=dylib` 时），`cjc` 默认动态链接仓颉库的 std 模块。

**值得注意的是：**

1. `--static-std` 和 `--dy-std` 选项一起使用时，仅最后一个选项生效。
2. `--dy-std` 与 `--static-libs` 选项不可一起使用，否则会报错。
3. 当编译可执行程序时链接了仓颉动态库（即通过 `--output-type=dylib` 选项编译的产物），必须显式指定 `--dy-std` 选项动态链接标准库，否则可能导致程序集中出现多份标准库，最终可能会导致运行时问题。

### `--static-libs`

静态链接仓颉库中除 std 及运行时模块外的其他模块。

此选项仅在编译动态链接库或可执行文件时生效。`cjc` 默认静态链接仓颉库中除 std 及运行时模块外的其他模块。

### `--dy-libs`

动态链接仓颉库非 std 的其他模块。

此选项仅在编译动态链接库或可执行文件时生效。

**值得注意的是：**

1. `--static-libs` 和 `--dy-libs` 选项一起使用时，仅最后一个选项生效；
2. `--static-std` 与 `--dy-libs` 选项不可一起使用，否则会报错；
3. `--dy-std` 单独使用时，会默认生效 `--dy-libs` 选项，并有相关告警信息提示；
4. `--dy-libs` 单独使用时，会默认生效 `--dy-std` 选项，并有相关告警信息提示。

### `--stack-trace-format=[default|simple|all]`

指定异常调用栈打印格式，用来控制异常抛出时的栈帧信息显示，默认为 `default` 格式。

异常调用栈的格式说明如下：

- `default` 格式：`省略泛型参数的函数名 (文件名:行号)`
- `simple` 格式： `文件名:行号`
- `all` 格式：`完整的函数名 (文件名:行号)`

### `--lto=[full|thin]`

使能且指定 `LTO` （`Link Time Optimization` 链接时优化）优化编译模式。

**值得注意的是：**

1. `Windows` 以及 `macOS` 平台不支持该功能；
2. 当使能且指定 `LTO` （`Link Time Optimization` 链接时优化）优化编译模式时，不允许同时使用如下优化编译选项：`-Os`、`-Oz`。

`LTO` 优化支持两种编译模式：

- `--lto=full`：`full LTO` 将所有编译模块合并到一起，在全局上进行优化，这种方式可以获得最大的优化潜力，同时也需要更长的编译时间。
- `--lto=thin`：相比于 `full LTO`，`thin LTO` 在多模块上使用并行优化，同时默认支持链接时增量编译，编译时间比 `full LTO` 短，因为失去了更多的全局信息，所以优化效果不如 `full LTO`。

    - 通常情况下优化效果对比：`full LTO` **>** `thin LTO` **>** 常规静态链接编译。
    - 通常情况下编译时间对比：`full LTO` **>** `thin LTO` **>** 常规静态链接编译。

`LTO` 优化使用场景：

1. 使用以下命令编译可执行文件。

    ```shell
    $ cjc test.cj --lto=full
    or
    $ cjc test.cj --lto=thin
    ```

2. 使用以下命令编译 `LTO` 模式下需要的静态库（`.bc` 文件），并且使用该库文件参与可执行文件编译。

    ```shell
    # 生成的静态库为 .bc 文件
    $ cjc pkg.cj --lto=full --output-type=staticlib -o libpkg.bc
    # .bc 文件和源文件一起输入给仓颉编译器编译可执行文件
    $ cjc test.cj libpkg.bc --lto=full
    ```

    > **注意：**
    >
    > `LTO` 模式下的静态库（`.bc` 文件）输入时需要将该文件的路径输入仓颉编译器。

3. 在 `LTO` 模式下，静态链接标准库（`--static-std` & `--static-libs`）时，标准库的代码也会参与 `LTO` 优化，并静态链接到可执行文件；动态链接标准库（`--dy-std` & `--dy-libs`）时，在 `LTO` 模式下依旧使用标准库中的动态库参与链接。

    ```shell
    # 静态链接，标准库代码也参与 LTO 优化
    $ cjc test.cj --lto=full --static-std
    # 动态链接，依旧使用动态库参与链接，标准库代码不会参与 LTO 优化
    $ cjc test.cj --lto=full --dy-std
    ```

### `--pgo-instr-gen`

使能插桩编译，生成携带插桩信息的可执行程序。

编译 macOS 与 Windows 目标时暂不支持使用该功能。

`PGO`（全称 `Profile-Guided Optimization`）是一种常用的编译优化技术，通过使用运行时 profiling 信息进一步提升程序性能。`Instrumentation-based PGO` 是使用插桩信息的一种 `PGO` 优化手段，它通常包含三个步骤：

1. 编译器对源码插桩编译，生成插桩后的可执行程序（instrumented program）；
2. 运行插桩后的可执行程序，生成配置文件；
3. 编译器使用配置文件，再次对源码进行编译。

```shell
# 生成支持源码执行信息统计（携带插桩信息）的可执行程序 test
$ cjc test.cj --pgo-instr-gen -o test
# 运行可执行程序 test 结束后，生成 default.profraw 配置文件
$ ./test
```

### `--pgo-instr-use=<.profdata>`

使用指定 `profdata` 配置文件指导编译并生成优化后的可执行程序。

编译 macOS 目标时暂不支持使用该功能。

> **注意：**
>
> `--pgo-instr-use` 编译选项仅支持格式为 `profdata` 的配置文件。可使用 `llvm-profdata` 工具可将 `profraw` 配置文件转换为 `profdata` 配置文件。

```shell
# 将 `profraw` 文件转换为 `profdata` 文件。
$ LD_LIBRARY_PATH=$CANGJIE_HOME/third_party/llvm/lib:$LD_LIBRARY_PATH $CANGJIE_HOME/third_party/llvm/bin/llvm-profdata merge default.profraw -o default.profdata
# 使用指定 `default.profdata` 配置文件指导编译并生成优化后的可执行程序 `testOptimized`
$ cjc test.cj --pgo-instr-use=default.profdata -o testOptimized
```

### `--target <value>` <sup>[frontend]</sup>

指定编译的目标平台的 triple。

参数 `<value>` 一般为符合以下格式的字符串：`<arch>(-<vendor>)-<os>(-<env>)`。其中：

- `<arch>` 表示目标平台的系统架构，例如 `aarch64`，`x86_64` 等；
- `<vendor>` 表示开发目标平台的厂商，常见的例如 `pc`，`apple` 等，在没有明确平台厂商或厂商不重要的情况下也经常写作 `unknown` 或直接省略；
- `<os>` 表示目标平台的操作系统，例如 `Linux`，`Win32` 等；
- `<env>` 表示目标平台的 ABI 或标准规范，用于更细粒度地区分同一操作系统的不同运行环境，例如 `gnu`，`musl` 等。在操作系统不需要根据 `<env>` 进行更细地区分的时候，此项也可以省略。

目前，`cjc` 已支持交叉编译的本地平台和目标平台如下表所示：

| 本地平台 (host)    | 目标平台 (target)   |
| ------------------ | ------------------ |
| x86_64-linux-gnu   | x86_64-windows-gnu     |
| aarch64-linux-gnu   | x86_64-windows-gnu     |

在使用 `--target` 指定目标平台进行交叉编译之前，请准备好对应目标平台的交叉编译工具链，以及可以在本地平台上运行的、向该目标平台编译的对应 Cangjie SDK 版本。

### `--target-cpu <value>`

> **注意：**
>
> 该选项为实验性功能，使用该功能生成的二进制可能存在潜在的运行时问题，请注意使用该选项的风险。此选项必须配合 `--experimental` 选项一同使用。

指定编译目标的 CPU 类型。

指定编译目标的 CPU 类型时，编译器在生成二进制时会尝试使用该 CPU 类型特有的扩展指令集，并尝试应用适用于该 CPU 类型的优化。为某个特定 CPU 类型生成的二进制通常会失去可移植性，该二进制可能无法在其他（拥有相同架构指令集的）CPU 上运行。

该选项支持以下经过测试的 CPU 类型：

**x86-64 架构：**

- generic

**aarch64 架构：**

- generic
- tsv110

`generic` 为通用 CPU 类型，指定 `generic` 时编译器会生成适用于该架构的通用指令，这样生成的二进制在操作系统和二进制本身的动态依赖一致的前提下，可以在基于该架构的各种 CPU 上运行，无关于具体的 CPU 类型。`--target-cpu` 选项的默认值为 `generic`。

该选项还支持以下 CPU 类型，但以下 CPU 类型未经过测试验证，请注意使用以下 CPU 类型生成的二进制可能会存在运行时问题。

**x86-64 架构：**

- alderlake
- amdfam10
- athlon
- athlon-4
- athlon-fx
- athlon-mp
- athlon-tbird
- athlon-xp
- athlon64
- athlon64-sse3
- atom
- barcelona
- bdver1
- bdver2
- bdver3
- bdver4
- bonnell
- broadwell
- btver1
- btver2
- c3
- c3-2
- cannonlake
- cascadelake
- cooperlake
- core-avx-i
- core-avx2
- core2
- corei7
- corei7-avx
- geode
- goldmont
- goldmont-plus
- haswell
- i386
- i486
- i586
- i686
- icelake-client
- icelake-server
- ivybridge
- k6
- k6-2
- k6-3
- k8
- k8-sse3
- knl
- knm
- lakemont
- nehalem
- nocona
- opteron
- opteron-sse3
- penryn
- pentium
- pentium-m
- pentium-mmx
- pentium2
- pentium3
- pentium3m
- pentium4
- pentium4m
- pentiumpro
- prescott
- rocketlake
- sandybridge
- sapphirerapids
- silvermont
- skx
- skylake
- skylake-avx512
- slm
- tigerlake
- tremont
- westmere
- winchip-c6
- winchip2
- x86-64
- x86-64-v2
- x86-64-v3
- x86-64-v4
- yonah
- znver1
- znver2
- znver3

**aarch64 架构：**

- a64fx
- ampere1
- apple-a10
- apple-a11
- apple-a12
- apple-a13
- apple-a14
- apple-a7
- apple-a8
- apple-a9
- apple-latest
- apple-m1
- apple-s4
- apple-s5
- carmel
- cortex-a34
- cortex-a35
- cortex-a510
- cortex-a53
- cortex-a55
- cortex-a57
- cortex-a65
- cortex-a65ae
- cortex-a710
- cortex-a72
- cortex-a73
- cortex-a75
- cortex-a76
- cortex-a76ae
- cortex-a77
- cortex-a78
- cortex-a78c
- cortex-r82
- cortex-x1
- cortex-x1c
- cortex-x2
- cyclone
- exynos-m3
- exynos-m4
- exynos-m5
- falkor
- kryo
- neoverse-512tvb
- neoverse-e1
- neoverse-n1
- neoverse-n2
- neoverse-v1
- saphira
- thunderx
- thunderx2t99
- thunderx3t110
- thunderxt81
- thunderxt83
- thunderxt88

除以上可选 CPU 类型外，该选项还可以使用 `native` 作为当前 CPU 类型。编译器会尝试识别当前机器的 CPU 类型，并使用该 CPU 类型作为目标类型生成二进制文件。

### `--toolchain <value>`, `-B <value>`, `-B<value>`

指定编译工具链中，二进制文件存放的路径。

这些二进制文件包括编译器、链接器、工具链提供的 C 运行时目标文件（如 `crt0.o`、 `crti.o` 等）。

在准备好编译工具链后，可以在将其存放在一个自定义路径，然后通过 `--toolchain <value>` 向编译器传入该路径，即可让编译器调用到该路径下的二进制文件进行交叉编译。

### `--sysroot <value>`

指定编译工具链的根目录路径。

对于目录结构固定的交叉编译工具链，如果没有指定该目录以外的二进制和动态库、静态库文件路径的需求，可以直接使用 `--sysroot <value>` 向编译器传入工具链的根目录路径，编译器会根据目标平台种类分析对应的目录结构，自动搜索所需的二进制文件和动态库、静态库文件。使用该选项后，无需再指定 `--toolchain`、`--library-path` 参数。

如果向 `triple` 为 `arch-os-env` 的平台进行交叉编译，且交叉编译工具链有以下目录结构：

```text
/usr/sdk/arch-os-env
├── bin
|   ├── arch-os-env-gcc (交叉编译器)
|   ├── arch-os-env-ld  (链接器)
|   └── ...
├── lib
|   ├── crt1.o          (C 运行时目标文件)
|   ├── crti.o
|   ├── crtn.o
|   ├── libc.so         (动态库)
|   ├── libm.so
|   └── ...
└── ...
```

对于仓颉源文件 `hello.cj` ，可以使用以下命令，将 `hello.cj` 交叉编译至 `arch-os-env` 平台：

```shell
cjc --target=arch-os-env --toolchain /usr/sdk/arch-os-env/bin --toolchain /usr/sdk/arch-os-env/lib --library-path /usr/sdk/arch-os-env/lib hello.cj -o hello
```

也可以使用简写的参数：

```shell
cjc --target=arch-os-env -B/usr/sdk/arch-os-env/bin -B/usr/sdk/arch-os-env/lib -L/usr/sdk/arch-os-env/lib hello.cj -o hello
```

如果该工具链的目录符合惯例的目录结构，可以不使用 `--toolchain`、`--library-path` 参数，直接使用以下命令：

```shell
cjc --target=arch-os-env --sysroot /usr/sdk/arch-os-env hello.cj -o hello
```

### `--strip-all`, `-s`

编译可执行文件或动态库时，指定该选项以删除输出文件中的符号表。

### `--discard-eh-frame`

编译可执行文件或动态库时，指定该选项可以删除 eh_frame 段以及 eh_frame_hdr 段中的部分信息（涉及到 crt 的相关信息不作处理），减少可执行文件或动态库的大小，但会影响调试信息。

编译 macOS 目标时暂不支持使用该功能。

### `--set-runtime-rpath`

将仓颉运行时库所在目录的绝对路径写入到二进制的 RPATH/RUNPATH 段中，使用该选项后在构建所在环境中运行该仓颉程序时无需再使用 LD_LIBRARY_PATH (适用于 Linux 平台) 或 DYLD_LIBRARY_PATH (适用于 macOS 平台) 设置仓颉运行时库目录。

编译 Windows 目标时不支持使用该功能。

### `--link-options <value>`<sup>1</sup>

指定链接器选项。

`cjc` 会将该选项的参数透传给链接器。可用的参数会因系统或指定的链接器不同而不同。可以多次使用 `--link-options` 指定多个链接器选项。

<sup>1</sup> 上标表示链接器透传选项可能会因为链接器的不同而不同，具体支持的选项请查阅链接器文档。

### `--disable-reflection`

关闭反射选项，即编译过程中不生成相关反射信息。

> **注意：**
>
> 交叉编译至 aarch64-linux-ohos 目标时，默认关闭反射信息，该选项不生效。

### `--profile-compile-time` <sup>[frontend]</sup>

打印各编译阶段的时间消耗数据。

### `--profile-compile-memory` <sup>[frontend]</sup>

打印各编译阶段的内存消耗数据。

## 单元测试选项

### `--test` <sup>[frontend]</sup>

`unittest` 测试框架提供的入口，由宏自动生成。当使用 `cjc --test` 选项编译时，程序入口不再是 `main`，而是 `test_entry`。unittest 测试框架的使用方法请参见《仓颉编程语言标准库 API》文档。

对于 `pkgc` 目录下的仓颉文件 `a.cj`:
<!-- run -->

```cangjie
import std.unittest.*
import std.unittest.testmacro.*

@Test
public class TestA {
    @TestCase
    public func case1(): Unit {
        print("case1\n")
    }
}
```

可以在 `pkgc` 目录下使用：

```shell
cjc a.cj --test
```

来编译 `a.cj` ，执行 `main` 会有如下输出：

> **注意：**
>
> 不保证用例每次执行的用时都相同。

```cangjie
case1
--------------------------------------------------------------------------------------------------
TP: default, time elapsed: 29710 ns, Result:
    TCS: TestA, time elapsed: 26881 ns, RESULT:
    [ PASSED ] CASE: case1 (16747 ns)
Summary: TOTAL: 1
    PASSED: 1, SKIPPED: 0, ERROR: 0
    FAILED: 0
--------------------------------------------------------------------------------------------------
```

对于如下目录结构：

```text
application
├── src
├── pkgc
|   ├── a1.cj
|   └── a2.cj
└── a3.cj
```

可以在 `application`目录下使用 `-p` 编译选项配合编译整包：

```shell
cjc pkgc --test -p
```

来编译整个 `pkgc` 包下的测试用例 `a1.cj` 和 `a2.cj`。

```cangjie
/*a1.cj*/
package a

import std.unittest.*
import std.unittest.testmacro.*

@Test
public class TestA {
    @TestCase
    public func caseA(): Unit {
        print("case1\n")
    }
}
```

```cangjie
/*a2.cj*/
package a

import std.unittest.*
import std.unittest.testmacro.*

@Test
public class TestB {
    @TestCase
    public func caseB(): Unit {
        throw IndexOutOfBoundsException()
    }
}
```

执行 `main` 会有如下输出（**输出信息仅供参考**）：

```cangjie
case1
--------------------------------------------------------------------------------------------------
TP: a, time elapsed: 367800 ns, Result:
    TCS: TestA, time elapsed: 16802 ns, RESULT:
    [ PASSED ] CASE: caseA (14490 ns)
    TCS: TestB, time elapsed: 347754 ns, RESULT:
    [ ERROR  ] CASE: caseB (345453 ns)
    REASON: An exception has occurred:IndexOutOfBoundsException
        at std/core.Exception::init()(std/core/exception.cj:23)
        at std/core.IndexOutOfBoundsException::init()(std/core/index_out_of_bounds_exception.cj:9)
        at a.TestB::caseB()(/home/houle/cjtest/application/pkgc/a2.cj:7)
        at a.lambda.1()(/home/houle/cjtest/application/pkgc/a2.cj:7)
        at std/unittest.TestCases::execute()(std/unittest/test_case.cj:92)
        at std/unittest.UT::run(std/unittest::UTestRunner)(std/unittest/test_runner.cj:194)
        at std/unittest.UTestRunner::doRun()(std/unittest/test_runner.cj:78)
        at std/unittest.UT::run(std/unittest::UTestRunner)(std/unittest/test_runner.cj:200)
        at std/unittest.UTestRunner::doRun()(std/unittest/test_runner.cj:78)
        at std/unittest.UT::run(std/unittest::UTestRunner)(std/unittest/test_runner.cj:200)
        at std/unittest.UTestRunner::doRun()(std/unittest/test_runner.cj:75)
        at std/unittest.entryMain(std/unittest::TestPackage)(std/unittest/entry_main.cj:11)
Summary: TOTAL: 2
    PASSED: 1, SKIPPED: 0, ERROR: 1
    FAILED: 0
--------------------------------------------------------------------------------------------------
```

### `--test-only` <sup>[frontend]</sup>

`--test-only` 选项用于单独编译包的测试部分。

如果启用此选项，编译器将仅编译包中的测试文件（以 `_test.cj` 结尾）。

> **注意：**
>
> 使用此选项时，应单独以常规模式编译相同的包，然后通过 `-L`/`-l` 链接选项添加依赖，或在使用 `LTO` 选项时添加依赖的 `.bc` 文件。否则，编译器将报缺少依赖的符号的错误。

示例:

```cangjie
/*main.cj*/
package my_pkg

func concatM(s1: String, s2: String): String {
    return s1 + s2
}

main() {
    println(concatM("a", "b"))
    0
}
```

```cangjie
/*main_test.cj*/
package my_pkg

@Test
class Tests {
    @TestCase
    public func case1(): Unit {
        @Expect("ac", concatM("a", "c"))
    }
}
```

使用编译器编译的命令如下：

```shell
# Compile the production part of the package first, only `main.cj` file would be compiled here
cjc -p my_pkg --output-type=static -o=output/libmain.a
# Compile the test part of the package, Only `main_test.cj` file would be compiled here
cjc -p my_pkg --test-only -L output -lmain
```

### `--mock <on|off|runtime-error>` <sup>[frontend]</sup>

如果传递了 `on` ，则该包将使能 mock 编译，该选项允许在测试用例中 mock 该包中的类。`off` 是一种显式禁用 mock 的方法。

> **注意：**
>
> 在测试模式下（当使能 `--test` ）自动启用对此包的 mock 支持，不需要显式传递 `--mock` 选项。

`runtime-error` 仅在测试模式下可用（当使能 `--test` 时），它允许编译带有 mock 代码的包，但不在编译器中做任何 mock 相关的处理（这些处理可能会造成一些开销并影响测试的运行时性能）。这对于带有 mock 代码用例进行基准测试时可能是有用的。使用此编译选项时，避免编译带有 mock 代码的用例并运行测试，否则将抛出运行时异常。

## 宏选项

`cjc` 支持以下宏选项，关于宏的更多内容请参见[“宏”](./Chapter_15_Macro.md)章节。

### `--compile-macro` <sup>[frontend]</sup>

编译宏定义文件，生成默认的宏定义动态库文件。

### `--debug-macro` <sup>[frontend]</sup>

生成宏展开后的仓颉代码文件。该选项可用于调试宏展开功能。

### `--parallel-macro-expansion` <sup>[frontend]</sup>

开启宏展开并行。该选项可用于缩短宏展开编译时间。

## 条件编译选项

`cjc` 支持以下条件编译选项，关于条件编译的更多内容请参见[“条件编译”](../compile_and_build/conditional_compilation.md)。

### `--cfg <value>` <sup>[frontend]</sup>

指定自定义编译条件。

## 并行编译选项

`cjc` 支持以下并行编译选项，以获得更高的编译效率。

### `--jobs <value>`, `-j <value>` <sup>[frontend]</sup>

设置并行编译时所允许的最大并行数。其中 `value` 必须是一个合理的非负整数，当 `value` 大于硬件支持的最大并行能力时，编译器将以硬件支持的最大并行能力执行并行编译。

如果该编译选项未设置，编译器会基于硬件能力自动计算最大并行数。

> **注意：**
>
> `--jobs 1` 表示完全使用串行方式进行编译。

### `--aggressive-parallel-compile`, `--apc`, `--aggressive-parallel-compile=<value>`, `--apc=<value>` <sup>[frontend]</sup>

开启此选项后，编译器会采用更加激进的策略（可能会对优化造成影响，从而导致程序运行性能下降）执行激进并行编译，以便获得更高的编译效率。其中 `value` 是一个可选参数，表示激进并行编译部分允许的最大并行数：

- 如果使用 `value`，则 `value` 必须是一个合理的非负整数，当 `value` 大于硬件支持的最大并行能力时，编译器会基于硬件能力自动计算最大并行数。建议将 `value` 设置为小于硬件的物理核数的非负整数。
- 如果不使用 `value`，则激进并行编译默认开启，且激进并行编译部分的并行数与 `--jobs` 一致。

此外，如果两次编译同一份代码时此选项的 `value` 值不同，或此选项的开关状态不同，编译器不保证这两次编译的产物的二进制一致性。

激进并行编译的开启或关闭规则如下：

- 在以下场景中，激进并行编译将由编译器强制关闭，无法启用：

    - `--fobf-string`
    - `--fobf-const`
    - `--fobf-layout`
    - `--fobf-cf-flatten`
    - `--fobf-cf-bogus`
    - `--lto`
    - `--coverage`
    - 编译 Windows 目标
    - 编译 macOS 目标

- 若使用 `--aggressive-parallel-compile=<value>` 或 `--apc=<value>`，则激进并行编译的开关由 `value` 控制：

    - `value <= 1`：关闭激进并行编译。
    - `value > 1`：开启激进并行编译，且激进并行编译的并行数取决于 `value`。

- 若使用 `--aggressive-parallel-compile` 或 `--apc`，则激进并行编译默认开启，且激进并行编译的并行数与 `--jobs` 一致。

- 若该编译选项未设置，编译器将根据场景默认开启或关闭激进并行编译：

    - `-O0` 或 `-g`：激进并行编译将由编译器默认开启，且激进并行编译的并行数与 `--jobs` 一致；可以通过 `--aggressive-parallel-compile=<value>` 或 `--apc=<value>` 且 `value <= 1` 关闭激进并行编译。
    - 非 `-O0` 且非 `-g`：激进并行编译将由编译器默认关闭；可以通过 `--aggressive-parallel-compile=<value>` 或 `--apc=<value>` 且 `value > 1` 开启激进并行编译。

## 优化选项

### `--fchir-constant-propagation` <sup>[frontend]</sup>

开启 chir 常量传播优化。

### `--fno-chir-constant-propagation` <sup>[frontend]</sup>

关闭 chir 常量传播优化。

### `--fchir-function-inlining` <sup>[frontend]</sup>

开启 chir 函数内联优化。

### `--fno-chir-function-inlining` <sup>[frontend]</sup>

关闭 chir 函数内联优化。

### `--fchir-devirtualization` <sup>[frontend]</sup>

开启 chir 去虚函数调用优化。

### `--fno-chir-devirtualization` <sup>[frontend]</sup>

关闭 chir 去虚函数调用优化。

### `--fast-math` <sup>[frontend]</sup>

开启此选项后，编译器会对浮点数作一些激进且有可能损失精度的假设，以便优化浮点数运算。

### `-O<N>` <sup>[frontend]</sup>

使用参数指定的代码优化级别。

指定越高的优化级别，编译器会越多地进行代码优化以生成更高效的程序，同时也可能会需要更长的编译时间。

`cjc` 默认使用 O0 级别的代码优化。当前 `cjc` 支持如下优化级别：O0、O1、O2、Os、Oz。

当优化等级等于 2 时，`cjc` 除了进行对应的优化外，还会开启以下选项：

- `--fchir-constant-propagation`
- `--fchir-function-inlining`
- `--fchir-devirtualization`

当优化等级等于 s 时， `cjc`除了进行 O2 级别优化外，将针对 code size 进行优化。

当优化等级等于 z 时， `cjc`除了进行 Os 级别优化外，还将进一步缩减 code size 大小。

> **注意：**
>
> 当优化等级等于 s 或 z 时，不允许同时使用链接时优化编译选项 `--lto=[full|thin]`。

### `-O` <sup>[frontend]</sup>

使用 O1 级别的代码优化，等价于 `-O1`。

## 代码混淆选项

`cjc` 支持代码混淆功能，以提供对代码的额外安全保护，默认不开启。

`cjc` 支持以下代码混淆选项：

### `--fobf-string`

开启字符串混淆。

混淆代码中出现的字符串常量，攻击者无法静态直接读取二进制程序中的字符串数据。

### `--fno-obf-string`

关闭字符串混淆。

### `--fobf-const`

开启常量混淆。

混淆代码中使用的数值常量，将数值运算指令替换成等效的、更复杂的数值运算指令序列。

### `--fno-obf-const`

关闭常量混淆。

### `--fobf-layout`

开启外形混淆。

外形混淆功能会混淆代码中的符号（包括函数名和全局变量名）、路径名、代码行号和函数排布顺序。使用该编译选项后，`cjc` 会在当前目录生成符号映射输出文件 `*.obf.map`。如果配置了 `--obf-sym-output-mapping` 选项，则 `--obf-sym-output-mapping` 的参数值将作为 `cjc` 生成的符号映射输出文件名。符号映射输出文件中包含混淆前后符号的映射关系，使用符号映射输出文件可以解混淆被混淆过的符号。

> **注意：**
>
> 外形混淆功能和并行编译功能相互冲突，请勿同时开启。如果和并行编译同时开启，并行编译将失效。

### `--fno-obf-layout`

关闭外形混淆。

### `--obf-sym-prefix <string>`

指定外形混淆功能在混淆符号时添加的前缀字符串。

设置该选项后，所有被混淆符号都会加上该前缀。在编译混淆多个仓颉包时可能出现符号冲突的问题，可以使用该选项给不同的包指定不同的前缀，避免符号冲突。

### `--obf-sym-output-mapping <file>`

指定外形混淆的符号映射输出文件。

符号映射输出文件记录了符号的原始名称、混淆后的名称和所属文件路径。使用符号映射输出文件可以解混淆被混淆过的符号。

### `--obf-sym-input-mapping <file,...>`

指定外形混淆的符号映射输入文件。

外形混淆功能会使用这些文件中的映射关系对符号进行混淆。因此在编译存在调用关系的仓颉包，请使用被调用包的符号映射输出文件作为调用包混淆时的 `--obf-sym-input-mapping` 选项的参数，以此保证同一个符号在调用包和被调用包两者混淆时混淆结果一致。

### `--obf-apply-mapping-file <file>`

提供自定义的外形混淆符号映射关系文件，外形混淆功能将按照文件里的映射关系混淆符号。

文件格式如下：

```text
<original_symbol_name> <new_symbol_name>
```

其中 `original_symbol_name` 是混淆前的名称，`new_symbol_name` 是混淆后的名称。`original_symbol_name` 由多个 `field` 组成。`field` 表示字段名，可以是模块名、包名、类名、结构体名、枚举名、函数名或变量名。`field` 之间用分隔符 `'.'` 分隔。如果 `field` 是函数名，则需要将函数的参数类型用括号 `'()'` 修饰并附加在函数名后面。对于无参函数括号内的内容为空。如果 `field` 存在泛型参数，也需要用括号 `'<>'` 将具体的泛型参数附加在 `field` 后面。

外形混淆功能会将仓颉应用中的 `original_symbol_name` 替换为 `new_symbol_name`。对于不在该文件中的符号，外形混淆功能会正常使用随机名称进行替换。如果该文件中指定的映射关系和 `--obf-sym-input-mapping` 中的映射关系相冲突，编译器会抛出异常并停止编译。

### `--fobf-export-symbols`

允许外形混淆功能混淆导出符号，该选项在开启外形混淆功能时默认开启。

开启该选项后，外形混淆功能会对导出符号进行混淆。

### `--fno-obf-export-symbols`

禁止外形混淆功能混淆导出符号。

### `--fobf-source-path`

允许外形混淆功能混淆符号的路径信息，该选项在开启外形混淆功能时默认开启。

开启该选项后，外形混淆功能会混淆异常堆栈信息中的路径信息，将路径名替换为字符串 `"SOURCE"`。

### `--fno-obf-source-path`

禁止外形混淆功能混淆堆栈信息中的路径信息。

### `--fobf-line-number`

允许外形混淆功能混淆堆栈信息中的行号信息。

开启该选项后，外形混淆功能会混淆异常堆栈信息中的行号信息，将行号替换为 `0`。

### `--fno-obf-line-number`

禁止外形混淆功能混淆堆栈信息中的行号信息。

### `--fobf-cf-flatten`

开启控制流平坦化混淆。

混淆代码中既存的控制流，使其转移逻辑变得复杂。

### `--fno-obf-cf-flatten`

关闭控制流平坦化混淆。

### `--fobf-cf-bogus`

开启虚假控制流混淆。

在代码中插入虚假的控制流，使代码逻辑变得复杂。

### `--fno-obf-cf-bogus`

关闭虚假控制流混淆。

### `--fobf-all`

开启所有混淆功能。

指定该选项等同于同时指定以下选项：

- `--fobf-string`
- `--fobf-const`
- `--fobf-layout`
- `--fobf-cf-flatten`
- `--fobf-cf-bogus`

### `--obf-config <file>`

指定代码混淆配置文件路径。

在配置文件中可以禁止混淆工具对某些函数或者符号进行混淆。

配置文件的具体格式如下：

```text
obf_func1 name1
obf_func2 name2
...
```

第一个参数 `obf_func` 是具体的混淆功能：

- `obf-cf-bogus`：虚假控制流混淆
- `obf-cf-flatten`：控制流平坦化混淆
- `obf-const`：常数混淆
- `obf-layout`：外形混淆

第二个参数 `name` 是需要被保留的对象，由多个 `field` 组成。`field` 表示字段名，可以是包名、类名、结构体名、枚举名、函数名或变量名。

`field` 之间用分隔符 `'.'` 分隔。如果 `field` 是函数名，则需要将函数的参数类型用括号 `'()'` 修饰并附加在函数名后面。对于无参函数括号内的内容为空。

例如，假设在包 `packA` 中有以下代码：

```cangjie
package packA
class MyClassA {
    func funcA(a: String, b: Int64): String {
        return a
    }
}
```

如果要禁止控制流平坦化功能混淆 `funcA`，用户可以编写如下规则：

```text
obf-cf-flatten packA.MyClassA.funcA(std.core.String, Int64)
```

用户也可以使用通配符编写更加灵活的规则，达到一条规则保留多个对象的效果。目前支持的通配符包含以下 3 类：

混淆功能通配符：

| 混淆功能通配符 | 说明                     |
| :-------------- | :----------------------- |
| `?`            | 匹配名称中的单个字符     |
| `*`            | 匹配名称中的任意数量字符 |

字段名通配符：

| 字段名通配符 | 说明                                                         |
| :------------ | :------------------------------------------------------------ |
| `?`          | 匹配字段名中单个非分隔符 `'.'` 的字符                        |
| `*`          | 匹配字段名中的不包含分隔符 `'.'` 和参数的任意数量字符        |
| `**`         | 匹配字段名中的任意数量字符，包括字段之间的分隔符 `'.'` 和参数。`'**'` 只有在单独作为一个 `field` 时才生效，否则会被当作 `'*'` 处理 |

函数的参数类型通配符：

| 参数类型通配符 | 说明                   |
| :-------------- | :---------------------- |
| `...`          | 匹配任意数量的参数     |
| `***`          | 匹配一个任意类型的参数 |

> **说明：**
>
> 参数类型也由字段名组成，因此也可以使用字段名通配符对单个参数类型进行匹配。

以下是通配符使用示例：

例子 1：

```text
obf-cf-flatten pro?.myfunc()
```

该规则表示禁止 `obf-cf-flatten` 功能混淆函数 `pro?.myfunc()`，`pro?.myfunc()` 可以匹配 `pro0.myfunc()`，但不能匹配 `pro00.myfunc()`。

例子 2：

```text
* pro0.**
```

该规则表示禁止任何混淆功能混淆包 `pro0` 下的任何函数和变量。

例子 3：

```text
* pro*.myfunc(...)
```

该规则表示禁止任何混淆功能混淆函数 `pro*.myfunc(...)`，`pro*.myfunc(...)` 可以匹配以 `pro` 开头的任意单层包内的 `myfunc` 函数，且可以为任意参数。

如果需要匹配多层包名，比如 `pro0.mypack.myfunc()`，请使用 `pro*.**.myfunc(...)`。请注意 `'**'` 只有单独作为字段名时才生效，因此 `pro**.myfunc(...)` 和 `pro*.myfunc(...)` 等价，无法匹配多层包名。如果要匹配以 `pro` 开头的所有包下的所有 `myfunc` 函数（包括类中名为 `myfunc` 的函数），请使用 `pro*.**.myfunc(...)`。

例子 4：

```text
obf-cf-* pro0.MyClassA.myfunc(**.MyClassB, ***, ...)
```

该规则表示禁止 `obf-cf-*` 功能混淆函数 `pro0.MyClassA.myfunc(**.MyClassB, ***, ...)`，其中 `obf-cf-*` 会匹配 `obf-cf-bogus` 和 `obf-cf-flatten` 两种混淆功能，`pro0.MyClassA.myfunc(**.MyClassB, ***, ...)` 会匹配函数 `pro0.MyClassA.myfunc`，且函数的第一个参数可以是任意包下的 `MyClassB` 类型，第二个参数可以是任意类型，后面可以接零至多个任意参数。

### `--obf-level <value>`

指定混淆功能强度级别。

可指定 1-9 强度级别。默认强度级别为 5。级别数字越大，强度则越高，该选项会影响输出文件的大小以及执行开销。

### `--obf-seed <value>`

指定混淆算法的随机数种子。

通过指定混淆算法的随机数种子，可以使同一份仓颉代码在不同构建时有不同的混淆结果。默认场景下，对于同一份仓颉代码，在每次混淆后都拥有相同的混淆结果。

## 安全编译选项

`cjc` 默认生成地址无关代码，在编译可执行文件时默认生成地址无关可执行文件。

在构建 Release 版本时，建议根据以下规则打开/关闭编译选项以提高安全性。

### 启用 `--trimpath <value>` <sup>[frontend]</sup>

从调试与异常信息中将指定的绝对路径前缀移除，使用该选项可以避免构建路径信息被写入二进制程序中。

使用该选项后，二进制中的源码路径信息通常不再完整，可能影响调试体验，建议在构建调试版本时关闭该选项。

### 启用 `--strip-all`, `-s`

移除二进制中的符号表，使用该选项可以删除运行时不需要的符号相关信息。

使用该选项后，二进制将无法调试，请在构建调试版本时关闭该选项。

### 禁用 `--set-runtime-rpath`

若可执行程序会被分发至不同环境运行，或其他普通用户对当前正在使用的仓颉运行时库目录拥有写权限，使用该选项可能导致安全风险，因此禁用该选项。

编译 Windows 目标时不涉及该选项。

### 启用 `--link-options "-z noexecstack"`<sup>1</sup>

设置线程栈不可执行。

仅编译 Linux 目标时可用。

### 启用 `--link-options "-z relro"`<sup>1</sup>

设置 GOT 表重定位只读。

仅编译 Linux 目标时可用。

### 启用 `--link-options "-z now"`<sup>1</sup>

设置立即绑定。

仅编译 Linux 目标时可用。

## 代码覆盖率插桩选项

> **注意：**
>
> Windows 和 macOS 版本目前不支持代码覆盖率插桩选项。

仓颉支持对代码覆盖率插桩（SanitizerCoverage，以下简称 SanCov），提供与 LLVM 的 SanitizerCoverage 一致的接口，编译器在函数级或 BasicBlock 级插入覆盖率反馈函数，用户只需要实现约定好的回调函数即可在运行过程中感知程序运行状态。

仓颉提供的 SanCov 功能以 package 为单位，即整个 package 只有全部插桩和全部不插桩两种情况。

### `--sanitizer-coverage-level=0/1/2`

插桩级别：

- 0 表示不插桩；
- 1 表示函数级插桩，仅在函数入口处插入回调函数；
- 2 表示 BasicBlock 级插桩，在各个 BasicBlock 处插入回调函数。

如果不指定，默认值为 2。

该编译选项仅影响 `--sanitizer-coverage-trace-pc-guard`、`--sanitizer-coverage-inline-8bit-counters` 和 `--sanitizer-coverage-inline-bool-flag` 的插桩级别。

### `--sanitizer-coverage-trace-pc-guard`

开启该选项，会在每个 Edge 插入函数调用 `__sanitizer_cov_trace_pc_guard(uint32_t *guard_variable)`，受 `sanitizer-coverage-level` 影响。

**值得注意的是**，该功能存在与 gcc/llvm 实现不一致的地方：不会在 constructor 插入 `void __sanitizer_cov_trace_pc_guard_init(uint32_t *start, uint32_t *stop)`，而是在 package 初始化阶段插入函数调用 `uint32_t *__cj_sancov_pc_guard_ctor(uint64_t edgeCount)`。

`__cj_sancov_pc_guard_ctor` 回调函数需要开发者自行实现，开启 SanCov 的 package 会尽可能早地调用该回调函数，入参是该 Package 的 Edge 个数，返回值是通常是 calloc 创建的内存区域。

如果需要调用 `__sanitizer_cov_trace_pc_guard_init`，建议在 `__cj_sancov_pc_guard_ctor` 中调用，使用动态创建的缓冲区计算该函数的入参和返回值。

一个标准的 `__cj_sancov_pc_guard_ctor` 参考实现如下：

```cpp
uint32_t *__cj_sancov_pc_guard_ctor(uint64_t edgeCount) {
    uint32_t *p = (uint32_t *) calloc(edgeCount, sizeof(uint32_t));
    __sanitizer_cov_trace_pc_guard_init(p, p + edgeCount);
    return p;
}
```

### `--sanitizer-coverage-inline-8bit-counters`

开启该选项后，会在每个 Edge 插入一个累加器，每经历过一次，该累加器加一，受 `sanitizer-coverage-level` 影响。

**值得注意的是**，该功能存在与 gcc/llvm 实现不一致的地方：不会在 constructor 插入 `void __sanitizer_cov_8bit_counters_init(char *start, char *stop)`，而是在 package 初始化阶段插入函数调用 `uint8_t *__cj_sancov_8bit_counters_ctor(uint64_t edgeCount)`。

`__cj_sancov_pc_guard_ctor` 回调函数需要开发者自行实现，开启 SanCov 的 package 会尽可能早地调用该回调函数，入参是该 Package 的 Edge 个数，返回值是通常是 calloc 创建的内存区域。

如果需要调用 `__sanitizer_cov_8bit_counters_init`，建议在 `__cj_sancov_8bit_counters_ctor` 中调用，使用动态创建的缓冲区计算该函数的入参和返回值。

一个标准的 `__cj_sancov_8bit_counters_ctor` 参考实现如下：

```cpp
uint8_t *__cj_sancov_8bit_counters_ctor(uint64_t edgeCount) {
    uint8_t *p = (uint8_t *) calloc(edgeCount, sizeof(uint8_t));
    __sanitizer_cov_8bit_counters_init(p, p + edgeCount);
    return p;
}
```

### `--sanitizer-coverage-inline-bool-flag`

开启该选项后，会在每个 Edge 插入布尔值，经历过的 Edge 对应的布尔值会被设置为 True，受 `sanitizer-coverage-level` 影响。

**值得注意的是**，该功能存在与 gcc/llvm 实现不一致的地方：不会在 constructor 插入 `void __sanitizer_cov_bool_flag_init(bool *start, bool *stop)`，而是在 package 初始化阶段插入函数调用 `bool *__cj_sancov_bool_flag_ctor(uint64_t edgeCount)`。

`__cj_sancov_bool_flag_ctor` 回调函数需要开发者自行实现，开启 SanCov 的 package 会尽可能早地调用该回调函数，入参是该 Package 的 Edge 个数，返回值是通常是 calloc 创建的内存区域。

如果需要调用 `__sanitizer_cov_bool_flag_init`，建议在 `__cj_sancov_bool_flag_ctor` 中调用，使用动态创建的缓冲区计算该函数的入参和返回值。

一个标准的 `__cj_sancov_bool_flag_ctor` 参考实现如下：

```cpp
bool *__cj_sancov_bool_flag_ctor(uint64_t edgeCount) {
    bool *p = (bool *) calloc(edgeCount, sizeof(bool));
    __sanitizer_cov_bool_flag_init(p, p + edgeCount);
    return p;
}
```

### `--sanitizer-coverage-pc-table`

该编译选项用于提供插桩点和源码之间的对应关系，当前只提供精确到函数级的对应关系。需要与 `--sanitizer-coverage-trace-pc-guard`、`--sanitizer-coverage-inline-8bit-counters`、`--sanitizer-coverage-inline-bool-flag` 共用，至少需要开启其中一项，可以同时开启多项。

**值得注意的是**，该功能存在与 gcc/llvm 实现不一致的地方：不会在 constructor 插入 `void __sanitizer_cov_pcs_init(const uintptr_t *pcs_beg, const uintptr_t *pcs_end);`，而是在 package 初始化阶段插入函数调用 `void __cj_sancov_pcs_init(int8_t *packageName, uint64_t n, int8_t **funcNameTable, int8_t **fileNameTable, uint64_t *lineNumberTable)`，各入参含义如下：

- `int8_t *packageName`: 字符串，表示包名（插桩用 c 风格的 int8 数组作为入参来表达字符串，下同）。
- `uint64_t n`: 共有 n 个函数被插桩。
- `int8_t **funcNameTable`: 长度为 n 的字符串数组，第 i 个插桩点对应的函数名为 funcNameTable\[i\]。
- `int8_t **fileNameTable`: 长度为 n 的字符串数组，第 i 个插桩点对应的文件名为 fileNameTable\[i\]。
- `uint64_t *lineNumberTable`: 长度为 n 的 uint64 数组，第 i 个插桩点对应的行号为 lineNumberTable\[i\]。

如果需要调用 `__sanitizer_cov_pcs_init`，需要自行完成仓颉 pc-table 到 C 语言 pc-table 的转化。

### `--sanitizer-coverage-stack-depth`

开启该编译选项后，由于仓颉无法获取 SP 指针的值，因此只能在每个函数入口处插入调用 `__updateSancovStackDepth`，在 C 侧实现该函数即可获得 SP 指针。

一个标准的 `updateSancovStackDepth` 实现如下：

```cpp
thread_local void* __sancov_lowest_stack;

void __updateSancovStackDepth()
{
    register void* sp = __builtin_frame_address(0);
    if (sp < __sancov_lowest_stack) {
        __sancov_lowest_stack = sp;
    }
}
```

### `--sanitizer-coverage-trace-compares`

开启该选项后，会在所有的 compare 指令和 match 指令调用前插入函数回调函数，具体列表如下，与 LLVM 系的 API 功能一致。参考 Tracing data flow。

```cpp
void __sanitizer_cov_trace_cmp1(uint8_t Arg1, uint8_t Arg2);
void __sanitizer_cov_trace_const_cmp1(uint8_t Arg1, uint8_t Arg2);
void __sanitizer_cov_trace_cmp2(uint16_t Arg1, uint16_t Arg2);
void __sanitizer_cov_trace_const_cmp2(uint16_t Arg1, uint16_t Arg2);
void __sanitizer_cov_trace_cmp4(uint32_t Arg1, uint32_t Arg2);
void __sanitizer_cov_trace_const_cmp4(uint32_t Arg1, uint32_t Arg2);
void __sanitizer_cov_trace_cmp8(uint64_t Arg1, uint64_t Arg2);
void __sanitizer_cov_trace_const_cmp8(uint64_t Arg1, uint64_t Arg2);
void __sanitizer_cov_trace_switch(uint64_t Val, uint64_t *Cases);
```

### `--sanitizer-coverage-trace-memcmp`

该编译选项用于在 String 、 Array 等比较中反馈前缀比较信息。开启该选项后，会对 String 和 Array 的比较函数前插入函数回调函数。具体对于以下对各 String 和 Array 的 API，分别插入对应桩函数：

- String==: __sanitizer_weak_hook_memcmp
- String.startsWith: __sanitizer_weak_hook_memcmp
- String.endsWith: __sanitizer_weak_hook_memcmp
- String.indexOf: __sanitizer_weak_hook_strstr
- String.replace: __sanitizer_weak_hook_strstr
- String.contains: __sanitizer_weak_hook_strstr
- CString==: __sanitizer_weak_hook_strcmp
- CString.startswith: __sanitizer_weak_hook_memcmp
- CString.endswith: __sanitizer_weak_hook_strncmp
- CString.compare: __sanitizer_weak_hook_strcmp
- CString.equalsLower: __sanitizer_weak_hook_strcasecmp
- Array==: __sanitizer_weak_hook_memcmp
- ArrayList==: __sanitizer_weak_hook_memcmp

## 实验性功能选项

### `--experimental` <sup>[frontend]</sup>

启用实验性功能，允许在命令行使用其他实验性功能选项。

> **注意：**
>
> 使用实验性功能生成的二进制文件可能存在潜在的运行时问题，请注意使用该选项的风险。

## 其他功能

### 编译器报错信息显示颜色

对于 Windows 版本的仓颉编译器，仅在运行于 Windows 10 version 1511 (Build 10586) 或更高版本的系统时，编译器报错信息才会显示颜色，否则不显示颜色。

### 设置 build-id

通过 `--link-options "--build-id=<arg>"`<sup>1</sup> 可以透传链接器选项以设置 build-id。

编译 Windows 目标时不支持此功能。

### 设置 rpath

通过 `--link-options "-rpath=<arg>"`<sup>1</sup> 可以透传链接器选项以设置 rpath。

编译 Windows 目标时不支持此功能。

### 增量编译

通过 `--incremental-compile`<sup>[frontend]</sup>开启增量编译。开启后，`cjc`会在编译时根据前次编译的缓存文件加快此次编译的速度。

> **注意：**
>
> 指定此选项时会保存增量编译缓存及日志到输出文件路径下的 `.cached`目录。

### `--no-prelude` <sup>[frontend]</sup>

关闭标准库 core 包自动导入功能。

> **注意：**
>
> 该选项仅能用于编译仓颉标准库 core 包，不能用于编译其他仓颉代码的场景。

## `cjc` 用到的环境变量

这里介绍一些仓颉编译器在编译代码的过程中可能使用到的环境变量。

### `TMPDIR` 或者 `TMP`

仓颉编译器会将编译过程中生成的临时文件放置在临时目录中。默认情况下，`Linux` 和 `macOS` 操作系统会将其放在 `/tmp` 目录下，而 `Windows` 操作系统则会将其放在 `C:\Windows\Temp` 目录下。仓颉编译器还支持自定义临时文件存放目录，在 `Linux` 和 `macOS` 操作系统上，可以通过设置环境变量 `TMPDIR` 来更改临时文件目录，而在 `Windows` 操作系统上，则可以通过设置环境变量 `TMP` 来更改临时文件目录。

例如：
在 Linux shell 中

```shell
export TMPDIR=/home/xxxx
```

在 Windows cmd 中

```shell
set TMP=D:\\xxxx
```


---

<!-- Content from source_zh_cn/Appendix/linux_toolchain_install.md -->
# Linux 版本工具链的支持与安装

仓颉工具链当前基于以下 Linux 发行版进行了完整功能测试：

- SUSE Linux Enterprise Server 12 SP5
- Ubuntu 18.04
- Ubuntu 20.04
- UnionTech OS Server 20
- Kylin Linux Advanced Server Release V10

## 适用于各 Linux 发行版的仓颉工具链依赖安装命令

> **注意：**
>
> 当前仓颉工具链依赖的某些工具在一些 Linux 发行版上可能无法通过系统默认软件源直接安装。可参考下一节[编译安装依赖工具](./linux_toolchain_install.md#编译安装依赖工具)进行手动安装。

### SUSE Linux Enterprise Server 12 SP5

```shell
$ zypper install \
         binutils \
         glibc-devel \
         gcc-c++
```

此外，还需要安装 OpenSSL 3，安装方法请参见[编译安装依赖工具](./linux_toolchain_install.md#编译安装依赖工具)。

### Ubuntu 18.04

```shell
$ apt-get install \
          binutils \
          libc-dev \
          libc++-dev \
          libgcc-7-dev
```

此外，还需要安装 OpenSSL 3，安装方法请参见[编译安装依赖工具](./linux_toolchain_install.md#编译安装依赖工具)。

### Ubuntu 20.04

```shell
$ apt-get install \
          binutils \
          libc-dev \
          libc++-dev \
          libgcc-9-dev
```

此外，还需要安装 OpenSSL 3，安装方法请参见[编译安装依赖工具](./linux_toolchain_install.md#编译安装依赖工具)。

### UnionTech OS Server 20

```shell
$ yum install \
      binutils \
      glibc-devel \
      libstdc++-devel \
      gcc \
```

此外，还需要安装 OpenSSL 3，安装方法请参见[编译安装依赖工具](./linux_toolchain_install.md#编译安装依赖工具)。

### Kylin Linux Advanced Server release V10

```shell
$ yum install \
      binutils \
      glibc-devel \
      libstdc++-devel \
      gcc \
```

此外，还需要安装 OpenSSL 3，安装方法请参见[编译安装依赖工具](./linux_toolchain_install.md#编译安装依赖工具)。

### 其他 Linux 发行版

根据使用的 Linux 发行版的不同，可能需要参考以上系统的依赖安装命令，使用系统包管理工具安装对应依赖。若使用的系统没有提供相关软件包，可能需要自行安装链接工具、C 语言开发工具、C++ 开发工具、GCC 编译器、以及 OpenSSL 3 以正常使用仓颉工具链。

## 编译安装依赖工具

当前仓颉工具链中的部分标准库（以及部分工具）使用了 OpenSSL 3 开源软件。对于系统包管理工具未提供 OpenSSL 3 的场景，用户可能需要源码编译安装 OpenSSL 3，本节提供了 OpenSSL 3 源码编译的方法和步骤。

### OpenSSL 3

从以下链接可以下载到 OpenSSL 3 的源码：

- <https://www.openssl.org/source/>
- <https://www.openssl.org/source/old/>

建议使用 OpenSSL 3.0.7 或更高版本。

> **注意：**
>
> 请在执行以下编译和安装命令前仔细阅读注意事项，并根据实际情况调整命令。不正确的配置和安装可能会导致系统其他软件不可用。如果在编译安装过程中遇到问题或希望进行额外的安装配置，请参见 OpenSSL 源码中的 `INSTALL` 文件或 OpenSSL 的 [FAQ](https://www.openssl.org/docs/faq.html)。

此处以 OpenSSL 3.0.7 为例，下载后使用以下命令解压压缩包：

```shell
$ tar xf openssl-3.0.7.tar.gz
```

解压完成后进入目录：

```shell
$ cd openssl-3.0.7
```

编译 OpenSSL：

> **注意：**
>
> 如果系统已经安装了 OpenSSL，建议使用 `--prefix=<path>` 选项指定一个自定义安装路径，例如 `--prefix=/usr/local/openssl-3.0.7` 或开发者的个人目录。在系统目录已经存在 OpenSSL 的场景下直接使用以下命令编译安装可能会使系统 OpenSSL 被覆盖，并导致依赖系统 OpenSSL 的应用不可用。

```shell
$ ./Configure --libdir=lib
$ make
```

测试 OpenSSL：

```shell
$ make test
```

将 OpenSSL 安装至系统目录（或先前指定的 `--prefix` 目录），可能需要提供 root 权限以成功执行以下命令：

```shell
$ make install
```

或

```shell
$ sudo make install
```

如果先前编译 OpenSSL 时没有通过 `--prefix` 设置自定义安装路径，则 OpenSSL 安装已经完成了。如果先前通过 `--prefix` 指定了自定义的安装路径，还需要设置以下变量，以使仓颉工具链可以找到 OpenSSL 3。

> **注意：**
>
> 如果系统中原先存在其他版本的 OpenSSL，通过以下方式配置后，除了仓颉工具链外，其他编译开发工具默认使用的 OpenSSL 版本也可能受到影响。如果使用其他编译开发工具时出现 OpenSSL 不兼容的情况，请仅为仓颉开发环境配置以下变量。

*请将 `<prefix>` 替换为指定的自定义安装路径。*

```shell
$ export LIBRARY_PATH=<prefix>/lib:$LIBRARY_PATH
$ export LD_LIBRARY_PATH=<prefix>/lib:$LD_LIBRARY_PATH
```

通过以上方式所配置的环境变量仅在当前执行命令的 `shell` 会话窗口有效。若希望 `shell` 每次启动时都自动配置，可以在 `$HOME/.bashrc`、`$HOME/.zshrc` 或其他 `shell` 配置文件（依开发者的 `shell` 种类而定）加入以上命令。

若希望配置可以默认对所有用户生效，可以执行以下命令：

*请将 `<prefix>` 替换为指定的自定义安装路径。*

```shell
$ echo "export LIBRARY_PATH=<prefix>/lib:$LIBRARY_PATH" >> /etc/profile
$ echo "<prefix>/lib" >> /etc/ld.so.conf
$ ldconfig
```

执行完毕后重新打开 `shell` 会话窗口即可生效。

至此，OpenSSL 3 已经成功安装，可以回到原来的章节继续阅读或尝试运行仓颉编译器了。


---

<!-- Content from source_zh_cn/Appendix/runtime_env.md -->
# runtime 环境变量使用手册

本节介绍 `runtime`（运行时）所提供的环境变量。

在 Linux shell 与 macOS shell 中，可以使用以下方式设置仓颉运行时提供的环境变量：

```shell
$ export VARIABLE=value
```

在 Windows cmd 中，可以使用以下方式设置仓颉运行时提供的环境变量：

```shell
> set VARIABLE=value
```

本节后续的示例均为 Linux shell 中的设置方式，若与运行平台不符，请根据运行平台选择合适的环境变量设置方式。

## runtime 初始化可选配置

注意：

1. 所有整型参数为 Int64 类型，浮点型参数为 Float64 类型;
2. 所有参数如果未显式规定最大值，默认隐式最大值为该类型最大值;
3. 所有参数若超出范围则设置无效，自动使用默认值。

### `cjHeapSize`

指定仓颉堆的最大值，支持单位为 kb（KB）、mb（MB）、gb（GB），支持设置范围为[4MB, 系统物理内存]，超出范围的设置无效，仍旧使用默认值。若物理内存低于 1GB，默认值为 64 MB，否则为 256 MB。

例如：

```shell
export cjHeapSize=4GB
```

### `cjRegionSize`

指定 region 分配器 thread local buffer 的大小，支持单位为 kb（KB）、mb（MB）、gb（GB)，支持设置范围为[4kb, 2048kb]，超出范围的设置无效，仍旧使用默认值。默认值为 64 KB。

例如：

```shell
export cjRegionSize=1024kb
```

### `cjLargeThresholdSize`

需要大量连续内存空间的对象（例如长数组）称为大对象。堆内频繁分配大对象可能导致堆内连续空间不足，从而触发堆溢出问题。通过增加大对象的最大值，可以提升堆内空间的连续性。

在仓颉语言中，大对象的阈值为 `cjLargeThresholdSize` 和 `cjRegionSize` 的较小者。`cjLargeThresholdSize` 支持的单位有 kb（KB）、mb（MB）、gb（GB)，支持的范围是 [4KB, 2048KB]，超出范围的设置无效，仍旧使用默认值。默认值为 32 KB。

> **说明：**
>
> 较大的大对象阈值可能影响程序性能，开发者可根据实际情况设置。

例如：

```shell
export cjLargeThresholdSize=1024kb
```

### `cjExemptionThreshold`

指定存活 region 的水线值，取值 (0,1]，该值与 region 的大小相乘，若 region 中存活对象的大小大于相乘后的值，则该 region 不会被回收（其中死亡对象继续占用内存）。该值指定得越大，region 被回收的概率越大，堆中的碎片空间就越少，但频繁回收 region 也会影响性能。超出范围的设置无效，仍旧使用默认值。默认值为 0.8，即 80%。

例如：

```shell
export cjExemptionThreshold=0.8
```

### `cjHeapUtilization`

指定仓颉堆的利用率，该参数用于 GC 后更新堆水线的参考依据之一，取值 (0, 1]，堆水线是指当堆中对象总大小达到水线值时则进行 GC。该参数指定越小，则更新后的堆水线会越高，则触发 GC 的概率会相对变低。超出范围的设置无效，仍旧使用默认值。默认值为 0.8，即 80%。

例如：

```shell
export cjHeapUtilization=0.8
```

### `cjHeapGrowth`

指定仓颉堆的增长率，该参数用于 GC 后更新堆水线的参考依据之一，取值必须大于 0。增长率的计算方式为 1 + cjHeapGrowth。该参数指定越大，则更新后的堆水线会越高，则触发 GC 的概率会相对变低。默认值为 0.15，表示增长率为 1.15。

例如：

```shell
export cjHeapGrowth=0.15
```

### `cjAlloctionRate`

指定仓颉运行时分配对象的速率，该值必须大于 0，单位为 MB/s，表示每秒可分配对象的数量。默认值为 10240，表示每秒可分配 10240 MB 对象。

例如：

```shell
export cjAlloctionRate=10240
```

### `cjAlloctionWaitTime`

指定仓颉运行时分配对象时的等待时间，该值必须大于 0，支持单位为 s、ms、us、ns，推荐单位为纳秒（ns）。若本次分配对象距离上一次分配对象的时间间隔小于此值，则将等待。默认值为 1000 ns。

例如：

```shell
export cjAlloctionWaitTime=1000ns
```

### `cjGCThreshold`

指定仓颉堆的参考水线值，支持单位为 kb（KB）、mb（MB）、gb（GB）, 取值必须为大于 0 的整数。当仓颉堆大小超过该值时，触发 GC。默认值为堆大小。

例如：

```shell
export cjGCThreshold=20480KB
```

### `cjGarbageThreshold`

当 GC 发生时，如果 region 中死亡对象所占比率大于此环境变量，此 region 会被放入回收候选集中，后续可被回收（如果受到其他策略影响也可能不被回收），默认值为 0.5，无量纲，支持设置的区间为[0.0, 1.0]。

例如：

```shell
export cjGarbageThreshold=0.5
```

### `cjGCInterval`

指定两次 GC 的间隔时间值，取值必须大于 0，支持单位为 s、ms、us、ns，推荐单位为毫秒（ms）。若本次 GC 距离上次 GC 的间隔小于此值，则本次 GC 将被忽略。该参数可以控制 GC 的频率。默认值为 150 ms。

例如：

```shell
export cjGCInterval=150ms
```

### `cjBackupGCInterval`

指定 backup GC 的间隔值，取值必须大于 0，支持单位为 s、ms、us、ns，推荐单位为秒（s），当仓颉运行时在该参数设定时间内未触发 GC，则触发一次 backup GC。默认值为 240 秒，即 4 分钟。

例如：

```shell
export cjBackupGCInterval=240s
```

### `cjProcessorNum`

指定仓颉线程的最大并发数，支持设置范围为 (0, CPU 核数 * 2]，超出范围的设置无效，仍旧使用默认值。调用系统 API 获取 cpu 核数，若成功默认值为 cpu 核数，否则默认值为 8。

例如：

```shell
export cjProcessorNum=2
```

### `cjStackSize`

指定仓颉线程的栈大小，支持单位为 kb（KB）、mb（MB）、gb（GB），支持设置范围为 Linux 平台下[64KB, 1GB]，Windows 平台下[128KB, 1GB]，超出范围的设置无效，仍旧使用默认值。默认值为 128KB。

例如：

```shell
export cjStackSize=100kb
```

### 运维日志可选配置

#### `MRT_LOG_FILE_SIZE`

指定 runtime 运维日志的文件大小，默认值为 10 MB，支持单位为 kb（KB）、mb（MB）、gb（GB），设置值需大于 0。

日志大小超过该值时，会重新回到日志开头进行打印。

最终生成日志大小略大于 MRT_LOG_FILE_SIZE。

例如：

```shell
export MRT_LOG_FILE_SIZE=100kb
```

#### `MRT_LOG_PATH`

指定 runtime 运维日志的输出路径，若该环境变量未设置或路径设置失败，则运维日志默认打印到 stdout（标准输出）或 stderr（标准错误）中。

例如：

```shell
export MRT_LOG_PATH=/home/cangjie/runtime/runtime_log.txt
```

#### `MRT_LOG_LEVEL`

指定 runtime 运维日志的最小输出级别，大于等于这个级别的日志会被打印，默认值为 e，支持设置值为[v|d|i|w|e|f|s]。v（VERBOSE）、d（DEBUGY）、i（INFO）、w（WARNING）、e（ERROR）、f（FATAL）、s（FATAL_WITHOUT_ABORT）。

例如：

```shell
export MRT_LOG_LEVEL=v
```

#### `MRT_REPORT`

指定 runtime GC 日志的输出路径，若该环境变量未设置或路径设置失败，该日志默认不打印。

例如：

```shell
export MRT_REPORT=/home/cangjie/runtime/gc_log.txt
```

#### `MRT_LOG_CJTHREAD`

指定 cjthread 日志的输出路径，若该环境变量未设置或路径设置失败，该日志默认不打印。

例如：

```shell
export MRT_LOG_CJTHREAD=/home/cangjie/runtime/cjthread_log.txt
```

#### `cjHeapDumpOnOOM`

指定是否要在发生堆溢出后输出堆快照文件，默认不开启。支持设置值为[on|off]，设定为 on 时开启功能，设定 off 或者其他值不开启功能。

例如：

```shell
export cjHeapDumpOnOOM=on
```

#### `cjHeapDumpLog`

指定输出堆快照文件的路径。注意指定的路径必须存在，且应用执行者对其具有读写权限。如果不指定，堆快照文件将输出到当前执行目录。

例如：

```shell
export cjHeapDumpLog=/home/cangjie
```

### 运行环境可选配置

#### `MRT_STACK_CHECK`

开启 native stack overflow 检查，默认不开启，支持设置值为 1、true、TRUE 开启功能。

例如：

```shell
export MRT_STACK_CHECK=true
```

#### `CJ_SOF_SIZE`

当 StackOverflowError 发生时，将自动进行异常栈折叠方便用户阅读，折叠后栈帧层数默认值是 32。可以通过配置此环境变量控制折叠栈长度，支持设置为 int 范围内的整数。
CJ_SOF_SIZE = 0，打印所有调用栈；
CJ_SOF_SIZE < 0，从栈底开始打印环境变量配置层数；
CJ_SOF_SIZE > 0，从栈顶开始打印环境变量配置层数；
CJ_SOF_SIZE 未配置，默认打印栈顶开始 32 层调用栈；

例如：

```shell
export CJ_SOF_SIZE=30
```

### 仓颉 GWP-Asan 内存安全检测

在仓颉与 C 代码互操作的过程中，可能出现一些仓颉堆内存安全问题。仓颉 GWP-Asan 提供了一种内存安全检测功能。它可以在仓颉程序运行过程中检测代码是否存在仓颉堆内存安全问题。GWP-Asan 通过对仓颉语言标准库提供的 acquireArrayRawData 和 releaseArrayRawData 接口（参见《仓颉编程语言库 API 文档》std.core 包一节）进行采样，并记录对比采样对象前后内存的 Canary 数据，从而检测仓颉与 C 语言互操作过程中是否出现了仓颉堆内存安全问题。

仓颉 GWP-Asan 是一种基于采样的检测工具，可以通过设置不同的值来调整采样频率，以平衡性能影响和检测覆盖率。在默认或更低采样频率下，CPU 性能损失和额外的内存占用极低。

> **说明：**
>
> 仓颉 GWP-Asan 内存安全检测仅支持 Linux 和 HarmonyOS 操作系统。

#### cjEnableGwpAsan

仓颉 GWP-Asan 内存安全检测功能默认关闭。通过将环境变量 `cjEnableGwpAsan` 设置为 `1`、`true` 或 `TRUE` 可以开启该功能。Linux 下设置参考如下：

```shell
export cjEnableGwpAsan=true
```

#### cjGwpAsanSampleRate

在仓颉 GWP-Asan 内存安全检测功能开启状态下，通过环境变量 `cjGwpAsanSampleRate` 设置采样频率。`cjGwpAsanSampleRate` 支持设置为 32 位整形数值范围内的正整数，即 $(0, 2^{31} - 1]$ 。默认值为 5000，即每 5000 次 acquireArrayRawData 接口调用，进行一次采样。Linux 设置参考如下：

```shell
export cjGwpAsanSampleRate=1000
```

> **说明：**
>
> 仓颉 GWP-Asan 内存安全检测中，采样会影响性能。采样率越高，对性能影响越大，能检出更多的问题；采样率越低，其对性能影响越小，能检出更少的问题。请根据实际情况设置采样率。

#### cjGwpAsanHelp

通过环境变量 `cjGwpAsanHelp` 可以设置是否在控制台输出 GWP-Asan 帮助信息。默认不开启。`cjGwpAsanHelp` 设置为`1`、`true` 或 `TRUE` 时，表示在控制台输出帮助信息。Linux 设置参考如下：

```shell
export cjGwpAsanHelp=true
```

#### 约束限制

- 仓颉 GWP-Asan 是一种基于采样的内存检查工具，内存越界问题可能无法完全检出。
- 仓颉 GWP-Asan 对仓颉堆内存的越界检测范围有限，无法检测内存读越界访问，仅能检测部分写越界访问：向前写越界 8 字节以内；向后写越界到尾部的填充区域（根据数组对象长度的不同，填充区域可能为 0-7 字节）。

#### 异常检测类型

**堆内存写越界**

堆内存写越界指的是，指针实际访问的内存长度超过了数组申请的长度，造成仓颉堆内存写越界。

1. 向前越界

    向前越界数组时，runtime 会报告 Head canary 检测失败，使用 `array[-1]` 表示。例如：

    ```cangjie
    unsafe {
        let array = Array<UInt8>(4, item: 0)
        let cp = acquireArrayRawData(array)
        // array 数组实际可访问的范围是 [0, 4)，而下述写操作访问了第 -2 个字节，导致仓颉堆内存向前溢出 2 个字节。错误报告中使用 array[-1] 表示该向前越界行为。
        cp.pointer.read(-2)
        releaseArrayRawData(array)
    }
    ```

    对应的错误报告如下：

    ```text
    2025-05-22 10:57:13.432786 41217 F Gwp-Asan sanity check failed on raw array addr 0x7f7c887368
    2025-05-22 10:57:13.432863 41217 F Head canary (array[-1]) mismatch: expect: 0x2, actual: 0x200000000000002
    2025-05-22 10:57:13.432878 41217 F Gwp-Asan Aborted.
    ```

2. 向后越界

    向后越界数组时，runtime 会报告 Tail canary 检测失败，并给出相对该数组（`array`）的位置。例如：

    ```cangjie
    unsafe {
        let array = Array<UInt8>(4, item: 0)
        let cp = acquireArrayRawData(array)

        // array 数组实际可访问的范围是 [0, 4)，而下述写操作访问了第 6 个字节，导致仓颉堆内存向前溢出 2 个字节。错误报告中使用 array[size+1] 表示该向后越界行为。
        cp.pointer.read(5)
        releaseArrayRawData(array)
    }
    ```

    对应的错误报告如下：

    ```text
    2025-05-22 10:53:09.564580 37872 F Gwp-Asan sanity check failed on raw array addr 0x7f6278a368
    2025-05-22 10:53:09.564761 37872 F Tail canary (array[size+1]) mismatch: expect: 0x6, actual: 0x2
    2025-05-22 10:53:09.564788 37872 F Gwp-Asan Aborted.
    ```

**仓颉 GC（Garbage Collection）异常**

使用 acquireArrayRawData 获取了数组的指针，但是未配套使用 releaseArrayRawData 释放数组的引用，可能造成仓颉 GC（Garbage Collection）异常。

在 runtime 退出时会检测被采样的数组是否调用了 releaseArrayRawData 释放。未释放时，会报告所有未释放的数组对应的堆地址。例如：

```cangjie
unsafe {
    let array = Array<UInt8>(4, item: 0)
    let cp = acquireArrayRawData(array)
    cp.pointer.read()

    // 未使用 releaseArrayRawData
    return
}
```

对应的错误报告如下：

```text
2025-05-22 10:53:09.564761 1248614 F Unreleased array: 0x7fffd77f92d8
2025-05-22 10:53:09.564788 1248614 F Detect un-released array
```


---

<!-- Content from source_zh_cn/Appendix/keyword.md -->
# 关键字

关键字是不能作为标识符使用的特殊字符串，仓颉语言的关键字如下表所示：

| 关键字          | 关键字        | 关键字       |
|--------------|------------|-----------|
| as           | abstract   | break     |
| Bool         | case       | catch     |
| class        | const      | continue  |
| Rune         | do         | else      |
| enum         | extend     | for       |
| func         | false      | finally   |
| foreign      | Float16    | Float32   |
| Float64      | if         | in        |
| is           | init       | import    |
| interface    | Int8       | Int16     |
| Int32        | Int64      | IntNative |
| let          | mut        | main      |
| macro        | match      | Nothing   |
| open         | operator   | override  |
| prop         | public     | package   |
| private      | protected  | quote     |
| redef        | return     | spawn     |
| super        | static     | struct    |
| synchronized | try        | this      |
| true         | type       | throw     |
| This         | unsafe     | Unit      |
| UInt8        | UInt16     | UInt32    |
| UInt64       | UIntNative | var       |
| VArray       | where      | while     |


---

<!-- Content from source_zh_cn/Appendix/operator.md -->
# 操作符

下表列出了仓颉支持的所有操作符的优先级及结合性，其中优先级一栏数值越小，对应操作符的优先级越高。

| 操作符                        | 优先级 | 含义              | 示例                                                      | 结合方向 |
|:---------------------------|:----|:----------------|:--------------------------------------------------------|------|
| `@`                        | 0   | 宏调用             | `@id`                                                   | 右结合  |
| `.`                        | 1   | 成员访问            | `expr.id`                                               | 左结合  |
| `[]`                       | 1   | 索引              | `expr[expr]`                                            | 左结合  |
| `()`                       | 1   | 函数调用            | `expr(expr)`                                            | 左结合  |
| `++`                       | 2   | 自增              | `var++`                                                 | 无    |
| `--`                       | 2   | 自减              | `var--`                                                 | 无    |
| `?`                        | 2   | 问号              | `expr?.id`, `expr?[expr]`, `expr?(expr)`, `expr?{expr}` | 无    |
| `!`                        | 3   | 按位求反、逻辑非        | `!expr`                                                 | 右结合  |
| `-`                        | 3   | 一元负号            | `-expr`                                                 | 右结合  |
| `**`                       | 4   | 幂运算             | `expr ** expr`                                          | 右结合  |
| `*`, `/`                   | 5   | 乘法，除法           | `expr * expr`,  `expr / expr`                           | 左结合  |
| `%`                        | 5   | 取模              | `expr % expr`                                           | 左结合  |
| `+`, `-`                   | 6   | 加法，减法           | `expr + expr`,  `expr - expr`                           | 左结合  |
| `<<`                       | 7   | 按位左移            | `expr << expr`                                          | 左结合  |
| `>>`                       | 7   | 按位右移            | `expr >> expr`                                          | 左结合  |
| `..`                       | 8   | 左闭右开区间操作符           | `expr..expr`                                            | 无    |
| `..=`                      | 8   | 左闭右闭区间操作符       | `expr..=expr`                                           | 无    |
| `<`                        | 9   | 小于              | `expr < expr`                                           | 无    |
| `<=`                       | 9   | 小于等于            | `expr <= expr`                                          | 无    |
| `>`                        | 9   | 大于              | `expr > expr`                                           | 无    |
| `>=`                       | 9   | 大于等于            | `expr >= expr`                                          | 无    |
| `is`                       | 9   | 类型检查            | `expr is Type`                                          | 无    |
| `as`                       | 9   | 类型转换            | `expr as Type`                                          | 无    |
| `==`                       | 10  | 判等              | `expr == expr`                                          | 无    |
| `!=`                       | 10  | 判不等             | `expr != expr`                                          | 无    |
| `&`                        | 11  | 按位与             | `expr & expr`                                           | 左结合  |
| `^`                        | 12  | 按位异或            | `expr ^ expr`                                           | 左结合  |
| <code>&vert;</code>        | 13  | 按位或             | <code>expr &vert; expr</code>                           | 左结合  |
| `&&`                       | 14  | 逻辑与             | `expr && expr`                                          | 左结合  |
| <code>&vert;&vert;</code>  | 15  | 逻辑或             | <code>expr  &vert;&vert; expr</code>                    | 左结合  |
| `??`                       | 16  | coalescing 操作符  | `expr ?? expr`                                          | 右结合  |
| <code>&vert;></code>       | 17  | pipeline 操作符    | <code>id &vert;> expr</code>                            | 左结合  |
| `~>`                       | 17  | composition 操作符 | `expr ~> expr`                                          | 左结合  |
| `=`                        | 18  | 赋值              | `id = expr`                                             | 无    |
| `**=`                      | 18  | 复合运算符           | `id **= expr`                                           | 无    |
| `*=`                       | 18  | 复合运算符           | `id *= expr`                                            | 无    |
| `/=`                       | 18  | 复合运算符           | `id /= expr`                                            | 无    |
| `%=`                       | 18  | 复合运算符           | `id %= expr`                                            | 无    |
| `+=`                       | 18  | 复合运算符           | `id += expr`                                            | 无    |
| `-=`                       | 18  | 复合运算符           | `id -= expr`                                            | 无    |
| `<<=`                      | 18  | 复合运算符           | `id <<= expr`                                           | 无    |
| `>>=`                      | 18  | 复合运算符           | `id >>= expr`                                           | 无    |
| `&=`                       | 18  | 复合运算符           | `id &= expr`                                            | 无    |
| `^=`                       | 18  | 复合运算符           | `id ^= expr`                                            | 无    |
| <code>&vert;=</code>       | 18  | 复合运算符           | <code>id &vert;= expr</code>                            | 无    |
| `&&=`                      | 18  | 复合运算符           | `id &&= expr`                                           | 无    |
| <code>&vert;&vert;=</code> | 18  | 复合运算符           | <code>id &vert;&vert;= expr</code>                      | 无    |


---

<!-- Content from source_zh_cn/Appendix/operator_function.md -->
# 操作符函数

下表列出了仓颉支持的所有操作符函数。

| 操作符函数               | 函数签名                                                           | 示例                                  |
|:--------------------|:---------------------------------------------------------------|:------------------------------------|
| `[]`   **（索引取值）**   | `operator func [](index1: T1, index2: T2, ...): R`             | `this[index1, index2, ...]`         |
| `[]`   **（索引赋值）**   | `operator func [](index1: T1, index2: T2, ..., value!: TN): R` | `this[index1, index2, ...] = value` |
| `()`                | `operator func ()(param1: T1, param2: T2, ...): R`             | `this(param1, param2, ...)`         |
| `!`                 | `operator func !(): R`                                         | `!this`                             |
| `**`                | `operator func **(other: T): R`                                | `this ** other`                     |
| `*`                 | `operator func *(other: T): R`                                 | `this * other`                      |
| `/`                 | `operator func /(other: T): R`                                 | `this / other`                      |
| `%`                 | `operator func %(other: T): R`                                 | `this % other`                      |
| `+`                 | `operator func +(other: T): R`                                 | `this + other`                      |
| `-`                 | `operator func -(other: T): R`                                 | `this - other`                      |
| `<<`                | `operator func <<(other: T): R`                                | `this << other`                     |
| `>>`                | `operator func >>(other: T): R`                                | `this >> other`                     |
| `<`                 | `operator func <(other: T): R`                                 | `this < other`                      |
| `<=`                | `operator func <=(other: T): R`                                | `this <= other`                     |
| `>`                 | `operator func >(other: T): R`                                 | `this > other`                      |
| `>=`                | `operator func >=(other: T): R`                                | `this >= other`                     |
| `==`                | `operator func ==(other: T): R`                                | `this == other`                     |
| `!=`                | `operator func !=(other: T): R`                                | `this != other`                     |
| `&`                 | `operator func &(other: T): R`                                 | `this & other`                      |
| `^`                 | `operator func ^(other: T): R`                                 | `this ^ other`                      |
| <code>&vert;</code> | <code>operator func &vert;(other: T): R</code>                 | <code>this &vert; other</code>      |


---

<!-- Content from source_zh_cn/Appendix/tokenkind_type.md -->
# TokenKind 类型

``` cangjie
public enum TokenKind <: ToString {
    DOT|                      /*  "."           */
    COMMA|                    /*  ","           */
    LPAREN|                   /*  "("           */
    RPAREN|                   /*  ")"           */
    LSQUARE|                  /*  "["           */
    RSQUARE|                  /*  "]"           */
    LCURL|                    /*  "{"           */
    RCURL|                    /*  "}"           */
    EXP|                      /*  "**"          */
    MUL|                      /*  "*"           */
    MOD|                      /*  "%"           */
    DIV|                      /*  "/"           */
    ADD|                      /*  "+"           */
    SUB|                      /*  "-"           */
    INCR|                     /*  "++"          */
    DECR|                     /*  "--"          */
    AND|                      /*  "&&"          */
    OR|                       /*  "||"          */
    COALESCING|               /*  "??"          */
    PIPELINE|                 /*  "|>"          */
    COMPOSITION|              /*  "~>"          */
    NOT|                      /*  "!"           */
    BITAND|                   /*  "&"           */
    BITOR|                    /*  "|"           */
    BITXOR|                   /*  "^"           */
    BITNOT|                   /*  "~"           */
    LSHIFT|                   /*  "<<"          */
    RSHIFT|                   /*  ">>"          */
    COLON|                    /*  ":"           */
    SEMI|                     /*  ";"           */
    ASSIGN|                   /*  "="           */
    ADD_ASSIGN|               /*  "+="          */
    SUB_ASSIGN|               /*  "-="          */
    MUL_ASSIGN|               /*  "*="          */
    EXP_ASSIGN|               /*  "**="         */
    DIV_ASSIGN|               /*  "/="          */
    MOD_ASSIGN|               /*  "%="          */
    AND_ASSIGN|               /*  "&&="         */
    OR_ASSIGN|                /*  "||="         */
    BITAND_ASSIGN|            /*  "&="          */
    BITOR_ASSIGN|             /*  "|="          */
    BITXOR_ASSIGN|            /*  "^="          */
    LSHIFT_ASSIGN|            /*  "<<="         */
    RSHIFT_ASSIGN|            /*  ">>="         */
    ARROW|                    /*  "->"          */
    BACKARROW|                /*  "<-"          */
    DOUBLE_ARROW|             /*  "=>"          */
    RANGEOP|                  /*  ".."          */
    CLOSEDRANGEOP|            /*  "..="         */
    ELLIPSIS|                 /*  "..."         */
    HASH|                     /*  "#"           */
    AT|                       /*  "@"           */
    QUEST|                    /*  "?"           */
    LT|                       /*  "<"           */
    GT|                       /*  ">"           */
    LE|                       /*  "<="          */
    GE|                       /*  ">="          */
    IS|                       /*  "is"          */
    AS|                       /*  "as"          */
    NOTEQ|                    /*  "!="          */
    EQUAL|                    /*  "=="          */
    WILDCARD|                 /*  "_"           */
    INT8|                     /*  "Int8"        */
    INT16|                    /*  "Int16"       */
    INT32|                    /*  "Int32"       */
    INT64|                    /*  "Int64"       */
    INTNATIVE|                /*  "IntNative"   */
    UINT8|                    /*  "UInt8"       */
    UINT16|                   /*  "UInt16"      */
    UINT32|                   /*  "UInt32"      */
    UINT64|                   /*  "UInt64"      */
    UINTNATIVE|               /*  "UIntNative"  */
    FLOAT16|                  /*  "Float16"     */
    FLOAT32|                  /*  "Float32"     */
    FLOAT64|                  /*  "Float64"     */
    RUNE|                     /*  "Rune"        */
    BOOLEAN|                  /*  "Bool"        */
    NOTHING|                  /*  "Nothing"     */
    UNIT|                     /*  "Unit"        */
    STRUCT|                   /*  "struct"      */
    ENUM|                     /*  "enum"        */
    VARRAY|                   /*  "VArray"      */
    THISTYPE|                 /*  "This"        */
    PACKAGE|                  /*  "package"     */
    IMPORT|                   /*  "import"      */
    CLASS|                    /*  "class"       */
    INTERFACE|                /*  "interface"   */
    FUNC|                     /*  "func"        */
    MACRO|                    /*  "macro"       */
    QUOTE|                    /*  "quote"       */
    DOLLAR|                   /*  "$"           */
    LET|                      /*  "let"         */
    VAR|                      /*  "var"         */
    CONST|                    /*  "const"       */
    TYPE|                     /*  "type"        */
    INIT|                     /*  "init"        */
    THIS|                     /*  "this"        */
    SUPER|                    /*  "super"       */
    IF|                       /*  "if"          */
    ELSE|                     /*  "else"        */
    CASE|                     /*  "case"        */
    TRY|                      /*  "try"         */
    CATCH|                    /*  "catch"       */
    FINALLY|                  /*  "finally"     */
    FOR|                      /*  "for"         */
    DO|                       /*  "do"          */
    WHILE|                    /*  "while"       */
    THROW|                    /*  "throw"       */
    RETURN|                   /*  "return"      */
    CONTINUE|                 /*  "continue"    */
    BREAK|                    /*  "break"       */
    IN|                       /*  "in"          */
    NOT_IN|                   /*  "!in"         */
    MATCH|                    /*  "match"       */
    WHERE|                    /*  "where"       */
    EXTEND|                   /*  "extend"      */
    WITH|                     /*  "with"        */
    PROP|                     /*  "prop"        */
    STATIC|                   /*  "static"      */
    PUBLIC|                   /*  "public"      */
    PRIVATE|                  /*  "private"     */
    INTERNAL|                 /*  "internal"    */
    PROTECTED|                /*  "protected"   */
    OVERRIDE|                 /*  "override"    */
    REDEF|                    /*  "redef"       */
    ABSTRACT|                 /*  "abstract"    */
    SEALED|                   /*  "sealed"      */
    OPEN|                     /*  "open"        */
    FOREIGN|                  /*  "foreign"     */
    INOUT|                    /*  "inout"       */
    MUT|                      /*  "mut"         */
    UNSAFE|                   /*  "unsafe"      */
    OPERATOR|                 /*  "operator"    */
    SPAWN|                    /*  "spawn"       */
    SYNCHRONIZED|             /*  "synchronized */
    UPPERBOUND|               /*  "<:"          */
    MAIN|                     /*  "main"        */
    IDENTIFIER|               /*  "x"           */
    PACKAGE_IDENTIFIER|       /*  "x-y"         */
    INTEGER_LITERAL|          /*  e.g. "1"      */
    RUNE_BYTE_LITERAL|        /*  e.g. "b'x'"   */
    FLOAT_LITERAL|            /*  e.g. "'1.0'"  */
    COMMENT|                  /*  e.g. "//xx"     */
    NL|                       /*  newline         */
    END|                      /*  end of file     */
    SENTINEL|                 /*  ";"             */
    RUNE_LITERAL|             /*  e.g. "r'x'"      */
    STRING_LITERAL|           /*  e.g. ""xx""     */
    SINGLE_QUOTED_STRING_LITERAL|  
                              /*  e.g. "'xx'"    */
    JSTRING_LITERAL|          /*  e.g. "J"xx""     */
    MULTILINE_STRING|         /*  e.g. """"aaa""""   */
    MULTILINE_RAW_STRING|     /*  e.g. "#"aaa"#"     */
    BOOL_LITERAL|             /*  "true" or "false"  */
    UNIT_LITERAL|             /*  "()"               */
    DOLLAR_IDENTIFIER|        /*  e.g. "$x"          */
    ANNOTATION|               /*  e.g. "@When"       */
    AT_EXCL|                  /*  e.g. "@!"          */
    ILLEGAL|
    ...
}
```


---

<!-- Content from source_zh_cn/Appendix/cangjie_package_compatibility.md -->
# 仓颉包兼容性检查

本章介绍从 0.59.4 版本开始引入的新特性**仓颉包兼容性检查**，在仓颉运行时加载仓颉包的过程中执行二进制兼容性检查，目的是帮助开发者识别兼容性问题，但无法拦截所有的二进制兼容性问题。

> **注意：**
>
> 该新特性仅适用于 0.59.4 及以后的版本。若运行时或标准库中存在 0.59.4 之前的版本，不保证兼容性，也无法确保正常运行。

## 检查规则

假设仓颉运行时的版本号为 `a.b.c`，待加载的仓颉包的版本号为 `x.y.z`。满足如下任一情况即为兼容：

- 当 `a` 和 `x` 均为 0 时，`a == x && b == y && c == z`。
- 当 `a` 和 `x` 均不为 0 时，`a == x`。

如果两个版本兼容，则继续执行后续包加载过程。如果不满足兼容性要求，则会出现以下两种报错场景：

- 场景一：被加载的是仓颉 core 包，则仓颉运行时终止执行，报错信息中包含仓颉运行时版本号和 core 包版本号。

    ```shell
    F executable cangjie file libcangjie-std-core.so version 0.59.3 is not compatible with deployed cangjie runtime version 0.59.5
    ```

- 场景二：被加载的包为仓颉 core 包以外的其他包，仓颉运行时报错并抛出 IncompatiblePackageException 异常，异常信息中包含仓颉运行时版本号和被加载包的版本号。

    ```shell
    E executable cangjie file liba.so version 0.59.5 is not compatible with deployed cangjie runtime version 0.59.3
    An exception has occurred:
    IncompatiblePackageException: executable cangjie file liba.so version 0.59.5 is not compatible with deployed cangjie runtime version 0.59.3
        at package_global_init(:0)
        at package_global_init(:0)
    ```


---

