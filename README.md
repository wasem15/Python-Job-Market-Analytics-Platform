# Python Career & Job Market Analytics

A Django web application that combines career information for Python developers with live vacancy data from the HeadHunter API.

The project demonstrates server-rendered web development, Django ORM modeling, third-party API integration, data cleaning, and content management through Django Admin.

## Highlights

- Career and skills information for Python developers
- Job-market demand and geographic content
- Live vacancy retrieval from the HeadHunter API
- Vacancy filtering, sorting, salary formatting, and skill extraction
- Django Admin for managing informational pages and uploaded media
- SQLite for local development
- Django templates for server-side rendering

## Architecture

```text
Browser
   │
   ▼
Django Views
   ├── Django ORM ─────► SQLite
   ├── Templates ──────► HTML/CSS
   └── HeadHunter API ─► Vacancy data
```

The vacancy flow retrieves a list of Python-related vacancies, filters the results, normalizes fields such as salary and key skills, and renders the latest entries in the application.

## Tech stack

- Python
- Django
- Django ORM
- SQLite
- Requests
- HTML / CSS
- HeadHunter API

## Project structure

```text
python/
├── djangoProject1/       # Django project configuration
├── main/                 # Application models, views, URLs, templates
├── main/migrations/      # Django database migrations
├── media/                # Local uploaded media
├── static/               # Static assets
├── manage.py             # Django management entry point
├── requirements.txt      # Python dependencies
└── .env.example          # Local environment template
```

## Getting started

### Prerequisites

- Python 3.11+
- pip
- Internet access for the HeadHunter API

### 1. Create and activate a virtual environment

```bash
cd python
python -m venv .venv
```

Windows:

```powershell
.venv\Scripts\Activate.ps1
```

macOS / Linux:

```bash
source .venv/bin/activate
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure environment variables

Copy `.env.example` and provide a local Django secret:

```text
DJANGO_SECRET_KEY=your-local-secret
DJANGO_DEBUG=true
DJANGO_ALLOWED_HOSTS=127.0.0.1,localhost
```

The project reads these values from the process environment. Do not commit real secrets.

### 4. Apply migrations

```bash
python manage.py migrate
```

### 5. Run the development server

```bash
python manage.py runserver
```

Open the local address shown by Django.

## Data source

Live vacancy data is obtained from the HeadHunter public API endpoint used by the application. API availability and returned data can change over time.

## Notes

The repository stores application media and static assets, while the local SQLite database and Python cache files are intentionally excluded from version control.

## License

License information should be added here when the project license is finalized.
