# AI Contribution Policy

AI tools may assist with development, but a human author takes responsibility for every commit.
The "No AI authors or co-authors" check enforces the first rule on all pull requests.

* Never add a co-author trailer for AI tools in commit messages.
* Avoid generating PR titles or descriptions with AI. If you do, keep them concise; humans read them.
* Keep PR discussion AI-free where you can. If you must paste LLM output into a comment or forward a
  reviewer's question to an LLM, understand the context yourself first and keep it short.
* A chain of small PRs always beats one huge slop PR. Maintainers may close slop PRs with a brief reason, and
  repeat offenders can be blocked.
* Full responsibility regardless of tooling. The author owns every line, comment, test and decision, whether
  hand-written or generated.
* Test locally before submitting. Generated code must compile and be covered by automated tests; if test
  automation is not feasible, explain why in the PR.
* Do not open a PR you will not see through review. No drive-by generated PRs abandoned mid-review.
* Optionally attach prompt history for heavily LLM-assisted contributions.
