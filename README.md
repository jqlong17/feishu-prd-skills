# 飞书 PRD 撰写与评审

用 Cursor、Codex 或 Workbuddy 打开本仓库，按 skill 写飞书 PRD，或给一篇已经写好的 PRD 打分。

## 使用方法

撰写：

```text
写一篇 PRD：资料柜要支持按入口上传文件，并在列表里预览。
```

改已有文档时，把飞书链接一起发来：

```text
更新这篇 PRD https://example.feishu.cn/docx/文档ID
把预览改成新开页面看原文件。
```

评审：

```text
评审这篇 PRD https://example.feishu.cn/docx/文档ID
```

评审只出意见和修改表，不改文档。你回复编号后，再按该条改。

## 输出样例

撰写时的章节和密度见 [参考 PRD](examples/reference-prd.md)。那是一份虚构的资料柜需求，用来看字段表、失败提示、图注和「本期不做」怎么写。不要把它的业务抄进别的产品。

评审结束时要有一张表，作者可以按编号改：

| 编号 | 原文 | 建议修改后 | 理由 |
| --- | --- | --- | --- |
| 1 | 「资料类型按扩展名判定。」 | 「资料类型在上传时确定。从「说明文档」上传的记为说明类。」 | 4.1 字段表。判定发生在上传当时。 |

## 支持的智能体

| 智能体 | skill |
| --- | --- |
| Cursor | `.cursor/skills/feishu-prd`、`.cursor/skills/feishu-prd-review` |
| Codex | `.codex/skills/feishu-prd`、`.codex/skills/feishu-prd-review` |
| Workbuddy | `.workbuddy/skills/feishu-prd`、`.workbuddy/skills/feishu-prd-review` |

正文在 `skills/feishu-prd` 和 `skills/feishu-prd-review`。上面三处与它一致。

撰写和改文档需要本机已登录 `lark-cli`（`lark-cli auth status --json --verify`）。评审只读文档。

## 不包含

- 不包含任何真实产品的飞书文档、客户项目名或线上地址。
- 参考 PRD 里的 `https://example.com` 只是图下链接的写法，不是可打开的站点。
- 不包含 API Key。
