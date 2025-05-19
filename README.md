# Car Website - FastAPI Project

A web application for a car website built with FastAPI.

## Setup Instructions

### 1. Clone the repository
```bash
git clone <repository-url>
cd car_website
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Create a .env file
Create a file named `.env` in the root directory with the following content:

```
# Database configuration
DATABASE_URL=sqlite:///./car_website.db

# FastAPI configuration
APP_HOST=0.0.0.0
APP_PORT=8000
DEBUG=True

# Security
SECRET_KEY=your_secret_key_here_change_this_in_production

# Other settings
ENVIRONMENT=development
```

### 5. Run the application
```bash
uvicorn app.main:app --reload
```

## Project Structure
```
car_website/
├── .env                  # Environment variables (create this file)
├── requirements.txt      # Project dependencies
├── app/
│   ├── __init__.py
│   ├── main.py           # FastAPI application entry point
│   ├── models/           # SQLAlchemy models
│   ├── schemas/          # Pydantic schemas
│   ├── crud/             # CRUD operations
│   ├── api/              # API endpoints
│   ├── core/             # Core application settings
│   └── templates/        # HTML templates
├── tests/                # Test directory
└── alembic/              # Database migrations
```

## Features
- Car listings
- User authentication
- Admin panel for managing cars
- Search functionality
- Responsive design 