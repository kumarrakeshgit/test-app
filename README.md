# Node Quiz CLI

A small Node.js command-line quiz application that loads questions from data/questions.json and runs an interactive quiz in the terminal. Suitable for learning/assessment scripts or as a minimal example of CLI input handling in Node.js.

## Prerequisites
- Node.js (v14+ recommended)
- npm (comes with Node.js)

## Installation
Run the following from your terminal:

```bash
# clone the repo (if not already)
git clone <repo-url>
cd <repo-directory>

# install dependencies
npm install
```

This README will be added on the branch `test-app`.

## Usage
Run the quiz from the project root:

```bash
# run directly with Node.js
node index.js
```
Follow the on-screen prompts to answer quiz questions. The app reads questions from `data/questions.json` and uses small helper modules in `src/` for colors and input handling.

## Key features
- **Question loader**— Loads quiz data from JSON (data/questions.json).
- **Interactive CLI**— Prompts user input and handles answers via src/input.js.
- **Quiz logic**— Manages question flow and scoring in src/quiz.js.
- **Simple styling**— Terminal color helpers in src/colors.js for readable output.

## Project structure
```
.
├── index.js                # Application entry point: starts the quiz
├── package.json            # npm metadata and scripts/dependencies
├── data/
│   └── questions.json      # Quiz questions (JSON)
└── src/
    ├── colors.js           # Terminal color/helper utilities
    ├── input.js            # Input/prompt handling for CLI
    └── quiz.js             # Core quiz logic (flow, scoring)
```

File roles:
- index.js — boots the app and wires modules together.
- package.json — project metadata and dependency list.
- data/questions.json — source of quiz questions and answers.
- src/colors.js — formats colored/styled terminal output.
- src/input.js — captures and validates user input.
- src/quiz.js — orchestrates quiz rounds and scoring.

## Contributing
- Create a feature branch off `main` (or `test-app` if reproducing this README).
- Open a pull request with a clear description and tests/examples where applicable.
- Keep changes small and focused; update `data/questions.json` for new content.

## License
Place your license here (e.g., MIT).
