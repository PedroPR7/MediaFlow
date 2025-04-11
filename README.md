# MediaFlow

MediaFlow is a media management system with separate API and client components.

## Prerequisites

- Docker
- Docker Compose
- Git

## Getting Started

1. Clone the repository with submodules:
```bash
git clone --recursive https://github.com/pointedsec/MediaFlow.git
```

2. Navigate to the project directory:
```bash
cd MediaFlow
```

3. Modify the `docker-compose.yml` file with the following environment variables:
```yml
 environment:
      PORT: 3000
      JWT_SECRET: "REPLACE WITH A SAME LENGTH JWT SECRET OR USE THE DEFAULT USED IN THE ORIGINAL FILE"
      GOOGLE_CLOUD_API_KEY: "YOUR_GOOGLE_CLOUD_API_KEY"
```

4. Start the application using Docker Compose:
```bash
docker compose up --build -d
```

This will start the following services:

- API (Backend) - Available at `http://localhost:3000`
- Client (Frontend) - Available at `http://localhost:5173`

# Development
To stop the services
```bash
docker compose down
```

To view logs:
```bash
docker compose logs -f
```

# Project Structure
```
MediaFlow/
├── api/          # Backend API service
├── client/       # Frontend client service
└── docker-compose.yml
```

# Contributing
- Fork the repository (Or api/client repository)
- Create your feature branch ( `git checkout -b feature/amazing-feature` )
- Commit your changes ( `git commit -m 'Add some amazing feature'` )
- Push to the branch ( `git push origin feature/amazing-feature` )
- Open a Pull Request

# License
This project is licensed under the MIT License - see the LICENSE file for details.