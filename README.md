# 阿丽小红书排版 Skill

一个开源的 Agent Skill,帮你把一篇文章一键转成小红书图文卡片。
风格:**New Brutalism**(新粗野主义)—— 黑粗边框、硬阴影、网格底纹、高对比色块。

> 兼容 Claude Code / Claude.ai / OpenClaw / OpenCode 所有支持 SKILL.md 标准的工具。

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

## 效果预览

> 把你真实用这个 Skill 做出来的 2–3 张卡片截图放在这里。
> 建议放进 `examples/` 文件夹,然后用 `![](examples/xxx.png)` 引用。

```
examples/
├── case1-skill-tutorial.png
├── case2-ai-toolkit.png
└── case3-productivity.png
```

---

## 安装方法

### Claude Code

把整个文件夹放到:

```bash
# 全局(所有项目都能用,推荐)
~/.claude/skills/xiaohongshu-infographic/

# 或项目级(只当前项目能用)
.claude/skills/xiaohongshu-infographic/
```

重启 Claude Code 自动识别,不需要手动激活。

### Claude.ai 网页版

1. 把整个文件夹打包成 `.zip`
2. 打开 Settings → Capabilities → Skills
3. 点上传,选择刚才的 zip
4. 需要 Pro 或以上版本,且开启 Code Execution

### OpenClaw

```bash
~/.openclaw/workspace/skills/xiaohongshu-infographic/
```

启动新 session 生效。

### OpenCode

```bash
# 全局
~/.config/opencode/skills/xiaohongshu-infographic/

# 或项目级
.opencode/skills/xiaohongshu-infographic/
```

OpenCode 也兼容 `.claude/skills/` 路径,已有 Claude Code 配置的话无需重复安装。

---

## 怎么用

把文章扔给 AI,加一句触发话即可。不用显式说"用 skill":

```
下面这篇文章帮我转成小红书图文卡片:

[粘贴你的文章]
```

或者:

```
帮我把这篇文章做成小红书出图
```

AI 会自动识别、读取视觉锚点、生成一个完整的 HTML 文件,
里面带导出按钮,点击一键打包下载所有卡片。

---

## 自定义

这个 Skill 设计成可以 fork 改成你自己的风格。常见改点:

| 想改的地方 | 改哪里 |
|-----------|--------|
| 主题配色 | `SKILL.md` 第 1 节色彩逻辑 + `references/reference.html` 的 `:root` 变量 |
| 卡片比例 | `references/reference.html` 里 `.canvas` 的 `width / height` |
| 字号红线 | `SKILL.md` 第 3 节字号红线 |
| Vibe Tag 署名 | 全局搜索「大头阿丽 · Vibe Coding 系列」替换为你自己的 |
| 页数上限 | `SKILL.md` 第 3 节「页数硬红线」(默认 19 张) |

改完记得同步更新 `SKILL.md` 里的规则描述,
不然 AI 可能按旧规则生成,跟你新的视觉锚点不一致。

---

## 文件结构

```
xiaohongshu-infographic/
├── SKILL.md              # 主文件,规则 + 触发条件
├── README.md             # 你正在看的这份
├── LICENSE               # MIT
├── references/
│   └── reference.html    # 视觉锚点,AI 执行前必读
└── examples/             # 真实作品截图(可选,强烈推荐放)
```

---

## 贡献

欢迎 fork 出你自己版本,也欢迎提 Issue 或 PR 改进本版本。
如果你基于这个 Skill 做出了不同风格(比如极简风、插画风),
告诉我一声,我会在这里列出来。

---

## 作者

**大头阿丽** · Vibe Coding 系列 1/100

- 小红书: [大头阿丽](https://www.xiaohongshu.com/user/profile/653c760900000000060041bc)
- 微信: `aliaigc`(备注「进群」加 AI 粉丝群,每天聊新工具、玩法、资讯)

---

## License

MIT —— 随便用、随便改、随便商用,署名不强制但很感谢。
