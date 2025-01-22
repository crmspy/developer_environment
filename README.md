# Docker Compose for Developers

This repository provides an easy-to-use Docker Compose configuration that helps developers quickly set up their development environment. The configuration includes the following services:

- **Redis**: In-memory data structure store, used as a database, cache, and message broker.
- **MySQL**: A widely used open-source relational database management system.
- **Jupyter Notebook**: An open-source web application for creating and sharing documents containing live code, equations, visualizations, and narrative text.
- **MongoDB**: A document-oriented NoSQL database for modern applications.

## Prerequisites

Make sure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1. **Clone the Repository**  
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Start the Services**  
   Run the following command to start all services:
   ```bash
   docker-compose up -d
   ```

3. **Access the Services**  
   - Redis: Connect using `localhost:6379`
   - MySQL: Access on `localhost:3306` with credentials set in the `docker-compose.yml`
   - Jupyter Notebook: Open [http://localhost:8888](http://localhost:8888) in your browser
   - MongoDB: Connect using `localhost:27017`

4. **Stop the Services**  
   To stop the running services, use:
   ```bash
   docker-compose down
   ```

## Configuration

You can modify the `docker-compose.yml` file to customize the configuration, such as database credentials, ports, and volumes.

### Example MySQL Configuration
```yaml
environment:
  MYSQL_ROOT_PASSWORD: root_password
  MYSQL_DATABASE: my_database
  MYSQL_USER: user
  MYSQL_PASSWORD: developer
```

### Example Jupyter Notebook Token
The default token for Jupyter Notebook is shown in the logs. To specify your own token, you can update the `docker-compose.yml` file:
```yaml
command: jupyter notebook --NotebookApp.token='your_token'
```

## Volumes

Persistent data for each service is stored in Docker volumes. You can find them under the `volumes` section of the `docker-compose.yml`.

## Troubleshooting

- If you encounter any issues, check the logs with:
  ```bash
  docker-compose logs
  ```
- Make sure the required ports are not already in use.

## License

This repository is licensed under the MIT License. Feel free to use and modify as needed.

---

Happy coding! 🎉
