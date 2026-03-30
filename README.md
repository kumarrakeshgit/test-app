# quiz-cli

Branch: `branch1`

## Project description
`quiz-cli` is an interactive Node.js command-line quiz game that loads multiple-choice questions from a local JSON file, prompts the user to pick a category and answer questions, and then displays a scored results summary with review of incorrect answers.

## Setup instructions
**Prerequisites**
- Node.js **>= 18** (per `package.json`)

**Install**
```bash
npm install
```

**Run**
```bash
npm start
```

## How to run the project
```bash
# from the repository root
npm install
npm start
```

## Key features
- **Interactive CLI prompts** — Uses Node.js `readline` to prompt for selections, confirmations, and “press enter to continue” pauses.
- **Category-based quizzes** — Loads categories and questions from `data/questions.json` and lets users choose which category to play.
- **Configurable question count** — Offers “All questions”, “3 questions”, or “5 questions” depending on the selected category size.
- **Question shuffling** — Randomizes question order with a Fisher–Yates shuffle before the quiz starts.
- **Progress display** — Shows a textual progress bar and “Question X of Y” while playing.
- **Scoring and answer review** — Tracks score, prints a final percentage and message, and lists incorrect answers with correct vs. chosen options.
- **ANSI color output** — Formats banners, statuses, and messages using internal ANSI escape-code helpers in `src/colors.js`.
