# DevOps AI — Production-Grade SaaS for AI-Powered Error Analysis

> **For sale: $5,000 — one-time payment, full source code transfer.**
> Contact: **gabrielbenez09@gmail.com**

A complete, multi-tenant SaaS platform that detects errors, analyzes root causes, and generates fixes automatically — built on a modern **Rust + Python + React** stack.

**524 tests passing** · **Multi-tenant** · **Stripe billing** · **LGPD/GDPR** · **2FA TOTP** · **Docker-ready**

---

## Why Buy This

Building a production-ready SaaS from scratch takes **6+ months** of senior engineering work (~340 hours, ~$25,000+ at market rate).

This codebase is **done** — security-hardened, fully tested, documented, and ready to deploy.

| Build it yourself | Hire an agency | **Buy this** |
|---|---|---|
| 6 months | $25,000+ | **$5,000 once** |
| Risk of bugs | Risk of delays | Battle-tested |
| No 2FA / billing | Extra cost | All included |

---

## What's Included

### 🦀 Rust Backend (Axum)
- 114 unit tests + 83 integration tests (197 total)
- JWT + API key auth, **TOTP 2FA with replay protection**
- **Argon2id** password hashing with timing-equalization
- Multi-tenant with **`pg_advisory_lock`** safety
- Stripe billing (webhooks, subscriptions, portal)
- Request ID middleware for cross-service log correlation
- Graceful shutdown with 35s drain timeout

### 🐍 Python Engine (FastAPI)
- 327 tests across 30 modules
- **88 error patterns** across 13 categories
- **Stack trace parser for 8 languages** (Java, Python, JS, Go, C#, Ruby, PHP, Rust)
- Thompson Sampling for learning from feedback
- Optional Claude / Gemini LLM integration
- In-process rate limiter (120 req/min/IP)

### ⚛️ React + TypeScript Frontend
- Exponential-backoff retry on transient 5xx errors
- Type guards for JSONB data shapes
- Token refresh on 401 with automatic retry

### 🗄️ PostgreSQL Schema
- **12 versioned migrations** (001..012)
- Migration runner with gap detection
- `pg_trgm` for similarity search
- Full tenant isolation

### 🔐 Security Hardening (production-grade)
- HSTS + Content-Security-Policy + X-Frame-Options
- Sanitized error responses (no SQL/internal leaks)
- TOTP replay protection (30s window)
- JWT `token_version` for mid-TTL revocation
- Constant-time webhook signature verification
- Constant-time `forgot_password` / `resend_verification`
- Argon2 dummy hash on login miss
- Production startup panics on insecure defaults

### 📊 Observability
- Prometheus + Grafana (pre-provisioned dashboards)
- Loki + Promtail for log aggregation
- Sentry integration (Rust + Python)
- Alertmanager with Slack/email routes

### 🇪🇺 Compliance
- LGPD/GDPR data export endpoint
- Account deletion endpoint
- Documented disclosure policy (SECURITY.md)

### 🐳 Infrastructure
- Docker Compose stack (11 services)
- Multi-stage Rust + Python Dockerfiles
- Nginx reverse proxy + Let's Encrypt certbot
- CI/CD with `cargo clippy -D warnings` (zero warnings)

### 📚 Knowledge Base Scraper (Bonus)
- GitHub Issues scraper → AI Structurer → PostgreSQL
- 73 tests
- Comes with **9 training datasets / 450 example errors**

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend API | Rust 2021 + Axum 0.7 + sqlx 0.7 |
| Engine | Python 3.12+ + FastAPI 0.115 + asyncpg |
| Frontend | React + TypeScript + Vite |
| Database | PostgreSQL 16 + Redis (optional) |
| Auth | JWT (HS256) + API keys + TOTP 2FA |
| Billing | Stripe (webhooks + customer portal) |
| Monitoring | Prometheus + Grafana + Loki + Sentry |
| Container | Docker + Docker Compose |

---

## Architecture

```
                 ┌─────────────┐
   Internet ───▶ │   Nginx     │ ── TLS termination, reverse proxy
                 └──────┬──────┘
                        │
            ┌───────────┴───────────┐
            ▼                       ▼
     ┌──────────────┐       ┌──────────────┐
     │ Rust Backend │ ◀───▶ │ Python Engine│
     │  (Axum)      │       │  (FastAPI)   │
     └──────┬───────┘       └──────────────┘
            │
            ▼
     ┌──────────────┐       ┌──────────────┐
     │  PostgreSQL  │       │    Redis     │
     │ (multi-tenant│       │ (rate-limit) │
     │  schema)     │       └──────────────┘
     └──────────────┘
```

---

## What You Get (after purchase)

✅ Full source code (private GitHub repo transfer)
✅ All 524 passing tests
✅ Production Docker Compose stack
✅ Documentation: README, SECURITY.md, CHANGELOG.md, CONTRIBUTING.md
✅ 9 training datasets (450 example errors)
✅ Commercial perpetual license (modify, deploy, monetize — no royalties)
✅ **30 days of email support** for setup questions

---

## What's NOT Included

- Hosted infrastructure (you deploy on your own AWS/GCP/Hetzner)
- API keys (Anthropic, GitHub, Stripe — bring your own)
- Domain / TLS certs
- Ongoing maintenance after 30-day support window

---

## Demo & Verification

Before purchase, available on request:
- 📹 Live walkthrough video (Discord/Google Meet, 30 min)
- 🔍 Read-only access to private repo (under NDA)
- 📊 Test results screenshot (`cargo test` + `pytest`)
- 🐳 Live demo instance for evaluation

---

## Why $5,000

| Item | Estimated value |
|---|---|
| Auth + 2FA + TOTP (40h) | $1,200 |
| Stripe billing (30h) | $900 |
| Multi-tenancy (30h) | $900 |
| LGPD/GDPR endpoints (15h) | $450 |
| Observability stack (25h) | $750 |
| Tests — 524 of them (80h) | $2,400 |
| Docker + CI infra (20h) | $600 |
| Knowledge base scraper (40h) | $1,200 |
| Engine + parsers (60h) | $1,800 |
| **Subtotal at $30/h (Brazil rate)** | **$10,200** |
| **Subtotal at $80/h (US junior senior rate)** | **$27,200** |
| **Your price** | **$5,000** |

**You're paying ~50% off the lowest reasonable cost** — that's the deal.

---

## Payment

- **$5,000 USD** via **Escrow.com** (buyer pays ~2.5% escrow fee)
- After funds release: GitHub private repo transferred to buyer's account
- 30-day email support starts on transfer date

---

## FAQ

**Q: Can I resell the code?**
A: No — single-buyer commercial license. You can deploy, modify, and run SaaS commercially with it.

**Q: Is it open-source?**
A: No. The public README you're reading is for demonstration. The actual code is under a commercial license.

**Q: Why are you selling?**
A: Built it as a portfolio-grade project. I'm focusing on other ventures and prefer one-time sale over running it as a SaaS.

**Q: Is the code maintained?**
A: It's stable and tested. After purchase, maintenance is the buyer's responsibility (30-day setup support included).

**Q: What language is the documentation in?**
A: English. Some internal comments are in Portuguese (original author is Brazilian) — fully readable but not a blocker.

**Q: Can I negotiate?**
A: Serious offers $4,500+ considered.

---

## Contact

📧 **gabrielbenez09@gmail.com**

Reply within 24h on weekdays. Mention "DevOps AI" in subject line.

---

## License

See [LICENSE.md](LICENSE.md). All rights reserved — source available for evaluation only.

---

*Built with Rust 🦀, Python 🐍, and engineering rigor.*
