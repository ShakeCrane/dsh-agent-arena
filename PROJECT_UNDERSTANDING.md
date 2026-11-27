# PROJECT_UNDERSTANDING.md · DSH Agent Arena

## 项目定位
DeepSeek Harness 的多 Agent 长会话协作插件。

## 权威与入口
- 项目约束与背景：[README.md](README.md)、`DEVELOPMENT-UBUNTU.md`（Ubuntu 工作副本独有）、[docs/localization.md](docs/localization.md)。
- 按任务选读实现或证据：[src/workspace.mjs](src/workspace.mjs)、[src/shared.mjs](src/shared.mjs)、[src/client](src/client)、[tests](tests)。
- 小队约定：[TEAM.md](TEAM.md)。

## 验收边界
插件变更按 npm run check 和相关用例验收；模拟宿主与真实 DSH 协作会话分开标记。隔离实例或会议之外，不碰用户真实聊天与模型凭据。

## 已核实与待核
- 2026-11-27（北京时间）：已核对本工作区入口、上述文档/源码路径和 Git HEAD `6e092d3b`。这是治理基线，不证明当前功能、部署或外部交付通过。
- 活动工单、真实环境版本和后续工作按需核对；未在此次文档整理中重新运行项目测试。
- 此远端版本基于 `ba9d5700`。以上 Ubuntu 工作副本独有路径不随本次文档提交发布。
