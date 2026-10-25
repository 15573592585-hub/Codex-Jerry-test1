# 秋招销售投递助手与持久上下文

面向制造业校招销售岗位的 Codex Skill。通过四版定稿简历匹配、官网核验、申请回执和原表登记，减少重复排版与重复调查。

## 安装

下载本仓库，将 `skills/campus-sales-apply` 文件夹复制到自己的 `~/.codex/skills/`，然后调用 `$campus-sales-apply`。也可在 Codex 中要求从本仓库安装该目录。

## 持久上下文

GitHub负责文件版本，不会自动延长模型上下文或阻止压缩。恢复效率来自短入口和按需读取：

1. 项目根目录 `AGENTS.md` 指向 `memory/CURRENT.md`。
2. CURRENT 只写当前任务、最近结果、下一步和待确认事项。
3. DECISIONS 保存稳定偏好，TOOL_NOTES 保存实测经验；完整历史按需查找。
4. 申请记录由本地原Excel派生，提交前重新读取原表和官网状态。
5. 私有记忆在独立 private 仓库同步；本公开仓库仅放示例。

参考 `templates/AGENTS.md` 和 `templates/CURRENT.md`。新聊天在同一工作目录即可读取项目入口，跨设备需先取得私有仓库与对应本地资料。远端登录态和桌面控件不会随记忆迁移。

## 数据范围

公开仓库不包含求职者资料、简历、投递历史、证件号、邮箱、手机号、截图、可编辑设计链接、Cookie或验证码。私有记忆也尽量只保存状态和资料索引，完整身份资料留本地。

本项目提供工作流程，不是批量免登录投递机器人。短信、风控、缺失资料、出差地区和网站限制仍须现场处理。不得虚构经历或代做测评。

来源：[OpenAI AGENTS.md文档](https://learn.chatgpt.com/docs/agent-configuration/agents-md)。

许可证：MIT。
