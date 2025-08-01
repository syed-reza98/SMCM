# Tests Directory

This directory contains test files and test configuration for the Social Media Campaign Manager.

## Test Structure

```
tests/
├── backend/             # Backend Python tests
│   ├── unit/           # Unit tests
│   ├── integration/    # Integration tests
│   └── fixtures/       # Test data fixtures
├── frontend/           # Frontend JavaScript/TypeScript tests
│   ├── components/     # Component tests
│   ├── pages/         # Page tests
│   ├── utils/         # Utility function tests
│   └── __mocks__/     # Mock files
├── e2e/               # End-to-end tests
│   ├── specs/         # Test specifications
│   └── fixtures/      # Test data
└── performance/       # Performance tests
```

## Running Tests

### Backend Tests
```bash
cd backend
python manage.py test
pytest
pytest --cov=. --cov-report=html
```

### Frontend Tests
```bash
cd frontend
npm test
npm run test:coverage
npm run test:watch
```

### End-to-End Tests
```bash
npm run test:e2e
```

## Test Guidelines

- Write tests for all new features
- Maintain test coverage above 80%
- Use meaningful test names
- Test both success and error cases
- Mock external API calls
- Use factories for test data creation

## Test Configuration

- Backend: pytest configuration in `backend/pytest.ini`
- Frontend: Jest/Vitest configuration in `frontend/package.json`
- E2E: Playwright configuration in `playwright.config.ts`