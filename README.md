# Mandato365: political intelligence platform

A SaaS platform for Brazilian federal deputies that turned public data (electoral, legislative, census, spending and social media) into daily strategy. I built it alone, from data model to production, and sold it through my company, Atlas Dados e Tecnologia.

**Status:** discontinued in 2026. While it ran, it was used by a parliamentary office and a political party.
**Demo video:** [watch on YouTube](https://youtu.be/IVAE4H_5Yfo) · **Portfolio:** [caiobandeira7.github.io](https://caiobandeira7.github.io)

> This repository is a case study. The source code is proprietary and stays private. Here you'll find the product, the architecture and the stack.

## The problem

Parliamentary offices and campaigns have data scattered across dozens of sources: the Electoral Court (TSE), the Chamber of Deputies, the public spending portal, the census (IBGE) and social media. They lack the time and tools to turn it into decisions. Mandato365 did that automatically, every day.

## Features

### AI press clipping
Monitors coverage of the politician and their party. Each story is classified by sentiment (positive, negative, neutral) and summarized by AI. Hours of daily reading arrive ready each morning.

<img width="700" alt="Press clipping with sentiment and AI summaries" src="https://github.com/user-attachments/assets/a9fc8cd8-f1a3-49fb-9404-4b64586f583d" />

### Social media analytics (Instagram, TikTok and X)
Post performance, competitor monitoring and viral content detection across platforms.

<img width="700" alt="Social media analytics overview" src="https://github.com/user-attachments/assets/73b06764-4673-4a2e-b7d5-0644648f10be" />

<details>
<summary>More screens</summary>

<img width="700" alt="Social media analytics" src="https://github.com/user-attachments/assets/fe08017a-3c85-4846-b003-399888139ab0" />
<img width="700" alt="Social media analytics" src="https://github.com/user-attachments/assets/5c4eaa50-c222-42ed-a164-9da443f9fed4" />
<img width="700" alt="Social media analytics" src="https://github.com/user-attachments/assets/db25c4cf-ee62-4bca-bb07-2874c7dd6e26" />
<img width="700" alt="Social media analytics" src="https://github.com/user-attachments/assets/c5feb09b-4bed-45b0-a976-12a04962fb9f" />

</details>

### Post sentiment analysis
Reads comments and engagement to show how the audience reacted, separating posts that went viral well from those that went viral badly.

<img width="700" alt="Post sentiment analysis" src="https://github.com/user-attachments/assets/a44a7c35-2735-4f04-9fa2-d7c1ad879236" />

### Electoral maps
Crosses votes, public funds, demographics, electoral return on investment and ideology by municipality. It answers where the votes are, where funding turned into votes and where it is worth investing next.

<img width="700" alt="Electoral map" src="https://github.com/user-attachments/assets/d3e9d43d-d035-4ed7-a4b0-77867d4741af" />

<details>
<summary>More screens</summary>

<img width="700" alt="Electoral map summary" src="https://github.com/user-attachments/assets/66ea76c0-75b4-4e2f-b5db-c3ccc9f98a2c" />
<img width="700" alt="Electoral map detail" src="https://github.com/user-attachments/assets/7dacda75-c7fb-4d67-a5b1-6f2c62f5b645" />

</details>

### Office financial dashboard
Tracks parliamentary amendments and budgets against electoral return.

<img width="700" alt="Financial dashboard" src="https://github.com/user-attachments/assets/6e191a5e-0cda-43d1-86af-ad10a9b8a388" />

### Speech generator
Drafts speeches grounded in IBGE census data for the deputy's region.

<img width="700" alt="Speech generator" src="https://github.com/user-attachments/assets/ff879d92-0a49-4c06-aec7-a03ec930c21e" />

### WhatsApp assistant
Alerts, a re-election score and mandate data delivered on WhatsApp.

## Architecture

```
┌───────────────────────────────────────────────────────────────┐
│ DATA SOURCES                                                  │
│ TSE · Chamber of Deputies · Spending portal · IBGE            │
│ Google News · Instagram · TikTok · X                          │
└──────────────────────────────┬────────────────────────────────┘
                               │ ingestion pipelines
                               ▼
┌───────────────────────────────────────────────────────────────┐
│ PROCESSING + AI                                               │
│ Normalization · Cross-referencing · Sentiment · Summaries     │
│ Content generation (Claude API)                               │
└──────────────────────────────┬────────────────────────────────┘
                               ▼
┌───────────────────────────────────────────────────────────────┐
│ APPLICATION (Next.js on Vercel)                               │
│ Dashboards · Maps · Reports · WhatsApp assistant              │
└───────────────────────────────────────────────────────────────┘
```

## Stack

| Layer | Technologies |
|---|---|
| Frontend | Next.js 14, TypeScript, Tailwind CSS, Recharts |
| Backend | Next.js API routes, Node.js |
| Database | PostgreSQL (Supabase) |
| AI | Anthropic Claude: sentiment, summarization, content generation |
| Data | TSE, Chamber of Deputies, public spending portal, IBGE, social media |
| Deploy | Vercel |

## What I did

Everything, as a solo developer: architecture and data modeling, full-stack development, AI integration, public-data ingestion pipelines, production deployment, sales and client operations.

The interface is in Portuguese because it was built for Brazilian politicians and their teams.

## Author

Caio Bandeira, data scientist in Brasília. [Portfolio](https://caiobandeira7.github.io) · [LinkedIn](https://www.linkedin.com/in/caio-bandeira-cv) · [GitHub](https://github.com/CaioBandeira7)
