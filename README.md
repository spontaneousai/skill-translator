# Skill Translator

![screenshot](screenshot.png)
![screenshot](example.png)
![GitHub stars](https://img.shields.io/github/stars/spontaneousai/skill-translator?style=flat)

将 Claude 的 Skill（`.skill` 或 `SKILL.md`）转译为其他 LLM 平台可用的 System Prompt 格式，纯静态单页，适合部署在 GitHub Pages。

**在线 Demo：** [https://spontaneousai.github.io/skill-translator](https://spontaneousai.github.io/skill-translator)

## 功能

- 拖拽或选择 `.skill` / `.md` / `.txt`，或在页面中直接粘贴 `SKILL.md` 正文
- 使用 JSZip 解析 `.skill`（zip），读取 `SKILL.md` 与 `references/` 下的 `.md`、`.txt`
- 解析 YAML frontmatter 中的 `name`、`description`，正文支持将 `references/…` 引用内联进输出
- 三种输出：**通用 System Prompt**、**Gemini Gem 风格**、**ChatGPT Custom GPT Instructions**（含未内联资源的 Knowledge 上传建议）
- 深色 / 浅色界面跟随系统（`prefers-color-scheme`）
- 页脚集成访问计数器

## 使用方法

**直接在线使用（推荐）：** 打开 [https://spontaneousai.github.io/skill-translator](https://spontaneousai.github.io/skill-translator)，无需安装任何东西。

1. 导入 Skill：拖拽 `.skill` 或 `SKILL.md` 文件到页面，或点击「选择文件」，或直接粘贴 `SKILL.md` 内容。
2. 点击「转译」，从三个 Tab 中选择目标平台（通用 / Gemini / ChatGPT）。
3. 点击「复制」，粘贴到对应平台的 System Prompt 输入框即可。

点击「载入示例」可快速体验完整流程。

## 本地运行（开发者）

无需 Node 或构建工具，用浏览器直接打开 `index.html` 即可，或启动一个简单的静态服务器：

```bash
python3 -m http.server 8080
# 浏览器访问 http://localhost:8080
```

## 许可证

MIT
