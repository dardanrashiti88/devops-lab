# Simple Hello World Application

This is a simple full-stack application that demonstrates a basic setup with a Node.js backend and a React frontend, containerized with Docker and configured with CI/CD using GitHub Actions.

## Project Structure

```
.
├── backend/               # Node.js backend application
│   ├── Dockerfile        # Backend container configuration
│   ├── package.json      # Backend dependencies
│   └── src/             # Backend source code
│       └── index.js     # Main backend entry point
├── frontend/            # React frontend application
│   ├── Dockerfile      # Frontend container configuration
│   ├── package.json    # Frontend dependencies
│   └── src/           # Frontend source code
│       └── App.js     # Main frontend component
├── docker-compose.yml  # Multi-container Docker configuration
└── .github/           # GitHub Actions workflows
    └── workflows/
        └── main.yaml  # CI/CD pipeline configuration
```

## Prerequisites

- Docker
- Docker Compose
- Node.js (for local development)
- npm (for local development)

## Getting Started

### Running with Docker Compose

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. Start the application:
   ```bash
   docker-compose up --build
   ```

3. Access the application:
   - Frontend: http://localhost:3000
   - Backend: http://localhost:3001

### Local Development

#### Backend

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

#### Frontend

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

## CI/CD Pipeline

The project includes a GitHub Actions workflow that:

1. Builds both frontend and backend containers
2. Runs tests (if configured)
3. Pushes the images to Docker Hub (if configured)

The workflow is triggered on:
- Push to main branch
- Pull requests to main branch

## Docker Configuration

- Backend container runs on port 3001
- Frontend container runs on port 3000
- Both containers are configured with proper health checks
- Development and production configurations are separated

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details. 