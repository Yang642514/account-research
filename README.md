# account-research

给 Claude Code 装上对标账号深度分析能力的 skill。

Claude Code 擅长联网和搜索，但缺少系统化的内容分析框架。这个 skill 补上的是：**全网搜索汇总 + 5 步分析工作流 + 结构化拆解报告**，帮助内容创作者从"找对标"过渡到"找定位"。

---

## 能力

| 能力 | 说明 |
|------|------|
| 多种输入方式 | 支持微信文章链接、本地文件/文本、或只给账号名自动搜索 |
| 智能搜索补充 | 材料不足时自动调用 web-access 全网搜索（微信、知乎、头条、小红书等） |
| 5 步分析工作流 | 赛道方向 → 用户痛点 → 定位公式（WWWH）→ 深度优势 → 行动建议 |
| 结构化报告 | 输出标准 Markdown 报告，附信息来源清单和证据追溯 |

---

## 安装

**方式一：让 Claude 自动安装**

```
帮我安装这个 skill：https://github.com/Yang642514/account-research
```

**方式二：手动**

```bash
git clone https://github.com/Yang642514/account-research ~/.claude/skills/account-research
```

## 依赖

- [web-access](https://github.com/eze-is/web-access) — 搜索引擎和网页抓取能力（搜索补充、微信文章 CDP 抓取均依赖此 skill）

安装 account-research 前，需先安装 web-access：

```bash
git clone https://github.com/eze-is/web-access ~/.claude/skills/web-access
```

web-access 需要 **Node.js 22+** 和 Chrome 开启远程调试（`chrome://inspect/#remote-debugging` → 勾选 Allow remote debugging）。

## 使用

安装后直接让 Agent 分析对标账号：

- "帮我拆解一下「某某公众号」的定位和内容策略"
- "分析一下这个账号：https://mp.weixin.qq.com/s/xxx"
- "我想学习「刘润」的内容风格，给分析一下"

## 工作流

```
用户输入（账号名 / 链接 / 文件）
       ↓
  收集材料 → 判断够不够（≥3篇图文 = 够）
       ↓
  不够 → 调用 web-access 全网搜索补充
       ↓
  5 步分析（赛道 / 痛点 / 定位公式 / 优势 / 建议）
       ↓
  输出结构化 Markdown 报告
```

## 设计哲学

> Skill = 哲学 + 技术事实，不是操作手册。分析框架给到位，搜索路径交给 web-access 自己判断。

详见 [SKILL.md](./SKILL.md)。

## License

MIT · 作者：[Yang642514](https://github.com/Yang642514)
