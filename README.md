# .github

Organization-level defaults for [evolution-gaming](https://github.com/evolution-gaming). Files here
apply to every repository in the organization that does not define its own.

## Contents

| File | Purpose |
| --- | --- |
| [AI_POLICY.md](AI_POLICY.md) | AI Contribution Policy — AI may assist, a human owns every commit. |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Default contributing guide, shown when opening issues and pull requests. |
| [.github/workflows/human-commit-ownership.yml](.github/workflows/human-commit-ownership.yml) | "AI Policy Check" — fails a pull request whose commits list an AI tool as author or co-author. |
| [workflow-templates/](workflow-templates) | Starter workflows offered when adding a workflow to a repository. |

GitHub picks up `CONTRIBUTING.md` automatically for repositories without their own copy. Workflows are
not inherited: copy `human-commit-ownership.yml` into a repository to enable the check there.

## Starter workflows for Scala projects

`workflow-templates/` adds **Scala CI** and **Scala Release** to the "New workflow" picker for any
repository in the organization with a `build.sbt`. Both are thin callers of the shared workflows in
[scala-github-actions](https://github.com/evolution-gaming/scala-github-actions), which is where the
inputs and behaviour are documented.

These are offered, not enforced — a new repository can still skip them. To guarantee CI on every
repository, add the shared workflow to an organization ruleset the way the AI Policy Check does.

## Enabling the AI Policy Check

1. Copy `.github/workflows/human-commit-ownership.yml` into the target repository.
2. Mark **AI Policy Check** as a required status check in branch protection or a ruleset.

Contributors who hit the check should drop the offending trailer (`git rebase -i` or
`git commit --amend`) and force-push.

## Changes

Open a pull request. Policy changes affect every repository in the organization, so keep them small and
explain the reasoning.
