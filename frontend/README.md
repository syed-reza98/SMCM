# Frontend Directory

This directory contains the React frontend application for the Social Media Campaign Manager.

## Structure

```
frontend/
├── public/              # Public assets
├── src/
│   ├── components/      # Reusable components
│   ├── pages/          # Page components
│   ├── hooks/          # Custom React hooks
│   ├── store/          # Redux store configuration
│   ├── services/       # API services
│   ├── utils/          # Utility functions
│   ├── types/          # TypeScript type definitions
│   └── styles/         # Global styles
├── package.json        # Dependencies and scripts
├── vite.config.ts      # Vite configuration
└── Dockerfile.dev      # Development Docker configuration
```

## Getting Started

1. Install dependencies:
   ```bash
   npm install
   ```

2. Start development server:
   ```bash
   npm run dev
   ```

3. Build for production:
   ```bash
   npm run build
   ```

## Development

- Application runs on http://localhost:3000
- API calls to http://localhost:8000
- Follow React best practices
- Use TypeScript for type safety
- Write tests with React Testing Library