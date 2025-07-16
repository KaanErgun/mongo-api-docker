# Mongo API Docker Compose

This project runs the following services together using Docker Compose:

- **MongoDB** (database)  
- **Node.js + Express + Mongoose API** (secure REST API access to MongoDB)

---

## Getting Started

### Requirements

- Docker  
- Docker Compose  
- Git  

---

## Installation

### 1. Clone the repository

"""bash
git clone https://github.com/KaanErgun/mongo-api-docker.git
cd mongo-api-docker
"""

### 2. Create the environment variables file

Copy `env.template` to `.env` and edit it as needed:

"""bash
cp env.template .env
nano .env
"""

**Example variables:**

"""env
MONGO_INITDB_ROOT_USERNAME=kts-admin
MONGO_INITDB_ROOT_PASSWORD=Zamazingo.987
MONGO_DB_NAME=mydb
MONGO_PORT=27017
API_PORT=3000
"""

> **Important:** Do not share your `.env` file! It is included in `.gitignore`.

---

### 3. Start the services with Docker Compose

"""bash
docker-compose up -d
"""

- This will start MongoDB and the API services.  
- MongoDB data is persisted in the `mongo_data/` folder.

---

## Usage

### API Health Check

"""bash
curl http://localhost:3000/
"""

Expected response:

"""
API is running!
"""

---

### Add a User

"""bash
curl -X POST http://localhost:3000/api/users \
  -H "Content-Type: application/json" \
  -d '{"name":"Ali","email":"ali@example.com"}'
"""

---

### List Users

"""bash
curl http://localhost:3000/api/users
"""

---

## Access MongoDB Shell

"""bash
docker exec -it mymongo mongosh -u $MONGO_INITDB_ROOT_USERNAME -p $MONGO_INITDB_ROOT_PASSWORD --authenticationDatabase admin
"""

---

## Project Structure

"""
.
├── docker-compose.yml
├── env.template
├── .gitignore
└── mongo_data/      # MongoDB persistent data folder
"""

---

## Security Notes

- Store sensitive info in `.env` and never share it.  
- Do not expose MongoDB directly to the internet; access only through API.  
- Future improvements can include JWT auth, rate limiting, and HTTPS.

---

## Contact and Contribution

Feel free to reach out or contribute via GitHub @KaanErgun.

---

## License

MIT License
