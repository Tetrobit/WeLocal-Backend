# WeLocal Backend Services

This repository contains the backend services for the WeLocal platform, a comprehensive solution for local community management and services.

## Services Overview

The platform consists of the following microservices:

1. **Ecology Service** (`welocal-ecology-service`)
   - Port: 8081
   - Manages environmental initiatives and monitoring

2. **Freemarket Service** (`welocal-freemarket-service`)
   - Port: 8082
   - Handles local marketplace and trading

3. **Small Business Service** (`welocal-small-business-service`)
   - Port: 8083
   - Manages local business listings and operations

4. **Farmers Service** (`welocal-farmers-service`)
   - Port: 8084
   - Handles agricultural and farming-related services

5. **Transport Service** (`welocal-transport-service`)
   - Port: 8085
   - Manages local transportation and logistics

6. **Local Services Service** (`welocal-local-services-service`)
   - Port: 8086
   - Handles various local community services

7. **Polls Service** (`welocal-polls-service`)
   - Port: 8087
   - Manages community polls and voting

## Infrastructure

The platform uses the following infrastructure components:

- **PostgreSQL**: Main database (Port: 5432)
- **Zabbix**: Monitoring system
  - Server (Port: 10051)
  - Web Interface (Port: 8080)

## Prerequisites

- Docker
- Docker Compose
- Git

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-backend.git
   cd welocal-backend
   ```

2. Initialize Git submodules:
   ```bash
   git submodule update --init --recursive
   ```

3. Start the services:
   ```bash
   docker-compose up -d
   ```

## Service Access

- PostgreSQL: `localhost:5432`
- Zabbix Web Interface: `http://localhost:8080`
- Ecology Service: `http://localhost:8081`
- Freemarket Service: `http://localhost:8082`
- Small Business Service: `http://localhost:8083`
- Farmers Service: `http://localhost:8084`
- Transport Service: `http://localhost:8085`
- Local Services Service: `http://localhost:8086`
- Polls Service: `http://localhost:8087`

## Database Configuration

Default database credentials:
- Username: `welocal`
- Password: `welocal123`
- Database: `welocal`

## Monitoring

The platform is monitored using Zabbix:
- Default Zabbix credentials:
  - Username: `Admin`
  - Password: `zabbix`

## Development

Each service is a separate Git submodule. To work on a specific service:

1. Navigate to the service directory:
   ```bash
   cd welocal-{service-name}-service
   ```

2. Make your changes and commit them:
   ```bash
   git add .
   git commit -m "Your changes"
   git push
   ```

3. Update the main repository:
   ```bash
   cd ..
   git add welocal-{service-name}-service
   git commit -m "Update {service-name} service"
   git push
   ```

## Service Dependencies

All services depend on:
- PostgreSQL database
- Zabbix monitoring system

## Health Checks

Each service includes health check endpoints:
- `/actuator/health` - Basic health status
- `/actuator/info` - Service information
- `/actuator/metrics` - Service metrics

## Logging

Logs can be accessed using Docker:
```bash
docker-compose logs -f [service-name]
```

## Troubleshooting

1. Check service status:
   ```bash
   docker-compose ps
   ```

2. View service logs:
   ```bash
   docker-compose logs [service-name]
   ```

3. Restart a service:
   ```bash
   docker-compose restart [service-name]
   ```

4. Rebuild a service:
   ```bash
   docker-compose up -d --build [service-name]
   ```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 