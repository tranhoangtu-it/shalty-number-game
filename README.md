# Shalty Number

[![React](https://img.shields.io/badge/React-19-61dafb?logo=react&logoColor=white)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178c6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7-646cff?logo=vite&logoColor=white)](https://vite.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-06b6d4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Capacitor](https://img.shields.io/badge/Capacitor-8-119eff?logo=capacitor&logoColor=white)](https://capacitorjs.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A progressive web app speed puzzle game inspired by [Schulte tables](https://en.wikipedia.org/wiki/Schulte_table). Tap numbers in ascending order before time runs out. Grids scale from 3x3 up to 8x9 across 10 difficulty levels.

## Features

- **10 Difficulty Levels** -- grids scale from 3x3 (9 numbers) to 8x9 (72 numbers) with increasing time limits
- **Local Leaderboard** -- top 10 high scores saved to browser storage
- **Smooth Animations** -- transitions and visual feedback powered by Framer Motion
- **PWA Support** -- installable on any device with a web manifest and service worker
- **Mobile Native Builds** -- iOS and Android via Capacitor
- **Docker Deployment** -- production-ready Nginx container included

## Level Progression

| Level | Grid | Numbers | Time Limit |
|------:|:----:|--------:|-----------:|
| 1     | 3x3  | 9       | 40 s       |
| 2     | 4x4  | 16      | 40 s       |
| 3     | 5x5  | 25      | 45 s       |
| 4     | 5x6  | 30      | 50 s       |
| 5     | 6x6  | 36      | 55 s       |
| 6     | 6x7  | 42      | 60 s       |
| 7     | 7x7  | 49      | 65 s       |
| 8     | 7x8  | 56      | 70 s       |
| 9     | 8x8  | 64      | 75 s       |
| 10    | 8x9  | 72      | 80 s       |

## Tech Stack

| Layer       | Technology                  |
|-------------|-----------------------------|
| Framework   | React 19                    |
| Language    | TypeScript 5.9              |
| Bundler     | Vite 7                      |
| Styling     | Tailwind CSS 3              |
| Animations  | Framer Motion 12            |
| Mobile      | Capacitor 8 (iOS / Android) |
| Deployment  | Docker + Nginx              |

## Getting Started

### Prerequisites

- **Node.js** >= 18
- **npm** >= 9

### Install and Run

```bash
# Clone the repository
git clone https://github.com/tranhoangtu-it/shalty-number-game.git
cd shalty-number-game

# Install dependencies
npm install

# Start the development server
npm run dev
```

### Build for Production

```bash
npm run build    # outputs to dist/
npm run preview  # preview the production build locally
```

### Lint

```bash
npm run lint
```

## Docker Deployment

```bash
# Using Docker Compose
docker compose up -d

# Or build and run manually
docker build -t shalty-number .
docker run -p 3000:3000 shalty-number
```

The app will be available at `http://localhost:3000`.

## Mobile Builds

The project uses [Capacitor](https://capacitorjs.com/) to target iOS and Android from the same codebase.

```bash
# Build the web app first
npm run build

# Sync web assets to native projects
npx cap sync

# Open in Xcode (macOS)
npx cap open ios

# Open in Android Studio
npx cap open android
```

## Project Structure

```
src/
  App.tsx                  # Root component and screen routing
  main.tsx                 # Entry point
  components/
    GameScreens.tsx        # Idle, win, lose, and level-complete overlays
    Grid.tsx               # Number grid renderer
    HUD.tsx                # Level, timer, and score display
    Leaderboard.tsx        # Top 10 scores overlay
    NameInput.tsx          # Player name entry
  hooks/
    useGameLogic.ts        # Core game state, timer, and level progression
    useLeaderboard.ts      # Local storage leaderboard management
```

## License

MIT
