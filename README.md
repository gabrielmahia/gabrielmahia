# Gabriel Mahia

**Decision infrastructure for under-resourced institutions.**  
Kenyan diaspora engineer — bridging Western technical patterns with East Africa.

13 deployed tools · 5 PyPI packages · shipped since January 2026  
Portfolio: [gabrielmahia.github.io](https://gabrielmahia.github.io) · Engineering blog: [aikungfu.dev](https://aikungfu.dev) · Guide: [nairobi-stack](https://gabrielmahia.github.io/nairobi-stack)

---

## Civic & government intelligence

| App | What it does | Live |
|---|---|---|
| [Mafuriko](https://github.com/gabrielmahia/floodwatch-kenya) | Urban flood intelligence — 25 cities, incident tracking, policy accountability | [↗](https://floodwatch-kenya.streamlit.app) |
| [Macho ya Wananchi](https://github.com/gabrielmahia/civic-decoder) | Civic intelligence — MP tracker, bill tracker, CDF watchdog, 13th Parliament | [↗](https://civic-decoder.streamlit.app) |
| [Hesabu](https://github.com/gabrielmahia/budget-sentinel) | County budget absorption — Controller of Budget data, 46 counties | [↗](https://budget-sentinel.streamlit.app) |
| [Hifadhi](https://github.com/gabrielmahia/landwatch) | Land & river watch — riparian encroachment, NEMA/WRMA data | [↗](https://hifadhi.streamlit.app) |
| [Jibu](https://github.com/gabrielmahia/jibu) | Civic rights AI — English + Kiswahili, Constitution, Employment Act, Land Act | [↗](https://jibu.streamlit.app) |

## Agriculture & climate intelligence

| App | What it does | Live |
|---|---|---|
| [WapiMaji](https://github.com/gabrielmahia/openresilience) | Drought & water stress — SMS alerts to Kenya's 47 counties, basic phone access | [↗](https://wapimaji.streamlit.app) |
| [JuaMazao](https://github.com/gabrielmahia/mazao-intel) | Crop price intelligence — WFP live data, smallholder market access | [↗](https://mazao-intel.streamlit.app) |

## Financial tools

| App | What it does | Live |
|---|---|---|
| [ChaguaSacco](https://github.com/gabrielmahia/sacco-scout) | SACCO comparison — SASRA 2023 data, dividends, loan rates, capital adequacy | [↗](https://sacco-scout.streamlit.app) |
| [Peleka](https://github.com/gabrielmahia/remit-lens) | Diaspora remittance comparison — true cost across 7 corridors | [↗](https://remit-lens.streamlit.app) |
| [Hela](https://github.com/gabrielmahia/hela) | Chama treasury — M-Pesa integration, rotating credit, cycles, payouts | [↗](https://hela.streamlit.app) |
| [Msimamo](https://github.com/gabrielmahia/quantum-maestro) | Macro trading — IWT regime detection, Warsh framework, Kelly sizing | [↗](https://quantum-maestro.streamlit.app) |

## Community platforms

| App | What it does | Live |
|---|---|---|
| [Jumuia](https://github.com/gabrielmahia/catholic-network-tools) | Parish stewardship — church finder, M-Pesa giving, AI assistant, USSD access | [↗](https://catholicparishsteward.streamlit.app) |
| [Dagoretti](https://github.com/gabrielmahia/dagoretti-community-hub) | School alumni hub — KCSE records, mentorship, community coordination | [↗](https://dagoretti-community-hub.streamlit.app) |

---

## East Africa open-source ecosystem

### Payments & AI tooling

| Repo | What it does | PyPI |
|---|---|---|
| [mpesa-mcp](https://github.com/gabrielmahia/mpesa-mcp) | MCP server — M-Pesa + Africa's Talking tools for AI agents | [mpesa-mcp](https://pypi.org/project/mpesa-mcp/) |
| [mpesa-python](https://github.com/gabrielmahia/mpesa-python) | SDK — Safaricom Daraja v3, STK Push, B2C, C2B, zero deps | [daraja-v3](https://pypi.org/project/daraja-v3/) |
| [daraja-mock](https://github.com/gabrielmahia/daraja-mock) | Test server — configurable scenarios, no Safaricom account needed | [daraja-mock](https://pypi.org/project/daraja-mock/) |
| [pesa-cli](https://github.com/gabrielmahia/pesa-cli) | CLI — stk-push, stk-query, b2c, balance, config | [pesa-cli](https://pypi.org/project/pesa-cli/) |
| [kenya-sms](https://github.com/gabrielmahia/kenya-sms) | Africa's Talking wrapper — bilingual EN/SW templates | [kenya-sms](https://pypi.org/project/kenya-sms/) |

### Chama (rotating credit)

| Repo | What it does |
|---|---|
| [chama-protocol](https://github.com/gabrielmahia/chama-protocol) | Domain library — Chama, Member, Cycle, Contribution, Loan |
| [chama-api](https://github.com/gabrielmahia/chama-api) | REST service — CRUD, idempotency, pagination, OpenAPI |
| [mpesa-webhooks](https://github.com/gabrielmahia/mpesa-webhooks) | FastAPI callback handler — idempotent, HMAC-verified |

### Reference data & guides

| Repo | What it does |
|---|---|
| [kenya-counties](https://github.com/gabrielmahia/kenya-counties) | 47 counties — IEBC codes, capitals, regions, 2019 KNBS census |
| [nairobi-stack](https://github.com/gabrielmahia/nairobi-stack) | Engineering guides — M-Pesa, SMS, USSD, mobile UX, Kenya DPA, chama patterns |

---

## Ecosystem architecture

```
kenya-counties ──────────────────────────────────────────────┐
                                                              │
mpesa-python (daraja-v3)  ← SDK (auth, STK Push, B2C, C2B)  │
  ├── mpesa-webhooks  ← callback handler                      ├──→ WapiMaji / openresilience
  ├── daraja-mock     ← test doubles                          │         ↑
  ├── pesa-cli        ← CLI                                   │      kenya-sms
  └── mpesa-mcp       ← MCP server (AI agents)               │
                                                              │
chama-protocol  ← domain library                              │
  ├── chama-api      ← REST service                           │
  └── Hela           ← Streamlit UI ──────────────────────────┘

nairobi-stack ← engineering guides for all of the above
gabrielmahia.github.io ← portfolio
```

---

## AI ecosystem contributions

| Project | Contribution |
|---|---|
| [context-hub](https://github.com/andrewyng/context-hub) | First African fintech docs — Daraja, Africa's Talking (SMS, USSD, Airtime) |
| [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) | mpesa-mcp — M-Pesa + Africa's Talking MCP server |

---

## Approach

**Opacity reduction at the point of decision.** Every project surfaces information
previously inaccessible to the people who most need it: county officers, NGO field
agents, smallholder farmers, diaspora workers, chama treasurers, parishioners.

Technical choices follow from users — SMS and USSD for farmers without smartphones,
Kiswahili at every access point, M-Pesa as the payment layer not an afterthought,
mobile-first on every interface.

---

## Governance

- License: CC BY-NC-ND 4.0 (apps) · MIT (libraries + MCP tools)
- DEMO / REAL labelling on every analytical system
- CI/CD: GitHub Actions (lint + test + publish) on every repository
- Security: HMAC webhook verification, privacy-first architecture
- All 5 packages published to PyPI via Trusted Publisher (OIDC — no API tokens)

---

*Open to collaboration on civic tech, humanitarian infrastructure, East African fintech, and institutional decision tools.*  
*contact@aikungfu.dev · [gabrielmahia.github.io](https://gabrielmahia.github.io)*
