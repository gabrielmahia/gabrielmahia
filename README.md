<!--  Gabriel Mahia — GitHub Profile  -->

# Gabriel Mahia

**Building decision infrastructure for under-resourced institutions.**

I design and ship systems that reduce opacity at the point of decision — giving people with limited time and incomplete information the clarity they need to act well.

The work spans three domains: spiritual, environmental, and financial. The tools built to serve them form a growing open-source ecosystem for East Africa.

---

## Production systems

### ✝️ [Catholic Network Tools](https://github.com/gabrielmahia/catholic-network-tools) — [Live](https://catholicparishsteward.streamlit.app)
Parish decision infrastructure for the global Catholic Church. 17-page platform: AI assistant with real-time Google Search grounding (Gemini 2.0 Flash), liturgical engine (correct A/B/C cycle, fasting rules per episcopal conference), role-gated sacramental records, bilingual parish directory (OpenStreetMap), and SMS/USSD access for basic phones. 56 tests. Full CI.

`python` `streamlit` `gemini` `google-search-grounding` `liturgical-engine` `role-based-access` `africa-talking` `multilingual`

---

### 💧 [OpenResilience Kenya](https://github.com/gabrielmahia/openresilience)
Water and food stress intelligence for Kenya's 47 counties. Composite indices (WSI/FSI/MSI/CRI) surface drought risk and market pressure in near real-time. SMS alerts in English and Kiswahili reach farmers on basic phones. Methodology documented against FAO, FEWS NET, and Kenya NDMA standards.

`python` `streamlit` `fastapi` `sms` `satellite-data` `kenya` `humanitarian` `drought`

---

### 📊 [Quantum Maestro](https://github.com/gabrielmahia/quantum-maestro)
Global macro trade analysis terminal. Formalises three practitioner frameworks — IWT 7-step verification (Teri Ijeoma), Passive Flow Windows, and the Warsh yield-curve filter — into a structured scoring workflow. VIX-regime position sizing via Kelly Criterion. NSE (Nairobi Securities Exchange) coverage. Simulation only.

`python` `streamlit` `yfinance` `algorithmic-analysis` `macro` `nse` `kelly-criterion`

---

## Kenya fintech infrastructure

### 💳 [mpesa-python](https://github.com/gabrielmahia/mpesa-python)
Production Python SDK for Safaricom M-Pesa Daraja v3. STK Push, B2C disbursement, C2B URL registration, account balance, STK status polling, and webhook parsing. Zero external dependencies. Stripe-quality typed exceptions. Auto-refreshing token cache. 33 unit tests, no network calls required.

`python` `mpesa` `safaricom` `daraja` `sdk` `kenya` `payments` `zero-dependencies`

---

### 🤝 [chama-protocol](https://github.com/gabrielmahia/chama-protocol)
Digital infrastructure for Kenya's rotating credit associations. Kenya has 300,000+ registered chamas managing KES 300B+ in informal capital. This library provides the core domain model (Chama, Member, Cycle, Round, Contribution), a financial ledger with idempotent M-Pesa receipt recording, and round summaries with disbursement logic. 25 unit tests.

`python` `chama` `rosca` `kenya` `microfinance` `mpesa` `domain-model`

---

### 💸 [RemitLens](https://github.com/gabrielmahia/remit-lens)
True cost comparison for diaspora remittances to Kenya. Compares Wise, Remitly, Sendwave, WorldRemit, Western Union, Mukuru, and LemFi. True cost = fee % + exchange rate spread % — because "zero fee" providers charge through worse rates. Live exchange rates from Frankfurter (ECB). 19 tests.

`python` `streamlit` `remittance` `kenya` `diaspora` `wise` `mpesa` `forex`

---

## Reference

### 📖 [nairobi-stack](https://github.com/gabrielmahia/nairobi-stack)
Engineering guide for building software products in East Africa. Covers: M-Pesa Daraja v3 integration, Africa's Talking SMS/USSD, mobile-first UX for Kenyan users (2G/3G, budget Android, offline-first), Kenya regulatory landscape (CBK, CA, ODPC/Data Protection Act), and chama digitisation.

`kenya` `east-africa` `mpesa` `sms` `ussd` `documentation` `developer-guide`

---

## Approach

The thread across all projects: **opacity reduction at the point of decision.**

A priest determining fasting obligations, an NGO field worker assessing drought risk, a trader evaluating a setup, a farmer deciding whether to plant — all face the same structural problem: consequential decision, limited time, incomplete information. These systems build the layer that makes the decision legible.

Technical choices follow from the users, not the other way around:
- SMS for farmers without smartphones
- USSD for parish communities without data plans
- Role-gated web interfaces for coordinators and administrators
- Zero-dependency Python libraries for environments with constrained package management
- Comprehensive tests so deployments don't break at 2AM in a time zone I'm not in

**Governance standards applied across all repositories:**
- AGPL-3.0 or CC BY-NC-ND 4.0 licensing with institutional deployment pathways
- DEMO/REAL/SIMULATION data labeling on every user-facing output
- Documented methodology for every scoring algorithm
- Security policy with responsible disclosure process
- CI/CD on every active repository

---

## Background

Nairobi, Kenya — based in the USA. Catholic social teaching, East African community networks, financial markets, and AI systems, studied across 35+ archived learning repositories and applied across three production platforms and four open-source libraries.

**Contact:** contact@aikungfu.dev  
**Open to:** collaboration on civic tech, humanitarian infrastructure, African fintech, and institutional decision tools
