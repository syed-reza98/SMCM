# Backend Directory

This directory contains the Django backend application for the Social Media Campaign Manager.

## Structure

```
backend/
├── smcm/                 # Main Django project
├── apps/                 # Django applications
│   ├── accounts/         # User management
│   ├── campaigns/        # Campaign management
│   ├── content/          # Content management
│   ├── analytics/        # Analytics and reporting
│   └── social_auth/      # Social media authentication
├── static/               # Static files
├── media/                # User uploaded files
├── requirements.txt      # Python dependencies
├── manage.py            # Django management script
└── Dockerfile.dev       # Development Docker configuration
```

## Getting Started

1. Create virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run migrations:
   ```bash
   python manage.py migrate
   ```

4. Create superuser:
   ```bash
   python manage.py createsuperuser
   ```

5. Start development server:
   ```bash
   python manage.py runserver
   ```

## Development

- API documentation available at `/api/docs`
- Admin interface at `/admin`
- Follow Django best practices and PEP 8
- Write tests for all new features