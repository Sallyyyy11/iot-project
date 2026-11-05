# Contribution workflow

1. Every member uses their **own GitHub account** and makes attributable commits.
2. Create a branch for each change: `feat/member-1-sensor`, `feat/member-2-coreiot`, `docs/member-3-tests` (edit naming to fit final roles).
3. Prefer a pull request reviewed by one other teammate before merging to `main`.
4. Reference feature IDs (`F01`) and grading codes (`T06`) in your pull request if applicable.
5. Include evidence: screenshots/log snippets in `docs/evidence/`, measurement rows in `docs/testing/`, and report notes in the PR description.
6. Never add real tokens, Wi-Fi credentials, or secrets. Use `.env.example` and `config.example.h`.
7. Before merging: make sure no placeholder code is represented as working and update the README to match real behavior.

Suggested commit format: `feat(firmware): add sensor sampling for F01 (Txx)`; `docs(test): record F01 latency results`.

Members should agree on a weekly lab checklist before using the limited board access.
