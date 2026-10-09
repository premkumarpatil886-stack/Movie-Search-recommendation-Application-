# Rock Paper Scissors Game

A browser-based Rock Paper Scissors game built with HTML, CSS, and JavaScript. It runs fully offline and needs no installation or libraries.

## Features (Feature Set C)

| Feature | Description |
|---|---|
| Difficulty selection | Easy, Medium, and Hard computer opponents |
| Multiple rounds | Choose a match of 3, 5, or 10 rounds |
| Score tracking | Live scoreboard for You, Draws, and Computer |
| Game history | Round-by-round log for the current match, plus saved past matches and an all-time record |
| Replay option | Play again with the same settings, or change settings |

## How to Run

1. Download all files and keep them in the same folder.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).

A single-file version, `rock-paper-scissors.html`, is also available. It has the HTML, CSS, and JavaScript combined, so it can be opened on its own.

## How to Play

1. Choose a difficulty and the number of rounds, then tap **Start match**.
2. Pick Rock, Paper, or Scissors each round. On a computer you can also press **R**, **P**, or **S**.
3. When all rounds are played, the player with the higher score wins the match.
4. Tap **Play again** to replay, or **Change settings** to pick new options.
5. Open the **History** tab to see past matches and your overall record.

### Game Rules

- Rock beats Scissors
- Scissors beats Paper
- Paper beats Rock
- Same move from both players is a draw (a draw still uses up a round)

## Difficulty Levels

| Level | Computer behaviour |
|---|---|
| Easy | Picks a move completely at random |
| Medium | 50% of the time plays the move that beats your most-used move, otherwise random |
| Hard | Learns which move you tend to play after your last two moves and plays the counter, with 15% randomness so it is not fully predictable |

The computer's memory lasts while the page stays open, so Hard mode gets better at predicting you across replays.

## Project Structure

```
rps-source/
├── index.html    # Page structure (setup, play, end, and history screens)
├── style.css     # Layout and design
├── script.js     # Game logic
└── README.md     # This file
```

## Key Functions (script.js)

| Function | Purpose |
|---|---|
| `computerMove()` | Chooses the computer's move based on the selected difficulty |
| `predictNext()` / `learn()` | Pattern prediction used by Hard mode |
| `startMatch()` | Resets the scores and starts a new match |
| `playRound()` | Plays one round, decides the winner, and updates the score and log |
| `finishMatch()` | Declares the match result and saves it to history |
| `renderHistory()` | Shows saved matches and the all-time record |

## Data Storage

Match history is saved in the browser's `localStorage` (up to the 50 most recent matches). If the browser blocks storage, history still works until the page is closed. Use **Clear history** in the History tab to delete saved matches.

## Technologies Used

- HTML5
- CSS3 (responsive, mobile-friendly layout)
- JavaScript (vanilla, no frameworks)

## Possible Future Improvements

- Sound effects
- Rock-Paper-Scissors-Lizard-Spock mode
- Two-player mode
- Statistics charts

## Author

Add your name, course (BCA), college name, and submission date here.
