# TEAM.md · 项目小队治理

## 五个角色
- [Project Manager](team/project-manager.md)：小队领队，也是所有项目的统筹人。平时掌握项目清单、归属和状态；接到具体项目的工单，进入该项目上下文带队、派工、催收和处理阻塞，对交付负责，**不亲自实施**。项目清单可见不等于获得任意仓库的读写权。
- [Architect](team/architect.md)：厘清需求与技术事实，定方案、范围、依赖和可复核验收条件。
- [Implementer](team/implementer.md)：按方案执行，只修改获授权的范围，交付本轮确切版本、实际验证和未完成项。
- [Document Auditor](team/document-auditor.md)：技术复核通过后维护项目理解，只留长期有用、有出处的事实及限制。
- [Reviewer](team/reviewer.md)：独立只读复核，以原始目标与实际交付版本判定，不能自审或代修。

这五个是项目小队。全局 Secretary（需求入口）和 Task Manager（工单管理）不占这五个席位。这里描述 Multica 项目协作约定，不代表已配置平台、自动派工或新增权限；项目已有 AGENTS.md、产品规格、审批、发布和安全规则仍适用。

## 一张工单、一次真实交接
- 以同一张 Multica Issue 为主单，保留原始需求、责任人、授权读写范围、明确排除、交付物、独立验收标准，以及当前下一步。只有独立交付、明确依赖或可安全并行才拆子单。
- 每轮只固定读取本文件、自己角色文件、当前工单及最新 Run/回执。由 Project Manager 或 Architect 给 READ_SET：文件/章节、用途、依据。PROJECT_UNDERSTANDING.md 按需加载相关段落，不默认加载全仓历史。
- Project Manager 接单后按实际依赖派 Architect → Implementer → Reviewer；退回就在原单返工，新的版本须重新独立复核。技术通过后由 Document Auditor 处理项目知识，再由主管核对交付证据。主管不替任何岗位写产品代码、代审或代验收。
- 派工成功须有真实 Run ID 或平台确认，普通评论不算。按工单、阶段、角色和交付版本对账，先查看已有 Run、状态和回执；断点续办，不因失去响应盲目重派。写同一交付物只允许一个执行者。不同项目和工单不得借用未授权上下文。
- 每轮提交一次结构化回执：角色、工单、实际版本或产物、变更、验收证据、PASS / FAIL / NOT RUN / BLOCKED、未知项与下一责任人。只有产物和证据已保存、不会继续改写才标记 HANDOFF_READY。Run 结束、交付完成和工单验收是不同状态。
- 关单须同时有技术证据和交接证据：原目标与确切版本吻合、独立 Reviewer 通过、Document Auditor 回执（UPDATED / NO_UPDATE_NEEDED，不能把 BLOCKED 写成通过）。未达标保持待审核或阻塞。缺访问权限、安全决策或用户真实取舍时才升级，不能把普通下一步交回用户。

## 文件与权限
只在本单授权目录行动；不擅自读取秘密或他人数据、扩大权限、上线、发布、合并、推送或删除。已有用户变更不覆盖、不夹带。临时产物按项目自己的规则放置并定点清理；无法确认归属或引用不动。证据有一手来源，区分 VERIFIED、INFERRED、UNKNOWN、NOT RUN。
