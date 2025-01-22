# Docker Compose Project

This project sets up a Docker Compose environment with Redis, MongoDB, and MySQL, all connected to a single network. Each service has volume persistence to ensure data is retained across container restarts.

## Services

- **Redis**: An in-memory data structure store, used as a database, cache, and message broker.
- **MongoDB**: A NoSQL database that uses a document-oriented data model.
- **MySQL**: A relational database management system based on SQL.

## Getting Started

### Prerequisites

- Docker installed on your machine.
- Docker Compose installed.

### Setup

1. Clone the repository or download the project files.
2. Navigate to the project directory:
   ```
   cd docker-compose-project
   ```
3. Start the services using Docker Compose:
   ```
   docker-compose up -d
   ```

### Accessing the Services

- **Redis**: Accessible on port `6379`.
- **MongoDB**: Accessible on port `27017`.
- **MySQL**: Accessible on port `3306`.

### Stopping the Services

To stop the services, run:
```
docker-compose down
```

### Volume Persistence

Data for each service is stored in volumes, ensuring that data is not lost when containers are stopped or removed. You can find the volumes in the Docker volumes directory on your host machine.

## License

This project is licensed under the MIT License.