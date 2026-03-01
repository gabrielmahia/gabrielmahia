# Gabriel Mahia

**Decision infrastructure for under-resourced institutions.**
Kenyan diaspora engineer based in the USA — bridging Western technical patterns with East Africa.

---

## Production platforms

| Repo | What it does |
|------|-------------|
| [catholic-network-tools](https://github.com/gabrielmahia/catholic-network-tools) | Parish stewardship platform — 17 pages, 56 tests, Gemini search grounding, serving the 1.3B Catholic community |
| [openresilience](https://github.com/gabrielmahia/openresilience) | Drought & food stress intelligence for NGOs and farmers — SMS alerts to Kenya's 47 counties |
| [quantum-maestro](https://github.com/gabrielmahia/quantum-maestro) | Macro trading analysis — IWT regime detection, Warsh framework, Kelly position sizing |

---

## East Africa open-source ecosystem

### Payments & fintech infrastructure

| Repo | What it does | Tests |
|------|-------------|-------|
| [mpesa-python](https://github.com/gabrielmahia/mpesa-python) | M-Pesa Daraja v3 SDK — STK Push, B2C, C2B, account balance. Zero external dependencies. | 33 |
| [mpesa-webhooks](https://github.com/gabrielmahia/mpesa-webhooks) | FastAPI handler for Daraja callbacks — idempotent, HMAC-verified, pluggable storage, dead-letter queue | 44 |
| [daraja-mock](https://github.com/gabrielmahia/daraja-mock) | Local test server for Daraja v3 — configurable scenarios (user cancellation, insufficient funds, timeout), no Safaricom account needed | 37 |
| [remit-lens](https://github.com/gabrielmahia/remit-lens) | Diaspora remittance comparison — true cost (fee + spread) across 7 providers, live ECB rates | 19 |

### Chama (rotating credit)

| Repo | What it does | Tests |
|------|-------------|-------|
| [chama-protocol](https://github.com/gabrielmahia/chama-protocol) | Domain library for Kenya's ROSCAs — Chama, Member, Cycle, Contribution, Loan models | 25 |
| [hela](https://github.com/gabrielmahia/hela) | Streamlit chama management app built on chama-protocol | — |

### Reference data

| Repo | What it does | Tests |
|------|-------------|-------|
| [kenya-counties](https://github.com/gabrielmahia/kenya-counties) | All 47 counties — IEBC codes, capitals, regions, 2019 KNBS census. Zero dependencies. | 36 |

### Civic & AI

| Repo | What it does |
|------|-------------|
| [jibu](https://github.com/gabrielmahia/jibu) | AI civic rights assistant for Kenya — labour law, land rights, consumer rights in English and Kiswahili |

### Engineering guides

| Repo | What it covers |
|------|---------------|
| [nairobi-stack](https://github.com/gabrielmahia/nairobi-stack) | M-Pesa integration · SMS infrastructure · Mobile-first UX · Kenya regulatory landscape · Chama digitisation |

---

## How the ecosystem fits together

```
mpesa-python          ← SDK layer (auth, STK Push, B2C, C2B)
    ↑ used by
mpesa-webhooks        ← callback handler (idempotency, dead-letter, HMAC)
daraja-mock           ← test doubles for both of the above

chama-protocol        ← domain library (Chama, Member, Loan, Contribution)
    ↑ used by
hela                  ← Streamlit UI built on chama-protocol

kenya-counties        ← reference data used by openresilience + hela
nairobi-stack         ← guides documenting all of the above
```

---

## Approach

**Opacity reduction at the point of decision.** Every project in this portfolio
surfaces information that was previously inaccessible, expensive, or hidden
to the people who most need it: parish administrators, NGO field officers,
smallholder farmers, diaspora workers sending money home, chama treasurers.

Technical choices follow from users. SMS for farmers without smartphones.
USSD patterns for parish systems in low-connectivity areas. Kiswahili at
every access point. M-Pesa as the payment layer, not an afterthought.

---

## Governance standards

- Licence: CC BY-NC-ND 4.0 (production platforms) · AGPL-3.0 (where noted)
- All systems: DEMO / REAL labelling, no implied institutional partnerships
- Methodology documentation included in every analytical system
- CI/CD: GitHub Actions (lint + test) on every active repository
- Security: HMAC webhook verification, privacy-first data architecture

---

*Open to collaboration on civic tech, humanitarian infrastructure, East African fintech, and institutional decision tools.*
*Contact: contact@aikungfu.dev*
