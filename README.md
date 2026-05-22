# Carbon Intel
### Strategic Intelligence Platform — Built on Bain's Five Frameworks

> **[→ Live Demo]()**

Structured competitive intelligence briefs for carbon removal and 5G/6G companies — generated in under 5 seconds using AI, with every strategic question explicitly mapped to one of Bain & Company's five core frameworks.

---

## What it does

Type any company name. Get a full consulting brief instantly.

**No API key required** for the 12 featured companies — results load immediately. Add an optional Anthropic API key to generate briefs for any company.

---

## Pre-loaded companies

| 🌿 Climate Tech | 📡 Telecom & 5G/6G |
|---|---|
| Climeworks | Ericsson |
| Heirloom Carbon | Nokia |
| 1PointFive | Qualcomm |
| Charm Industrial | Samsung Networks |
| Sustaera | Mavenir |
| Verdox | Rakuten Symphony |

---

## Each brief contains

- **Company masthead** — tagline, founding, HQ, category, stage
- **TRL readiness bar** — Technology Readiness Level 1–9 with visual indicator
- **Competitive moat** — type, strength rating, and three moat dimensions
- **Key metrics** — cost curve / deployment data / revenue model
- **Funding** — raised, round
- **Strategic thesis** — investor narrative and three proof points
- **Risk flags** — High / Medium / Low with colour coding
- **5 strategic questions** — each tagged to its Bain framework

---

## The five Bain frameworks

Every strategic question is explicitly assigned to one of Bain's core frameworks:

| Code | Framework | What it asks |
|---|---|---|
| `FP` | Full Potential | What does this company look like at its performance ceiling? |
| `WTP` | Where to Play / Win | Which market, segment, or geography gives structural advantage? |
| `NPS` | Net Promoter System | What do highest-value customers actually care most about? |
| `RAP` | RAPID Decision | Where do key decisions stall — and who actually decides? |
| `EV` | Elements of Value | Which value dimensions drive willingness to pay? |

---

## Two domains

**Climate Tech** — focused on carbon removal: DAC, enhanced weathering, BECCS, ocean CDR. Metrics cover cost per tonne, cost trajectory, and key cost reduction levers.

**Telecom & 5G/6G** — focused on network infrastructure: RAN, Open RAN, vRAN, private 5G, 6G readiness. Metrics cover deployment scale, 6G readiness, and revenue model.

The same five-framework structure powers both domains. Only the vocabulary changes.

---

## How it works

A single `index.html` file. No build step, no dependencies, no server.

```
User types company name
        ↓
Check pre-built library (instant for 12 companies)
        ↓
If not found + API key present → call Anthropic API
        ↓
Parse JSON response → render 14-section brief
```

For the 12 pre-loaded companies, everything is embedded in the HTML — no network calls, no latency, works offline.

For custom companies, the app calls `api.anthropic.com/v1/messages` with a schema-driven prompt that tells Claude to fill a predefined JSON template as a senior strategy consultant. `max_tokens: 2048` ensures the JSON never gets cut off mid-response.

---

## Deploy in 3 steps

**1. Fork or download** — grab `index.html`

**2. Upload to GitHub** — create a new public repo, upload the file

**3. Enable GitHub Pages** — Settings → Pages → main branch → / (root) → Save

Your live URL:
```
https://YOUR_USERNAME.github.io/carbon-intel
```

No Node. No npm. No build pipeline. One file.

---

## Optional: generate briefs for any company

The 12 pre-built companies cover the core demo. To generate a brief for any other company:

1. Get an API key from [console.anthropic.com](https://console.anthropic.com)
2. Paste it into the optional key field at the bottom of the app
3. Type any company name and hit Analyze

Each brief costs approximately $0.003–$0.008 to generate (less than one cent).

---

## Built with

- **Vanilla HTML/CSS/JS** — zero framework, zero build step
- **Claude Sonnet 4** (Anthropic API) — AI intelligence layer
- **Schema-driven prompting** — structured JSON output via template injection
- **Google Fonts** — Playfair Display, DM Sans, DM Mono

---

## About

Built by **Yoshita Dharni** — Duke MEM 2025, Merit Scholar.

This project bridges hands-on consulting work (Sustaera DAC competitive strategy, Ericsson enterprise SaaS) with Bain's analytical frameworks — demonstrating how AI tooling can accelerate the competitive intelligence work consulting teams do manually.

[LinkedIn](https://linkedin.com/in/yoshita-dharni) · [Email](mailto:yoshita.dharni@gmail.com)

---

*Frameworks referenced: Bain & Company Full Potential, Where to Play/Win, Net Promoter System, RAPID Decision Framework, Elements of Value.*
