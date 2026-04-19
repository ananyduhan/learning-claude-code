# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Install dependencies (requires Python 3.x and a virtual environment)
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt

# Run the app (http://localhost:5001)
python app.py

# Run tests
pytest

# Run a single test file
pytest tests/test_foo.py
```

## Architecture

This is a Flask app called **Spendly** — a step-by-step learning project for building an expense tracker.

- **`app.py`** — All routes live here. Implemented routes render Jinja2 templates; placeholder routes return strings noting which step implements them (Steps 3–9).
- **`database/db.py`** — SQLite helpers (`get_db`, `init_db`, `seed_db`) to be implemented in Step 1. `get_db()` should enable `row_factory` and foreign keys.
- **`templates/`** — Jinja2 templates extending `base.html`, which provides the nav and footer.
- **`static/css/style.css`** — Apple-inspired design system; all visual work should use the CSS variables and component classes defined here rather than inline styles.

## Design System

`DESIGN.md` is the authoritative reference for colors, typography, spacing, and component patterns. Consult it before adding or modifying any UI. The palette uses CSS variables (e.g., `--color-primary`, `--spacing-md`) defined in `style.css`.
