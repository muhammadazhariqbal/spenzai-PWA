# Spenzai

**A privacy-first expense tracker built for real-world use**

[**Live App →**](https://spenzai.pages.dev)

---

## Overview

Spenzai is a Progressive Web App (PWA) I built to solve a personal problem: existing expense trackers were too complicated. I wanted something I'd actually use every day—fast entry, clear insights, no friction.

The result is a calculator-style expense tracker that works completely offline and keeps all data local to the user's device.

---

## The Problem

Most budgeting apps fail because they:
- Require too much setup (linking accounts, creating budgets)
- Have features most people never use
- Make users feel judged about spending
- Require internet and cloud accounts
- Don't respect privacy

I wanted something dead simple: log an expense in 2 seconds, see spending patterns, done.

---

## Key Features

### Fast Expense Entry
- Calculator-style interface (tap numbers, not keyboards)
- Pre-set categories for one-tap selection
- Optional notes field
- Takes literally 2 seconds to log an expense

### Smart Insights
- Automatic categorization into Wants, Needs, and Savings
- Visual breakdown by category with percentages
- Daily, monthly, and yearly views
- Spending history with full transaction list

### Privacy by Design
- All data stored locally using LocalForage (IndexedDB)
- No accounts, no authentication
- No analytics or tracking
- Export feature gives users full data ownership
- Works completely offline after first load

### Progressive Web App
- Installable on any device (mobile, tablet, desktop)
- Full offline functionality
- Fast loading with service workers
- Native app-like experience

---

## Technical Implementation

### Frontend Architecture
- **React 18** with functional components and hooks
- **React Router** for navigation
- **Vite** for fast development and optimized builds
- **Tailwind CSS** for utility-first styling

### Data Management
- **LocalForage** for persistent local storage (IndexedDB wrapper)
- No external database or API calls
- Data structure designed for quick reads and aggregations
- JSON export functionality for data portability

### Visualization
- **Recharts** for spending charts and graphs
- Custom components for category breakdowns
- Responsive design for all screen sizes

### PWA Implementation
- **Vite PWA Plugin** for service worker generation
- **Workbox** for caching strategies
- Offline-first architecture
- Install prompts for mobile devices

### State Management
- React hooks (useState, useEffect, useContext)
- Local storage as single source of truth
- No complex state management needed due to simple data flow

---

## Tech Stack

```json
{
  "frontend": "React 18 + Vite",
  "styling": "Tailwind CSS",
  "storage": "LocalForage (IndexedDB)",
  "routing": "React Router v6",
  "charts": "Recharts",
  "pwa": "Vite PWA Plugin + Workbox",
  "deployment": "Cloudflare Pages",
  "build": "Vite (esbuild)",
  "package-manager": "Yarn 3"
}
```

---

## Development Decisions

### Why LocalForage?
- Better API than raw IndexedDB
- Automatic fallback to localStorage if needed
- Promise-based, works well with async/await
- No learning curve for IndexedDB complexity

### Why No Backend?
- User privacy is paramount
- Reduces infrastructure costs to zero
- Faster performance (no network calls)
- Works offline naturally
- Simpler architecture

### Why PWA?
- No app store approval needed
- Works on all platforms from one codebase
- Users can install without friction
- Service workers enable offline functionality
- Smaller download size than native apps

### Why Calculator Interface?
- Faster than typing on mobile keyboards
- Familiar interaction pattern
- Reduces input errors
- Makes logging feel quick and easy

---

## Build & Deployment

### Local Development
```bash
yarn install
yarn dev
```

### Production Build
```bash
yarn build
```

### Deployment
- Automatic deployment via Cloudflare Pages
- Connected to GitHub repository
- Every push to main triggers new build
- Edge network for fast global access
- Free tier covers all needs

---

## Challenges Solved

### Performance
- Optimized re-renders with proper React hooks usage
- Lazy loading for heavy components
- Service worker caching for instant loads
- Efficient date filtering for large datasets

### Data Structure
- Designed schema for fast aggregations
- Category system balances flexibility and simplicity
- Date-based queries optimized for common views

### UX Design
- Minimal steps from open to logged expense
- Visual feedback for all actions
- No dead ends or confusing navigation
- Progressive disclosure (advanced features when needed)

### PWA Complexities
- Service worker update strategies
- Cache invalidation
- Install prompt timing
- iOS Safari PWA quirks

---

## User Impact

- **Speed:** Most users log expenses in under 3 seconds
- **Adoption:** No account requirement removes friction
- **Privacy:** Users trust it because data stays local
- **Retention:** Simple design means people actually keep using it

---

## Future Considerations

Things I'm considering (but avoiding feature creep):
- Multi-language support (Urdu, Arabic)
- Recurring expense templates
- Simple budget alerts (optional)
- Data sync (optional, encrypted, user-controlled)

---

## What I Learned

- **Less is More:** Removing features is harder than adding them
- **Privacy Matters:** Users actively choose apps that respect data
- **PWAs Work:** When done right, PWAs feel native
- **Local-First:** Not every app needs a backend
- **Real-World Testing:** Building for yourself ensures you solve real problems

---

## Links

- **Live App:** [spenzai.pages.dev](https://spenzai.pages.dev)
- **Author:** [Muhammad Azhar Iqbal](https://www.linkedin.com/in/muhammadazhariqbal/)

---

Built with ❤️ because existing expense trackers were too complicated.
