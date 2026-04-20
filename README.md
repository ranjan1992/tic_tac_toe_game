# Tic Tac Toe Game 🎮

A simple two-player Tic Tac Toe game built with React, Bootstrap, and Reactstrap. Players take turns as **Circle** and **Cross** on a 3×3 grid, with instant win detection and toast notifications.

---

## How the Game Works

```
         GAME START
             │
             ▼
     ┌───────────────┐
     │  Circle's Turn │
     └───────┬───────┘
             │  player clicks a cell
             ▼
     ┌───────────────────┐
     │  Is cell empty?   │
     └──┬────────────────┘
        │ NO                    YES
        ▼                        ▼
  ┌─────────────┐        ┌───────────────┐
  │ Toast Error │        │  Mark placed  │
  │"Already     │        │  on the board │
  │  filled!"   │        └──────┬────────┘
  └─────────────┘               │
                                ▼
                    ┌───────────────────────┐
                    │  Check win condition  │
                    │  (rows, cols, diags)  │
                    └──────────┬────────────┘
                               │
                    ┌──────────┴──────────┐
                 Winner?                  No
                    │                     │
                    ▼                     ▼
           ┌──────────────┐     ┌─────────────────┐
           │ Show winner  │     │  Switch turn    │
           │ message +    │     │  Circle ↔ Cross │
           │ Reload btn   │     └────────┬────────┘
           └──────┬───────┘              │
                  │                      ▼
                  │              ┌───────────────┐
                  │              │  Next player  │
                  │              │  clicks...    │
                  │              └───────────────┘
                  │ click Reload
                  ▼
           ┌──────────────┐
           │  Reset board │
           │  all empty   │
           └──────────────┘
```

### Board Layout

```
 Cell 0 │ Cell 1 │ Cell 2
────────┼─────────┼────────
 Cell 3 │ Cell 4 │ Cell 5
────────┼─────────┼────────
 Cell 6 │ Cell 7 │ Cell 8
```

### Win Conditions Checked

```
Rows:       [0,1,2]  [3,4,5]  [6,7,8]
Columns:    [0,3,6]  [1,4,7]  [2,5,8]
Diagonals:  [0,4,8]  [2,4,6]
```

### Example Winning Board

```
  ✕  │  ○  │  ✕
─────┼─────┼─────
  ○  │  ✕  │  ○        ✕ wins via diagonal [0,4,8]
─────┼─────┼─────
  ○  │  ○  │  ✕
```

---

## Features

- Two-player turn-based gameplay (Circle vs Cross)
- Automatic win detection across all rows, columns, and diagonals
- Toast notifications for invalid moves and win announcements
- One-click game reset
- Responsive layout using Bootstrap grid

---

## Tech Stack

| Library | Purpose |
|---|---|
| React 18 | UI framework |
| Reactstrap 9 | Bootstrap-based React components |
| Bootstrap 5 | Styling and layout |
| react-icons | Icons for Circle, Cross, and empty cells |
| react-toastify | In-app notifications |

---

## Project Structure

```
tic_tac_toe_game-master/
├── public/
│   ├── index.html          # HTML entry point
│   └── manifest.json       # Web app manifest
├── src/
│   ├── components/
│   │   └── Icon.js         # Renders Circle, Cross, or default icon
│   ├── App.js              # Main game logic and UI
│   ├── App.css             # Game-specific styles
│   └── index.js            # React entry point
├── package.json
└── README.md
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- npm (comes with Node.js)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/tic_tac_toe_game.git
   cd tic_tac_toe_game
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open your browser and go to `http://localhost:3000`

---

## Available Scripts

| Script | Description |
|---|---|
| `npm start` | Runs the app in development mode |
| `npm run build` | Builds the app for production |
| `npm test` | Runs the test suite |
| `npm run eject` | Ejects from Create React App (irreversible) |

---

## How to Play

1. The game starts with **Circle's** turn.
2. Click any empty cell on the 3×3 grid to place your mark.
3. Players alternate turns automatically.
4. The first player to align three marks in a row, column, or diagonal wins.
5. A success toast appears announcing the winner.
6. Click **Reload the Game** to start a new round.

> If you click an already-filled cell, an error notification will appear.

---

## License

This project is open source and available under the [MIT License](LICENSE).
