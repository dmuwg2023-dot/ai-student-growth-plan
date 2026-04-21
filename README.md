# AI Student Growth Plan

面向所有智能体的大学生成长规划 Agent 工作流包。

它用于帮助大学生完成一套可执行的成长闭环：

```text
深度自我剖析 -> 五位导师 Agent 分析 -> 主 Agent 生成计划 -> 每日监督执行 -> 周复盘迭代
```

本项目不是只绑定 Codex。任何支持长提示词、角色设定、文件上传、知识库、项目指令或工作流编排的智能体，都可以直接使用。

## Fastest Universal Use

如果你使用 ChatGPT、Claude、Gemini、豆包、DeepSeek、Kimi、Dify、Coze 或其他智能体，最简单的方法是：

1. 打开 [`UNIVERSAL_AGENT.md`](./UNIVERSAL_AGENT.md)
2. 把整份内容复制到智能体的“系统提示词 / 项目指令 / 知识库 / 角色设定”里
3. 对智能体说：

```text
请按照 AI Student Growth Plan 的流程，帮我生成一份个性化大学生成长计划，并设计每日监督完成目标的闭环。
```

如果智能体支持上传文件，直接上传这些文件即可：

```text
UNIVERSAL_AGENT.md
ai-student-growth-plan/references/agents.md
ai-student-growth-plan/references/prompt-library.md
ai-student-growth-plan/references/output-formats.md
```

## What It Includes

- 深度访谈 Agent：通过聊天或语音访谈挖掘真实问题
- 五位导师 Agent：校园成长、专业学业、职业发展、心理能量、时间执行
- 主 Agent：综合整理为学期、周度、每日计划
- 监督 Agent：每日早晚打卡和证据复盘
- 周复盘 Agent：识别执行模式并调整下周计划
- 可复制提示词和输出模板

## Universal Installation Guide

不同平台的使用方式见：

[INSTALL.md](./INSTALL.md)

## Codex Skill Installation

如果你使用 Codex，也可以通过 skill installer 从本 GitHub 仓库安装：

```powershell
python "$HOME\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo dmuwg2023-dot/ai-student-growth-plan --path ai-student-growth-plan
```

也可以用 GitHub URL：

```powershell
python "$HOME\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --url https://github.com/dmuwg2023-dot/ai-student-growth-plan/tree/main/ai-student-growth-plan
```

安装后重启 Codex，让新 skill 生效。

## Example Prompts

通用智能体调用：

```text
请根据 AI Student Growth Plan 的流程，为一名大二计算机专业学生生成一份 AI 赋能学期成长计划。学生目标是提高绩点、准备实习、减少拖延。请输出深度访谈问题、自我剖析报告、五位导师建议、主 Agent 计划、每日监督和周复盘流程。
```

提示词合集调用：

```text
请只生成一套可复制提示词，包括深度访谈、通话转文字、五位导师 Agent、主 Agent、每日监督和周复盘。
```

Codex skill 调用：

```text
Use $ai-student-growth-plan to create a personalized semester growth plan for a sophomore computer science student who wants to improve GPA, prepare for internship, and reduce procrastination.
```

## Repository Layout

```text
UNIVERSAL_AGENT.md
INSTALL.md
AGENTS.md
agent-package.json
ai-student-growth-plan/
  SKILL.md
  agents/openai.yaml
  references/
    agents.md
    output-formats.md
    prompt-library.md
examples/
  sample-request.md
LICENSE
README.md
```

## License

MIT
