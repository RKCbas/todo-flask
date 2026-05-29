# Todo Flask

A task management web app built with Flask and SQLAlchemy. Supports creating, completing, editing, and deleting tasks, with a clean editorial UI.

## Stack

- **Backend**: Python 3 + Flask 3
- **Database**: SQLite via Flask-SQLAlchemy
- **Frontend**: Jinja2 templates + vanilla CSS (Playfair Display + IBM Plex Mono)

## Setup

```bash
# 1. Clone the repo
git clone <repo-url>
cd todo-flask

# 2. Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate        # Windows
source venv/bin/activate     # macOS/Linux

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
python app.py
```

The app will be available at `http://127.0.0.1:5000`.

## Features

| Feature | Route |
| --- | --- |
| List all tasks | `GET /` |
| Add a task | `POST /` |
| Toggle complete | `GET /complete/<id>` |
| Edit a task | `GET /update/<id>` → `POST /update/<id>` |
| Delete a task | `GET /delete/<id>` |

## Project structure

```text
todo-flask/
├── app.py              # Flask app, models, routes
├── requirements.txt
├── instance/
│   └── test.db         # SQLite database (auto-created)
├── static/
│   └── css/
│       └── main.css
└── templates/
    ├── base.html
    ├── index.html
    └── update.html
```
