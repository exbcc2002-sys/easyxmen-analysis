# EasyXMen（开源小满）BSW 源码分析

本仓库整理了针对 EasyXMen（开源小满）源码框架的分析工作，包含分析所使用的源码、详细报告和汇报演示文稿。主要分析成果见下列两个文档。

## 内容导航

| 路径 | 内容 |
| --- | --- |
| [AUTOSAR_BSW_Defense_Report.docx](./AUTOSAR_BSW_Defense_Report.docx) | 详细分析报告：整体架构、模块依赖、源码机制、调试方法及普华开发板适配方案。 |
| [AUTOSAR_BSW_Modules_Presentation.pptx](./AUTOSAR_BSW_Modules_Presentation.pptx) | 20 页汇报演示文稿：核心模块职责、状态机、关键接口及模块协作关系。 |
| [src/](./src/) | 分析所使用的 EasyXMen 源码，包含 BSWCode、Drivers、Examples、RTOS 和 Test 等目录。 |

## 分析范围

围绕 AUTOSAR Classic Platform 的 12 个核心 BSW 模块展开：

- 系统与模式管理：EcuM、BswM、ComM。
- 通信与路由：PduR、Com、CanIf、CanTp。
- 诊断与存储：Dcm、Dem、NvM。
- 数据完整性保护：Crc、E2E。

重点梳理系统启动、CAN 通信、诊断与持久化存储等链路，以及模块的关键数据结构、状态机和 API。

## 阅读与使用

建议先阅读演示文稿了解整体关系，再结合详细报告查阅 [BSWCode](./src/BSWCode/) 中的具体实现；Crc 与 E2E 位于 [Libraries](./src/BSWCode/Libraries/)。Word 和 PowerPoint 文档可下载后使用 Microsoft Office 或兼容软件打开。

源码的目录说明与运行条件见 [上游 README](./src/README.md)。构建和运行需结合目标硬件、配置工具及对应配置文件，具体以源码随附说明为准。

## 源码来源与许可

EasyXMen 上游项目地址：https://atomgit.com/easyxmen/XMen 。本仓库用于整理源码分析成果，源码版权归原项目及相关权利人所有。

源码随附的许可及声明保留于 [LICENSE.txt](./src/LICENSE.txt)、[EXCEPTION.md](./src/EXCEPTION.md)、[HEADER.MD](./src/HEADER.MD) 和 [NOTICE.txt](./src/NOTICE.txt)。分析文档未另行指定开放许可。
