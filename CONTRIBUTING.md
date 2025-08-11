# Contribution Guidelines
Please follow these guidelines to maintain consistency across Proforce-Galaxies projects.

## 1️⃣ Code of Conduct
All contributors must follow the **Proforce-Galaxies Code of Conduct** (see `organization-wiki/security-policy.md`).

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
1. Fork or branch from `main`.
2. Make your changes in a dedicated branch.
3. Ensure all tests pass locally.
4. Submit a pull request using the PR template.

---

## 5️⃣ Code Style
- Use the language-specific linting rules.
- Keep functions small and single-purpose.
- Comment complex logic.

---

## 6️⃣ Pull Request Review
- At least 1 Unit Lead must approve.
- Resolve all review comments before merging.
- No direct merges to `main`.

---

## 7️⃣ Licensing
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
