graph TD
    Users -->|HTTPS| CDN[CDN / Edge Cache]
    CDN --> LB[Load Balancer]
    LB --> API[API Gateway]
    API --> App[App Servers (Docker/K8s)]
    App --> Cache[Redis / Memcached]
    App --> Queue[RabbitMQ / Kafka]
    Cache --> DB[Database Cluster (PostgreSQL / MongoDB)]
