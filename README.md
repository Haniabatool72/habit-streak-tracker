# 🔥 Habit Streak Tracker

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![License](https://img.shields.io/badge/license-MIT-orange)

A lightweight habit tracker with a clean **web interface** and an optional **command line tool**.
Built with pure Python and vanilla HTML/CSS/JS, so there is nothing to install.

## ✨ Features

- Add, complete and delete habits
- Current streak, longest streak and total days at a glance
- Responsive dark UI (desktop and mobile)
- JSON REST API
- Optional CLI
- Unit tests for the core logic and the server

## 🚀 Getting Started

### Requirements
- Python 3.8 or higher

### Run the web app
```bash
git clone https://github.com/Haniabatool72/habit-streak-tracker.git
cd habit-streak-tracker
python server.py
```
Open **http://127.0.0.1:8000** in your browser.

Use a different port:
```bash
python server.py 5000
```

### Use the CLI
```bash
python tracker.py add "Read 10 pages"
python tracker.py done "Read 10 pages"
python tracker.py list
```

## 🧪 Run Tests
```bash
python -m unittest discover -s tests -v
```

## 🔌 API

| Method | Endpoint      | Body              | Description     |
|--------|---------------|-------------------|-----------------|
| GET    | `/api/habits` | none              | List all habits |
| POST   | `/api/habits` | `{"name": "..."}` | Add a habit     |
| POST   | `/api/done`   | `{"name": "..."}` | Mark done today |
| POST   | `/api/delete` | `{"name": "..."}` | Delete a habit  |

Data is saved in `habits.json`. Change the location with the `HABIT_FILE` environment variable.

## 📁 Project Structure
```
habit-streak-tracker/
├── server.py        # web server + JSON API
├── tracker.py       # core logic + CLI
├── static/          # frontend (HTML, CSS, JS)
├── tests/           # unit tests
├── README.md
├── LICENSE
└── .gitignore
```

## 🗺️ Roadmap
- [ ] Weekly progress chart
- [ ] Dark/light theme toggle
- [ ] Export to CSV
- [ ] Reminders

## 🤝 Contributing
Pull requests are welcome. Please open an issue first to discuss big changes.

## 📄 License
Released under the [MIT License](LICENSE)..
