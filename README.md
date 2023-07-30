# full-stack container project for TinyPLM
Full - Stack Library

- Go-Lang for API
- Next.js with Tailwind CSS for UI
- Redis for Cache and Queue
- Minio for Object Storage
- Postgres for DB

### Inspiration

https://github.com/AleksK1NG/Go-Clean-Architecture-REST-API/tree/master

### Go-Lang for API

1. Go Gin Web APi - https://github.com/gin-gonic/gin
2. SQL-C - ORM - https://github.com/sqlc-dev/sqlc
3. Postgres Driver - https://github.com/jackc/pgx
4. [viper](https://github.com/spf13/viper) - Go configuration with fangs
5. [go-redis](https://github.com/go-redis/redis) - Type-safe Redis client for Golang
6. [zap](https://github.com/uber-go/zap) - Logger
7. [validator](https://github.com/go-playground/validator) - Go Struct and Field validation
8. [jwt-go](https://github.com/dgrijalva/jwt-go) - JSON Web Tokens (JWT)
9. [uuid](https://github.com/google/uuid) - UUID
10. [migrate](https://github.com/golang-migrate/migrate) - Database migrations. CLI and Golang library.
11. [minio-go](https://github.com/minio/minio-go) - AWS S3 MinIO Client SDK for Go


| Health Check   | Text        | https://codewithyury.com/how-to-create-health-check-for-restful-microservice-in-golang/      |
| Readiness   | Text        | And more      |
| Liveliness   | Text        | And more      |
| Open API 3   | Text        | And more      |
| JWT Auth   | Text        | And more      |
| Graceful Shutdown   | Text        | And more      |
| Go Docker Container with Compression, Security, Distroless  | Text        | And more      |

### Commands

    # start detached
    docker-compose up -d

    # Stop services only
    docker-compose stop

    # Stop and remove containers, networks..
    docker-compose down 

    # Down and remove volumes
    docker-compose down --volumes 

    # Down and remove images
    docker-compose down --rmi <all|local> 
    
#### Recomendation for local development most comfortable usage:
    make local // run all containers
    make run // it's easier way to attach debugger or rebuild/rerun project

#### 🙌👨‍💻🚀 Docker-compose files:
    docker-compose.local.yml - run postgresql, redis, aws, prometheus, grafana containrs
    docker-compose.dev.yml - run docker development environment

### Docker development usage:
    make docker

### Local development usage:
    make local
    make run
