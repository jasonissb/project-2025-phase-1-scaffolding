# Group 1 README

## Project Overview
This repository is the Phase 1 scaffolding for the Taohi Flight Booking System. It includes a small Java utility class to validate date and datetime strings and a Python test suite to check repository/report integrity.

## Repository Structure
- `src/DateTimeChecker.java`: Java utility with methods to validate dates and datetimes (to be implemented).
- `starter_tests/test_repository.py`: Pytest-based checks ensuring required files and report formatting rules.

## Getting Started
1. Ensure you have Python 3.9+ available.
2. (Optional) Create a virtual environment.
3. Install tooling used by tests:
   - `pip install pymarkdownlnt`
   - Install `pandoc` (download installer from the official site).
   - Install `weasyprint` (see official docs for Windows prerequisites).

## Running Tests
From the repository root, run:

```bash
pytest -x -v starter_tests
```

Notes:
- Tests expect `project-phase1-report.md` to exist in the repository root.
- The report must pass `pymarkdownlnt scan` and be convertible to PDF via `pandoc --pdf-engine=weasyprint`.

## Java Code
Implement the following methods in `src/DateTimeChecker.java`:
- `isValidDate(String dateString)`: Validate `YYYY-MM-DD` format and ensure the date is later than today.
- `isValidDateTime(String dateTimeString)`: Validate `YYYY-MM-DDTHH:MM` format and ensure the date part is later than today (UTC, 24h, no seconds).

## Reporting
- Required file: `project-phase1-report.md` in the repository root.
- Lint command: `pymarkdownlnt scan project-phase1-report.md`.
- PDF export: `pandoc --shift-heading-level-by=-1 --from=gfm -o project-phase1-report.pdf --pdf-engine=weasyprint project-phase1-report.md`.

## License
For academic use only.  
This repository is part of CITS5501/3501 at UWA and must not be shared outside the unit.


