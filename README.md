# Gabriel Mahia

**Decision infrastructure for under-resourced institutions.**
Kenyan diaspora engineer based in the USA — building systems that reduce opacity at the point of decision,
borrowing patterns from the West and localising them for East Africa.

---

## Production platforms

| Repo | What it does |
|------|-------------|
| [catholic-network-tools](https://github.com/gabrielmahia/catholic-network-tools) | Parish management and stewardship platform. 17 pages, 56 tests, Gemini search grounding. Live. |
| [openresilience](https://github.com/gabrielmahia/openresilience) | Drought and food stress intelligence for NGOs and farmers across Kenya's 47 counties. SMS alerts via Africa's Talking. |
| [quantum-maestro](https://github.com/gabrielmahia/quantum-maestro) | Macro trading analysis — IWT regime detection, Warsh framework, Kelly sizing. |

---

## East Africa fintech — open-source toolkit

### Application layer
| Repo | What it does |
|------|-------------|
| [hela](https://github.com/gabrielmahia/hela) | Streamlit chama management app — contributions, loans, fines, cycle dashboard. |
| [remit-lens](https://github.com/gabrielmahia/remit-lens) | True cost comparison for diaspora remittances to Kenya. 7 providers, live ECB rates, hidden spread surfaced. |
| [jibu](https://github.com/gabrielmahia/jibu) | AI civic rights assistant for Kenya — labour law, land rights, government services. Kiswahili + English. |

### Libraries and SDKs
| Repo | What it does |
|------|-------------|
| [mpesa-python](https://github.com/gabrielmahia/mpesa-python) | M-Pesa Daraja v3 SDK — STK Push, B2C, C2B, account balance. Zero dependencies. 33 tests. |
| [chama-protocol](https://github.com/gabrielmahia/chama-protocol) | Domain model for Kenya's rotating credit associations — Chama, Member, Cycle, Contribution, Loan. |
| [mpesa-webhooks](https://github.com/gabrielmahia/mpesa-webhooks) | Production FastAPI handler for Daraja callbacks — idempotent, dead-letter queue, pluggable storage. 42 tests. |

### Test infrastructure
| Repo | What it does |
|------|-------------|
| [daraja-mock](https://github.com/gabrielmahia/daraja-mock) | Local test server for the Daraja v3 API. Configurable failure scenarios. Zero dependencies. 32 tests. |

### Reference data
| Repo | What it does |
|------|-------------|
| [kenya-counties](https://github.com/gabrielmahia/kenya-counties) | Kenya's 47 counties — codes, capitals, regions, 2019 census population, area. Zero dependencies. 36 tests. |

### Documentation
| Repo | What it does |
|------|-------------|
| [nairobi-stack](https://github.com/gabrielmahia/nairobi-stack) | Engineering guide for building in East Africa — M-Pesa, SMS, mobile UX, regulatory landscape, chama domain. |

---

## How the toolkit fits together

```
mpesa-python          ← STK Push, B2C, C2B, account balance
    └── mpesa-webhooks    ← handles the callbacks (idempotent, DLQ)
    └── daraja-mock       ← test companion (zero Safaricom account needed)

chama-protocol        ← domain model (Chama, Member, Cycle, Contribution, Loan)
    └── hela              ← Streamlit UI on top of chama-protocol

kenya-counties        ← reference data used by openresilience + hela
nairobi-stack         ← documentation: M-Pesa, SMS, UX, regulatory, chama
```

---

## Approach

Every project here is organised around one question:
**what does this person need to decide, and what data are they missing?**

For a parish treasurer that is contribution history and member stewardship trends.
For an NGO field officer in drought response it is rainfall, NDVI, and water stress by county.
For a diaspora engineer integrating payments it is a test server that behaves like Safaricom without requiring Safaricom.

The answer in each case is the same: reduce the information asymmetry, preserve privacy, and build within the institutional trust networks that already exist.

---

## Standards

- **Licensing:** CC BY-NC-ND 4.0 across all open-source repos
- **Trust integrity:** DEMO data clearly labelled, no simulated data presented as real
- **CI:** lint + test on every push across Python 3.10 / 3.11 / 3.12
- **Security:** responsible disclosure at contact@aikungfu.dev

---

*Open to collaboration on civic tech, humanitarian infrastructure, African fintech, and institutional decision tools.*
*Email: contact@aikungfu.dev*
