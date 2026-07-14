---
name: campus-romance-showrunner
description: Use this skill to run the top-level workflow for a 100k-word Chinese high-school campus romance novel, including story bible updates, long-form outline control, chapter sequencing, subagent assignment, and project file discipline.
---

# Campus Romance Showrunner

Use this as the main production skill for the 温州十年前高中校园言情 project.

## Inputs

- `planning/story_bible.md`
- `planning/outline.md`
- `planning/workflow.md`
- `reviews/continuity_log.md`
- Latest chapter plan and chapter draft when present

## Core Duties

1. Maintain the story bible as the source of truth.
2. Keep the novel around 100,000 Chinese characters across 32-38 chapters.
3. Ensure each chapter has a visible small story, not only mood.
4. Assign clean-context subagents only for bounded jobs:
   - chapter planning
   - chapter drafting
   - continuity checking
   - style polishing
   - arc review
5. Do not allow subagents to change core canon without updating the story bible.
6. Save artifacts before moving to the next stage.

## Long-Form Structure

Use four arcs:

1. 熟悉：办公室、听写本、第一次记住对方。
2. 靠近：学习事务掩护下的试探、帮忙、流言。
3. 拉扯：受欢迎带来的误会、班主任关注、成绩压力。
4. 分别：高考、暑假、不同大学、开放余味。

Every 1-3 chapters should form a small event loop:

```text
任务/事件 -> 靠近或误会 -> 公开压力 -> 私下余波 -> 下一章钩子
```

## Required Production Loop

For each chapter:

1. Read story bible, outline, continuity log, and previous chapter ending.
2. Create `chapters/chapter_xx_plan.md`.
3. Draft `chapters/chapter_xx.md`.
4. Run continuity check.
5. Run anti-AI and style polish.
6. Update `reviews/continuity_log.md`.
7. Every 5 chapters update `reviews/arc_reviews.md`.

## Decision Rules

- If the user gives new canon, update `planning/story_bible.md` first.
- If a chapter contradicts canon, fix the chapter rather than silently changing canon.
- If the story feels flat, add public pressure or a concrete object proof.
- If the romance escalates too physically, convert intimacy into restraint, object, silence, or timing.
- If prose explains theme, replace the explanation with action, image, or dialogue.

## Output Contract

When reporting progress, mention:

- files created or updated
- current chapter/state
- any canon decisions made
- next production step

