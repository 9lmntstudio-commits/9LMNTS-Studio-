# 9LMNTS STUDIO — MASTER WEB & COMPETITION OS SUITE

> **Official Repository**: [https://github.com/9lmntstudio-commits/9LMNTS-Studio-](https://github.com/9lmntstudio-commits/9LMNTS-Studio-)  
> **Agency Entity**: 9LMNTS Studio (`9lmntsstudio.com`) | Founder & Creative Director: **Darnley Sanon** (Ottawa, Canada)  
> **E-Commerce Infrastructure**: Strictly **PayPal E-Commerce Services** (PayPal Complete Payments, PayPal Pay Later / Pay in 4, and Recurring Subscriptions)

---

## 1. Executive Repository Overview

This repository houses the production codebase for **9LMNTS Studio**, combining:
1. **The Flagship 9LMNTS Studio Portal (`index.html`)**: Mobile-first Dark-Luxe cyber-industrial agency interface with service sprint tiers ($1,500, $2,500, $5,000), monthly retainers ($1,500/mo, $2,500/mo, $5,000/mo), the Universal 4-Box In-Venue Monetization Grid, and native **PayPal E-Commerce Services** with interactive **PayPal Pay Later (Pay in 4)** installment checkout modals.
2. **The 25 Competition OS Arenas (`/competition-suite/`)**: Full standalone tournament engines engineered on the Sound Clash OS architecture (8-contender brackets, real-time vote percentage bars, 70/30 prize pot surges, and PayPal commerce checkout).
3. **Google AI Studio to n8n Automation Engine (`/n8n/`)**: Production workflow JSON and Gemini Function Calling schema allowing Google AI Studio to query pricing and generate verified PayPal payment plan orders through n8n (`loabrain.app.n8n.cloud`).
4. **Master API Wiring Map (`/api/`)**: Complete configuration matrix linking Google AI Studio, n8n, PayPal E-Commerce, ManyChat, Supabase, and GitHub.

---

## 2. Master Pricing Matrix & Payment Plan Structure

All checkout flows, client agreements, and platform tiers operate under **PayPal E-Commerce Services**:

| Service Category | Tier Name | Price (CAD) | Payment Plan / Financing Option | Billing Mode |
| :--- | :--- | :--- | :--- | :--- |
| **Agency Sprints** | Starter Sprint | **$1,500.00** | **PayPal Pay in 4:** 4 bi-weekly payments of **$375.00** (0% interest) | One-time or Pay in 4 |
| **Agency Sprints** | Pro Custom Sprint | **$2,500 – $3,500** | **PayPal Pay in 4:** 4 bi-weekly payments of **$625.00** (0% interest) | One-time or Pay in 4 |
| **Agency Sprints** | Enterprise Scale Build | **$5,000.00** | **PayPal Monthly Installment Financing** | One-time or Financing |
| **Monthly Retainers** | Pro Retainer | **$1,500.00 /mo** | Continuous UI/UX & remote tech support (1 event/mo) | Recurring Subscription |
| **Monthly Retainers** | Premier Operations | **$2,500 – $3,500 /mo** | Dedicated on-site operator (2 events/mo) + priority SLA | Recurring Subscription |
| **Monthly Retainers** | Enterprise Retainer | **$5,000.00 /mo** | Dedicated on-site operator for all events + bespoke SLA | Recurring Subscription |
| **9LMNTS OS Series** | Free Performance | **$0 Upfront** | 80/20 Revenue Split (80% Creator / 20% Studio) | PayPal Split Disbursement |
| **9LMNTS OS Series** | Monthly Maintenance | **$500.00 /mo** | Dedicated monthly updates & server optimization | Recurring Subscription |
| **In-Venue Grid** | Box 01: Cover & Ballot | **$20.00** | **PayPal Pay in 4:** 4 payments of **$5.00** | Instant Checkout |
| **In-Venue Grid** | Box 02: Micro-Tip | **$10.00** | Direct Contender Appreciation | Instant Checkout |
| **In-Venue Grid** | Box 03: Power Hype Pack | **$50.00** | **PayPal Pay in 4:** 4 payments of **$12.50** (25x Votes) | Instant Checkout |
| **In-Venue Grid** | Box 04: VIP Hospitality | **$150 – $250** | **PayPal Pay in 4:** 4 payments of **$37.50** | Instant Checkout |

---

## 3. Google AI Studio to n8n Wiring Guide

### A. Setup in n8n Cloud (`loabrain.app.n8n.cloud`)
1. Open your n8n workspace at [https://loabrain.app.n8n.cloud/](https://loabrain.app.n8n.cloud/).
2. Create a new workflow, click the canvas, and press `Ctrl+V` (or import `/n8n/google_ai_studio_to_n8n_paypal_workflow.json`).
3. Activate the workflow. Your production webhook URL will be:
   `https://loabrain.app.n8n.cloud/webhook/google-ai-studio-paypal`

### B. Setup in Google AI Studio
1. Open [Google AI Studio](https://aistudio.google.com/).
2. In the System Instructions box, paste the content from `/n8n/google_ai_studio_system_prompt.txt`.
3. Under **Tools / Function Calling**, import the tool declarations from `/n8n/google_ai_studio_tool_definition.json`:
   - `query_pricing_and_payment_plans`
   - `create_paypal_ecommerce_order`
4. When testing in Google AI Studio, Gemini will intelligently call the n8n webhook, compute the exact PayPal Pay in 4 installment breakdown, and return the PayPal checkout session link.

---

## 4. Deploying to GitHub (`9LMNTS-Studio-`)

To push this entire package to your new GitHub repository:

```bash
# 1. Initialize git repository in this folder
git init

# 2. Add all files (website, 25 competition platforms, n8n workflows, API wiring)
git add .

# 3. Commit the build
git commit -m "feat: deploy 9LMNTS Studio website & 25 Competition OS suite with PayPal E-Commerce Services"

# 4. Set the main branch
git branch -M main

# 5. Link to your new repository
git remote add origin https://github.com/9lmntstudio-commits/9LMNTS-Studio-.git

# 6. Push to GitHub (use your GitHub Personal Access Token when prompted)
git push -u origin main --force
```

---

## 5. Directory Architecture

```
9LMNTS-Studio-/
├── index.html                               # Master Agency & OS Portal with PayPal Pay in 4 Modal
├── competition-suite/                       # All 25 Competition OS Platforms
│   ├── index.html                           # 25-Arena Visual Navigation Hub
│   ├── 01_Sound_Clash_OS.html               # DJ & Sound Systems
│   ├── 02_Comedian_OS_Roast_Battle.html     # Stand-Up & Roast Battles
│   ├── 03_Bars_OS_Battle_Rap.html           # Battle Rap & Cyphers
│   ├── 04_Runway_OS_Fashion_Battle.html     # Fashion Designers & Runway
│   ├── 05_Feast_OS_Chef_Battle.html         # Culinary Arts & Street Food
│   ├── 06_Hoops_OS_3v3_Streetball.html      # 3v3 Basketball Tournaments
│   ├── 07_GameOS_Pro_Esports.html           # Project LOA Esports Tournaments
│   ├── 08_Pitch_Battle_OS_Corporate.html    # Startup Demo Days & Pitches
│   └── ... (All 25 platforms complete)
├── n8n/
│   ├── google_ai_studio_to_n8n_paypal_workflow.json  # Importable n8n Canvas
│   ├── google_ai_studio_tool_definition.json         # Gemini Function Calling Schema
│   └── google_ai_studio_system_prompt.txt            # System Prompt for AI Studio
├── api/
│   ├── api_wiring_config.json               # Master API mapping & routing specs
│   ├── paypal_ecommerce_pricing_matrix.json # Canonical pricing & Pay in 4 data
│   └── .env.example                         # Environment secrets template
├── netlify.toml                             # Edge redirects & security headers
├── .gitignore                               # Git hygiene
└── README.md                                # Master documentation
```
