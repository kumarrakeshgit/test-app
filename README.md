# Quiz CLI

## Project overview

Quiz CLI is a small interactive command-line quiz game written for Node.js. It loads question banks (JSON) and presents multiple-choice questions in categories, tracks score, shows a progress bar, and displays results with colorized terminal output. It runs in Node.js (ES modules) as a terminal/CLI application.

## Setup instructions

Prerequisites:

- Node.js v18 or newer (package.json specifies "engines": { "node": ">=18.0.0" })

Install & run:

```bash
# Install (no dependencies required)
# Ensure Node v18+ is installed

# Run via npm script
npm start

# Or run directly
node index.js
```


## Usage examples

- **Interactive categories** — Choose a category from the question bank (e.g., "JavaScript Basics", "Node.js Fundamentals") before starting a quiz.
- **Select number of questions** — Pick "All questions", or a limited set (3 or 5) depending on the category size.
- **Multiple-choice answers** — Select an answer by entering the number shown next to each option.
- **Progress bar** — Visual progress bar and question count are displayed during the quiz.
- **Immediate feedback** — Each question shows whether your answer was correct, the correct answer when wrong, and an optional explanation from the question data.
- **Review incorrect answers** — After finishing, incorrect questions are listed with your answer and the correct one for review.
- **Replay prompt** — After results, you can choose to play again without restarting the program.

## File structure

```text
.
├── index.js
├── package.json
├── data/
│   └── questions.json
└── src/
    ├── colors.js
    ├── input.js
    └── quiz.js
```

- index.js — Application entry point; loads questions, handles the main loop and user flow.
- package.json — Project metadata, Node engine requirement, and npm scripts (start/test).
- data/questions.json — JSON file containing categorized question banks, answers, and explanations.
- src/colors.js — Small helpers for ANSI colorized terminal output.
- src/input.js — Readline-based utilities for prompting, selecting options, confirmations, and waiting for Enter.
- src/quiz.js — Core quiz logic: shuffling, asking questions, scoring, progress bar, and result presentation.

## Other details

- Uses native ES modules ("type": "module") and Node.js built-ins (fs, readline, path, url). No external dependencies are required.
- Questions are stored in data/questions.json and can be edited or extended with the same shape: { question, options, answer, explanation }.
- The project targets Node.js >= 18 to leverage modern platform features and the built-in fs/promises API.
- Run `npm start` to launch the CLI. For automated tests, the repository includes a `test` script that runs `node --test` (if tests are added).
- The code demonstrates common JS concepts (classes, async/await, array methods, destructuring) suitable for learning or small demos.
