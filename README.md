# 个人 AI 简报

GitHub Actions 每天北京时间 08:00 采集公开来源，08:13 和 08:37 补跑，向指定 Telegram 私聊投递。整点高峰可能延迟。Actions 使用 public repo 的标准 runner。

简报覆盖大模型、Agent 和 Skills、开源工具、Linux 和 Android 开发。资讯取近期官方发布，项目从 GitHub 搜索并检查近期维护与描述。近期同项目限推一次，标题近似和链接也参与去重。空日会发状态提示。Git 中的投递状态只记录日期和公开内容标识。

## 部署

配置 Actions Secrets：`TELEGRAM_BOT_TOKEN`、`TELEGRAM_CHAT_ID`，以及可选的 `GEMINI_API_KEY`。Gemini key 应来自免费项目。模型只接收公开摘要材料，API 或输出失败时使用中文模板。可在 Actions 手动预览或关闭模型生成。

若当天状态为 `pending`，先在 Telegram 核实是否收到消息。若确认未收到，删除当天的 pending 条目、提交，再手动重跑。若已收到，将它改为 sent。明确拒绝会自动撤销 pending，允许补跑。若 GitHub 停用定时任务，可在 Actions 页面重新启用。
