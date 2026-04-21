# AI Student Growth Plan

一个面向所有智能体的大学生成长规划 Agent 工作流包，用于生成“AI 赋能大学生成长计划”：从深度自我剖析、五位导师 Agent 分析，到主 Agent 落地日计划，再到每日监督与周复盘。

它不是只绑定 Codex 的工具。任何支持长提示词、角色设定、文件读取或工作流编排的智能体，都可以直接使用本仓库里的 Agent 定义、提示词和输出模板。

Codex 用户可以把它作为 skill 安装；其他智能体用户可以直接复制 `references/` 里的提示词和模板使用。

## What It Includes

- 深度访谈 Agent：通过聊天或语音访谈挖掘真实问题
- 五位导师 Agent：校园成长、专业学业、职业发展、心理能量、时间执行
- 主 Agent：综合整理为学期、周度、每日计划
- 监督 Agent：每日早晚打卡和证据复盘
- 周复盘 Agent：识别执行模式并调整下周计划
- 可复制提示词和输出模板

## Universal Usage

如果你使用 ChatGPT、Claude、Gemini、豆包、DeepSeek、Kimi 或其他智能体，可以直接按这个顺序使用：

1. 打开 `ai-student-growth-plan/references/prompt-library.md`
2. 复制 `P1 Deep Interview Prompt`，让智能体先做深度访谈
3. 用 `P2` 整理访谈记录
4. 用 `P3` 生成自我剖析报告
5. 用 `P5` 生成五位导师 Agent 分析
6. 用 `P6` 让主 Agent 生成学期、周度、每日计划
7. 用 `P7` 和 `P8` 做每日监督与周复盘

如果你的智能体支持上传文件，可以直接上传这些文件：

```text
ai-student-growth-plan/references/agents.md
ai-student-growth-plan/references/prompt-library.md
ai-student-growth-plan/references/output-formats.md
```

然后输入：

```text
请使用这些 Agent 定义和提示词模板，帮我生成一份个性化大学生成长计划，并设计每日监督完成目标的闭环。
```

## Codex Skill Installation

如果你使用 Codex，可以通过 skill installer 从本 GitHub 仓库安装：

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
请根据 prompt-library.md 和 agents.md 的流程，为一名大二计算机专业学生生成一份 AI 赋能学期成长计划。学生目标是提高绩点、准备实习、减少拖延。请输出深度访谈问题、自我剖析报告、五位导师建议、主 Agent 计划、每日监督和周复盘流程。
```

Codex skill 调用：

```text
Use $ai-student-growth-plan to create a personalized semester growth plan for a sophomore computer science student who wants to improve GPA, prepare for internship, and reduce procrastination.
```

提示词合集调用：

```text
请只生成一套可复制提示词，包括深度访谈、通话转文字、五位导师 Agent、主 Agent、每日监督和周复盘。
```

## Repository Layout

```text
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
