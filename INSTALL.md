# Universal Installation And Usage

There is no single install protocol shared by all AI agents. This repository is therefore packaged in three layers:

1. `UNIVERSAL_AGENT.md`: one-file universal instructions for any agent.
2. `ai-student-growth-plan/references/`: modular prompts and templates.
3. `ai-student-growth-plan/`: Codex skill adapter.

## ChatGPT / Custom GPT

Use one of these methods:

- Paste `UNIVERSAL_AGENT.md` into Custom GPT Instructions.
- Upload `UNIVERSAL_AGENT.md` and the `references/` files as knowledge files.
- In a normal chat, paste `UNIVERSAL_AGENT.md` first, then ask for a student growth plan.

Starter prompt:

```text
Use the AI Student Growth Plan workflow to help me create a personalized semester plan and daily accountability loop.
```

## Claude / Claude Projects

Use one of these methods:

- Add `UNIVERSAL_AGENT.md` to Project Instructions.
- Upload `UNIVERSAL_AGENT.md`, `agents.md`, `prompt-library.md`, and `output-formats.md` to the project.

Starter prompt:

```text
Follow the uploaded AI Student Growth Plan instructions and generate a complete plan for my semester.
```

## Gemini / Gems

Use one of these methods:

- Paste `UNIVERSAL_AGENT.md` into Gem instructions.
- Upload the reference files if the product supports files.

Starter prompt:

```text
Act as the AI Student Growth Plan agent and guide me from self-analysis to daily supervision.
```

## DeepSeek / Kimi / Doubao

Use one of these methods:

- Paste `UNIVERSAL_AGENT.md` into the chat before asking for a plan.
- Copy specific prompts from `prompt-library.md` step by step.
- For voice interview workflows, start with the Deep Interview prompt.

Starter prompt:

```text
我会给你一套 AI Student Growth Plan 工作流。请先读取，然后按“深度访谈 -> 五位导师 -> 主计划 -> 每日监督 -> 周复盘”的流程帮助我。
```

## Dify / Coze / Agent Builders

Recommended setup:

- System prompt: paste `UNIVERSAL_AGENT.md`
- Knowledge files: upload `agents.md`, `prompt-library.md`, `output-formats.md`
- Opening message: ask the user for school, major, year, current worries, timetable, and goals
- Workflow nodes:
  1. intake
  2. deep interview
  3. self-analysis
  4. five mentor agents
  5. chief planner
  6. daily accountability
  7. weekly review

## Codex

Install as a Codex skill:

```powershell
python "$HOME\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo dmuwg2023-dot/ai-student-growth-plan --path ai-student-growth-plan
```

Or:

```powershell
python "$HOME\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --url https://github.com/dmuwg2023-dot/ai-student-growth-plan/tree/main/ai-student-growth-plan
```

Restart Codex after installation.

## Minimal Copy-Paste Use

If the platform cannot install or upload files, copy this into the chat:

```text
请扮演 AI Student Growth Plan agent。你的流程是：深度自我剖析 -> 五位导师 Agent 分析 -> 主 Agent 生成学期/周度/每日计划 -> 每日监督执行 -> 周复盘迭代。请先询问我的学校、专业、年级、学习现状、长期方向、当前最困扰的 3 个问题、课表和重要截止日期，然后帮我生成完整计划。
```
