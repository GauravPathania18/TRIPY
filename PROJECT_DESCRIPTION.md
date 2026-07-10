# Trippy — AI-Powered Luxury Travel Planner

**Trippy** is a full-stack travel planning web application designed to help users plan premium trips faster and smarter. It combines an interactive 3D globe experience, AI-generated itineraries, climate intelligence, and a workspace for managing destinations, bookings, and saved trips.

---

## What this project does
- Lets users explore curated **destinations** and **tour packages**.
- Provides an **AI Planner** that generates structured, day-by-day travel itineraries tailored to user inputs (destination, budget, duration, interests, and requirements).
- Adds **real-time travel context** via weather/climate guidance so itineraries are more practical.
- Offers a user dashboard to **save trips**, manage **favorites**, and track **notifications**.

---

## Key features

### 🌍 Interactive 3D Globe
- Explore destinations through an embedded 3D globe section (Three.js-based).
- Use visual destination discovery to discover where to go next.

### 🤖 AI Itinerary Planner (Google Gemini)
- Generates a structured trip output as valid JSON and renders it in the UI.
- Supports:
  - Destination-based planning
  - Budget-aware estimation
  - Day-by-day activity suggestions
  - Packing checklist
  - Visa guidance
  - Weather intelligence / seasonal expectations
- Includes an offline-friendly fallback when the Gemini API key is not configured.

### 🎛️ AI Destination Discovery & Recommendations
- Destination discovery endpoint that can create new destinations dynamically (including category, travel style, climate, and coordinates).
- Recommendation endpoint that returns exactly 5 destination suggestions for a given vibe, budget, and duration.

### 🌦️ Weather / Climate Intelligence Integration
- Backend weather endpoint returns current conditions using either:
  - OpenWeatherMap (when an API key is available), or
  - Open-Meteo (fallback, plus geocoding where needed)
- Produces normalized weather fields (temperature, description, humidity, wind speed, condition, location, and source).

### 👤 Authentication & Role-based Access
- User registration, login, and session-based “me” verification.
- Mock token auth and user roles (e.g., admin access for content management features).

### 📦 Destinations, Packages, and Booking Management
- Public browsing for destinations and packages.
- Admin-only APIs to create destination and package entries.
- Booking endpoints:
  - Create bookings for the user
  - Admin can update booking status
- Notification creation on booking and booking-status changes.

### 💾 Saved Trips & Favorites
- Users can save generated itineraries (“Saved Trips”).
- Users can favorite destinations and retrieve favorites from the backend.

### 📰 Blogs, Reviews, and Community Content
- Blog browsing and blog detail views.
- Admin can create blogs.
- Blog comments endpoints.
- Review endpoints with filtering by destination or package.

### 🔔 Notifications Inbox
- User-specific notifications view.
- Mark notifications as read.

---

## Tech stack (high level)
- **Frontend:** React (TypeScript), Vite, Tailwind CSS, Motion (animations), Recharts (charts)
- **3D visualization:** Three.js
- **Backend:** Express + TypeScript, mock JSON database for persistence
- **AI:** Google Gemini API via `@google/genai`

---

## Current architecture notes
- The backend and frontend are served together via a single server entry (`server.ts`).
- The project uses a mock database (`server/db.ts`, `server/db.json`, `server/mockData.ts`) for development.
- Multiple AI endpoints provide structured outputs, with fallbacks to keep the app usable offline.

---

## Project value
Trippy turns travel planning into an interactive, AI-assisted workflow—helping users move from “Where do I want to go?” to a realistic itinerary, packing guidance, and weather-aware planning in minutes, wrapped in a premium globe-driven experience.
