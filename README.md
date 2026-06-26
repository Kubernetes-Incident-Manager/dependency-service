# Dependency Service

## Overview
The **Dependency Service** manages and tracks relationships between different systems, microservices, and infrastructure components. In the event of an incident, it helps identify potential downstream impacts and root causes by mapping out service dependencies.

## Features
- Manages a dependency graph of services and infrastructure.
- Provides APIs to query impacted systems during an incident.
- Built with Python and FastAPI.

## Getting Started

### Prerequisites
- Python 3.10+
- `pip` package manager
- Docker (optional for containerized deployment)

### Installation
1. Navigate to the service directory:
   ```bash
   cd services/dependency-service
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Service
To run the service locally for development:
```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

## Docker
Build the Docker image:
```bash
docker build -t incident-tracker/dependency-service .
```
Run the Docker container:
```bash
docker run -p 8000:8000 incident-tracker/dependency-service
```
