# SDLC Model Requirements

**Owner:** Ahmed Falulur Rahuman  

**Planner card:** [PRD] - Requirements pass 1, off slice 1 : 90  

**Pass:** 1 - Research Slice 1

## Problem statement

We need a clear SDLC model that shows where AI can help, where humans still need to be involved, and what checks should happen before AI-assisted work moves forward. The model should be practical for large software teams and easy to follow across the whole lifecycle.

## Target user

The main users are developers, testers and architects working in organisations with 100+ developers. We are using one shared lifecycle for everyone, with different levels of detail for junior and experienced users. For now, the junior layer comes first.

## User stories

### US-01 - Show where AI fits in the lifecycle

**Source:** Slice 1 - lifecycle structure

**User story:**  

As a developer, tester or architect, I want to see where AI fits across the SDLC, so I know where it can help and where humans still need to be involved.

**Acceptance criteria:**

- The model shows all eight lifecycle stages.
- It is clear that teams can move back and forth between stages instead of following a strict waterfall.
- Each stage shows the main AI and human responsibilities.

---

### US-02 - Explain the red, amber and green model

**Source:** Slice 1 - red/amber/green model

**User story:**  

As a developer, tester or architect, I want AI tasks to be clearly marked as red, amber or green, so I can quickly understand how much human involvement is needed.

**Acceptance criteria:**

- Red means the human makes the decision or approval.
- Amber means AI helps, but a human checks and approves the result.
- Green means AI can carry out the task while a human monitors it.
- Colours are applied to tasks, not the whole stage.

**Flag:** Leon's worked examples may still change how the red, amber and green model is explained.

---

### US-03 - Check AI-generated requirements and user insights

**Source:** Slice 1 - Stage 2 and Stage 4

**User story:**  

As a BA or developer, I want AI-generated requirements and user insights to be checked by a human, so incorrect assumptions do not get treated as real requirements.

**Acceptance criteria:**

- AI-generated user stories are treated as drafts until a human checks them.
- Requirements have clear and testable acceptance criteria before they are treated as ready.
- AI-generated user journeys or user insights are checked against real users, stakeholders or existing evidence.

**Flag:** Slice 1 proposes changing Stage 2 from GREEN to AMBER and journey mapping from GREEN to AMBER.

---

### US-04 - Verify AI-generated work before accepting it

**Source:** Slice 1 - approval gates; D2 - verification gap

**User story:**  

As a tester or developer, I want AI-generated work to be checked before it is accepted, so mistakes or made-up information are caught early.

**Acceptance criteria:**

- The model shows who is responsible for checking AI-generated work.
- The work is checked against its requirements or acceptance criteria.
- If the check fails, the work must be corrected before it moves forward.

---

### US-05 - Record AI involvement and responsibility

**Source:** Slice 1 - auditability; D2 - liability and authorship

**User story:**  

As a developer, tester or architect, I want AI-assisted changes to record what AI did and who approved it, so the change can be understood later and responsibility is clear.

**Acceptance criteria:**

- The AI tool or agent used is recorded.
- The important change and human approval are recorded.
- A human role is responsible for the final approval.

---

### US-06 - Put safeguards around AI agents

**Source:** Slice 1 - prompt-injection, supply-chain risk and regulatory controls

**User story:**  

As a developer or architect, I want limits around what an AI agent can access and change, so it cannot make unsafe or unrelated changes.

**Acceptance criteria:**

- The model shows what files, tools or systems an agent is allowed to access.
- Important security, legal, accessibility and organisational rules are enforced outside the AI where needed.
- AI agents are not allowed to approve or police their own work.

---

### US-07 - Show when AI can be given more responsibility

**Source:** Slice 1 - governance thresholds and Stage 8

**User story:**  

As an architect or developer, I want to know what needs to be true before AI is given more responsibility, so we do not automate high-risk work too early.

**Acceptance criteria:**

- The model shows what checks or evidence are needed before AI gets more control.
- Higher-risk tasks require stronger human oversight.
- Deployment, rollback and incident decisions clearly show where human approval is still required.

---

### US-08 - Show how AI affects teamwork and review

**Source:** D2 - collaboration, handoffs and decision load

**User story:**  

As a member of a software team, I want the model to show how AI changes handoffs and review work, so faster AI output does not create confusion or too much work for reviewers.

**Acceptance criteria:**

- The model shows how work is handed between roles.
- Teams have a shared place for requirements and acceptance criteria.
- Human review points are clearly shown.
- The model considers review workload, not just how fast AI can produce work.

---

### US-09 - Show when a prototype can be used as the specification

**Source:** D2 - requirements and specification gap

**User story:**  

As a BA or developer, I want the model to show when prototype feedback is enough to guide the work and when written requirements are still needed, so the team has a clear source of truth.

**Acceptance criteria:**

- The model distinguishes prototype or screen-based work from backend or non-visual changes.
- The model makes it clear what the source of truth is for the work.
- Written requirements are still required when a prototype cannot clearly describe the change.

---

### US-10 - Show what actually happens inside each lifecycle stage

**Source:** Slice 1 - lifecycle structure and stage mechanics

**User story:**  

As a developer, tester or architect, I want each lifecycle stage to show the actual steps, tools and checks involved, so I know what to do next instead of only seeing a high-level stage name.

**Acceptance criteria:**

- Each stage includes the main actions or artifacts involved.
- Each stage shows who or what is responsible, such as a human, agent or sub-agent.
- A reader can tell what the next step or approval point is from the model.

---

## Unresolved questions

These still need clarification:

1. What is the minimum human check required at each stage?
2. What AI audit information does NBN need to keep?
3. What should allow a task to move from amber to green?
4. Does the team agree with changing Stage 2 from GREEN to AMBER?
5. Does the team agree with changing journey mapping from GREEN to AMBER?
6. Which NBN rules or regulations need to be enforced as hard limits?
7. How much control should AI have over deployment and rollback?
8. What should be the default way of handling collaboration and review when AI speeds up development?

## Pass 1 note

This is the first requirements pass. Later research, developer interviews and test findings can update these stories if new evidence changes what we currently know.
