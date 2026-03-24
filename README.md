# Quiz CLI

## Project overview

Quiz CLI is a small interactive command-line quiz game written for Node.js. It loads question categories from a local JSON file and runs a terminal-based quiz session (category selection, question count selection, shuffled questions, progress display, scoring and review). The project is designed to run in a terminal (Node.js >= 18) and demonstrates ES modules, readline-based input, and ANSI-colored output.

## Setup instructions

Prerequisites

- Node.js v18 or newer (package.json specifies "engines.node": ">=18.0.0").

Install / run

```bash
# Install (no external dependencies required, but run npm install for standard workflow)
npm install

# Start via npm script
npm start

# Or run directly with Node
node index.js
```

Minimal usage

1. Run the application (see commands above).
2. Choose a category when prompted.
3. Choose how many questions to answer (All / 3 / 5 when available).
4. Select answers by entering the option number and pressing Enter.
5. Review results and choose whether to play again.

## Usage examples (key capabilities)

- **Category selection** — Choose a question category loaded from data/questions.json.
- **Question count selection** — Pick a subset (All / 3 / 5) when the category contains enough questions.
- **Shuffled questions** — Questions are shuffled each run using the Fisher–Yates algorithm.
- **Interactive selection prompts** — Prompts implemented with readline helpers (select, confirm, prompt) returning Promises.
- **Progress bar and status** — Visual progress bar and question numbering displayed for each question.
- **Immediate feedback** — After each answer the CLI shows whether it was correct and prints the explanation (if present).
- **Results summary & review** — Final score, performance message, and a review list of incorrect answers with correct options.
- **ANSI-colored output** — Terminal text is colorized via internal utilities in src/colors.js (no external dependency).

## File structure

```bash
README.md
package.json        # project manifest (entry: index.js, Node engine >=18, type: module)
index.js            # CLI entry point: loads data, orchestrates quiz loop and I/O
data/questions.json # Question data organized by category
src/
  colors.js         # Helper functions to apply ANSI color/style codes
  input.js          # Readline helpers: createInterface, prompt, select, confirm, pressEnter
  quiz.js           # Quiz class: shuffling, asking questions, scoring, results display
```

File roles (one-line each)

- README.md — This documentation file describing how to run and use the CLI.
- package.json — Project metadata and npm scripts; declares module type and Node engine.
- index.js — Program entry. Loads question data, prompts user for category and question count, runs the Quiz loop, and handles errors and replay.
- data/questions.json — JSON file containing categories and their questions/options/answers/explanations. Edit this file to add or modify quiz content.
- src/colors.js — Utility functions that wrap text in ANSI escape codes for color and style.
- src/input.js — Abstractions over readline to provide prompt, select, confirm and pressEnter utilities that return Promises.
- src/quiz.js — Quiz logic: shuffles questions, presents options, tracks answers/score, renders progress, and prints a final review.

## Any other relevant details extracted from the codebase

- The project uses ES Modules (package.json sets "type": "module").
- There are no external runtime dependencies; the CLI relies on Node's built-in modules (fs, path, readline).
- To add new content, edit data/questions.json. Each question object must include: "question" (string), "options" (array of strings), "answer" (index of correct option), and an optional "explanation" (string).
- The start script defined in package.json runs `node index.js`.
- index.js prints colored error messages and exits with non-zero status on exceptions.
- The application is interactive and assumes it is run in a terminal (TTY). Running in non-interactive environments may not behave as intended.

---

If you'd like, I can also add a CONTRIBUTING.md or show an example of adding a new category to data/questions.json.