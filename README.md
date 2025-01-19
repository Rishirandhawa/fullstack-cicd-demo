# Fullstack CI/CD Demo

A production-ready fullstack application demonstrating modern CI/CD practices, with React frontend and FastAPI backend.

## 🚀 Features

### Frontend (React + TypeScript)
- TypeScript for type safety
- React with modern hooks and patterns
- Redux Toolkit for state management
- Comprehensive testing setup with Jest and Testing Library
- ESLint and Prettier for code quality
- Multi-stage Docker builds for optimal image size

### Backend (FastAPI + PostgreSQL)
- FastAPI for high-performance API development
- PostgreSQL with SQLAlchemy ORM
- Alembic for database migrations
- Comprehensive testing with pytest
- Type hints and Pydantic models
- OpenAPI documentation

### DevOps & CI/CD
- GitHub Actions for automated CI/CD
- Separate workflows for frontend and backend
- Automated testing on each PR
- Security scanning for dependencies
- Docker containerization
- Kubernetes deployment manifests
- Automated deployments to production

## 📋 Prerequisites

- Node.js 18+
- Python 3.11+
- Docker and Docker Compose
- Kubernetes cluster (for production deployment)
- PostgreSQL (for local development)

## 🛠 Local Development

### Backend Setup
```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your configurations

# Run migrations
alembic upgrade head

# Start development server
uvicorn app.main:app --reload
```

### Frontend Setup
```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

## 🧪 Running Tests

### Backend Tests
```bash
cd backend
pytest -v --cov
```

### Frontend Tests
```bash
cd frontend
npm test
```

## 🐋 Docker Development

```bash
# Build and run all services
docker-compose up --build

# Run specific service
docker-compose up backend
docker-compose up frontend
```

## 🚀 Deployment

### Prerequisites
- Kubernetes cluster
- kubectl configured
- GitHub Container Registry access

### Deployment Steps
```bash
# Apply Kubernetes configurations
kubectl apply -f kubernetes/

# Verify deployments
kubectl get deployments
kubectl get pods
kubectl get services
```

## 🔒 Security Features

- CORS configuration
- Environment variables management
- Kubernetes secrets for sensitive data
- Resource limits and quotas
- Health checks and probes
- Regular security scanning
- Dependency updates

## 📊 Monitoring and Logging

- Kubernetes liveness and readiness probes
- Health check endpoints
- Resource monitoring
- Application logs through Kubernetes

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📝 Development Workflow

1. Pull Requests are required for all changes
2. CI must pass before merging
3. Reviews required for all PRs
4. Squash merge for clean history
5. Delete branches after merging

## 📄 License

MIT

## 🔗 Architecture

```plaintext
├── frontend/                # React frontend
│   ├── src/                # Source code
│   ├── tests/              # Test files
│   └── Dockerfile          # Frontend container
├── backend/                # FastAPI backend
│   ├── app/                # Application code
│   ├── tests/              # Test files
│   └── Dockerfile          # Backend container
├── kubernetes/             # K8s manifests
└── .github/
    └── workflows/          # CI/CD pipelines
```

## ⚙️ Environment Variables

### Backend
- `POSTGRES_SERVER`: Database host
- `POSTGRES_USER`: Database user
- `POSTGRES_PASSWORD`: Database password
- `POSTGRES_DB`: Database name

### Frontend
- `REACT_APP_API_URL`: Backend API URL

## 👥 Support

For support, please open an issue in the repository.