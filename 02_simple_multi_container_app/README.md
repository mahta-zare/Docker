A simple Python Flask app with MySQL backend as database. 

The requirements are Flask and `mysql-connector-python` because the code imports `mysql.connector` which needs pure python and no system deps.

To run the container:

```bash
docker compose up --build -d
```
Here is a table of common services and their port number:

| Port            | Service                                                   | Description                |
| --------------- | --------------------------------------------------------- | -------------------------- |
| **22**          | SSH                                                       | Remote login to servers    |
| **80**          | HTTP                                                      | Standard web traffic       |
| **443**         | HTTPS                                                     | Secure web traffic         |
| **3306**        | MySQL                                                     | MySQL database             |
| **5432**        | PostgreSQL                                                | PostgreSQL database        |
| **6379**        | Redis                                                     | In-memory data store       |
| **27017**       | MongoDB                                                   | MongoDB database           |
| **5000 / 8000** | Flask / FastAPI / general dev servers                     | Common for Python web apps |
| **8080**        | Alternate HTTP port (often used by web servers in Docker) |                            |
| **3000**        | Node.js / React dev server                                |                            |
| **9200**        | Elasticsearch                                             |                            |
| **9092**        | Kafka                                                     |                            |
| **15672**       | RabbitMQ management UI                                    |                            |


There are convention-based paths inside containers for popular services, ususally matching their default Linux installation paths.

### Rules of thumb

- Anything under `/var/lib/...` → persistent data storage.

- Anything under `/usr/share/...` → static files or web content.

- Anything under `/etc/...` → configuration files.