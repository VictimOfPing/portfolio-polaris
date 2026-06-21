# EasyMappy by Polaris

![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React_18-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript_5.6-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_3.4-38B2AC?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)
![Mapbox](https://img.shields.io/badge/Mapbox-000000?style=flat-square&logo=mapbox&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

EasyMappy solves the discovery gap for travelers who want local-quality recommendations without spending hours comparing search results, reviews, maps, and social content.
The product turns curated city datasets into paid interactive maps, guided tours, and an AI assistant for Milan, Rome, Florence, Venice, and Naples.

## Project Snapshot

- **Product:** EasyMappy by Polaris
- **Sector:** Travel tech, digital tourism, local discovery
- **Business model:** Paid access to curated city-map packages
- **Live product:** [polaris-mu-azure.vercel.app](https://polaris-mu-azure.vercel.app)
- **Repository status:** Production-oriented Next.js application with tests, deployment docs, PWA support, and API integrations

## Preview

<img src="./public/hero_main.webp" alt="EasyMappy city discovery product preview" width="100%" />

## Tech Stack

![Next.js](https://img.shields.io/badge/Next.js-App_Router-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-UI-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Postgres-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-Checkout_Webhooks-635BFF?style=for-the-badge&logo=stripe&logoColor=white)
![Mapbox](https://img.shields.io/badge/Mapbox-Interactive_Maps-000000?style=for-the-badge&logo=mapbox&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-Assistant-412991?style=for-the-badge&logo=openai&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-Unit_Tests-C21325?style=for-the-badge&logo=jest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-E2E-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)

## Core Features

- Curated city map catalogue with five Italian cities, three paid tiers, and 105 POIs per tier across restaurants, nightlife, and practical services.
- Interactive map experience with Mapbox rendering, route planning, POI detail views, favorites, reviews, tour progress, and mobile-first controls.
- Monetized access flow using Stripe Checkout, webhook-driven access-code generation, Resend transactional email, and 30-day protected sessions.
- AI assistant layer for contextual city guidance, backed by OpenAI integrations plus Telegram and WhatsApp webhook routes.
- Admin and host workflows for orders, users, POI submissions, local partners, guest codes, blog review, and operational stats.

## Architecture

The application is built with the Next.js App Router and keeps product surfaces, server routes, domain logic, and data files separated.

```text
app/                      Next.js pages, layouts, API routes, middleware-protected areas
components/               UI, marketing sections, maps, chatbot, dashboards, forms
lib/                      Auth, Stripe, Supabase, analytics, email, SEO, data loading, i18n
logic/                    POI ranking, curation, fallback, harvesting, top-place selection
data/                     City datasets grouped by city and vertical
public/                   Product imagery, city JSON payloads, PWA manifest, service worker
__tests__/                Unit, integration, and UI test coverage
```

Key runtime flows:

```text
Visitor -> pricing/package selection -> Stripe Checkout -> webhook -> access code -> protected city map
User -> city/tier/map route -> POI data loader -> Mapbox viewer -> tour controls -> favorites/reviews
User -> chatbot route -> intent/context extraction -> AI/local responder -> guided recommendations
Admin/host -> dashboard routes -> Supabase-backed operations -> codes, submissions, orders, stats
```

## Results and Impact

- Shipped as a live travel-tech product on Vercel with production routes for marketing, purchase, protected maps, dashboard, admin, host, blog, and privacy flows.
- Productized local discovery into a repeatable city-map model: five cities, three tiers per city, bundled pricing, and structured JSON datasets ready for expansion.
- Replaced manual recommendation workflows with a guided map, automated tour logic, AI assistance, and searchable POI detail pages.
- Added commercial infrastructure around the experience: payments, access control, email delivery, coupon validation, gift cards, guest codes, analytics, PWA support, and offline downloads.

## Run Locally

```bash
npm install
npm run dev
```

For a production check:

```bash
npm run verify
npm run test
npm run build
```

Required environment variables are documented in [.env.example](./.env.example), with deployment notes in [DEPLOY.md](./DEPLOY.md) and Supabase setup in [SUPABASE_SETUP.md](./SUPABASE_SETUP.md).

## Contact

- Product: [EasyMappy by Polaris](https://polaris-mu-azure.vercel.app)
- Support: [support@polaris.app](mailto:support@polaris.app)
- General contact: [hello@polaris.app](mailto:hello@polaris.app)
- Portfolio case study: [live product and implementation scope](https://polaris-mu-azure.vercel.app)
