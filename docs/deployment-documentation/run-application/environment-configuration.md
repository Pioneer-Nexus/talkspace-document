---
sidebar_position: 1
sidebar_label: Configuration
tags:
   - instruction
   - deployment
---

# Environment configuration

Before running the application, we need to add the configuration file by copying file `composes/.env.example` into `composes/.env`.

### Configuration file explaination

The configuration is stored to the `.env` file in `composes/`.

```bash
COLLECTOR_ZIPKIN_HTTP_PORT=9411
COLLECTOR_OTLP_ENABLED=true

MONGODB_INITDB_ROOT_USERNAME=admin
MONGODB_INITDB_ROOT_PASSWORD=password

DB_CONNECTION_STRING=mongodb://mongo:27017/talkspace
ENV=local
HOST=localhost
PORT=9000

JWT_SECRET=secret
JWT_EXPIRED=86400 # unit: seconds
JWT_REFRESH_EXPIRED=86400 # unit: seconds

TIME_ZONE=Asia/Ho_Chi_Minh

TRACING_URL=http://tracing:14268/api/traces
ELASTICSEARCH_URL=http://elasticsearch:9200

REDIS_URL=redis://cache:6379
```

**Configuration meaning:**

| Field                            | Description                                    |
| -------------------------------- | ---------------------------------------------- |
| **MONGODB_INITDB_ROOT_USERNAME** | root username for mongodb                      |
| **MONGODB_INITDB_ROOT_PASSWORD** | root password for mongodb                      |
| **DB_CONNECTION_STRING**         | connection string for backend to connect to db |
| **ENV**                          | backend environment                            |
| **HOST**                         | host of the backend                            |
| **PORT**                         | port in which backend server running           |
| **JWT_SECRET**                   | jwt secret key                                 |
| **JWT_EXPIRED**                  | jwt access token expiration in seconds         |
| **JWT_REFRESH_EXPIRED**          | jwt refresh token expiration in seconds        |
| **TIME_ZONE**                    | time zone of the backend                       |
| **TRACING_URL**                  | tracing url                                    |
| **ELASTICSEARCH_URL**            | elastic search url                             |
| **REDIS_URL**                    | redis url                                      |