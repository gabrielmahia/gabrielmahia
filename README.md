# Gabriel Mahia

**Ninajenga miundombinu ya maamuzi kwa Afrika Mashariki.**  
*Building decision infrastructure for East Africa.*

Kenyan diaspora engineer. The problem I keep solving: institutions that hold data that communities need, with no bridge between the two. I build the bridge.

13 deployed tools · 5 PyPI packages · official MCP Registry · January 2026 →

---

> *"Opacity is not the absence of data. It is data in a form that cannot be acted on."*

---

## What I've built and why

Not a portfolio. A position.

Every tool here was built because a specific community was making decisions without information that existed but was inaccessible to them. The design constraint is always the same: works on a 3G connection, readable in Kiswahili, free to use, degrades gracefully when the internet is slow.

**For governments and watchdogs**
- [Hesabu](https://hesabu.streamlit.app) — tracks county budget absorption across 46 counties. Built because the Controller of Budget publishes this data in PDFs that no county officer has time to read.
- [Macho ya Wananchi](https://macho-ya-wananchi.streamlit.app) — MP attendance, bill status, CDF utilisation for Kenya's 13th Parliament.
- [Jibu](https://jibuyangu.streamlit.app) — constitutional rights AI in English + Kiswahili. LSK and Judiciary feeds live.

**For farmers and field agents**
- [WapiMaji](https://wapimaji.streamlit.app) — water stress + drought alerts via SMS to basic phones. All 47 counties.
- [JuaMazao](https://juamazao.streamlit.app) — live WFP food prices + rainfall by agricultural zone. Designed for the smallholder making a planting decision.
- [Mafuriko](https://floodwatch-kenya.streamlit.app) — 25-city flood intelligence with NDMA signals.

**For diaspora and community finance**
- [TumaPesa](https://tumapesa.streamlit.app) — true cost of remittances across 7 corridors. World Bank 5.26% benchmark shown.
- [Hela](https://helaismoney.streamlit.app) — chama treasury with M-Pesa and diaspora FX rates built in.
- [Jumuia](https://jumuia.streamlit.app) — parish giving and stewardship. USD/GBP/EUR/CAD → KES live.

**For developers building on East African infrastructure**
- [mpesa-mcp](https://github.com/gabrielmahia/mpesa-mcp) — MCP server: give your AI agent M-Pesa and Africa's Talking. On the [official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.gabrielmahia).
- [daraja-v3](https://pypi.org/project/daraja-v3/) — Python SDK for Safaricom Daraja. Zero dependencies.
- [nairobi-stack](https://gabrielmahia.github.io/nairobi-stack) — engineering guides: M-Pesa, USSD, SMS, Kenya DPA, mobile-first UX, live data APIs.

---

## What I care about in code

No magic dependencies. When a library breaks in a Streamlit Cloud free tier at 2am, there is nobody to call. Every production path has a fallback. Every live data function degrades to seed data. Every secret is an environment variable.

The test suite is not aspirational. 307 tests run on every push. Live data functions are mocked so CI does not depend on external APIs. DEMO and REAL data are labelled differently in every analytical system, because trust is harder to rebuild than a dashboard.

I choose SMS over push notifications, USSD over apps, M-Pesa over Stripe, Kiswahili alongside English, and free tiers over infrastructure that requires a credit card. These are not constraints. They are the design.

---

## Architecture in one picture

```
kenya-counties (reference data)
      │
mpesa-python (daraja-v3) ── mpesa-mcp (AI agents) ── official MCP Registry
      ├── daraja-mock    (test doubles)
      ├── pesa-cli       (CLI)
      └── kenya-sms      (Africa's Talking)
            │
      chama-protocol ── Hela (chama treasury UI)
            │
      13 Streamlit apps ── all 47 counties ── all live data
            │
      nairobi-stack (guides for builders doing this next)
```

---

## What I want to hear about

- You work for an NGO, county government, or religious institution in East Africa and one of these tools is close to what you need but not quite
- You're building on M-Pesa or Africa's Talking and hit something the docs don't cover
- You work in humanitarian tech and want to talk about what decision infrastructure for low-resource environments actually looks like

contact@aikungfu.dev · [aikungfu.dev](https://aikungfu.dev) · [full portfolio](https://gabrielmahia.github.io)

---

<sub>CC BY-NC-ND 4.0 (apps) · MIT (libraries) · 307 tests · 13/13 apps with live data · Kiswahili at every civic access point</sub>
