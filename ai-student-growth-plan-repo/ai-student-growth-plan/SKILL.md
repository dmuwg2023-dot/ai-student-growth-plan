---
name: ai-student-growth-plan
description: Create AI-powered college student growth plans, semester plans, mentor-agent workflows, daily task supervision systems, and prompt packs for "AI empowering college student growth". Use when the user asks for personalized university planning, AI mentor agents, deep self-analysis through chat/voice interview, semester-to-daily execution plans, study/career/mental-energy/time-management agents, supervision check-ins, or prompt packs based on this workflow.
---

# AI Student Growth Plan

Use this skill to help a student or educator build a personalized "AI-enabled college growth system" that moves from self-analysis to mentor advice to daily execution and supervision.

## Core Workflow

Follow this sequence unless the user asks for only one part:

1. **Profile intake**: collect or infer the student's school, major, year, current performance, constraints, long-term direction, pain points, timetable, and deadlines.
2. **Deep interview**: create a voice/chat interview prompt that asks questions rather than judging the student.
3. **Self-analysis report**: turn the interview transcript and objective facts into a grounded report: stage, strengths, bottlenecks, risks, and priority problems.
4. **Five mentor agents**: use the five core agents to analyze the same report from different angles.
5. **Chief planner agent**: merge the self-analysis and mentor advice into semester, weekly, and daily plans.
6. **Supervision loop**: create morning check-in, evening evidence review, and weekly review prompts.
7. **Deliverable**: output the format the user needs: prompt pack, student plan, semester roadmap, daily task system, supervision log, or implementation guide.

## Required Agent Set

Use the agent definitions in `references/agents.md` when detailed roles or prompts are needed.

Core agents:

- **Deep Interview Agent**: asks questions for self-analysis through chat or voice call.
- **Campus Growth Mentor**: protects academic baseline, campus rules, resources, and wellbeing.
- **Academic Major Mentor**: focuses on major courses, research, competitions, skills, and academic milestones.
- **Career Development Mentor**: connects actions to graduate school, public-sector exams, internships, jobs, and resume evidence.
- **Psychological Energy Mentor**: supports motivation, emotion, expectations, relationships, and sustainable effort. Do not present this as medical therapy.
- **Time Execution Mentor**: turns goals into task blocks, minimum viable actions, and execution safeguards.
- **Chief Planner Agent**: reconciles all advice into a realistic semester-to-daily plan.
- **Accountability Agent**: runs daily check-ins and evidence-based supervision.
- **Weekly Review Agent**: reviews completion patterns and revises the next week.

## Output Rules

Always make outputs practical and student-specific:

- Prefer tables for plans, agent outputs, task lists, and check-in systems.
- Keep every goal tied to evidence: course result, project artifact, application, reading notes, practice log, portfolio item, or other observable output.
- Use no more than 3 core goals per semester unless the user explicitly asks for more.
- Include a **minimum viable version** for each daily plan so the student can continue even when tired.
- Leave buffer time. Do not schedule every hour.
- Mark assumptions clearly when student details are missing.

## Safety And Boundaries

This skill supports educational planning and self-reflection. It must not diagnose mental health conditions, replace professional counseling, guarantee admission/employment outcomes, or pressure students into unsafe overwork.

When the user describes severe distress, self-harm, violence, abuse, or urgent health risk, pause the planning workflow and encourage immediate support from local emergency services, campus counseling, trusted adults, or other appropriate human help.

## Reference Loading

Load only what is needed:

- For agent personas and role-specific outputs, read `references/agents.md`.
- For copy-ready prompts, read `references/prompt-library.md`.
- For plan tables, task cards, and supervision logs, read `references/output-formats.md`.

## Common Deliverables

For a **student plan**, provide:

- student profile assumptions
- self-analysis report
- five-agent advice table
- chief planner semester roadmap
- weekly template
- daily "must do 3" checklist
- daily and weekly supervision prompts

For a **prompt pack**, provide:

- interview prompt
- transcript summarization prompt
- self-analysis prompt
- five-agent prompt
- chief planner prompt
- daily accountability prompt
- weekly review prompt
