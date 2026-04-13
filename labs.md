# ✅ GH‑900 Labs – Day 1

| Module | Exercise Name | Link |
| --- | --- | --- |
| Introduction to GitHub | A guided tour of GitHub | [Introduction to GitHub](https://github.com/skills/introduction-to-github) |
| Communicate effectively on GitHub using Markdown | Communicate using Markdown | [Communicate using Markdown](https://github.com/skills/communicate-using-markdown) |
| Contribute to an open-source project on GitHub | Create your first pull request | [Create your first PR](https://learn.microsoft.com/en-us/training/modules/contribute-open-source/4-exercise-create-pr/?ns-enrollment-type=learningpath&ns-enrollment-id=learn.github-foundations) |
| Manage repository changes by using pull requests on GitHub | Reviewing pull requests | [Review Pull Requests](https://github.com/skills/review-pull-requests) |

---

```mermaid
flowchart TD
A[Create branch & make changes] --> B[Push branch]
B --> C[Open Pull Request]
C --> D[Review]
D --> E{Decision}
E -->|Comment| D
E -->|Request changes| F[Update code]
F --> B
E -->|Approve| G[Merge]
G --> H["Delete branch (optional)"]
```
