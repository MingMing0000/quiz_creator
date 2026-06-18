# Quiz Creator — OOP rewrite with CLI authoring and Tkinter GUI

Quiz Creator is a Python project rewritten in an object-oriented style that separates authoring and delivery. The project provides a command-line interface (CLI) for creating and managing quizzes and a Tkinter-based graphical application for taking quizzes. This split keeps authoring fast and scriptable while giving end users a simple GUI for taking quizzes.

## Features

- CLI authoring tool: create, edit, reorder, and delete questions and quizzes from the terminal for a fast, scriptable workflow.
- Tkinter quiz-taking GUI: an intuitive interface for students or testers with forms for answering, progress indicators, and results screens.
- OOP architecture: clear domain classes (Quiz, Question, QuizManager, Persistence) and separation between data and UI layers for easier maintenance and testing.
- Save/load quizzes: store quizzes locally in JSON or CSV for sharing and reloading.
- Quiz modes: immediate feedback, end-of-quiz summary, and optional timed mode.
- Import/export support for sharing quizzes across machines.

## Quick Install & Run

Requirements

- Python 3.8+ (Tkinter is included in the standard library on most OSes).

Create a quiz (example)

```bash
python create_quiz.py
# or run the provided CLI entrypoint:
# python -m quiz_creator.cli create
```

Follow the interactive prompts to add questions and save the quiz as JSON or CSV.

Take a quiz (example)

```bash
python quiz_app.py path/to/quiz.json
# or run the GUI entrypoint, if provided:
# python -m quiz_creator.gui path/to/quiz.json
```

The Tkinter GUI will open and guide the user through the quiz with progress and scoring.

## Data formats

- JSON: recommended for full fidelity (question metadata, choices, correct answers, explanations).
- CSV: supported for simpler interchange (best for multiple-choice and true/false formats).

## Project structure (example)

- create_quiz.py         # CLI entrypoint for creating/editing quizzes
- quiz_app.py            # GUI entrypoint that launches the Tkinter quiz-taking app
- quiz_creator/          # core OOP modules (Quiz, Question, Persistence, CLI helpers, GUI wrappers)
- tests/                 # unit tests for core classes

Adjust paths/names above to match the actual structure in this repository.

## Suggested short repo description (<= 100 chars)

Quiz Creator (OOP): CLI authoring + Tkinter GUI for taking quizzes (Python)

## Contributing

Contributions, bug reports, and feature requests are welcome. If you add new question types or change storage formats, please include tests for the core domain classes.

## License

Include a LICENSE file in this repository or replace this section with your chosen license.
