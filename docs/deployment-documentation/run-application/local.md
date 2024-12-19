---
sidebar_position: 3
sidebar_label: Local (for frontend)
tags:
   - architecture
   - backend
---

# Local environment

This is the environment configured for **frontend team** to develop frontend application. It'll run both backend and its infrastructures to run the backend application. To run the application in local mode, please follow these steps:

### Step 1:

Copy file `composes/.env.example` into `composes/.env`.

### Step 2:

Run the following command in the terminal:

```bash
docker-compose -f "composes/dev.yml" up -d
```
