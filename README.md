# 🔗 Distributed URL Shortener Service

A scalable URL shortening service inspired by TinyURL and Bitly.

The application generates collision-resistant short URLs, supports analytics, custom aliases, URL expiration, and Redis caching for high-performance lookups.

---

## Features

- User Authentication
- Short URL Generation
- Custom Aliases
- URL Expiration
- Click Analytics
- RESTful APIs
- Redis Caching
- Dockerized Deployment
- Unit Testing

---

## System Architecture

```
                +-------------------+
                |      Client       |
                +---------+---------+
                          |
                     REST API
                          |
                +---------v----------+
                |   Spring Boot API  |
                +---------+----------+
                          |
        +-----------------+------------------+
        |                                    |
   Redis Cache                     PostgreSQL Database
```

---

## Tech Stack

| Layer | Technology |
|--------|------------|
| Backend | Spring Boot |
| Language | Java |
| Database | PostgreSQL |
| Cache | Redis |
| Testing | JUnit |
| Build Tool | Maven |
| Containerization | Docker |
| Version Control | Git |

---

## Key Components

### URL Generator

- Collision-resistant Short IDs
- Base62 Encoding

### Cache Layer

- Redis
- Frequently Accessed URLs

### Persistent Storage

- PostgreSQL
- URL Metadata
- Analytics

---

## REST API

| Method | Endpoint | Description |
|----------|---------------------|---------------------------|
| POST | /api/url | Shorten URL |
| GET | /{shortCode} | Redirect |
| GET | /api/analytics/{id} | URL Analytics |
| PUT | /api/url/{id} | Update URL |
| DELETE | /api/url/{id} | Delete URL |

---

## Database Schema

Tables

- Users
- URLs
- Analytics

---

## Project Structure

```
url-shortener/

controllers/
services/
repository/
models/
config/
security/
cache/
tests/

README.md
pom.xml
Dockerfile
docker-compose.yml
```

---

## Installation

Clone Repository

```bash
git clone https://github.com/yourusername/distributed-url-shortener.git
```

Run

```bash
docker-compose up --build
```

Run without Docker

```bash
mvn spring-boot:run
```

---

## Performance Optimizations

- Redis Caching
- Database Indexing
- Efficient Query Design
- Connection Pooling
- Layered Architecture

---

## Testing

- Unit Testing using JUnit
- Exception Handling
- API Validation
- Input Sanitization

---

## Future Enhancements

- QR Code Generation
- Rate Limiting
- URL Preview
- Distributed Load Balancing
- Kubernetes Deployment
- Monitoring with Prometheus & Grafana

---

## License

Developed for educational and portfolio purposes.
