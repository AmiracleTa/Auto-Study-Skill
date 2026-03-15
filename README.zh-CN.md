[English](README.md) | [简体中文](README.zh-CN.md)

# Auto-Study

Auto study skill 是一个面向 **网页学习平台** 像是 **雨课堂、学习通、pintia** 或其他 **答题场景** 的 agent skill。让 agent 学会在浏览器中使用学习平台、读取文本或图片、返回答案、选择选项、进行填空等操作。使用独立的浏览器 profile 保持登录状态，减少潜在的安全问题，并支持后台运行。

目前支持 **Windows** 或 **WSL** 环境，浏览器支持 **Windows Chrome**

## 效果预览

**雨课堂**

`user: 做完 oop-6 这 50 题，先不要提交`

https://github.com/user-attachments/assets/816565a6-a28b-4a12-a4c5-e75b99978868

**学习通**

`user: 打开学习通`

`user: 做 10.1-10.5 的章节测验，直接提交`

> *wait for some time...*

`agent:`

```text
10.1 - 10.5 的章节测验都已经做完并提交了喵～
- 10.1：100 分
- 10.2：100 分
- 10.3：100 分
- 10.4：100 分
- 10.5：100 分

我还把每一节的截图和答案记录都存好了：
- quiz/markdown/xuexitong-10.1-以法治为重器：法治的价值定位.md
- quiz/markdown/xuexitong-10.2-以系统为谋划：法治的推进战略.md
- quiz/markdown/xuexitong-10.3-以世界为方法：法治的世界结构（上）.md
- quiz/markdown/xuexitong-10.4-以世界为方法：法治的世界结构（下）.md
- quiz/markdown/xuexitong-10.5-以中国为目的：法治的中国语境.md
```

>  自动生成 markdown，截取题目，分析答案，记录分数

<img width="1632" height="1773" alt="Image" src="https://github.com/user-attachments/assets/96d5dbff-6cd3-45dc-9957-d2a094b141ba" />

**其他使用方式**

`user: 给我 4.1章节测验的答案`

`user: 简短分析一下每道题目`

## 安装 skill

### 交给你的 agent

直接告诉你的 agent：`帮我安装这个 skill, https://github.com/AmiracleTa/Auto-Study-Skill`

---

### 手动安装

#### 复制仓库

把此仓库复制到 agent 的 `skills` 文件夹。

**OpenClaw:** `~/.openclaw/workspace/skills`

**Codex:** `~/.codex/skills`

#### 安装依赖

- Google Chrome (Windows)
- [Agent Browser CLI](https://github.com/vercel-labs/agent-browser)
- [Agent Browser Skill](https://clawhub.ai/MaTriXy/agent-browser-clawdbot)

## 行为

- 默认直接给答案，不附加额外解释。
- 除非明确要求，否则做完后不自动提交。

详细策略参考 [SKILL.md](SKILL.md)。

## 默认配置

- CDP 端口：`9344`
- profile 根目录：`%LOCALAPPDATA%\AutoStudy\browser`

## 工作流

1. 使用特定 CDP 端口，启动或连接 Chrome
2. 读取浏览器页面和状态
3. 按照用户要求进行相应操作

## 详细策略

- [SKILL.md](SKILL.md) 核心策略
- [references/xuexitong.md](references/xuexitong.md) 学习通专用策略
- [references/yuketang.md](references/yuketang.md) 雨课堂专用策略
- [references/pintia.md](references/pintia.md) pintia 专用策略
- [references/runtime-windows.md](references/runtime-windows.md) Windows 运行说明
- [references/runtime-wsl.md](references/runtime-wsl.md) WSL 运行说明
- [references/browser.md](references/browser.md) 浏览器相关说明

## 合规使用

使用这个 skill 时，需要自行确保符合法律法规、学校或机构规则以及平台服务条款

这个 skill 的设计目标是：**知识学习、普通测验、网页答题辅助**

不要用于 **正式考试，绕过技术限制或其他不被允许的自动化**

---

***AI 不是人类，谨慎使用自动提交***
