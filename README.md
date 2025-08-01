# Social Media Campaign Manager (SMCM) 🚀

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-4.2+-green.svg)](https://www.djangoproject.com/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-12+-blue.svg)](https://www.postgresql.org/)

An open source web application designed to help online businesses and marketers plan, schedule, track, and analyze multi-platform social media marketing campaigns with ease and efficiency.

## 🌟 Key Features

### 📅 Multi-Platform Scheduling
- **Universal Scheduler**: Plan and schedule posts across Facebook, Instagram, Twitter/X, LinkedIn, and TikTok from a single interface
- **Smart Timing**: AI-powered optimal posting time suggestions based on audience analytics
- **Bulk Operations**: Schedule multiple posts across platforms simultaneously
- **Content Calendar**: Visual calendar view for campaign planning and management

### 📊 Analytics & Insights
- **Real-time Dashboard**: Comprehensive analytics dashboard with key performance metrics
- **Cross-Platform Analytics**: Unified analytics across all connected social media platforms
- **Engagement Tracking**: Monitor likes, shares, comments, and other engagement metrics
- **ROI Analytics**: Track campaign performance and return on investment
- **Custom Reports**: Generate automated reports with scheduled delivery

### 👥 Team Collaboration
- **Multi-User Support**: Role-based access control for team members
- **Workflow Management**: Content approval workflows and team collaboration tools
- **Asset Sharing**: Shared content library for team resources
- **Activity Tracking**: Audit logs for team actions and changes

### 🎨 Content Management
- **Media Library**: Centralized storage for images, videos, and other assets
- **Content Templates**: Reusable post templates for consistent branding
- **Hashtag Manager**: Organize and manage hashtag collections
- **Content Approval**: Review and approval system for team-generated content

### 🤖 AI-Powered Features
- **Content Suggestions**: AI-powered content recommendations based on trends
- **Hashtag Optimization**: Smart hashtag suggestions for maximum reach
- **Audience Insights**: AI-driven audience analysis and segmentation
- **Performance Predictions**: Predictive analytics for content performance

### 🔧 Advanced Tools
- **Campaign Templates**: Pre-built campaign templates for different industries
- **A/B Testing**: Test different content variations to optimize performance
- **Social Listening**: Monitor brand mentions and industry trends
- **Integration APIs**: Connect with third-party tools and services

## 🛠️ Tech Stack

### Backend
- **Framework**: Django 4.2+ (Python)
- **API**: Django REST Framework
- **Database**: PostgreSQL 12+
- **Task Queue**: Celery with Redis
- **Authentication**: Django Allauth + JWT

### Frontend
- **Framework**: React 18+ with TypeScript
- **State Management**: Redux Toolkit
- **UI Library**: Material-UI (MUI)
- **Charts**: Recharts
- **Build Tool**: Vite

### Infrastructure
- **Containerization**: Docker & Docker Compose
- **Web Server**: Nginx (production)
- **Caching**: Redis
- **File Storage**: Local/AWS S3 (configurable)

### Development Tools
- **Code Quality**: Black, Flake8, ESLint, Prettier
- **Testing**: pytest, React Testing Library
- **API Docs**: DRF Spectacular (OpenAPI/Swagger)

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- Node.js 16+
- PostgreSQL 12+
- Redis 6+
- Docker & Docker Compose (recommended)

### Option 1: Docker Setup (Recommended)

1. **Clone the repository**
   ```bash
   git clone https://github.com/syed-reza98/SMCM.git
   cd SMCM
   ```

2. **Configure environment**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

3. **Start the application**
   ```bash
   docker-compose up
   ```

4. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8000
   - Admin Panel: http://localhost:8000/admin
   - API Documentation: http://localhost:8000/api/docs

### Option 2: Manual Setup

1. **Clone and setup backend**
   ```bash
   git clone https://github.com/syed-reza98/SMCM.git
   cd SMCM/backend
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

2. **Setup frontend**
   ```bash
   cd ../frontend
   npm install
   ```

3. **Configure database**
   ```bash
   # Create PostgreSQL database
   createdb smcm_db
   
   # Run migrations
   cd ../backend
   python manage.py migrate
   python manage.py createsuperuser
   ```

4. **Start services**
   ```bash
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

## 📖 Documentation

- [Installation Guide](docs/installation.md)
- [Configuration](docs/configuration.md)
- [API Documentation](docs/api.md)
- [User Guide](docs/user-guide.md)
- [Developer Guide](docs/developer-guide.md)
- [Deployment Guide](docs/deployment.md)

## 🔌 Social Media Platform Setup

### Supported Platforms

| Platform | Features | API Requirements |
|----------|----------|------------------|
| Facebook | Posts, Stories, Analytics | Facebook Developer Account |
| Instagram | Posts, Stories, Reels | Instagram Business Account |
| Twitter/X | Tweets, Threads | Twitter Developer Account |
| LinkedIn | Posts, Articles | LinkedIn Developer Account |
| TikTok | Videos, Analytics | TikTok for Business |

### API Key Setup

1. **Facebook/Instagram**
   - Create a Facebook Developer account
   - Set up a Facebook App
   - Configure Instagram Basic Display API
   - Add API keys to `.env` file

2. **Twitter/X**
   - Apply for Twitter Developer account
   - Create a new project and app
   - Generate API keys and access tokens
   - Configure in environment variables

3. **LinkedIn**
   - Create LinkedIn Developer application
   - Request marketing API access
   - Configure OAuth settings
   - Add credentials to environment

See [Platform Setup Guide](docs/platform-setup.md) for detailed instructions.

## 🧪 Testing

### Backend Tests
```bash
cd backend
python manage.py test
pytest --cov=.
```

### Frontend Tests
```bash
cd frontend
npm test
npm run test:coverage
```

### End-to-End Tests
```bash
npm run test:e2e
```

## 🚢 Deployment

### Production Deployment

1. **Environment Setup**
   ```bash
   cp .env.example .env.production
   # Configure production settings
   ```

2. **Docker Production**
   ```bash
   docker-compose -f docker-compose.prod.yml up -d
   ```

3. **Manual Deployment**
   - See [Deployment Guide](docs/deployment.md) for detailed instructions
   - Supports AWS, Google Cloud, DigitalOcean, and VPS deployments

## 🤝 Contributing

We welcome contributions from the community! Please read our [Contributing Guidelines](CONTRIBUTING.md) before getting started.

### Ways to Contribute

- 🐛 Report bugs and issues
- 💡 Suggest new features
- 📝 Improve documentation
- 🧪 Add tests
- 💻 Submit code improvements

### Development Workflow

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Write tests
5. Submit a pull request

See our [Contributing Guide](CONTRIBUTING.md) for detailed instructions.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌟 Community & Support

- **GitHub Issues**: [Report bugs and request features](https://github.com/syed-reza98/SMCM/issues)
- **Discussions**: [Join community discussions](https://github.com/syed-reza98/SMCM/discussions)
- **Documentation**: [Read the docs](docs/)
- **Email**: [Contact maintainers](mailto:support@smcm.dev)

## 🙏 Acknowledgments

- Thanks to all [contributors](https://github.com/syed-reza98/SMCM/contributors)
- Built with ❤️ by [CodeStorm Hub](https://github.com/syed-reza98)
- Inspired by the need for accessible social media management tools

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/syed-reza98/SMCM)
![GitHub forks](https://img.shields.io/github/forks/syed-reza98/SMCM)
![GitHub issues](https://img.shields.io/github/issues/syed-reza98/SMCM)
![GitHub pull requests](https://img.shields.io/github/issues-pr/syed-reza98/SMCM)

---

**Made with ❤️ for the social media marketing community**