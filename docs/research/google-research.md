# Source Note Template

**For:** Zafir (Google) and Chirag (Microsoft)
**Feeds:** Slice 1 - the spine
**Commit to:** `/docs/research/`

---

## Before you start — the question you are answering
Not "how does Google use AI?" Because that is largely unpublished. Ben's warning: if the only thing you can find is a blog post, it does not count.

**Answer this instead:**
What steps does this organisation say its software lifecycle has, where does it require a human to approve something, and what does the published evidence say about whether AI-generated work passes those same checks?


## Two source types, both required

**1. Documented practice, what the organisation says it does**
Formal, citable documentation of their engineering process.

- Zafir: Google's engineering practices documentation, their testing and code review guidance
- Chirag: Microsoft's DevOps documentation, their engineering playbook, Azure DevOps practice guides


**2. Empirical evidence — what actually happens with AI in the loop**
Two or three papers minimum, from **Google Scholar** or **arXiv**. Search terms that might work: AI-assisted software development, LLM code generation quality, Copilot developer productivity, automated code review effectiveness, generated code defect rates.

---

# Source Note — [Organisation]

**Author:** Zafir Hasan

**Date:** 24 August 2026

**Time spent:**

## 1. Sources

| # | Source | Type | Date accessed |
|---|---|---|---|
| S1 | https://google.github.io/eng-practices/ | Documentation | 23 August 2026|
| S2 | https://abseil.io/resources/swe-book | Documentation | 23 August 2026 |
| S3 | https://sre.google/sre-book/table-of-contents/ | Documentation | 23 August 2026 |
| S4 | https://arxiv.org/html/2509.14745v1 | Paper | 23 August 2026 |
| S5 | https://arxiv.org/html/2603.28592v1 | Paper | 24 August 2026 |
| S6 | https://arxiv.org/html/2602.08915 | Paper | 24 August 2026 |


## 2. The lifecycle stages, in their words

Google's software development lifecycle is described across several sources, each covering different stages in detail: the eng-practices guide examines code review, the Software Engineering at Google book explores release and production maintenance. When analyzed holistically, these sources describe a five-stage lifecycle from design to maintainance.

### 2.1. Design

Many teams at Google require an approved design document before starting work on any major project. This is written by a software engineer using a team-approved template and shared in platforms such as Google Docs, to allow for collaboration. The design document is sometimes discussed and debated at team meetings (this differs from team to team), thus acting as a sort of code review before any actual coding.

The design document is where engineers factor in the various facets of design such as security implications, internationalization, storage requirements and privacy converns, and et cetera. These sections are often reviewed by experts in said domains. Google's aim with the design document is to cover the goals of the design, its implementation strategy, and to propose key design decisions coupled with their corresponding trade-offs. Once approved, the design document acts as a record that can be reviewed in the future and as a benchmark in determining whether the project successfully achieved its goals.

### 2.2. Development

The first step in the development stage is the edit-compile-debug loop. After this has been completed by the author engineer, the author sends the code change, commonly called a Changelist (CL for short), in for the pre-submit tests. Pre-submit tests can take several hours in some instances. Thus, to minimize waiting time, teams create a fast subset of tests (often the unit tets for the project) that are run before a change is submitted for code review.

The code review is done by a separate engineer to ensure an improvement in the code health of Google's code base. Google follows a mantra of "continuous improvement", where code changes/CLs are not held to a "perfect" standard, rather reviewers look for whether the CL is better code (i.e. when it improve the overall code health of the system). Several aspects such as design, functionality, complexity, testing, documentation, and so on, are considered during a code review.

Any conflicts on a code review are resolved on a step-by-step basis. The first step is where the author and reviewer try to come to consensus. This is done using guides such as the [code review standard guide](https://google.github.io/eng-practices/review/reviewer/standard.html), the [CL author guide](https://google.github.io/eng-practices/review/developer/), and the [reviewer's guide](https://google.github.io/eng-practices/review/reviewer/).

If the author and reviewer cannot come to consensus, they usually opt for a face-to-face meeting or a video conference, instead of just trying to resolve the issue through code review comments. When this does not resolve the situation, it is often escalated to a broader team discussion, Technical Lead, code maintainer, or an Eng Manager. 

### 2.3. Testing



### 2.4. Deployment

### 2.5. Maintainance

## 3. Human approval gates

## 4. Mechanics inside each stage

## 5. Where AI appears and where it does not

## 6. What the papers say

## 7. Borrow
At least two ideas we should take into our model, each with a reason.

1.
2.

## 8. Reject

## 9. Open questions


