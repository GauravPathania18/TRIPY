<div align="center">
<img width="1200" height="475" alt="Trippy Banner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Trippy - AI-Powered Luxury Travel Planner

A bespoke full-stack travel planning application featuring an interactive 3D globe, predictive climate intelligence, and custom AI itinerary routing powered by Google Gemini AI.

## Features

- 🌍 **Interactive 3D Globe Visualization** - Explore destinations with Three.js globe rendering
- 🤖 **AI Itinerary Planner** - Generate personalized travel itineraries with Google Gemini AI
- 📊 **Analytics Dashboard** - View travel statistics and booking analytics
- 🏖️ **Destination Management** - Browse curated travel packages and destinations
- 👤 **User Authentication** - Secure login and registration system
- 💳 **Booking Management** - Track and manage travel bookings
- 🎨 **Modern UI** - Built with React, Tailwind CSS, and Recharts visualizations

## Tech Stack

**Frontend:**
- React 19 with TypeScript
- Vite (build tool)
- Tailwind CSS v4
- Three.js (3D globe)
- D3.js (data visualization)
- Recharts (charts and analytics)
- Motion (animations)

**Backend:**
- Express.js (Node.js)
- TypeScript
- Mock Database (JSON)
- CORS enabled

**AI Integration:**
- Google Gemini API

## Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Google Gemini API key (get it from [Google AI Studio](https://ai.google.dev/))

## Installation & Setup

1. **Clone or extract the project:**
   ```bash
   cd Trippy
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure environment variables:**
   - Copy `.env.example` to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Edit `.env` and add your Gemini API key:
     ```
     GEMINI_API_KEY=your_gemini_api_key_here
     ```

4. **Run the development server:**
   ```bash
   npm run dev
   ```
   - The app will be available at `http://localhost:3000`
   - Frontend and backend run together with hot module reloading enabled

## Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with Express + Vite HMR |
| `npm run build` | Build frontend (Vite) and bundle backend (esbuild) |
| `npm start` | Run production build |
| `npm run clean` | Remove build artifacts |
| `npm run lint` | Run TypeScript type checking |

## Project Structure

```
Trippy/
├── src/                    # Frontend React components
│   ├── components/         # React components
│   │   ├── Dashboard.tsx
│   │   ├── AIPlanner.tsx
│   │   ├── GlobeSection.tsx
│   │   ├── Destinations.tsx
│   │   └── ...
│   ├── App.tsx
│   ├── main.tsx
│   ├── index.css
│   └── types.ts
├── server/                 # Backend
│   ├── db.ts              # Mock database
│   ├── db.json            # Database storage
│   └── mockData.ts        # Seed data
├── server.ts              # Express server entry point
├── vite.config.ts         # Vite configuration
├── tsconfig.json          # TypeScript configuration
└── package.json           # Dependencies & scripts
```

## API Endpoints

The backend provides REST API endpoints for:
- **Authentication** - User registration and login
- **Travel Data** - Destinations, packages, bookings
- **AI Planning** - Trip itinerary generation via Gemini API

## Environment Variables

- `GEMINI_API_KEY` - Your Google Gemini API key (required)

See [.env.example](.env.example) for a template.

## Development Notes

- Frontend hot reloading is enabled for faster development
- Mock database persists data during the session
- CORS is enabled for local development
- TypeScript provides type safety across frontend and backend

## Deployment

To build for production:

```bash
npm run build
npm start
```

The build output will be in the `dist/` directory.

## License

Built with [Google AI Studio](https://ai.studio)
