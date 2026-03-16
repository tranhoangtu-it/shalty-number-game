# shalty-number-game

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Capacitor](https://img.shields.io/badge/Capacitor-119EFF?style=flat-square&logo=capacitor&logoColor=white)

Speed puzzle game inspired by Schulte tables. Find all numbers in ascending order as fast as possible. Available as PWA and native mobile app.

## Features

- 10 difficulty levels with increasing grid sizes
- Global leaderboards
- Smooth animations (Framer Motion)
- PWA — install from browser
- Native iOS/Android via Capacitor
- Offline support

## Tech Stack

- **Frontend**: React + TypeScript + Vite
- **Styling**: Tailwind CSS + Framer Motion
- **Mobile**: Capacitor (iOS/Android)
- **Deployment**: Docker

## Getting Started

```bash
npm install
npm run dev
```

### Mobile Build

```bash
npx cap sync
npx cap open ios    # or android
```

### Docker

```bash
docker compose up
```

## License

See [LICENSE](./LICENSE) for details.
