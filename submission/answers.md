# SDT316 Week 4 — Git Assignment

## Task 1 — Merge Conflict

The merge commit `1381bfb` has two parents: one from main and one from feature-merge. The graph shows the history forking into two paths and rejoining at the merge commit.

## Task 2 — Rebase

1. The SHA changed from `c8cc59b` to `3fbd788` because rebase recreated the commit with a different parent, even though its file contents stayed unchanged.

2. GitHub rejected the normal push because the rebased branch had rewritten history, so the update was not a fast-forward.

3. Task 1 has a branching history with a two-parent merge commit, while Task 2 has a linear history after rebase and fast-forward.

4. Rebasing a branch that teammates have already pulled is risky because their local history will diverge from the rewritten remote history.

## Task 3 — Commit History and Pull Request

### Merge strategies

- Create a merge commit: Preserves all three commits and adds a merge commit with two parents, as demonstrated in Task 1.
- Squash and merge: Combines the three commits into one new commit on main, losing their individual history.
- Rebase and merge: Replays the commits onto main to produce a linear history, similar to Task 2.

Squash and merge would destroy the three separate commits because it combines their changes into a single commit.

### Why keep three commits?

The "typo" and "oops forgot a setting" commits were corrections to previous changes, so they were folded into their corresponding commits using fixup. The remaining three commits represent independent, meaningful changes to notes, configuration, and usage documentation.

## Pull Request

PR #1: Add project notes, config and usage.

The pull request was merged using "Create a merge commit", preserving all three curated commits on main.
