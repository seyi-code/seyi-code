# Seyi Code

**Independent AI systems builder** — chatbots, voice agents, and automation that take the repetitive work off real businesses.

[![Live Site](https://img.shields.io/badge/Live-seyi--qiing.vercel.app-33d1b6?style=flat-square)](https://seyi-qiing.vercel.app)
[![Stack](https://img.shields.io/badge/Stack-React%20%2B%20FastAPI-12151c?style=flat-square)](#tech-stack)
[![License](https://img.shields.io/badge/License-Private-9aa2b1?style=flat-square)](#)

---

## Who I am

I'm **Seyi Code** — digital creator, full-stack engineer, and solo AI systems builder.

I design and ship practical AI tools for small and mid-sized businesses (especially in African and global SME contexts): website chatbots, voice receptionists, lead automation, and custom workflows. I also build complete web platforms — church management systems, school ERPs, membership platforms, and more.

I work 1:1. No agency overhead, no resold templates. The person you talk to is the person who builds and maintains the system.

**Products & work**
- AI chatbot / voice / automation packages for service businesses
- Custom platforms (Church Platform, Force Schools ERP, NCOF membership platform, ModernBank prototype, and more)
- Digital products for creators (prompt packs, content systems)

---

## This repository

This is the source for my personal / agency landing site — a production-ready React + FastAPI app that showcases services, live demo chatbot, pricing, projects, and contact flow.

### Features

- Sticky navigation with smooth-scroll sections
- Hero with clear value proposition and dual CTAs
- Services, pricing tiers, FAQ, about, and projects
- **Live chatbot** (rule-based + optional Claude-backed backend)
- Contact form + WhatsApp / email deep links
- Fully responsive, keyboard-accessible, respects `prefers-reduced-motion`
- Single source of truth for all copy (`frontend/src/data/content.js`)

### Tech stack

| Layer     | Choice                | Why |
|-----------|-----------------------|-----|
| Frontend  | React 18 + Vite       | Fast, static-friendly, easy to deploy anywhere |
| Styling   | Plain CSS + variables | No lock-in, tiny bundle, easy re-skin |
| Backend   | Python + FastAPI      | Typed API, optional real LLM, contact handling |
| Chatbot   | Rule-based + Claude   | Works offline by default; upgrade to LLM when ready |
| Deploy    | Vercel                | Frontend + serverless-friendly backend options |

---

## Project structure

```
seyi-qing/
├── frontend/                  # React + Vite site
│   ├── src/
│   │   ├── data/content.js    # ALL editable copy (brand, services, pricing…)
│   │   ├── components/        # Navbar, Hero, Services, Chatbot, etc.
│   │   ├── utils/chatbotEngine.js
│   │   └── index.css          # Design tokens + styles
│   └── public/                # favicon, OG image, headshot
├── backend/                   # Optional FastAPI service
│   ├── main.py                # /api/chat + /api/contact
│   └── requirements.txt
├── package.json               # Root scripts (dev / build / preview)
└── vercel.json
```

---

## Getting started

### Frontend only (recommended to start)

```bash
cd frontend
npm install
npm run dev          # http://localhost:5173
```

Production build:

```bash
npm run build        # → frontend/dist
npm run preview
```

### Backend (optional)

```bash
cd backend
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env       # add ANTHROPIC_API_KEY for real AI replies
uvicorn main:app --reload  # http://localhost:8000  ·  docs at /docs
```

Then in `frontend/src/utils/chatbotEngine.js` set `USE_BACKEND = true` and point `BACKEND_URL` at your API.

---

## Making it yours

Everything brand-facing lives in **one place**:

- **Copy & pricing** → `frontend/src/data/content.js`
- **Colors & type** → `frontend/src/index.css` (`:root` variables)
- **Meta / social** → `frontend/index.html` + `frontend/public/og.svg`

Change the name, services, prices, or contact details there and the whole site updates.

---

## Live projects (examples)

| Project              | Status | Stack                                      |
|----------------------|--------|--------------------------------------------|
| AI Receptionist Chatbot | Live | React · FastAPI · Claude                   |
| Church Platform      | Live   | FastAPI · PostgreSQL · Next.js · Expo · Stripe |
| Force Schools (ERP)  | Live   | Next.js · Prisma · TypeScript · Tailwind   |
| NCOF Platform        | Live   | FastAPI · PostgreSQL · Next.js             |
| ModernBank (prototype) | Live | Next.js · FastAPI                        |

---

## Contact

- **WhatsApp** — [+1 312 487 9790](https://wa.me/13124879790)
- **Email** — [logzmaster.biz@gmail.com](mailto:logzmaster.biz@gmail.com)

---

<div align="center">

**Seyi Code** — AI systems that handle the repeats.

*Built independently. No agency. No platform lock-in.*

</div>
