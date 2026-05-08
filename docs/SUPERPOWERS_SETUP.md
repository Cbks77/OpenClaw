# 🦸 Superpowers — OpenClaw Integration

**Status:** ✅ **INSTALLED & ACTIVE**

Superpowers is a complete software development methodology framework for AI coding agents.

---

## 📦 What's Installed

✅ **Superpowers skills** copied to: `~/.openclaw/plugin-skills/superpowers/`  
✅ **Source repo** added as git submodule: `~/OpenClaw/superpowers/`  
✅ **14 skills** ready to use

---

## 🛠️ Available Skills

### Core Development Workflow

1. **brainstorming** — Refines rough ideas through Socratic questions, explores alternatives, presents design in digestible chunks
2. **writing-plans** — Breaks work into 2-5 minute tasks with exact file paths, complete code, verification steps
3. **executing-plans** — Batch execution with human checkpoints
4. **subagent-driven-development** — Fast iteration with two-stage review (spec compliance, then code quality)
5. **using-git-worktrees** — Creates isolated workspace on new branch for parallel development
6. **finishing-a-development-branch** — Verifies tests, presents merge/PR options, cleans up worktree

### Testing & Debugging

7. **test-driven-development** — Enforces RED-GREEN-REFACTOR: write failing test, watch it fail, write minimal code, watch it pass
8. **systematic-debugging** — 4-phase root cause process with defense-in-depth techniques
9. **verification-before-completion** — Ensures fixes actually work before declaring success

### Collaboration & Review

10. **requesting-code-review** — Pre-review checklist, reviews against plan
11. **receiving-code-review** — Responding to feedback systematically
12. **dispatching-parallel-agents** — Concurrent subagent workflows

### Meta Skills

13. **using-superpowers** — Introduction to the skills system (auto-loaded at session start)
14. **writing-skills** — Create new skills following best practices

---

## 🎯 Philosophy

Superpowers enforces these principles:

- **Test-Driven Development** — Write tests first, always
- **Systematic over ad-hoc** — Process over guessing
- **Complexity reduction** — Simplicity as primary goal
- **Evidence over claims** — Verify before declaring success

---

## 🔄 Core Workflow

When you start a development task, Superpowers guides you through:

1. **Brainstorm** → Agent asks clarifying questions, refines spec
2. **Design** → Present design in chunks for validation
3. **Git Worktree** → Create isolated workspace on new branch
4. **Plan** → Break work into 2-5 minute tasks
5. **Execute** → TDD cycle (RED-GREEN-REFACTOR) for each task
6. **Review** → Code review against plan
7. **Finish** → Verify tests, merge/PR, cleanup

---

## 🚀 How to Use in OpenClaw

Skills are **auto-discovered** by OpenClaw from `~/.openclaw/plugin-skills/superpowers/`.

### Triggering Skills

OpenClaw will automatically suggest relevant skills when:
- You start a development task
- You're about to write code
- You're debugging an issue
- You're reviewing code

You can also explicitly invoke skills by mentioning them:
```
"Use the brainstorming skill to design this feature"
"Apply test-driven-development for this component"
"Help me debug this systematically"
```

---

## 📖 Skill Descriptions

### brainstorming
**When:** Starting any new feature or project  
**What:** Asks clarifying questions, refines requirements, explores alternatives, presents design in sections  
**Output:** Saves design document

### writing-plans
**When:** After design is approved  
**What:** Breaks work into bite-sized tasks (2-5 minutes each) with exact file paths, complete code, verification steps  
**Output:** Detailed implementation plan

### test-driven-development
**When:** During implementation  
**What:** Enforces RED-GREEN-REFACTOR cycle:
1. Write failing test
2. Watch it fail
3. Write minimal code to pass
4. Watch it pass
5. Refactor
6. Commit

**Anti-pattern:** Deletes code written before tests

### subagent-driven-development
**When:** Executing a plan with multiple tasks  
**What:** Dispatches fresh subagent per task with two-stage review:
1. **Spec compliance** — Does it do what the plan asked?
2. **Code quality** — Is it well-written, tested, maintainable?

**Output:** Fast iteration without human bottleneck for small tasks

### systematic-debugging
**When:** Diagnosing bugs or unexpected behavior  
**What:** 4-phase root cause process:
1. **Reproduce** — Reliable repro steps
2. **Isolate** — Narrow down the failure point
3. **Trace** — Root cause analysis
4. **Fix** — Defense-in-depth solution

**Includes:** Root-cause-tracing, condition-based-waiting techniques

### using-git-worktrees
**When:** Starting work on a new feature branch  
**What:** Creates isolated workspace on new branch, runs project setup, verifies clean test baseline  
**Why:** Allows parallel development without switching branches

### finishing-a-development-branch
**When:** All tasks in a branch are complete  
**What:** Verifies tests, presents options (merge/PR/keep/discard), cleans up worktree  
**Output:** Clean integration back to main

### requesting-code-review
**When:** Between tasks or at branch completion  
**What:** Reviews code against plan, reports issues by severity (critical/major/minor)  
**Rule:** Critical issues block progress

### receiving-code-review
**When:** You receive feedback from a reviewer  
**What:** Systematic process for responding to feedback, prioritizing fixes, updating plan

### dispatching-parallel-agents
**When:** Plan has independent tasks that can run concurrently  
**What:** Spawns multiple subagents to work in parallel  
**Benefit:** Faster completion for large plans

### verification-before-completion
**When:** After fixing a bug or completing a task  
**What:** Ensures the fix actually works before declaring success  
**Includes:** Test runs, manual verification, edge case checks

### writing-skills
**When:** You need to create a new skill for a recurring pattern  
**What:** Complete guide for creating skills following Superpowers best practices  
**Includes:** Testing methodology, eval procedures

---

## 🔗 Key Resources

- **Source repo:** https://github.com/obra/superpowers
- **OpenClaw integration:** `~/OpenClaw/superpowers/`
- **Skills directory:** `~/.openclaw/plugin-skills/superpowers/`
- **Release notes:** https://github.com/obra/superpowers/blob/main/RELEASE-NOTES.md
- **Discord community:** https://discord.gg/35wsABTejz

---

## ⚠️ Important Notes

### Red Flags (Rationalization Patterns)

If you catch yourself thinking:
- "This is just a simple question" → Questions are tasks. Check for skills.
- "I need more context first" → Skill check comes BEFORE clarifying questions.
- "Let me explore the codebase first" → Skills tell you HOW to explore.
- "This doesn't need a formal skill" → If a skill exists, use it.
- "I'll just do this one thing first" → Check BEFORE doing anything.

**→ STOP. You're rationalizing. Invoke the skill.**

### Skill Priority

The rule: **If there's even a 1% chance a skill might apply, invoke it.**

Skills override default system behavior but **user instructions always take precedence**:
1. User's explicit instructions (highest priority)
2. Superpowers skills
3. Default system prompt (lowest priority)

---

## 🚀 Quick Start

Try this in your next development session:

```
"Let's build a React todo list"
```

If Superpowers is working, the **brainstorming** skill should auto-trigger and start asking clarifying questions before writing any code.

---

**You're now charged up with Superpowers!** 🦸🔥

Every coding session now follows a systematic, test-driven, evidence-based methodology.
