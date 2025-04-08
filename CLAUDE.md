# OpenAlgo Development Guide

## Commands
- Run dev server: `python app.py`
- Build CSS: `npm run build:css`
- Watch CSS changes: `npm run watch:css` or `npm run dev`
- Production deployment: `gunicorn --worker-class eventlet -w 1 app:app`
- Install dependencies: `pip install -r requirements.txt && npm install`

## Code Style Guidelines
- **Imports**: Standard library → third-party → local modules
- **Naming**: snake_case for variables/functions, PascalCase for classes
- **Structure**: Organize routes by feature in blueprint modules
- **Error Handling**: Use specific exception types in try/except blocks
- **Documentation**: Include docstrings for public functions and classes
- **Environment**: Use python-dotenv for configuration management
- **Route Decorators**: Use decorators for rate limiting and session validation
- **Formatting**: 4-space indentation, maximum 120 chars line length
- **Testing**: Add tests for new features in strategies/ folder
- **Type Hints**: Use type annotations where appropriate

The codebase is a Flask application with tailwind CSS. Follow existing patterns in related modules when adding new code. Keep security in mind when handling API keys and authentication.