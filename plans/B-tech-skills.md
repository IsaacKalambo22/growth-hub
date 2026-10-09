[Back to ROADMAP](../ROADMAP.md)

# Track B: Tech Skills Plan

**Goal:** Move from strong web developer to well-rounded full-stack/product engineer who can design, secure, ship and scale real systems.

**Starting point (from my portfolio):**
- Advanced: React, Next.js, JavaScript, HTML/CSS
- Intermediate: TypeScript, Node.js, MySQL, MongoDB
- Familiar: Flutter, Docker, AWS, FastAPI

**Principle:** Learn by building. Every skill below is tied to a small project I can push to GitHub.

**Time budget:** about 5-6 hrs/week (1 hr Fri focused study + 2 build sessions + Sat practice). Adjust to what is realistic.

---

## How the 12 months are organized

| Quarter | Theme | Main outcome |
|---|---|---|
| Q1 (Months 1-3) | Strong foundations | Advanced TypeScript, PostgreSQL, API design, testing |
| Q2 (Months 4-6) | Security, payments, DevOps | Secure payment flow, Docker, CI/CD, cloud deploy |
| Q3 (Months 7-9) | Performance, video, mobile | Low-bandwidth app, video streaming, Expo/Flutter app |
| Q4 (Months 10-12) | AI and scale | RAG-based tutor, observability, system design, certification |

---

## Q1: Foundations (Months 1-3)

### 1. Advanced TypeScript (Month 1)
**Learn:** strict mode, generics, utility types, discriminated unions, type narrowing, zod/valibot for runtime validation, shared types between frontend and backend.
**Practice project:** `ts-practice`: rewrite one existing project (e.g. Employee Management) in strict TypeScript with zod-validated API inputs.
**Done when:**
- [ ] Project compiles with `strict: true` and no `any`
- [ ] All API inputs validated with zod
- [ ] Can explain generics and unions without notes

### 2. SQL and PostgreSQL (Months 1-2)
**Learn:** relational design, normalization, joins, indexes, transactions, constraints, migrations, query plans (`EXPLAIN`), an ORM (Prisma or Drizzle).
**Practice project:** `subscription-db`: schema for users, plans, subscriptions, payments, payouts; write reports (monthly revenue per teacher, active subscribers).
**Done when:**
- [ ] Schema designed with foreign keys and indexes
- [ ] Can write joins and aggregates without an ORM
- [ ] Migrations versioned in Git

### 3. Backend architecture and API design (Months 2-3)
**Learn:** REST conventions, pagination, filtering, error formats, auth middleware, rate limiting, service/repository layers, NestJS or well-structured Express, OpenAPI docs.
**Practice project:** `clean-api-starter`: reusable backend template with auth, roles, validation, logging, tests.
**Done when:**
- [ ] OpenAPI/Swagger docs generated
- [ ] Role-based access tested
- [ ] Template reused in the platform

### 4. Testing (Month 3)
**Learn:** unit tests (Vitest/Jest), integration tests with a test database, end-to-end tests (Playwright), test-driven fixes for bugs.
**Done when:**
- [ ] 70%+ coverage on core business logic (payments, access control)
- [ ] One Playwright test: sign up > pay (sandbox) > watch lesson

---

## Q2: Security, payments, DevOps (Months 4-6)

### 5. Application security (Month 4)
**Learn:** OWASP Top 10, password hashing, sessions vs JWT, CSRF/XSS/SQL injection, secure file uploads, secrets management, rate limiting, audit logs, protecting minors' data.
**Practice:** run a security checklist on an existing project and fix findings.
**Done when:**
- [ ] Written security checklist in my repo
- [ ] Dependency scanning enabled (Dependabot)
- [ ] No secrets in Git history

### 6. Payments engineering (Month 5)
**Learn:** payment lifecycle, idempotency keys, webhooks with signature verification, reconciliation, refunds, a ledger-style table, handling duplicate and late callbacks. Use the PayChangu sandbox/docs.
**Practice project:** `paychangu-webhook-example`: a small public repo showing safe payment initiation, webhook handling and verification.
**Done when:**
- [ ] Duplicate webhook does not double-credit
- [ ] Failed/pending payments recover correctly
- [ ] Daily reconciliation script exists

### 7. Docker and CI/CD (Month 5-6)
**Learn:** Dockerfiles, multi-stage builds, docker-compose, GitHub Actions (lint, test, build, deploy), environment management, preview deployments.
**Done when:**
- [ ] App runs locally with one `docker compose up`
- [ ] Every pull request runs tests automatically
- [ ] Merge to main deploys automatically

### 8. Cloud fundamentals (Month 6)
**Learn:** object storage (S3/R2), CDN, managed databases, backups and restores, DNS, SSL, queues, cost monitoring.
**Practice:** deploy a project with a managed database, daily backups, and a tested restore.
**Done when:**
- [ ] Backup restore tested at least once
- [ ] Monthly cost estimate documented

---

## Q3: Performance, video, mobile (Months 7-9)

### 9. Performance for weak networks (Month 7)
**Learn:** Lighthouse, Core Web Vitals, image optimization, code splitting, caching, service workers, PWA install and offline pages, data-saving design.
**Done when:**
- [ ] Main pages load fast on throttled 3G in DevTools
- [ ] PWA installable on Android
- [ ] Data usage per page measured and documented

### 10. Video streaming basics (Month 8)
**Learn:** HLS and adaptive bitrate, encoding, signed/expiring URLs, DRM vs watermarking concepts, cost per GB, managed video providers.
**Practice project:** `low-bandwidth-video-player`: player with quality selector, audio-only mode and resume position.
**Done when:**
- [ ] Upload > encode > stream works end to end
- [ ] Signed URLs expire correctly
- [ ] Estimated cost per student per month calculated

### 11. Mobile development (Months 8-9)
**Choose one:** Expo/React Native (reuses React skills, faster) or Flutter (already familiar, strong UI performance). Do not learn both now.
**Learn:** navigation, state, secure token storage, offline storage (SQLite), background downloads, push notifications, Play Store release process.
**Practice project:** mobile client for one flow: login > browse > download a lesson > watch offline.
**Done when:**
- [ ] App installable via APK/internal testing track
- [ ] Offline playback works

---

## Q4: AI and scale (Months 10-12)

### 12. AI engineering (Month 10-11)
**Learn:** LLM APIs, prompt design, embeddings, vector search, retrieval-augmented generation (RAG), evaluation of answers, guardrails for minors, cost control.
**Practice project:** `curriculum-tutor`: answers questions only from uploaded syllabus notes, cites the source note, refuses off-topic content. Builds on Student Bot.
**Done when:**
- [ ] 30-question evaluation set with measured accuracy
- [ ] Answers always cite a note
- [ ] Per-user usage limits in place

### 13. Observability and system design (Month 11-12)
**Learn:** structured logs, metrics, tracing basics, error tracking (Sentry), uptime alerts, load testing, caching layers, queues, scaling a monolith before microservices.
**Done when:**
- [ ] Alerts fire on errors and downtime
- [ ] Load test of 500 concurrent users documented
- [ ] Architecture diagram and decision records (ADRs) in the repo

### 14. Certification (optional, Month 12)
Pick **one** that fits: AWS Cloud Practitioner, or a PostgreSQL/Cloud associate-level exam. Skip if it takes time from the platform.

---

## Learning resources (free-first)
- MDN Web Docs, TypeScript Handbook, PostgreSQL documentation
- roadmap.sh (backend, DevOps, PostgreSQL roadmaps) for checklists
- freeCodeCamp and CS50 for gaps
- OWASP Cheat Sheet Series
- Docker and GitHub Actions official docs
- Official docs for PayChangu, your video provider, and Expo/Flutter

---

## Monthly review checklist
- [ ] What did I ship?
- [ ] What did I learn that I can explain simply?
- [ ] What repo/commit proves it?
- [ ] What is the next month's one skill focus?
- [ ] Am I building, or only watching tutorials? (Target: 70% building, 30% study)

---

## GitHub plan for this track
- Repo: `learning-log` (public). One folder per skill with notes and small exercises.
- Pin 3-4 repos: `clean-api-starter`, `paychangu-webhook-example`, `low-bandwidth-video-player`, `curriculum-tutor`.
- Every repo needs a README with: what it does, how to run, screenshots/diagram, what I learned.
- Commit at least 4 days per week, even small commits.

### Weekly log template
```
## Week X: YYYY-MM-DD
Skill focus:
Built/committed:
Learned:
Stuck on:
Next week:
```
