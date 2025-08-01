# Contributing to Social Media Campaign Manager (SMCM)

Thank you for your interest in contributing to SMCM! We welcome contributions from the community and are excited to see what you'll bring to the project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Development Setup](#development-setup)
- [Pull Request Process](#pull-request-process)
- [Issue Reporting](#issue-reporting)
- [Coding Standards](#coding-standards)
- [Testing Guidelines](#testing-guidelines)
- [Documentation](#documentation)

## Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct:

- **Be respectful**: Treat everyone with respect and kindness
- **Be inclusive**: Welcome newcomers and help them get started
- **Be collaborative**: Work together towards common goals
- **Be patient**: Remember that everyone has different skill levels
- **Be constructive**: Provide helpful feedback and suggestions

## How to Contribute

There are many ways to contribute to SMCM:

- **Report bugs** by creating detailed issue reports
- **Suggest features** through feature request issues
- **Improve documentation** by fixing typos or adding examples
- **Write code** to fix bugs or implement new features
- **Review pull requests** to help maintain code quality
- **Help with testing** by running the application and reporting issues

## Development Setup

### Prerequisites

- Python 3.9+
- Node.js 16+
- PostgreSQL 12+
- Redis 6+
- Docker & Docker Compose (optional but recommended)

### Local Development Setup

1. **Fork and clone the repository**
   ```bash
   git clone https://github.com/your-username/SMCM.git
   cd SMCM
   ```

2. **Set up the backend**
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Set up the frontend**
   ```bash
   cd frontend
   npm install
   ```

4. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

5. **Set up the database**
   ```bash
   # Using Docker (recommended)
   docker-compose up -d db redis
   
   # Or install PostgreSQL and Redis locally
   # Create database and run migrations
   cd backend
   python manage.py migrate
   ```

6. **Start the development servers**
   ```bash
   # Option 1: Using Docker Compose (recommended)
   docker-compose up
   
   # Option 2: Manual startup
   # Terminal 1 - Backend
   cd backend
   python manage.py runserver
   
   # Terminal 2 - Frontend
   cd frontend
   npm run dev
   
   # Terminal 3 - Celery Worker
   cd backend
   celery -A smcm worker --loglevel=info
   ```

### Docker Development Setup

```bash
# Clone the repository
git clone https://github.com/your-username/SMCM.git
cd SMCM

# Copy environment file
cp .env.example .env

# Start all services
docker-compose up

# Access the application
# Frontend: http://localhost:3000
# Backend API: http://localhost:8000
# Admin Panel: http://localhost:8000/admin
```

## Pull Request Process

1. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Write clean, maintainable code
   - Follow coding standards
   - Add tests for new functionality
   - Update documentation as needed

3. **Test your changes**
   ```bash
   # Backend tests
   cd backend
   python manage.py test
   pytest
   
   # Frontend tests
   cd frontend
   npm test
   
   # Linting
   cd backend
   flake8 .
   black .
   isort .
   
   cd frontend
   npm run lint
   ```

4. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```
   
   Use conventional commit messages:
   - `feat:` for new features
   - `fix:` for bug fixes
   - `docs:` for documentation changes
   - `style:` for formatting changes
   - `refactor:` for code refactoring
   - `test:` for adding tests
   - `chore:` for maintenance tasks

5. **Push and create a Pull Request**
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Pull Request Requirements**
   - Clear title and description
   - Reference related issues
   - Include screenshots for UI changes
   - All tests must pass
   - Code review approval required

## Issue Reporting

When reporting issues, please include:

- **Clear title** that summarizes the problem
- **Environment details** (OS, browser, Python/Node versions)
- **Steps to reproduce** the issue
- **Expected behavior** vs actual behavior
- **Screenshots** if applicable
- **Error messages** or logs

### Issue Templates

Use these labels for different types of issues:

- `bug` - Something isn't working
- `enhancement` - New feature or improvement
- `documentation` - Documentation improvements
- `good first issue` - Good for newcomers
- `help wanted` - Extra attention needed

## Coding Standards

### Python (Backend)

- Follow PEP 8 style guide
- Use Black for code formatting
- Use isort for import sorting
- Use type hints where appropriate
- Write docstrings for functions and classes
- Maximum line length: 88 characters

```python
# Example
def create_campaign(
    user: User,
    title: str,
    platforms: List[str],
    schedule_date: datetime
) -> Campaign:
    """Create a new social media campaign.
    
    Args:
        user: The user creating the campaign
        title: Campaign title
        platforms: List of social media platforms
        schedule_date: When to publish the campaign
        
    Returns:
        Created Campaign instance
    """
    pass
```

### JavaScript/TypeScript (Frontend)

- Use ESLint and Prettier for code formatting
- Use TypeScript for type safety
- Follow React best practices
- Use functional components with hooks
- Write meaningful component and variable names

```typescript
// Example
interface CampaignProps {
  campaign: Campaign;
  onEdit: (id: string) => void;
}

const CampaignCard: React.FC<CampaignProps> = ({ campaign, onEdit }) => {
  // Component implementation
};
```

## Testing Guidelines

### Backend Testing

- Write unit tests for models, views, and utilities
- Use Django's TestCase or pytest
- Aim for 80%+ code coverage
- Test both success and error cases

```python
# Example test
class CampaignModelTest(TestCase):
    def test_campaign_creation(self):
        campaign = Campaign.objects.create(
            title="Test Campaign",
            user=self.user
        )
        self.assertEqual(campaign.title, "Test Campaign")
```

### Frontend Testing

- Write unit tests for components and utilities
- Use React Testing Library
- Test user interactions and edge cases
- Write integration tests for critical flows

```typescript
// Example test
test('renders campaign title', () => {
  render(<CampaignCard campaign={mockCampaign} onEdit={jest.fn()} />);
  expect(screen.getByText('Test Campaign')).toBeInTheDocument();
});
```

## Documentation

- Update README.md for significant changes
- Add inline code comments for complex logic
- Update API documentation for backend changes
- Include examples in documentation
- Keep documentation up to date with code changes

## Getting Help

- **Discord**: Join our community Discord server
- **GitHub Discussions**: For questions and general discussion
- **Issues**: For bug reports and feature requests
- **Email**: Contact the maintainers at [email]

## Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes for significant contributions
- Special mentions in project announcements

Thank you for contributing to SMCM! 🎉