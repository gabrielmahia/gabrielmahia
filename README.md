# Gabriel Mahia

**Decision infrastructure for under-resourced institutions.**
Kenyan diaspora engineer, USA — bridging Western technical patterns with East Africa.

---

## Production platforms

| Repo | What it does |
|------|-------------|
| [catholic-network-tools](https://github.com/gabrielmahia/catholic-network-tools) | Parish stewardship — 17 pages, 56 tests, Gemini search grounding |
| [openresilience](https://github.com/gabrielmahia/openresilience) | Drought & food stress intelligence — SMS alerts to Kenya's 47 counties |
| [quantum-maestro](https://github.com/gabrielmahia/quantum-maestro) | Macro trading analysis — IWT regime detection, Warsh framework, Kelly sizing |

---

## East Africa open-source ecosystem

### Payments infrastructure

| Repo | Layer | Tests |
|------|-------|-------|
| [mpesa-python](https://github.com/gabrielmahia/mpesa-python) | SDK — STK Push, B2C, C2B, zero deps | 33 |
| [mpesa-webhooks](https://github.com/gabrielmahia/mpesa-webhooks) | FastAPI callback handler — idempotent, HMAC-verified, dead-letter | 44 |
| [daraja-mock](https://github.com/gabrielmahia/daraja-mock) | Test server — configurable scenarios, no Safaricom account needed | 37 |
| [pesa-cli](https://github.com/gabrielmahia/pesa-cli) | CLI — STK Push, B2C, balance, config management | 34 |
| [remit-lens](https://github.com/gabrielmahia/remit-lens) | Diaspora remittance comparison — true cost across 7 providers | 19 |

### Chama (rotating credit)

| Repo | Layer | Tests |
|------|-------|-------|
| [chama-protocol](https://github.com/gabrielmahia/chama-protocol) | Domain library — Chama, Member, Cycle, Contribution, Loan | 25 |
| [chama-api](https://github.com/gabrielmahia/chama-api) | REST service — CRUD, idempotency, pagination, OpenAPI | 36 |
| [hela](https://github.com/gabrielmahia/hela) | Streamlit UI — built on chama-protocol | — |

### Communications

| Repo | Layer | Tests |
|------|-------|-------|
| [kenya-sms](https://github.com/gabrielmahia/kenya-sms) | Africa's Talking wrapper — bilingual EN/SW templates, delivery tracking | 43 |

### Reference data

| Repo | What it provides | Tests |
|------|-----------------|-------|
| [kenya-counties](https://github.com/gabrielmahia/kenya-counties) | 47 counties — IEBC codes, capitals, regions, 2019 KNBS census | 36 |

### Civic & AI

| Repo | What it does |
|------|-------------|
| [floodwatch-kenya](https://github.com/gabrielmahia/floodwatch-kenya) | Urban flood resilience — incident tracking, policy accountability, 5 Kenya cities |
| [jibu](https://github.com/gabrielmahia/jibu) | Civic rights AI — labour law, land rights, consumer rights in EN + Kiswahili |

### Engineering guides

| Repo | Covers |
|------|--------|
| [nairobi-stack](https://github.com/gabrielmahia/nairobi-stack) | M-Pesa · SMS · Mobile-first UX · Regulatory · Chama patterns |

---

## Ecosystem map

```
kenya-counties ─────────────────────────────────┐
                                                 │
mpesa-python          ← SDK (auth, STK, B2C)    │
    ├── mpesa-webhooks ← callback handler        ├─→ openresilience
    ├── daraja-mock    ← test doubles            │       ↑
    └── pesa-cli       ← CLI                     │    kenya-sms
                                                 │
chama-protocol ← domain library                  │
    ├── chama-api      ← REST service            │
    └── hela           ← Streamlit UI ───────────┘

kenya-sms ← bilingual SMS layer (used by openresilience, hela)
nairobi-stack ← guides documenting all of the above
```

---

## Approach

**Opacity reduction at the point of decision.** Every project surfaces information
previously inaccessible to the people who most need it: parish administrators,
NGO field officers, smallholder farmers, diaspora workers, chama treasurers.

Technical choices follow from users — SMS for farmers without smartphones,
USSD patterns for low-connectivity areas, Kiswahili at every access point,
M-Pesa as the payment layer not an afterthought.

---

## Governance

- License: CC BY-NC-ND 4.0 (all repos)
- DEMO / REAL labelling on every analytical system
- CI/CD: GitHub Actions (lint + test) on every repository
- Security: HMAC webhook verification, 600-mode credentials, privacy-first architecture

---

*Open to collaboration on civic tech, humanitarian infrastructure, East African fintech, and institutional decision tools.*
*contact@aikungfu.dev*
