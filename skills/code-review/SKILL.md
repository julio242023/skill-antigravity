---
name: "code-review"
description: "AI code review and quality audit skill. Reviews code for security, modularity, performance, GCP production readiness, and adherence to clean architecture principles."
version: 1.0.0
---

# Code Review Skill

Conduct thorough, systematic code reviews on pull requests, feature branches, and refactored components.

## Checklist
1. **Security & OWASP:** Input validation (Zod), CSP headers, SQL/XSS injection prevention, RBAC access control.
2. **Architecture & Modularity:** Clean separation of routes, controllers, services, and domain models.
3. **Performance & Observability:** Structured JSON logging (GCP Cloud Logging), async/await error handling, memory efficiency.
4. **Code Quality:** Strong TypeScript typing, zero hardcoded magic strings, clean variable names, unit test coverage.
