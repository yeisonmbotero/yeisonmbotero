<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&duration=3200&pause=900&color=3DE1FF&center=true&vCenter=true&width=720&lines=Hi%2C+I'm+Yeison+Munera+%F0%9F%91%8B;Revenue+Operations+Engineer;AI+voice+%26+SMS+agents+in+production;n8n+%C2%B7+Supabase+%C2%B7+CRM+automation" alt="Typing intro" />

**I build the systems that make revenue teams scale: AI agents that call and text leads, the pipelines behind them, and the dashboards that prove they work.**

📍 Colombia · 🌎 Remote · 🗣️ English / Español

[![Website](https://img.shields.io/badge/TechCube-portfolio-3DE1FF?style=for-the-badge&logo=vercel&logoColor=white)](https://techcube-site-pearl.vercel.app)
[![Email](https://img.shields.io/badge/Email-yeisonmbotero%40gmail.com-9B6BFF?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yeisonmbotero@gmail.com)

</div>

---

### 🧭 What I do

I'm a **Revenue Operations Engineer**. For the last two years I've designed, shipped and operated the automation layer of lending and tax-services companies in the US: outbound AI calling, conversational SMS, CRM automation, lead enrichment, cold email infrastructure and live reporting.

My home turf is **n8n** (self-hosted, 24/7) as the backend, **Supabase / Postgres** as the source of truth, and **LLMs** (DeepSeek, OpenAI, Claude) orchestrated with hard guardrails. I don't train models. I make them reliable in production.

I also build the front end: websites, dashboards, client portals and a native iOS app.

---

### 📈 Results in production

| | |
|---|---|
| 📞 **35K+** outbound AI calls and **130** qualified sales handoffs | voice + SMS funnel, PTS Financial Services |
| 🏢 **1 → 28 branches** on one calling platform, ~13–14K leads per monthly batch | Sunset Finance |
| ⚡ Branch onboarding **30–40 min → 3–5 min**; **18 branches** live in a single day | Sunset Finance |
| 🎯 Call-outcome classifier **45% → 100%** accuracy on a 151-call backtest | PTS Financial Services |
| 🧹 **56 per-branch workflows → 2 workers** with an atomic Postgres claim: **3,123 / 3,123** calls, 0 duplicates | Sunset Finance |
| 💸 AI cost **~$0.0005** per conversational call, because ~77% of calls skip the LLM | Sunset Finance |
| 🚑 Recovered **1,973 / 1,983** silently dropped calls; n8n DB **5.5 GB → 1.3 GB**, CPU **101% → 3%** | Sunset Finance |
| 📨 Own cold email infrastructure: **23 inboxes / 11 domains**, **$200 → ~$88** per month | PTS Financial Services |
| 🔎 **7K+ CRM contacts** enriched from **4,300+ companies** at **$0** in data credits | PTS AI CRM |
| 🖥️ Live dashboard load time **~2.5 min → ~1.5 s** | PTS Financial Services |

---

### 🛠️ Featured work

| Project | What it is |
|---|---|
| 📞 [**ai-voice-sales-funnel**](https://github.com/yeisonmbotero/ai-voice-sales-funnel) | AI voice + SMS lead-qualification funnel: 10 follow-up stages, 130–200-node after-call workflows, LLM classifiers grounded on telephony end-reasons, Google Calendar booking bridge. Case study with 12 production incidents. *n8n · Atlas voice AI · Twilio · Zoho CRM · Supabase · DeepSeek* |
| 🏢 [**multi-branch-call-orchestrator**](https://github.com/yeisonmbotero/multi-branch-call-orchestrator) | Multi-tenant outbound calling for a 28-branch lender: Latin-square cohort scheduler, `FOR UPDATE SKIP LOCKED` dispatch, self-service CSV ingestion, hybrid deterministic + RAG outcome pipeline. *n8n · Postgres · pgvector · Next.js* |
| 📨 [**cold-email-infrastructure**](https://github.com/yeisonmbotero/cold-email-infrastructure) | Cold email stack I built to replace a vendor: domains, DNS (SPF / DKIM / DMARC), inbox provisioning, warmup and runbooks. $200 → ~$88 per month. *Cloudflare · Google Workspace · Smartlead · Clay* |
| 🔌 [**ghl-mcp-server**](https://github.com/yeisonmbotero/ghl-mcp-server) | MCP server for GoHighLevel, backed by a reverse-engineered map of GHL's internal API (259 endpoints from 4,600+ captured calls). *Python · FastMCP* |
| 🏭 [**webfactory**](https://github.com/yeisonmbotero/webfactory) | A website factory: a business URL goes in, and out comes a deployed, audited landing page. The auditor blocks the deploy if the page fails. *Python · Playwright* |
| 🛡️ [**claude-code-security-audit**](https://github.com/yeisonmbotero/claude-code-security-audit) | Security layer for AI coding agents: HMAC-signed drift detection, hook scanner, real-time command guard, skill quarantine. *Python stdlib* |
| 🎙️ [**local-voice-dictation**](https://github.com/yeisonmbotero/local-voice-dictation) | Offline voice dictation with faster-whisper on a global hotkey. Includes the write-ups of two nasty concurrency bugs. *Python · CoreAudio / Win32* |

---

### 🧩 How the voice funnel works

```mermaid
flowchart LR
    A[Meta Ads / CSV batches] --> B[Clay enrichment]
    B --> C[(Supabase<br/>call_requests)]
    C -->|poll + atomic claim| D[Dispatchers<br/>cn1 → cn10]
    D -->|createSchedule| E[Atlas voice AI]
    E -->|call_completed webhook| F[Ingester]
    F --> G[After-call agents<br/>outcome · interest · notes]
    G --> H[Zoho CRM<br/>status · notes · owner]
    G --> I[Handoff email +<br/>Google Calendar booking]
    G -->|next touch| C
    J[Connie SMS agent<br/>RAG over playbook] --> I
    C --> K[Live dashboards]
```

---

### 🧰 Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=supabase,postgres,nextjs,react,ts,js,python,swift,docker,linux,vercel,cloudflare,git,github&perline=14" alt="Stack" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" />
  <img src="https://img.shields.io/badge/GoHighLevel-188BF6?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/Zoho_CRM-E42527?style=flat-square&logo=zoho&logoColor=white" />
  <img src="https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white" />
  <img src="https://img.shields.io/badge/Clay-EC5B39?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/Smartlead-7C5CFC?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/Make-6D00CC?style=flat-square&logo=make&logoColor=white" />
  <img src="https://img.shields.io/badge/Zapier-FF4A00?style=flat-square&logo=zapier&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/DeepSeek-4D6BFE?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white" />
  <img src="https://img.shields.io/badge/pgvector-336791?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" />
</p>

**Also shipped:** a native iOS app (SwiftUI, ~40K lines) with RoomPlan / ARKit / LiDAR room capture, on-device 360° panorama stitching and a Street View-style tour viewer on a Supabase backend. The product is still pre-launch, so the code is private.

---

### 📊 Activity

<p align="center">
  <img src="https://streak-stats.demolab.com?user=yeisonmbotero&theme=tokyonight&hide_border=true&background=0b0e16&ring=3DE1FF&fire=9B6BFF&currStreakLabel=3DE1FF" alt="GitHub streak" />
</p>

---

<div align="center">

**How I work:** I treat every production incident as a root-cause write-up, not a patch. I verify with data before I call something fixed. And I use AI coding agents (Claude Code) as a daily tool to ship faster without lowering the bar.

⭐ If something here is useful to you, let's talk: [yeisonmbotero@gmail.com](mailto:yeisonmbotero@gmail.com)

</div>
