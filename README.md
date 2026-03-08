# Racespot.tv - Website Relaunch

## Project Setup

**Tech Stack:**
- Next.js 14+ (React Framework)
- Strapi (Headless CMS)
- Tailwind CSS (Styling)
- next-i18next (Internationalization: DE/EN)
- YouTube API Integration
- Google Sheets API Integration

## Pages

1. **Home** - Hero Section, Services Overview, Team, Latest News
2. **Broadcasts** - Portfolio of past broadcasts
3. **Events** - Upcoming and past events
4. **Services** - Broadcast, Esports, Events services
5. **Calendar** - Interactive calendar (Google Sheets sync)
6. **Live** - Embedded YouTube live streams
7. **News** - Blog/News articles

## Project Structure

```
racespot-website/
├── public/              # Static files (images, logos)
├── src/
│   ├── pages/          # Next.js pages
│   │   ├── index.tsx
│   │   ├── broadcasts/
│   │   ├── events/
│   │   ├── services/
│   │   ├── calendar/
│   │   ├── live/
│   │   └── news/
│   ├── components/     # Reusable components
│   │   ├── Navigation
│   │   ├── Footer
│   │   ├── Hero
│   │   ├── Services
│   │   ├── Calendar
│   │   ├── YouTubeEmbed
│   │   └── ...
│   ├── styles/         # Global CSS
│   ├── lib/            # Utilities
│   │   ├── strapi.ts   # Strapi API calls
│   │   ├── youtube.ts  # YouTube API
│   │   └── sheets.ts   # Google Sheets API
│   └── config/         # Configuration files
├── public/locales/     # i18n translations (DE/EN)
├── .env.local          # Environment variables
├── next.config.js      # Next.js configuration
├── tailwind.config.js  # Tailwind configuration
└── strapi/             # Strapi CMS folder
```

## Key Features

### 1. Multilingual (DE/EN)
- next-i18next integration
- Language switcher
- SEO-friendly URLs

### 2. YouTube Integration
- Embed latest videos
- Live stream detection
- Playlist support

### 3. Google Sheets Sync
- Event calendar from Google Sheets
- Auto-update without redeployment
- Fields: Event Name, Sim, Organizer, Format, Stream Link

### 4. SEO Optimized
- Meta tags (title, description, OG)
- Schema.org structured data
- Sitemap generation
- Robots.txt

### 5. CMS (Strapi)
- Content management for News, Services, etc.
- Media management
- Role-based access

## Setup Instructions

### Prerequisites
- Node.js 18+
- npm or yarn
- Docker (optional, for Strapi)

### Installation

```bash
# Clone or navigate to project
cd racespot-website

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env.local
# Edit .env.local with your keys:
# - NEXT_PUBLIC_STRAPI_URL
# - NEXT_PUBLIC_YOUTUBE_API_KEY
# - GOOGLE_SHEETS_API_KEY

# Run development server
npm run dev

# Build for production
npm run build
npm run start
```

### Strapi Setup (optional for now)
```bash
cd strapi
npm install
npm run develop
```

## Deployment

**Vercel** (recommended for Next.js):
```bash
# Connect GitHub repo to Vercel
# Auto-deploys on push to main
```

## API Keys Needed

1. **YouTube Data API v3** - Get from Google Cloud Console
2. **Google Sheets API** - Get from Google Cloud Console
3. **Strapi** - Self-hosted or cloud

## Content from Current Website

(Will be imported from racespot.tv/de)

---

**Status:** 🚧 In Development
**Last Updated:** 2026-03-08
