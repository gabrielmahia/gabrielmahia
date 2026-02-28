<!--  Gabriel Mahia — GitHub Profile  -->

# Gabriel Mahia

**Building decision infrastructure for under-resourced institutions.**

I design and ship systems that reduce opacity at the point of decision — giving people with limited time and incomplete information the clarity they need to act well.

The work spans four domains: spiritual, environmental, financial, and civic. The tools built to serve them form a growing open-source ecosystem for East Africa.

Kenya × USA.

---

## Production platforms

### ✝️ [Catholic Network Tools](https://github.com/gabrielmahia/catholic-network-tools) — [Live](https://catholicparishsteward.streamlit.app)
Parish decision infrastructure for 1.3B Catholics. 17-page Streamlit platform: AI assistant with real-time Google Search grounding (Gemini 2.0 Flash), liturgical engine (correct A/B/C cycle, fasting rules per episcopal conference), role-gated sacramental records, bilingual parish directory via OpenStreetMap, and SMS/USSD access for basic phones. 56 tests, CI.

`python` `streamlit` `gemini` `real-time-search` `role-based-access` `africa-talking` `sms` `multilingual`

---

### 💧 [OpenResilience Kenya](https://github.com/gabrielmahia/openresilience)
Water and food stress intelligence for Kenya's 47 counties. Composite indices (WSI/FSI/MSI/CRI) surface drought risk and market pressure with SMS alerts reaching farmers on basic phones in English and Kiswahili. Methodology documented against FAO, FEWS NET, and Kenya NDMA standards.

`python` `streamlit` `fastapi` `sms` `drought` `kenya` `humanitarian` `satellite-data`

---

### 📊 [Quantum Maestro](https://github.com/gabrielmahia/quantum-maestro)
Global macro trade analysis terminal. Formalises three practitioner frameworks — IWT 7-step verification (Teri Ijeoma), Passive Flow Windows, and the Warsh yield-curve filter — into a structured scoring workflow. VIX-regime position sizing via Kelly Criterion. NSE (Nairobi Securities Exchange) coverage. Simulation only.

`python` `streamlit` `yfinance` `algorithmic-analysis` `macro` `nse` `kenya`

---

## East Africa open-source

### 💳 [mpesa-python](https://github.com/gabrielmahia/mpesa-python)
Production Python SDK for Safaricom M-Pesa Daraja v3. STK Push, B2C disbursement, C2B registration, account balance, webhook parsing. Zero external dependencies. Auto-refreshing token cache. 33 unit tests — no network calls required.

`python` `mpesa` `safaricom` `daraja` `sdk` `kenya` `zero-dependencies` `payments`

---

### 🤝 [chama-protocol](https://github.com/gabrielmahia/chama-protocol)
Core domain model for Kenya's rotating credit associations. Kenya has 300,000+ registered chamas managing KES 300B+ in informal capital. This library provides Chama, Member, Cycle, Round, and Contribution models with an idempotent M-Pesa ledger. Used by [hela](https://github.com/gabrielmahia/hela). 25 unit tests.

`python` `chama` `rosca` `kenya` `microfinance` `domain-model` `library`

---

### 💰 [hela](https://github.com/gabrielmahia/hela)
Streamlit chama management app built on chama-protocol. Digitise your rotating savings group: track contributions, see who owes what, generate round summaries, and record M-Pesa receipts as payments arrive.

`python` `streamlit` `chama` `kenya` `mpesa` `savings` `community-finance`

---

### 💸 [RemitLens](https://github.com/gabrielmahia/remit-lens)
True cost comparison for diaspora remittances to Kenya. Compares Wise, Remitly, Sendwave, WorldRemit, Western Union, Mukuru, and LemFi. True cost = fee % + exchange rate spread % — because "zero fee" providers often charge through worse rates. Live ECB exchange rates. 19 unit tests.

`python` `streamlit` `remittance` `kenya` `diaspora` `forex` `mpesa`

---

### ⚖️ [jibu](https://github.com/gabrielmahia/jibu)
AI civic assistant for Kenya. Bridges the gap between what Kenyan citizens are entitled to and what they know they're entitled to. Labour rights, land law, consumer rights, government services — in plain Kiswahili and English. Powered by Gemini with Kenya-specific legal grounding.

`python` `ai` `gemini` `kenya` `civic-tech` `kiswahili` `rights` `government`

---

## Reference

### 📖 [nairobi-stack](https://github.com/gabrielmahia/nairobi-stack)
Engineering guide for building software products in East Africa. M-Pesa Daraja v3 integration, Africa's Talking SMS/USSD patterns, mobile-first UX for Kenyan users (2G/budget Android/offline-first), Kenya regulatory landscape (CBK, CA, ODPC), and chama digitisation patterns.

`kenya` `east-africa` `mpesa` `ussd` `sms` `guide` `developer-reference`

---

## Approach

The thread across all projects: opacity reduction at the point of decision.

A priest determining fasting obligations, an NGO field worker assessing drought risk, a trader evaluating a setup, a farmer deciding whether to plant, a citizen asserting their rights — all face the same structural problem: consequential decision, limited time, incomplete information. These systems build the layer that makes the decision legible.

Technical choices follow from the users:
- SMS and USSD for communities without data plans
- Zero-dependency Python libraries for constrained environments
- Role-gated interfaces for multi-level organisations
- Kiswahili at every access point, not as an afterthought
- Comprehensive tests so deployments don't break at 2AM in a different time zone

**Governance across all repositories:** CC BY-NC-ND or AGPL-3.0 licensing · DEMO/REAL labeling · methodology documentation · responsible disclosure · CI/CD

---

**Contact:** contact@aikungfu.dev  
**Open to:** collaboration on civic tech, humanitarian infrastructure, African fintech, and institutional decision tools
