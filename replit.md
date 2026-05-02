# Creoinc - Instagram Creator Registration Platform

## Overview
A multi-page web application for Instagram creator onboarding and registration for the Creoinc platform.

## Tech Stack
- **Frontend**: React + TypeScript + Vite + Tailwind CSS + Shadcn UI
- **Backend**: Express.js + TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Routing**: wouter
- **Forms**: react-hook-form + zod validation
- **State**: @tanstack/react-query

## Pages
1. **Roadmap** (`/`) - Landing page with monetization roadmap, rules & guidelines
2. **Register** (`/register`) - Creator registration form (Full Name, Instagram Username, Email, Followers Count, Category/Niche, Languages)
3. **Policy** (`/policy`) - Terms of service, privacy policy, creator guidelines
4. **Contact** (`/contact`) - Gmail contact info, social profile links, contact form
5. **Payment** (`/payment`) - Plan selection (Starter/Professional/Enterprise) with payment form

## Database Schema
- `creators` table: id, full_name, instagram_username, email, followers_count, category, languages[], profile_link, payment_status, payment_plan, created_at

## API Endpoints
- `POST /api/creators` - Register new creator
- `GET /api/creators` - List all creators
- `GET /api/creators/:id` - Get creator by ID
- `PATCH /api/creators/:id/payment` - Update payment status

## Key Files
- `shared/schema.ts` - Database schema and Zod validation
- `server/db.ts` - PostgreSQL connection
- `server/storage.ts` - DatabaseStorage implementation
- `server/routes.ts` - API routes
- `client/src/App.tsx` - Router and app layout
- `client/src/components/navigation.tsx` - Top navigation bar
- `client/src/pages/` - All page components
