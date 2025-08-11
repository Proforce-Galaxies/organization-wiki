# Contribution Guidelines
Please follow these guidelines to maintain consistency across Proforce-Galaxies projects.

## 1️⃣ Code of Conduct
All contributors must follow the **Proforce-Galaxies Code of Conduct** (see [here](organization-wiki/security-policy.md)).

## 2️⃣ Branch Naming Convention
Format:
`<unit>/<feature|bugfix|hotfix>/<short-description>`

Example:
`embedded/feature/motor-driver-integration`


---

## 3️⃣ Commit Message Format
Follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

`type(scope): short description`

Examples:
`feat(firmware): add motor control function`
`fix(api): correct data parsing bug`

---

## 4️⃣ Development Process
1. Fork the repo or create a feature branch from `main`.
2. Make your changes in a dedicated branch and commit.
3. Ensure all tests pass locally.
4. Push the branch and submit a pull request using the PR template.

---

## 5️⃣ Code Standards
- Use the language-specific linting rules.
- Keep functions small and single-purpose.
- Follow our [Git Workflow](../tools-workflow/git-workflow.md).
- Use meaningful commit messages (Conventional Commits).
- Keep PRs focused and under **500 lines changed** when possible.
- Comment complex logic.

---

## 6️⃣ Pull Request Review
- At least 1 Unit Lead must approve before merging.
- Address all review comments and mark conversations resolved.
- No direct merges to `main`.

---

## 7️⃣ Testing
- Add or update unit tests for your changes.
- Ensure all tests pass before requesting a review.

## 8️⃣ Licensing
By contributing, you agree that your contributions are licensed under the same license as the repository.

---

## Workflow
1. Create a feature branch from `main`.
2. Push changes to your branch.
3. Open a Pull Request to `main`.
4. Unit Lead review is required before merging.
5. All review comments must be resolved before merging.

## Reviews
- CODEOWNERS will auto-request reviewers.
- PRs without review will not be accepted.

## Merging
- Only Unit Leads may merge to `main`.
