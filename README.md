# account-research

全平台对标账号深度拆解 skill。通过搜索汇总 + 6 章分析工作流 + 结构化报告，帮助内容创作者从"找对标"过渡到"找定位"。

---

## 能力

| 能力 | 说明 |
|------|------|
| 全平台支持 | X、知乎、小红书、少数派、B站、虎嗅等，不限于公众号 |
| 分级拆解 | 快速拆解（10-15 篇）和深度拆解（30+ 篇）两种模式 |
| 聚焦分析 | 可选重点关注：选题灵感 / 内容结构模仿 / 变现路径参考 / 全面拆解 |
| 变现路径分析 | 独立章节分析变现方式、用户付费驱动力、可复制性 |
| 结构化报告 | 标准 Markdown 报告，含信息来源、证据追溯、行动建议 |

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

- [web-access](https://github.com/eze-is/web-access) — 搜索引擎和网页抓取能力

web-access 需要 **Node.js 22+** 和 Chrome 开启远程调试（`chrome://inspect/#remote-debugging` → 勾选 Allow remote debugging）。

## 使用

安装后直接让 Agent 分析对标账号：

- "帮我拆解一下「一泽Eze」的内容策略和变现路径"
- "分析一下这个推特账号：@eze_is_1"
- "我想学习「刘润」的内容结构，给分析一下"
- "对标拆解这个小红书账号"

## 工作流

```
启动 → 收集 3 个问题（账号名、分析模式、重点关注）
  ↓
搜索确认主阵地 → 按平台优先级逐平台搜索（实时汇报进度）
  ↓
快速模式 10-15 篇 / 深度模式 30+ 篇，达标即停
  ↓
6 章分析（选题 / 内容结构 / 用户画像与定位 / 变现路径 / 行动建议）
  ↓
询问保存位置 → 输出 Markdown 报告
```

## 设计哲学

> 对标的三个核心角度：找爆款选题、找内容结构、找变现路径。搜索策略按实际可搜索能力排序，不硬搜搜不到的平台。分析过程中零交互，用户可随时发消息干预。

详见 [SKILL.md](./SKILL.md)。

## License

MIT · 作者：[晴天](https://github.com/Yang642514)
