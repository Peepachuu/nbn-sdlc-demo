# Research slice 2: build modules at operational depth

> Slice 2 of three. Slice 1 (the spine) established the eight stages and tested their colours; this document goes inside the build stages at the depth Alessio asked for on 15 Aug: "how a commit is done, how branches are made, how harnesses are used." It is written as a how-to for the junior layer: each module opens with a plain-English story, then the mechanics, then the human gate and the failure mode. Requirements and module list: `slice2-build-modules-requirements.md`.

> Status: module 1 drafted. Modules 2 to 6 pending. Marked slots exist for Zafir's spike timings and Leon's colour write-up; the document does not wait for them.

Nothing here is invented. Every mechanic is documented practice (cited), observed in the workshop record (D2 v2), demonstrated in our own repository, or practitioner input from Leon Gouletsas (31 Aug meeting, recorded). Where a gate is named, it is also labelled with the mechanism that holds it, using Sidney's D1 capability inventory (`docs/reports/D1-claude-certification.md`, section 3): hook, CI check, or human. Skills, CLAUDE.md and sub-agents shape the work but do not hold a gate.

---

## Module 1: Issue to branch

### The story

A junior developer picks up a card from the board: "add a notes feature." Before any AI touches anything, two artifacts already exist, and they are the whole trick. The issue describes the task with its acceptance criteria written out, and those acceptance criteria also live in the repository as a Markdown file. When the developer (or an agent) starts work, the prompt doesn't paste context in, it points at the file by name: "implement issue #41 against the criteria in `docs/acceptance/notes.md`." The repository is the shared memory, so every person and every agent reads the same brief.

This pattern wasn't handed down from Google. Several teams at the NBN workshop invented it independently on the day, because it routes around the thing that burned every team: chat tools don't share context, Git does (D2 v2, section 7.3).

### The mechanics

Our repository runs the simplest workable version of this, one protected `main`, two branch types (docs/GIT-WORKFLOW.md):

```
git checkout main && git pull
git checkout -b feature/notes        # feature/{kebab-case}; hotfix/* for urgent fixes
# work happens here
git push -u origin feature/notes
gh pr create --base main
```

`main` is protected: no direct pushes, everything through a PR, CI green before merge. Branch names are flags for reviewers, not machinery; `hotfix/` just says "urgent" out loud.

With an agent in the loop, the entry point moves but the shape holds. GitHub's coding agent is assigned the issue itself (set Copilot as assignee); it reads the issue, explores the repo for context, works on its own branch, and opens a draft PR, so "issue to branch" becomes one step, with the branch and PR created for you (docs.github.com). Claude Code does the same from a prompt that names the issue. Either way the issue is the contract: an agent given a vague issue produces a vague branch.

### The human gate

A person decides what becomes an issue and what its acceptance criteria say. That's the whole gate for this module, and it's load-bearing: the spine's Stage 5 verdict (AMBER, confirmed by both source notes) rests on planning staying human-owned while AI fills in scaffolding. Definition of Ready is the checklist form of this gate (Microsoft playbook): a story that hasn't passed it doesn't get a branch.

### The failure mode

Scope creep per branch. Agent-authored PRs bundle multiple purposes at over three times the human rate (40.0% vs 12.2%, Watanabe et al., [arXiv 2509.14745](https://arxiv.org/abs/2509.14745)), and "too large to review" is a leading rejection reason. The fix is enforced at this end, not at review: one issue, one branch, one describable change. If the issue can't be described in one sentence, it's two issues. Google's small-CL rule ("write CLs that are smaller than you think you need") is the same discipline with forty years of scale behind it.

### Colour

Task-level, per Leon's framing (31 Aug): drafting the issue text and acceptance criteria from a feature request is green-to-orange work (generation against known context, human approves). Deciding that the work should happen, and what done means, is red. The branch mechanics are neither, they're deterministic tooling.

Gate mechanism (D1 s3): human. Definition of Ready is a checklist a person walks through, not a hook. Nothing in this module runs deterministically except the branch protection on `main`, which belongs to Module 3.

---

## Module 2: How a commit is done

*(pending; the commit-msg hook in our repo is the worked example of D1's hook row, and the co-author trailer is the smallest available answer to D1's provenance gap, s6)*

## Module 3: How branches become merges

*(pending)*

## Module 4: How harnesses are used

*(pending; backbone is D1 s3: sort each harness into hook, CI check or human before writing its commands, and carry D1's sub-agent finding into the "are the tests correct" section: an agent checking an agent widens coverage but is not an oracle)*

## Module 5: Design-system enforcement in build

*(pending; backbone is Leon's overlay-diff check and design-system-as-constraint, 31 Aug)*

## Module 6: Deploy mechanics

*(pending)*
