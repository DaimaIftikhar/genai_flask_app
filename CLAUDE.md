# Project Agent Rules

## Source of Truth
- GitHub Issues are the source of truth for task scope and acceptance criteria.
- Do not start implementation unless a linked GitHub Issue exists.
- Only work on issues labelled `agent-ready`.

## Safety Boundaries
- Never push directly to main, staging, production, or release branches.
- Never merge a pull request.
- Never deploy an application.
- Never modify production data.
- Never rotate or reveal secrets.
- Never modify infrastructure, billing, domains, cloud credentials, authentication, or permissions unless the issue explicitly requires it and a human has approved it.

## Implementation Rules
- Read the linked GitHub Issue before editing code.
- Keep changes limited to the task scope.
- Reuse existing project patterns and architecture.
- Create one branch for one issue.
- Do not change unrelated files.
- Do not remove existing functionality without explicit approval.
- Add or update tests for changed behavior.

## Verification Rules
- Run relevant unit tests.
- Run linting and formatting checks where configured.
- Run build checks where configured.
- For UI changes, verify the real user flow in the browser when possible.
- Report failed tests honestly.
- Do not claim completion without test evidence.

## Pull Request Rules
Every pull request must include:
- Linked GitHub Issue
- Summary of changes
- Files changed
- Tests run and results
- Manual verification steps
- Known limitations and follow-up work
- Risk notes for migrations, permissions, billing, auth, or infrastructure work
