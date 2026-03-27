# quiz-cli

Version: 1.0.0  
License: MIT  
Engine: Node.js >= 18.0.0  

## Project Overview
quiz-cli is a lightweight, dependency-free Node.js interactive CLI quiz application. It runs in the terminal, presents multiple-choice questions organized by category, tracks score and progress with a visual progress bar, shows explanations after each answer, and reviews incorrect answers at the end.

## Features
- No external dependencies — uses only Node.js built-ins
- Category selection (JavaScript, Node.js, General)
- Configurable question count per session
- Questions shuffled randomly each session
- Visual progress bar during quiz
- Explanations shown after each answer
- Final score and results summary
- Review of incorrect answers at the end
- Play again option

## Project Structure
- `index.js` – Entry point, bootstraps the app and runs the main game loop
- `src/colors.js` – ANSI color helper utilities for colorized terminal output
- `src/input.js` – Readline wrappers (prompt, select, confirm, pressEnter)
- `src/quiz.js` – Quiz class with shuffle, progress bar, scoring, and results
- `data/questions.json` – Question bank organized by category

## Prerequisites
- Node.js >= 18.0.0

## Installation
```bash
git clone <repo-url>
cd quiz-cli
```
No external dependencies to install.

## Usage
```bash
node index.js
# or
npm start
```

## How to Add Questions
Edit `data/questions.json`. Each question requires:
- `question` (string)
- `options` (array of strings)
- `answer` (0-based index of correct option)
- `explanation` (optional string)

## Running Tests
```bash
npm test
```

## Contributing
1. Fork the repository
2. Create a feature branch
3. Make changes and test locally
4. Open a pull request

## License
MIT
