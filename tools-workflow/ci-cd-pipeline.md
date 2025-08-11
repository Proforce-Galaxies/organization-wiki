# CI/CD Pipeline Standards

---

## 1️⃣ Overview
We use GitHub Actions (or alternative CI service) for:
- Build automation
- Test execution
- Deployment

---

## 2️⃣ Pipeline Stages
1. **Build** → Compile code and check dependencies.
2. **Test** → Run unit, integration, and E2E tests.
3. **Lint** → Enforce code style.
4. **Deploy** → Push artifacts to staging/production.

---

## 3️⃣ Rules
- All PRs must pass pipeline checks before merging.
- Failed builds block merges.
- Secrets managed via GitHub Secrets (never in code).

---

## 4️⃣ Example Actions Workflow
name: CI

on: [push, pull_request]

jobs:

build:

runs-on: ubuntu-latest

steps:
- uses: actions/checkout@v3
- name: Set up Node.js

uses: actions/setup-node@v3

with:
node-version: 18
- run: npm install
- run: npm test
