# Gabriel Mahia

**Decision infrastructure for under-resourced institutions.**  
Kenyan diaspora engineer, USA — bridging Western technical patterns with East Africa.

---

## Production platforms

| Platform | What it does | Live |
|---|---|---|
| [Jumuia](https://github.com/gabrielmahia/catholic-network-tools) | Parish stewardship — church finder, giving, AI assistant, accountability | [↗](https://share.streamlit.io/gabrielmahia/catholic-network-tools) |
| [Stahimili](https://github.com/gabrielmahia/openresilience) | Drought & water stress — SMS alerts to Kenya's 47 counties | [↗](https://share.streamlit.io/gabrielmahia/openresilience) |
| [Msimamo](https://github.com/gabrielmahia/quantum-maestro) | Macro trading — IWT regime detection, Warsh framework, Kelly sizing | [↗](https://share.streamlit.io/gabrielmahia/quantum-maestro) |

---

## Civic & resilience tools

| App | What it does | Live |
|---|---|---|
| [Hakiki](https://github.com/gabrielmahia/civic-decoder) | Civic intelligence — Kenya budget transparency, CDF tracking | [↗](https://share.streamlit.io/gabrielmahia/civic-decoder) |
| [Hesabu](https://github.com/gabrielmahia/budget-sentinel) | County budget intelligence — devolution accountability | [↗](https://share.streamlit.io/gabrielmahia/budget-sentinel) |
| [Hifadhi](https://github.com/gabrielmahia/landwatch) | Land & river watch — riparian encroachment, tenure alerts | [↗](https://share.streamlit.io/gabrielmahia/landwatch) |
| [Mafuriko](https://github.com/gabrielmahia/floodwatch-kenya) | Flood intelligence — 25 cities, policy accountability, incident tracking | [↗](https://share.streamlit.io/gabrielmahia/floodwatch-kenya) |

---

## Agriculture & finance tools

| App | What it does | Live |
|---|---|---|
| [Mazao](https://github.com/gabrielmahia/mazao-intel) | Crop price intelligence — smallholder market access, EN + Kiswahili | [↗](https://share.streamlit.io/gabrielmahia/mazao-intel) |
| [Chagua](https://github.com/gabrielmahia/sacco-scout) | SACCO finder Kenya — compare rates, governance, coverage | [↗](https://share.streamlit.io/gabrielmahia/sacco-scout) |
| [Peleka](https://github.com/gabrielmahia/remit-lens) | Diaspora remittance comparison — true cost across 7 providers | [↗](https://share.streamlit.io/gabrielmahia/remit-lens) |
| [Hela](https://github.com/gabrielmahia/hela) | Chama treasury — rotating credit, cycles, payouts | [↗](https://share.streamlit.io/gabrielmahia/hela) |
| [Dagoretti](https://github.com/gabrielmahia/dagoretti-community-hub) | School alumni hub — KCSE records, community coordination | [↗](https://share.streamlit.io/gabrielmahia/dagoretti-community-hub) |

---

## East Africa open-source ecosystem

### Payments infrastructure

| Repo | Layer | Tests |
|---|---|---|
| [mpesa-python](https://github.com/gabrielmahia/mpesa-python) | SDK — STK Push, B2C, C2B, zero deps | 33 |
| [mpesa-webhooks](https://github.com/gabrielmahia/mpesa-webhooks) | FastAPI callback handler — idempotent, HMAC-verified | 44 |
| [daraja-mock](https://github.com/gabrielmahia/daraja-mock) | Test server — configurable scenarios, no Safaricom account needed | 12 |
| [pesa-cli](https://github.com/gabrielmahia/pesa-cli) | CLI — stk-push, stk-query, b2c, balance, config | 9 |
| [mpesa-mcp](https://github.com/gabrielmahia/mpesa-mcp) | MCP server — AI agent tools for M-Pesa + Africa's Talking | 4 |

### Chama (rotating credit)

| Repo | Layer | Tests |
|---|---|---|
| [chama-protocol](https://github.com/gabrielmahia/chama-protocol) | Domain library — Chama, Member, Cycle, Contribution, Loan | 25 |
| [chama-api](https://github.com/gabrielmahia/chama-api) | REST service — CRUD, idempotency, pagination, OpenAPI | — |

### Communications

| Repo | Layer | Tests |
|---|---|---|
| [kenya-sms](https://github.com/gabrielmahia/kenya-sms) | Africa's Talking wrapper — 8 bilingual EN/SW templates | 19 |

### Reference data

| Repo | What it provides | Tests |
|---|---|---|
| [kenya-counties](https://github.com/gabrielmahia/kenya-counties) | 47 counties — IEBC codes, capitals, regions, 2019 KNBS census | 36 |

### Engineering guides

| Repo | Covers |
|---|---|
| [nairobi-stack](https://github.com/gabrielmahia/nairobi-stack) | M-Pesa · SMS · Mobile-first UX · Regulatory · Chama patterns |

---

## AI ecosystem contributions

| Project | Contribution |
|---|---|
| [context-hub](https://github.com/andrewyng/context-hub) | First African fintech docs — Daraja, Africa's Talking (SMS, USSD, Airtime), Paystack, MTN MoMo |
| [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) | First African entry — mpesa-mcp in Finance & Fintech section |

---

## Ecosystem architecture

```
kenya-counties ──────────────────────────────────────────┐
                                                          │
mpesa-python        ← SDK (auth, STK Push, B2C)          │
  ├── mpesa-webhooks ← callback handler                   ├──→ openresilience / Stahimili
  ├── daraja-mock    ← test doubles                       │         ↑
  ├── pesa-cli       ← CLI                                │      kenya-sms
  └── mpesa-mcp      ← MCP server (AI agents)            │
                                                          │
chama-protocol ← domain library                           │
  ├── chama-api     ← REST service                       │
  └── hela / Hela   ← Streamlit UI ──────────────────────┘

kenya-sms ← bilingual SMS (used by openresilience, hela)
nairobi-stack ← guides documenting all of the above
```

---

## Approach

**Opacity reduction at the point of decision.** Every project surfaces information
previously inaccessible to the people who most need it: parish administrators,
NGO field officers, smallholder farmers, diaspora workers, chama treasurers.

Technical choices follow from users — SMS and USSD for farmers without smartphones,
Kiswahili at every access point, M-Pesa as the payment layer not an afterthought,
mobile-first on every interface.

---

## Governance

- License: CC BY-NC-ND 4.0 (apps) / MIT (libraries + MCP tools)
- DEMO / REAL labelling on every analytical system
- CI/CD: GitHub Actions (lint + test) on every repository
- Security: HMAC webhook verification, 600-mode credentials, privacy-first architecture
- PyPI: [mpesa-python](https://pypi.org/project/mpesa-python/) · [kenya-counties](https://pypi.org/project/kenya-counties/) · [mpesa-mcp](https://pypi.org/project/mpesa-mcp/) *(daraja-mock, kenya-sms, pesa-cli: releasing)*

---

*Open to collaboration on civic tech, humanitarian infrastructure, East African fintech, and institutional decision tools.*  
*contact@aikungfu.dev*
