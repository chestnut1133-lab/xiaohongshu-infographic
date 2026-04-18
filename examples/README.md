# 阿丽小红书排版 Skill

一个开源的 Agent Skill,帮你把一篇文章一键转成小红书图文卡片。
风格:**New Brutalism**(新粗野主义)—— 黑粗边框、硬阴影、网格底纹、高对比色块。

> 兼容 Claude Code / Claude.ai / OpenClaw / OpenCode 所有支持 SKILL.md 标准的工具。

---

## 效果预览

![](examples/Vibe_Coding_Card_1.png)
![](examples/Vibe_Coding_Card_2.png)
![](examples/Vibe_Coding_Card_3.png)

<details>
<summary>点开看全部 14 张卡片</summary>

![](examples/Vibe_Coding_Card_4.png)
![](examples/Vibe_Coding_Card_5.png)
![](examples/Vibe_Coding_Card_6.png)
![](examples/Vibe_Coding_Card_7.png)
![](examples/Vibe_Coding_Card_8.png)
![](examples/Vibe_Coding_Card_9.png)
![](examples/Vibe_Coding_Card_10.png)
![](examples/Vibe_Coding_Card_11.png)
![](examples/Vibe_Coding_Card_12.png)
![](examples/Vibe_Coding_Card_13.png)
![](examples/Vibe_Coding_Card_14.png)

</details>

以上是我用这个 Skill 做的《从 0 做 1 个自己的 Skill》这篇文章的完整出图。

---

## 它是什么

这是我自己发小红书用的排版 Skill。每篇文章手动在 Figma 里排版要花大半天,
每次流程几乎一样。于是把它封装成了 Skill:丢进一篇文章,自动出一整套卡片。

**适合的场景:**
- 写好的长文 / 笔记 / 教程 → 转成图文卡片
- 想要统一风格、不每次重新调配色
- 喜欢 New Brutalism 那种"硬核、冲击力、技术范儿"的视觉

**不适合:**
- 你的风格是极简、治愈、温柔系 —— 这个 Skill 不对味,建议 fork 改色
- 只需要单张海报 —— 这个 Skill 是给多页卡片设计的(1–19 张)

---

## 安装方法

### Claude Code

把整个文件夹放到:

```bash