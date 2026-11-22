# Personal Expense Tracker

A minimal, modern, full-stack Personal Expense Tracker built with **HTML5**, **CSS3**, **Vanilla JavaScript**, **Python (Flask)**, and **SQLite**.

Track income and expenses, view monthly reports, filter transaction history, and manage display currency — all stored locally in SQLite with no external database required.

---

## Requirements

- **Python 3.10 or higher** — [Download here](https://www.python.org/downloads/)
  - ⚠️ Windows: during install, **check "Add Python to PATH"**
- A modern browser (Chrome, Firefox, Edge)

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/personal-expense-tracker.git
cd personal-expense-tracker
```

### 2. Create a virtual environment

**Windows (PowerShell)**
```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

> If you get a red "execution policy" error, run this first:
> ```powershell
> Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
> ```

**Windows (Command Prompt)**
```cmd
python -m venv venv
venv\Scripts\activate.bat
```

**Mac / Linux**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set up environment (optional)

```bash
# Windows
copy .env.example .env

# Mac / Linux
cp .env.example .env
```

Open `.env` and set a secure `SECRET_KEY` (required only for production).

### 5. Run the app

```bash
python app.py
```

Open your browser and go to: **http://127.0.0.1:5000**

To stop the server, press **Ctrl + C**.

---

## Every time you want to run it again

You only need to activate the venv and run `app.py` — no reinstalling needed.

**Windows (PowerShell)**
```powershell
.\venv\Scripts\Activate.ps1
python app.py
```

**Mac / Linux**
```bash
source venv/bin/activate
python app.py
```

---

## Features

- **Dashboard** — total balance, income, expenses, monthly summary, category breakdown
- **Add Transaction** — record income or expense with category, amount, date and description
- **Transaction History** — search, filter by type/category/date, edit or delete entries
- **Monthly Reports** — bar chart and donut chart breakdown per month
- **Settings** — switch display currency (BDT, USD, EUR, GBP, INR)

---

## Tech Stack

| Layer    | Technology                        |
|----------|-----------------------------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript   |
| Backend  | Python 3, Flask                   |
| Database | SQLite (file stored in `instance/`)|
| Charts   | Inline SVG (no external libraries)|

---

## Project Structure

```
personal-expense-tracker/
├── app.py              # Flask routes and API endpoints
├── database.py         # SQLite CRUD helpers and validation
├── requirements.txt    # Python dependencies
├── .env.example        # Environment variable template
├── instance/           # Auto-created — holds expenses.db (git-ignored)
├── templates/
│   └── index.html      # Single-page app template
└── static/
    ├── css/style.css
    └── js/script.js
```

---

## Notes

- The SQLite database (`instance/expenses.db`) is created automatically on first run.
- The `venv/` folder and `instance/` folder are git-ignored — each user gets their own.
- Changing the display currency only changes the symbol shown — stored amounts are unchanged.
