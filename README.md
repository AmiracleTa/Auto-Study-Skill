[English](README.md) | [简体中文](README.zh-CN.md)

# Auto-Study

The Auto-Study skill is an agent skill for **web-based learning platforms** such as **Yuketang**, **Xuexitong**, **pintia**, and other **question-answering scenarios**.

It teaches the agent to use learning platforms in a browser, read text or images, return answers, choose options, fill in blanks, and carry out similar actions. It uses a separate browser profile to preserve login state, reduce potential security risks, and support background execution.

It currently supports **Windows** or **WSL**, and browser support is limited to **Google Chrome on Windows**.

## Preview

**Yuketang**

`user: Finish these 50 OOP-6 questions, but don't submit them yet`

https://github.com/user-attachments/assets/816565a6-a28b-4a12-a4c5-e75b99978868

**Xuexitong**

`user: Open Xuexitong`

`user: Finish the chapter quizzes for 10.1-10.5 and submit them directly`

> *wait for some time...*

`agent:`

```text
The chapter quizzes for 10.1 - 10.5 are all completed and submitted.
- 10.1: 100
- 10.2: 100
- 10.3: 100
- 10.4: 100
- 10.5: 100

I also saved the screenshots and answer records for each section:
- quiz/markdown/xuexitong-10.1-以法治为重器：法治的价值定位.md
- quiz/markdown/xuexitong-10.2-以系统为谋划：法治的推进战略.md
- quiz/markdown/xuexitong-10.3-以世界为方法：法治的世界结构（上）.md
- quiz/markdown/xuexitong-10.4-以世界为方法：法治的世界结构（下）.md
- quiz/markdown/xuexitong-10.5-以中国为目的：法治的中国语境.md
```

> Auto-generated markdown with captured questions, answer analysis, and recorded scores.

<img width="1632" height="1773" alt="Image" src="https://github.com/user-attachments/assets/96d5dbff-6cd3-45dc-9957-d2a094b141ba" />

**Other usage examples**

`user: Give me the answers for the 4.1 chapter quiz`

`user: Briefly analyze each question`

## Install the Skill

### Let your agent handle it

Just tell your agent: `Help me install this skill, https://github.com/AmiracleTa/Auto-Study-Skill`

---

### Manual Installation

#### Copy the repository

Copy this repository into your agent's `skills` folder.

**OpenClaw:** `~/.openclaw/workspace/skills`

**Codex:** `~/.codex/skills`

#### Install dependencies

- Google Chrome (Windows)
- [Agent Browser CLI](https://github.com/vercel-labs/agent-browser)
- [Agent Browser Skill](https://clawhub.ai/MaTriXy/agent-browser-clawdbot)

## Behavior

- By default, it returns answers directly without extra explanation.
- Unless explicitly requested, it does not submit automatically after finishing.

For detailed strategy, see [SKILL.md](SKILL.md).

## Default Configuration

- CDP port: `9344`
- Profile root directory: `%LOCALAPPDATA%\AutoStudy\browser`

## Workflow

1. Start or connect to Chrome using a dedicated CDP port
2. Read the browser page and current state
3. Perform the requested actions according to the user's instructions

## Detailed Strategy

- [SKILL.md](SKILL.md) Core strategy
- [references/xuexitong.md](references/xuexitong.md) Xuexitong-specific strategy
- [references/yuketang.md](references/yuketang.md) Yuketang-specific strategy
- [references/pintia.md](references/pintia.md) pintia-specific strategy
- [references/runtime-windows.md](references/runtime-windows.md) Windows runtime instructions
- [references/runtime-wsl.md](references/runtime-wsl.md) WSL runtime instructions
- [references/browser.md](references/browser.md) Browser-related notes

## Acceptable Use

When using this skill, you are responsible for ensuring compliance with applicable laws and regulations, school or institutional rules, and platform terms of service.

This skill is designed for: **learning, ordinary quizzes, and browser-based answering assistance**

Do not use it for **formal exams, bypassing technical restrictions, or any other disallowed automation**.

---

***AI is not a human. Use auto-submit with caution.***
