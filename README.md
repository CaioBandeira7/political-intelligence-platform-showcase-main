[README.md](https://github.com/user-attachments/files/32026781/README.md)
# Mandato365 — Political Intelligence Platform

> **A SaaS political intelligence platform running in production, built from scratch by a solo developer.**
> > It turns public data (electoral, legislative, demographic, and digital) into strategic decisions — with AI, in minutes.
> >
> > 🌐 **Live platform:** [mandato365.com.br](https://www.mandato365.com.br)
> > 🎥 **Demo video:** [watch on YouTube](https://youtu.be/IVAE4H_5Yfo)
> > 🏛️ **Status:** In production, actively used by a real parliamentary office and a political party.
> >
> > > ⚠️ **About this repository:** this is a **public showcase**. The source code is **proprietary and private**, as this is a commercial product in operation, with real clients and custom data pipelines. Here you'll find the product overview, features, architecture, and stack — everything you need to understand what was built, without exposing the implementation. For a live technical demo or a conversation about the code, get in touch.
> > >
> > > ---
> > >
> > > ## 🎯 The problem
> > >
> > > Parliamentary offices and campaigns drown in data scattered across dozens of sources — electoral records, congress, public spending portals, census (IBGE), social media — and lack the time or tools to turn it into decisions. Mandato365 bridges that gap: **from raw data to strategy, automatically.**
> > >
> > > ---
> > >
> > > ## ⚙️ Features
> > >
> > > ### 📰 AI news clipping
> > > Automatically monitors all media coverage of a politician and their party. Each story is classified by **sentiment (positive / negative / neutral)** and gets an **AI-generated summary**.
> > > **Why it matters:** what used to take hours of manual reading every day now arrives ready, with a real-time read on public image.
> > >
> > > <img width="1488" height="1057" alt="8d2d6db3-e22f-4098-958b-4182313999a9" src="https://github.com/user-attachments/assets/a9fc8cd8-f1a3-49fb-9404-4b64586f583d" />
### 📊 Social media analytics (Instagram, TikTok & Twitter/X)
Tracks post performance, monitors opponents, and identifies viral content across multiple platforms.
**Why it matters:** elections are also won online — and what gets measured gets improved.
> > > <img width="1448" height="1086" alt="2640adab-3c13-4be2-82aa-8f6ac6f42c70" src="https://github.com/user-attachments/assets/73b06764-4673-4a2e-b7d5-0644648f10be" />
> > > <img width="1448" height="1086" alt="50ee5b15-f53b-4d53-a673-403e0d528926" src="https://github.com/user-attachments/assets/fe08017a-3c85-4846-b003-399888139ab0" />
> > > <img width="1448" height="1086" alt="73de4f6e-ce22-46c0-a7c4-eb4c905088c4" src="https://github.com/user-attachments/assets/5c4eaa50-c222-42ed-a164-9da443f9fed4" />
> > > <img width="1448" height="1086" alt="4fb4cd81-aa93-4db9-ab3f-a54743aa79bb" src="https://github.com/user-attachments/assets/db25c4cf-ee62-4bca-bb07-2874c7dd6e26" />
> > > <img width="1448" height="1086" alt="f11a586e-c09f-407a-a480-7872b2ed458c" src="https://github.com/user-attachments/assets/c5feb09b-4bed-45b0-a976-12a04962fb9f" />



### 🧠 Post sentiment analysis
AI that reads engagement and reveals how audiences are reacting to published content.
**Why it matters:** it separates content that went viral well from content that went viral badly.
> > > <img width="1448" height="1086" alt="e3b5765a-c6a2-4842-b0f5-d22a811c323d" src="https://github.com/user-attachments/assets/a44a7c35-2735-4f04-9fa2-d7c1ad879236" />

### 🗺️ Smart electoral maps
Territorial cross-referencing of **votes, public funds, demographics, electoral ROI, and ideology** per municipality.
**Why it matters:** it answers every campaign's golden question — *"where are my votes, where did funding turn into votes, and where is it worth investing?"*
> > > <img width="2690" height="584" alt="56710d2a-bf5e-49ab-8e6a-dca969fdc29b" src="https://github.com/user-attachments/assets/66ea76c0-75b4-4e2f-b5db-c3ccc9f98a2c" />
> > > <img width="1672" height="941" alt="57839e05-ad7c-4334-adb0-2d35d79f7dfa" src="https://github.com/user-attachments/assets/d3e9d43d-d035-4ed7-a4b0-77867d4741af" />
> > > <img width="1448" height="1086" alt="de2f54fd-e03f-4f9a-894b-405695a89a47" src="https://github.com/user-attachments/assets/7dacda75-c7fb-4d67-a5b1-6f2c62f5b645" />


### 💰 Office financial dashboard
Tracks parliamentary amendments and budgets, cross-referenced with electoral return.
**Why it matters:** it shows where public resources are producing results and where they're being wasted.
> > > <img width="1452" height="1083" alt="8691fd10-0fab-41ad-aad9-bb56c55ffe65" src="https://github.com/user-attachments/assets/6e191a5e-0cda-43d1-86af-ad10a9b8a388" />

### ✍️ Parliamentary speech generator
Generates AI-powered speeches grounded in **real census data (IBGE)**.
**Why it matters:** speeches backed by concrete regional data, ready in minutes.
> > > <img width="1672" height="941" alt="b6106095-2bd9-4b9c-8c9b-4adeda2aa46e" src="https://github.com/user-attachments/assets/ff879d92-0a49-4c06-aec7-a03ec930c21e" />

### 💬 WhatsApp assistant
Strategic alerts, re-election score, and mandate data in real time, straight to your phone.
**Why it matters:** information reaches the politician wherever they actually are.

---

## 🏗️ Architecture (overview)

```
┌─────────────────────────────────────────────────────────────┐
│                       DATA SOURCES                           │
│   Electoral Records · Congress · Public Spending Portal      │
│   Census (IBGE) · Google News · Instagram / TikTok / Twitter │
└─────────────────────────────┬───────────────────────────────┘
                              │  (ingestion pipelines)
                              ▼
┌─────────────────────────────────────────────────────────────┐
│              PROCESSING + AI LAYER                           │
│   Normalization · Data cross-referencing · AI analysis (LLM) │
│   Sentiment · Summarization · Content generation             │
└─────────────────────────────┬───────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    APPLICATION (Next.js)                     │
│   Dashboards · Maps · Reports · API · WhatsApp Assistant     │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech stack

| Layer | Technologies |
|---|---|
| **Frontend** | Next.js 14, TypeScript, Tailwind CSS, Recharts |
| **Backend** | Next.js API Routes, Node.js |
| **Database** | PostgreSQL |
| **AI / LLM** | Anthropic Claude (sentiment analysis, summarization, content generation) |
| **Data** | Electoral records, Congress, Public Spending Portal, Census (IBGE), social media |
| **Infra / Deploy** | Vercel (production) |

---

## 👤 About the development

A project **built from scratch by a single developer**, end to end:
- Architecture and data modeling
- - Full-stack development
  - - AI integration for automated analysis and content generation
    - - Ingestion and cross-referencing pipelines for public data
      - - Production deployment and operation
       
        - This isn't a portfolio prototype — it's a product **running, with real clients.**
       
        - ---

        ## 📬 Contact

        Interested in a live demo, partnership, or opportunity?

        - 🌐 [mandato365.com.br](https://www.mandato365.com.br)
        - - 💼 [LinkedIn](https://www.linkedin.com/in/YOUR-PROFILE)
          - - 📧 caiobritobandeira@hotmail.com


> 🌐 **A note on language:** the platform's interface is in **Portuguese** because it was built for Brazilian politicians and their teams. The codebase is fully localizable — it can be adapted and translated to any other language and political context.
           
      
            <sub>© 2026 Mandato365 · Data-driven political intelligence · Proprietary code.</sub>
