---
sidebar_position: 2
sidebar_label: Developement (for backend)
tags:
   - architecture
   - backend
---

# Development

This is the environment configured for **backend team** to develop. It'll setup db, caching and other infrastructures to run the backend code. To run the application in development mode, please follow these steps:

### Step 1:

Copy file `composes/.env.example` into `composes/.env`.

### Step 2:

Run the following command in the terminal:

```bash
docker-compose -f "composes/dev.yml" up -d
```
