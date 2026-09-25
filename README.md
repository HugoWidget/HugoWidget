# HugoWidget

HugoWidget 是一个专注于 **Windows 平台下希沃教学设备辅助工具** 的开源组织。我们致力于为广大电教管理员、学校 IT 运维人员以及技术爱好者提供功能丰富、稳定可靠的希沃系统增强与维护方案。

## 组织目标

- **增强希沃系统功能**：通过 DLL 注入、脚本注入、进程管理等方式，解除锁屏限制、优化教学体验。
- **简化维护流程**：提供自动化 PE 维护工具集。
- **降低使用门槛**：整合所有工具至统一的控制台菜单（HugoProgs）或图形界面（HugoWidgets），无需记忆复杂命令。
- **坚持开源精神**：所有项目遵循 GPLv3 或兼容许可证，代码透明，欢迎贡献。

## 项目概览

主要项目：

| 项目            | 形态     | 一句话描述                                                   |
| --------------- | -------- | ------------------------------------------------------------ |
| **HugoProgs**   | 控制台   | 一站式希沃运维工具集控制台管理中心，分层菜单整合全部子工具，支持自启动与 `.hps` 脚本 |
| **HugoWidgets** | 图形界面 | HugoProgs 的 GUI 版本，基于 Qt6 与插件框架，提供多标签页操作界面 |

子项目或其他项目：

| 类别              | 项目                                                         | 主要功能                                                     |
| ----------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **基础信息获取**  | HugoInfo                                                     | 展示本机基础信息                                             |
| **锁屏/屏保解除** | HugoLock, HugoLockAssistant, HugoDbg, HugoScreenSaver        | 实时隐藏锁屏窗口、通过 CDP 注入前端脚本、模拟点击解除屏保、置顶操作面板 |
| **冰点还原管理**  | HugoFreezeApi, HugoFreezeDriver, HugoFrzDrvHook, HugoFreezeDisk, HugoFreezeFile | 查询/设置磁盘冻结状态，编辑配置文件                          |
| **希沃服务管控**  | HugoDisable, HugoLaunchTool, HugoInstaller, HugoProtect      | 禁用服务、启停进程、安装/卸载希沃管家、开关文件保护          |
| **虚拟磁盘挂载**  | HugoMount                                                    | 挂载/卸载希沃的配置盘和日志盘                                |
| **密码**          | HugoPassword, HugoBreak                                      | 破解希沃管理密码/锁屏密码（支持 V1/V2/V3）、修改dll以直接解除密码 |
| **DLL 注入**      | HugoInjector                                                 | 将指定 DLL 注入目标进程                                      |
| **监控行为检测**  | HugoMonitor                                                  | 检测希沃管家的录屏/摄像行为并提示或拦截                      |
| **PE 维护工具集** | HugoWinPE (PEOutside + PEInside), PETools                    | 自动配置 BCD 启动项，进入 WinPE 后自动解除冰点、重命名服务、创建清理任务；并提供轻量级 PE 辅助工具 |
| **其他**          | HugoLogs                                                     | 管理所有日志文件                                             |
| **一站式控制台**  | HugoProgs                                                    | 整合上述所有功能的命令行菜单系统，支持 .hps 脚本自动执行     |
| **图形界面版本**  | HugoWidgets                                                  | 提供友好 GUI                                                 |
| **测试**          | HugoTest                                                     | 模拟希沃功能用于测试                                         |

还有`HugoUtils`项目，为包含了上述几乎所有功能的公共库，上述大部分项目都依赖于`HugoUtils`和其包含的`WinUtils`项目

## 文档索引

| 项目            | 用户文档                                                     | 开发者文档                                                   |
| --------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **HugoProgs**   | [HugoProgs 用户文档](https://github.com/HugoWidget/HugoProgs/blob/master/docs/User.md)<br>安装、菜单操作、自启动配置、`.hps` 脚本 | [HugoProgs 开发者文档](https://github.com/HugoWidget/HugoProgs/blob/master/docs/Developer.md)<br>架构、构建、菜单注册、新增子工具 |
| **HugoWidgets** | [HugoWidgets 用户文档](https://github.com/HugoWidget/HugoWidgets/blob/master/docs/User.md)<br>安装、界面说明、各功能页操作、命令行参数 | [HugoWidgets 开发者文档](https://github.com/HugoWidget/HugoWidgets/blob/master/docs/Developer.md)<br>插件框架、新增功能页、构建调试 |

## 快速上手

### 1. 获取安装包

推荐使用 [HugoSetup](https://github.com/HugoWidget/HugoSetup) 提供的已配置版本，无需自行编译：

### 2. 运行

> 两个项目的大量功能（虚拟磁盘、文件保护、冰点、注入等）**都需要管理员权限**，建议全程以管理员身份运行。

## 技术栈

- **编程语言**：C++ (主要)、Python、JavaScript
- **构建工具**：Visual Studio 2022, PyInstaller
- **图形界面**：Qt6 + Qlementine 风格

## 许可证

大部分项目采用 **GNU General Public License v3.0**，部分组件使用 **LGPLv3** 或 **MIT** 许可证，其他第三方依赖遵循其原始许可。详情请参阅各仓库中的 `LICENSE` 文件及 `licenses` 文件夹。

## 如何参与

- 所有项目均已停更，不再接受PR，你可以fork组织仓库来进行进一步开发。
- HugoUtils 与 HugoWidgets 为例外：HugoUtils 作为核心库，为方便开发者使用，仍然接受PR；HugoWidgets 未完工，需要社区的进一步支持。
- 如果想对项目标星但显示 `You can't star HugoWidget/Repository`，可以在搜索页面重新尝试，或访问 [topic](https://github.com/topics/hugowidget)
- 如果项目有功能性问题但仓库已经 Archive，你可以在此仓库提出你的问题。

## 免责声明

本项目**仅用于研究或教育目的**。请勿用于违反当地法律、侵犯著作权或软件 EULA 的用途。使用者需自行承担因不当使用带来的一切后果，开发者不承担任何责任。
