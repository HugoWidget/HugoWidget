# HugoWidget

HugoWidget 是一个专注于 **Windows 平台下希沃教学设备辅助工具** 的开源组织。我们致力于为广大电教管理员、学校 IT 运维人员以及技术爱好者提供功能丰富、稳定可靠的希沃系统增强与维护方案。

项目正在进行维护更新，请耐心等待。

<!--

## 🎯 组织目标

- **增强希沃系统功能**：通过 DLL 注入、脚本注入、进程管理等方式，解除锁屏限制、优化教学体验。
- **简化维护流程**：提供自动化 PE 维护工具集。
- **降低使用门槛**：整合所有工具至统一的控制台菜单（HugoProgs）或图形界面（HugoWidgets），无需记忆复杂命令。
- **坚持开源精神**：所有项目遵循 GPLv3 或兼容许可证，代码透明，欢迎贡献。

## 📦 核心项目概览

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

-->

## 🛠️ 技术栈

- **编程语言**：C++ (主要)、Python、JavaScript
- **构建工具**：Visual Studio 2022, PyInstaller
- **图形界面**：Qt6 + Qlementine 风格

## 📄 许可证

大部分项目采用 **GNU General Public License v3.0**，部分组件使用 **LGPLv3** 或 **MIT** 许可证，其他第三方依赖遵循其原始许可。详情请参阅各仓库中的 `LICENSE` 文件及 `licenses` 文件夹。

## 🤝 如何参与

- 欢迎提交 Issue、Pull Request 或加入讨论。
- 若想进一步讨论或有意贡献代码，欢迎加入社群，并参与HugoWidget项目。

## ⚠️ 免责声明

本项目**仅用于研究或教育目的**。请勿用于违反当地法律、侵犯著作权或软件 EULA 的用途。使用者需自行承担因不当使用带来的一切后果，开发者不承担任何责任。
