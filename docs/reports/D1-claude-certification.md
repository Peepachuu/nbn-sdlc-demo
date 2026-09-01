# D1 — Claude Certification Report

**Owner:** Sidney Zeng (PM)
**Planner card:** [PRD] - Claude Certification Report D1
**Status:** Draft
**Repo path:** `docs/reports/D1-claude-certification.md`

---
## 1. Purpose and scope
This report records the team's completion of the Anthropic Academy certification and translates it into a capability inventory for the lifecycle model.

Its job is narrow and specific. When the lifecycle map (D4) states that an agent performs a step, this document identifies which mechanism that is, whether it is a skill, a hook, a command, a sub-agent or an MCP server and what it can automate, and where it stops. The "where it stops" column is what the map's red, amber and green boundaries rest on.

It is an input to D4, not a training record.

---
## 2. What the certification covers
Five courses were completed across the team, four per person. All are free, self-paced, and hosted at [anthropic.skilljar.com](https://anthropic.skilljar.com).

### 2.1 The path, by role
| Course | PM · BA · UX | Developers |
|---|---|---|
| Claude 101 | ✓ | ✓ |
| AI Fluency: Framework & Foundations | ✓ | ✓ |
| AI Capabilities and Limitations | ✓ | ✓ |
| Introduction to Claude Cowork | ✓ | — |
| Claude Code 101 | — | ✓ |

Three courses are common to all five members. The fourth differs by role: non-technical roles took Cowork, which covers Claude working directly on files and projects, while the developers took Claude Code 101, which covers the terminal-based coding agent.

### 2.2 Claude 101
Core product usage. Projects and artifacts for organising work, working with skills, connecting external tools, enterprise search, and research workflows.

Where it is relevant to this project: **skills are introduced here**, meaning all five team members have been exposed to the concept, not only the developers.

### 2.3 AI Fluency: Framework & Foundations
Built with Prof. Joseph Feller (University College Cork) and Prof. Rick Dakan (Ringling College). The course is organised around the **4D Framework**, and two of the four bear directly on this project.

| Competency | What it covers | Relevance to the lifecycle model |
|---|---|---|
| **Delegation** | Deciding what to hand to the model and what to keep, including project planning | This is the same judgement the map makes at every box. Red, amber and green are delegation decisions |
| **Description** | Communicating the task clearly; includes a deep dive on effective prompting | Feeds the prompt practice module named in the client brief |
| **Discernment** | Evaluating what comes back — process, output and performance | This is the human check. It is what a reviewer does |
| **Diligence** | Responsibility and accountability for AI-assisted work | This is the client's liability question in the framework's own vocabulary |

The course also teaches the **Description-Discernment loop** as an explicit cycle: describe, evaluate, refine. That loop is the operational shape of every amber-tier step in our model.

Using this vocabulary is preferable to inventing our own. It is published, it is taught, and NBN staff who complete the same certification will already have it.

### 2.4 AI Capabilities and Limitations
The most directly useful course for the model, and the one to draw on for the classification boundaries.

Anthropic describes it as the companion to AI Fluency: where the 4D framework teaches the human competencies, this course teaches the machine properties those competencies are responding to. It is organised around four properties:

| Property | What it explains | The failure mode it predicts |
|---|---|---|
| **Next token prediction** | How generation actually works | Output that is fluent and plausible but wrong. The reason a passing test suite proves nothing on its own |
| **Knowledge** | What the model knows and when that knowledge ends | Hallucination clustering in exact details such as names, dates, citations, URLs and a training cutoff that makes any claim about current tooling unreliable |
| **Working memory** | Context window limits | Degradation on long tasks and information dropped without warning |
| **Steerability** | How reliably the model follows direction | Instructions followed probabilistically rather than deterministically, which is why rules cannot be treated as controls |

The course's stated outcome is that a learner can look at an unexpected output, recognise which kind of unexpected it is, and respond with a targeted fix.

**This is the section of the certification that maps most directly onto our model.** Each property predicts a class of failure, and each class of failure implies where a human check belongs. Steerability in particular is the reason a rules file cannot serve as a governance control which was a point our workshop review reached independently.

### 2.5 Claude Code 101 (developers)

Covers the agentic loop, context window, tools and permissions and installation across terminal, VS Code, JetBrains, Desktop and web; approval mode, auto-accept and Plan Mode; the **Explore > Plan > Code > Commit** workflow; context management; and code review.

The customisation section is the part this report depends on. It covers, in order: the CLAUDE.md file, sub-agents, skills, MCP, and hooks.

That confirms all five mechanisms in section 3 were formally taught rather than encountered incidentally.

### 2.6 Introduction to Claude Cowork (PM, BA, UX)

Claude working directly on local files and projects. Covers the task loop, standing context via global instructions and projects, skills, and plugins.

Three lessons matter beyond their apparent scope:

- **"Plugins: Encode your team's expertise"** - packaging team practice into a reusable, distributable form
- **"Validating skills for plugins"** - a verification step before a skill is shared
- **"Share what you build with your team"** - distribution across a team




---

## 3. Capability inventory



---

## 4. Team baseline



---

## 5. Candidate applications


---

## 6. Gaps



---

## 7. Handoff


---

## Sources

Anthropic Academy, [anthropic.skilljar.com](https://anthropic.skilljar.com).

- [Claude 101](https://anthropic.skilljar.com/claude-101)
- [AI Fluency: Framework & Foundations](https://anthropic.skilljar.com/ai-fluency-framework-foundations)
- [AI Capabilities and Limitations](https://anthropic.skilljar.com/ai-capabilities-and-limitations)
- [Claude Code 101](https://anthropic.skilljar.com/claude-code-101)
- [Introduction to Claude Cowork](https://anthropic.skilljar.com/introduction-to-claude-cowork)

Team completion certificates, August 2026, verified individually. Links recorded in the Master Document. 