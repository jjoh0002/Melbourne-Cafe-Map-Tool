# Melbourne Coffee Map

A web app for fussy coffee drinkers in Melbourne. Track cafes, their coffee beans, and brewing methods.

## Features

- 🗺️ **Interactive Map** - Mapbox-powered map of Melbourne cafes
- ☕ **Coffee Details** - Bean brands and brewing methods for each cafe
- 🤖 **AI-Found Data** - Automated discovery with human verification
- ✅ **Verification System** - Customers and cafes can verify/correct data
- 📱 **Mobile Friendly** - Works on all devices

## Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Maps**: Mapbox GL JS
- **Database**: Supabase (free tier) - *coming soon*
- **Hosting**: Vercel (free tier)

## Getting Started

### 1. Clone and Install

```bash
cd melbourne-coffee-map/my-app
npm install
```

### 2. Set Up Environment Variables

Create a `.env.local` file:

```bash
cp .env.local.example .env.local
```

Edit `.env.local` and add your Mapbox token:

```env
NEXT_PUBLIC_MAPBOX_TOKEN=your_mapbox_token_here
```

**Get a free Mapbox token:**
1. Go to https://account.mapbox.com
2. Sign up for free (50,000 loads/month)
3. Create an access token
4. Paste it in `.env.local`

### 3. Run Development Server

```bash
npm run dev
```

Open http://localhost:3000

## Data Model

### Cafe Data Sources

| Source | Badge Color | Description |
|--------|-------------|-------------|
| 🤖 AI Found | Amber | Scraped from web/social - needs verification |
| ✅ Customer Verified | Emerald | Verified by coffee drinkers |
| 🏪 Cafe Official | Blue | Provided by the cafe themselves |

### Cafe Properties

- `name` - Cafe name
- `address` - Street address
- `lat/lng` - Map coordinates
- `coffeeBeans` - Array of bean brands used
- `brewingMethods` - Array of available brewing methods
- `dataSource` - How the data was obtained
- `rating` - Customer rating (1-5)
- `instagram` - Instagram handle
- `website` - Website URL
- `lastUpdated` - Date of last update

## Next Steps / Roadmap

### Phase 1: MVP (Current)
- ✅ Basic map with sample data
- ✅ Cafe detail view
- ✅ Filter by data source

### Phase 2: Database Integration
- [ ] Supabase setup
- [ ] Real cafe data from Melbourne
- [ ] User submissions

### Phase 3: AI Data Collection
- [ ] Instagram scraping for bean rotation posts
- [ ] Google Places API integration
- [ ] Review analysis for brewing methods

### Phase 4: Community Features
- [ ] User verification system
- [ ] Cafe owner dashboard
- [ ] Bean rotation notifications

## Deployment

### Deploy to Vercel

```bash
npm i -g vercel
vercel
```

Or connect your GitHub repo to Vercel for auto-deploys.

**Required Environment Variables on Vercel:**
- `NEXT_PUBLIC_MAPBOX_TOKEN`

## Contributing

Found a cafe not listed? Data incorrect? Help us improve:

1. Click "+ Add Cafe" button
2. Fill in the details
3. Submit for review

## License

MIT License - Feel free to use this for your own city!

## Acknowledgments

Built for fussy coffee drinkers everywhere ☕
