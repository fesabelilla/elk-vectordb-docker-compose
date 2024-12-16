# ELK Stack Docker Compose

## Prerequisites
- Docker
- Docker Compose

## Setup

### 1. Clone Repository
```bash
git clone <repository-url>
cd elk-docker-stack
```

### 2. Prepare System
```bash
# Increase max map count for Elasticsearch
sudo sysctl -w vm.max_map_count=262144
```

### 3. Start ELK Stack
```bash
# Start services
docker-compose up -d

# Check running containers
docker-compose ps
```

## Services
- **Elasticsearch**: `localhost:9200`
- **Kibana**: `localhost:5601`
- **Logstash**: `localhost:5044`, `localhost:5000`

## Useful Commands
```bash
# Stop services
docker-compose down

# View logs
docker-compose logs [service]
```

## Notes
- Not for production use
- Requires minimum 4GB RAM
- Security features are disabled

## Troubleshooting
- Check logs: `docker-compose logs`
- Verify network: `docker network ls`
