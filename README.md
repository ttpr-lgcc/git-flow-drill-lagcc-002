---
languages: git
tags: git-flow, branching, commits, practice
resources: 2
---

# Git Flow Drill

![Git workflow illustration](https://git-scm.com/images/branching-illustration@2x.png)

## Background

Git is not something you "learn" the way you learn a theorem. You learn it the way you learn to tie your shoes — by doing the motion until you stop watching your hands. This drill has you run the full Git workflow **ten times** on ten deliberately tiny tasks. The content of each task doesn't matter; the **process** is the point.

Companion handbook page: [Module 1 — Program Setup, Git & GitHub](https://lgcc.github.io/modules/01-setup).

## Objectives

By the end of this exercise you will be able to run this loop without looking up any commands:

```
status → branch → edit → status → add → commit → push
```

## Instructions

### Setup (one time)

```bash
# clone the lab repo
git clone git@github.com:ttpr-lgcc/git-flow-drill-lagcc-002.git
cd git-flow-drill-lagcc-002

# create a branch named after your GitHub username — this is your "workspace" for the drill
git checkout -b <your-username>

# push the branch to the remote so it exists on GitHub
git push -u origin <your-username>
```

All ten tasks happen on **your personal branch**. You'll commit ten separate times — once per task — so the instructor can see each rep as its own commit.

### Per-task loop (run this ten times)

For each task `<NN>` from 01 to 10:

1. **Read the task** in [`tasks/<NN>.md`](./tasks/).
2. **Create the file** `submissions/<your-username>/task-<NN>.md` with the content the task asks for.
3. **Check what changed:**
   ```bash
   git status
   ```
   Exactly one new file should appear. If something unexpected shows up, stop and figure out why.
4. **Stage only the file you just created:**
   ```bash
   git add submissions/<your-username>/task-<NN>.md
   ```
5. **Commit with a message that describes the task:**
   ```bash
   git commit -m "feat(task-<NN>): <one-line description of what you did>"
   ```
   Example: `git commit -m "feat(task-01): add my name to the cohort list"`
6. **Push:**
   ```bash
   git push
   ```

Then move on to task `<NN+1>`. All ten commits land on your branch; you do **not** go back to `main` between tasks.

## The tasks

| # | What you're doing | Commit type |
|---|---|---|
| [01](./tasks/01.md) | Add your name to a cohort list | `feat` |
| [02](./tasks/02.md) | Fix three typos in a sentence | `fix` |
| [03](./tasks/03.md) | Name your favorite programming language | `feat` |
| [04](./tasks/04.md) | Answer a one-line question | `feat` |
| [05](./tasks/05.md) | Add an emoji to a line | `feat` |
| [06](./tasks/06.md) | Rename a placeholder | `refactor` |
| [07](./tasks/07.md) | Add a bullet to a list | `feat` |
| [08](./tasks/08.md) | Write a one-sentence bio | `feat` |
| [09](./tasks/09.md) | Add a useful resource link | `docs` |
| [10](./tasks/10.md) | Document one thing you learned | `docs` |

## On pace

- First three tasks may each take 10–15 minutes. Normal.
- By task 7, each rep should take under 3 minutes.
- If task 10 still feels slow, you haven't drilled enough — ask the instructor for 2–3 more bonus tasks and repeat.

## Reflection (required)

Before you call this exercise done, add one final file `submissions/<your-username>/reflection.md` answering:

1. Which task was hardest and why?
2. What part of the loop feels automatic now?
3. What part do you still have to think about?

Commit it as:

```bash
git commit -m "docs: add git-flow-drill reflection"
git push
```

## Checklist

- [ ] My branch `<my-username>` exists on the remote
- [ ] Ten task files plus one reflection file live in `submissions/<my-username>/`
- [ ] There are ten commits plus one reflection commit on my branch (check with `git log --oneline`)
- [ ] Each commit message describes the task (not `update` or `done`)
- [ ] I can run `status → branch → add → commit → push` without looking up commands

## Resources

- [Pro Git Book](https://git-scm.com/book/en/v2) — chapters 2 and 3 cover everything in this drill
- [Oh Shit, Git!?!](https://ohshitgit.com/) — how to undo common mistakes
