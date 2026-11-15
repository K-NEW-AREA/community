# RDK S100 四通道 CAN FD 收发器扩展板
[返回公共目录](../README.md#硬件) · [原始项目](https://github.com/K-NEW-AREA/RDKS100_mini_mcu_expansion_board) · [项目问题反馈](https://github.com/K-NEW-AREA/RDKS100_mini_mcu_expansion_board/issues)
## 基本信息
| 项目 | 说明 |
| --- | --- |
| 类型 | 硬件 / 通信扩展板 |
| 贡献者 | [fengsvkn](https://github.com/fengsvkn)，依据原仓库提交记录 |
| 适用平台 | D-Robotics RDK S100，J23 100-Pin MCU 扩展接口（作者说明） |
| 用途 | 引出 CAN5–CAN8 四路 CAN FD 物理收发通道，面向机器人、多节点电机和总线实验 |
| 获取条件 | GitHub 公开可下载；立创开源广场的编辑、下载条件以该平台实际要求为准 |
| 原仓库许可 | [Apache-2.0](https://github.com/K-NEW-AREA/RDKS100_mini_mcu_expansion_board/blob/main/LICENSE)；上游器件资料与外部平台内容按各自条款使用 |
| 收录日期 | 2026-11-15 |
| 核验版本 | [44bae74](https://github.com/K-NEW-AREA/RDKS100_mini_mcu_expansion_board/tree/44bae74b29e35ecf38ba4841009e5f7e3a36cc62)，尚无 Release；README 提及 v2，尚无对应发布标签 |
| 当前状态 | 已收录；公开文件获取与工程压缩包目录检查通过；EDA 导入、打样及实物通信未由社区独立验证 |
## 开源在哪里、包含什么
主仓库位于 K-NEW AREA 组织内。作者也在 README 中提供了[立创开源广场入口](https://oshwhub.com/1888848995a/project_tfmruivo)。本页提供目录与复用说明，设计文件继续在原仓库维护。
截至核验版本，GitHub 根目录有三个文件：
- README.md：背景、通道架构、器件选型摘要、PCB 规格、安装和软件配置说明。
- LICENSE：Apache-2.0 原文。
- ProPrj_mini 地瓜RDK S100 mcu拓展版（已验证功能性可用）.epro2：412,269 字节的工程包。已下载并检查 ZIP 目录，含 project2.json、.epru 与图片；此检查不代表 EDA 导入或电路正确性验证。
根目录未单独提供完整 BOM、Gerber、贴片坐标、原理图 PDF、测试报告或固件。工程包可能可导出其中部分内容，需在作者指定的软件版本中确认；不能仅凭根目录缺少独立文件判断设计未开放。
## 如何开始
1. 打开原始项目，通过 Code → Download ZIP 获取文件；需要复现时使用上表固定提交版本。
2. 阅读原 README，并确认适用主板版本、工程软件版本与导入方法。工程导入步骤尚待补充。
3. 完成工程查看、制造文件导出或通信测试后，在原项目反馈具体技术问题；[社区反馈入口](https://github.com/K-NEW-AREA/community/issues/new?template=02-feedback.md)用于汇总复用和衍生贡献。请关联本页及固定版本。
## 设计说明与验证边界
据原 README，该板采用 4 颗 MCP2542FD 收发器，板尺寸约 40.25 × 39.52 mm，并提供 ESD 防护及统一待机控制。README 中的最高 8 Mbps 属于作者列出的收发器能力，社区没有完成整板该速率测试。
工程文件名写有“已验证功能性可用”，本页将其记录为作者声明；当前公开根目录未见测试环境、步骤、日志或独立复现报告。
复用时可留意以下说明：
- 终端电阻：README 同时提到总线两端 120Ω 与板上 0Ω/100Ω 选焊位。应结合原理图确认位号、默认装配、等效阻值和配置，不能把这些描述直接当作装配指令。
- 软件路径：说明 MCU 域 CAN5–CAN8 如何通过所用 SDK/固件映射到 Linux SocketCAN；README 中 canX 命令还需要实际接口名和环境依据。
- 连接器与引脚：统一架构图中的 CN1 与 BOM 中 CN2 的位号描述，并补充有方向标记的接线图。
## 可继续贡献的内容
- 工程软件版本、导入教程、带版本的原理图和 PCB 预览。
- 完整 BOM、Gerber、贴片坐标及与工程版本的对应关系。
- 实物照片、已测试主板/固件版本、实际速率、收发步骤与日志。
- 原始 CAN 日志、误码或丢帧记录、不同速率测试、失败接线排查等实验数据。此类产物可单独投稿“实验数据”，并关联本硬件版本。
使用中有具体问题，可直接在原项目提交 Issue。

