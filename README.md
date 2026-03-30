# Quiz CLI

## Project description
Quiz CLI is an interactive command-line quiz game that runs in Node.js. It loads multiple-choice questions from a local JSON file, lets the user pick a category and number of questions, then walks through the quiz with scored results and a review of incorrect answers.

## Setup instructions
**Prerequisites**
- Node.js **>= 18** (per `package.json` engines)

**Install**
```bash
npm install
```

**Run (minimal example)**
```bash
npm start
# or
node index.js
```

## How to run the project
1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the CLI:
   ```bash
   npm start
   ```
3. In the terminal:
   - Choose a quiz category.
   - Choose how many questions to answer.
   - Enter the option number for each question.

## Key features
- **Category-based quizzes** — Reads categories and questions from `data/questions.json` and prompts you to choose one.
- **Question count selection** — Offers “All questions”, and conditionally offers “3 questions”/“5 questions” based on category size.
- **Randomized question order** — Shuffles questions using a Fisher–Yates shuffle before the quiz starts.
- **Validated multiple-choice input** — Re-prompts until a valid numeric option is entered.
- **Progress indicators** — Shows a visual progress bar and “Question X of Y” during the quiz.
- **Scoring and explanations** — Tracks score and displays the correct answer and optional explanation after each question.
- **Results and review** — Prints a final score summary and lists incorrectly answered questions with your answer vs. the correct one.
- **Colorized terminal output** — Uses a small ANSI color helper (`src/colors.js`) for consistent CLI formatting.
