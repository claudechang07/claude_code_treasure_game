# 🏴‍☠️ Treasure Hunt Game

An interactive treasure chest game built with React + TypeScript. Click on the chests to find the hidden treasure — but watch out for skeletons!

**Live Demo:** https://claudechang07.github.io/claude_code_treasure_game/

---

## Gameplay

- Three treasure chests are displayed on screen
- One chest hides a treasure, the others contain skeletons
- Click a chest to open it:
  - 💰 **Treasure** → +$100
  - 💀 **Skeleton** → -$50
- The game ends when you find the treasure or open all chests
- Try to maximize your score!

---

## Tech Stack

| Category | Technology |
|---|---|
| Framework | React 18 + TypeScript |
| Build Tool | Vite |
| Styling | Tailwind CSS |
| UI Components | shadcn/ui + Radix UI |
| Animation | Framer Motion (motion/react) |
| Deployment | GitHub Pages |

---

## Getting Started

### Prerequisites

- Node.js 18+
- npm

### Installation

```bash
git clone https://github.com/claudechang07/claude_code_treasure_game.git
cd claude_code_treasure_game
npm install
```

### Development

```bash
npm run dev
```

Opens at http://localhost:3000

### Build

```bash
npm run build
```

Output in `build/`

### Deploy to GitHub Pages

```bash
npm run deploy
```

---

## Project Structure

```
src/
├── App.tsx              # Main game logic and UI
├── assets/
│   ├── treasure_closed.png
│   ├── treasure_opened.png
│   └── treasure_opened_skeleton.png
├── components/
│   └── ui/              # shadcn/ui components
├── index.css
└── styles/
    └── globals.css
```

---

## How It Works

Game state is managed entirely in `src/App.tsx` with React `useState`:

- On mount, one of three chests is randomly assigned the treasure
- Clicking a chest calls `openBox()`, which updates score and checks end conditions
- The game ends when the treasure chest is opened or all three chests are opened
- `resetGame()` re-initializes the state for a new round

---

## Contributors

| Avatar | Name | Role |
|---|---|---|
| ![claudechang07](https://avatars.githubusercontent.com/claudechang07?s=40) | [claudechang07](https://github.com/claudechang07) | Developer |
| <img src="https://www.anthropic.com/favicon.ico" width="40" height="40"> | [Claude Code](https://claude.ai/code) | AI Assistant |

---

## License

MIT
