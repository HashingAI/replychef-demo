# ReplyChef demo

给忙到没时间回评论的餐厅经理做的助手：新差评进来后按经理口吻起草一条像真人写的回复，经理点一下确认就发；同时把评论归类分析，每天给一份总结。

这是一个纯前端、可点击的 demo，用来给餐厅 pitch。所有评论都是样例数据（按真实开业周差评模式改写，人名已替换），「重写」按钮切换的是预设版本，正式版会现场调用模型生成（prompt 已在 `index.html` 的 `replyPrompt()` 里）。

## 在线预览

开启 GitHub Pages 后：`https://<owner>.github.io/replychef-demo/`

## 本地打开

直接双击 `index.html` 就行，没有构建步骤，没有依赖（字体走 Google Fonts，断网也能看，只是字体回落）。

## 页面里有什么

- 收件箱：Google / Yelp 评论 + AI 草稿 + 「人味检查」打分 + 发布 / 复制 / 重写
- 评论分析：7 天好中差评、差评原因排行、星级走势、高频词、回复率
- 每日总结：模拟早上发到经理手机的那条消息
- 餐厅资料：AI 起草时只引用这里的事实

## 文档

- `docs/ReplyChef_BRD_v0.1.docx`：业务需求文档（可行性、范围、功能、风险、里程碑）
- `docs/voice-guide.md`：人味回复写作指南，含禁用短语和 8 条可机检规则

## 平台现状（2026 年 9 月）

- Google Business Profile API：可以拉评论、收新评论推送、发回复，需要申请 Basic Access 并由餐厅授权
- Yelp：完整评论和回复接口只对签约合作伙伴开放，demo 里 Yelp 是「起草 + 复制粘贴」
