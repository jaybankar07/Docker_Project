
# Docker Project

[![FastAPI CI](https://github.com/jaybankar07/Docker_Project/actions/workflows/ci.yml/badge.svg)](https://github.com/jaybankar07/Docker_Project/actions/workflows/ci.yml)

A simple FastAPI project with Docker containerization and automated testing using Pytest and GitHub Actions.

## Technologies Used

- Python 3.11
- FastAPI
- Uvicorn
- Docker
- Pytest
- GitHub Actions

## Project Structure

```text
Docker_Project/
│
├── main.py
├── requirements.txt
├── Dockerfile
├── tests/
│   └── test_main.py
│
└── .github/
    └── workflows/
        └── ci.yml
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/jaybankar07/Docker_Project.git
cd Docker_Project
```

### 2. Create Virtual Environment

```bash
python -m venv .venv
```

### 3. Activate Virtual Environment

**Windows:**

```bash
.venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

## Run the Application

```bash
uvicorn main:app --reload
```

Open your browser:

```text
http://127.0.0.1:8000/docs
```

## Run Tests

```bash
python -m pytest tests/test_main.py -v
```

## Docker Setup

### Build Docker Image

```bash
docker build -t fastapi-app .
```

### Run Docker Container

```bash
docker run -d -p 8000:8000 --name fastapi-container fastapi-app
```

### Check Running Containers

```bash
docker ps
```

### Stop Container

```bash
docker stop fastapi-container
```

## GitHub Actions

This project uses GitHub Actions to automatically run tests whenever code is pushed to the repository.

The CI workflow helps ensure that the application is working correctly.

## Author

**Jay Bankar**

GitHub: [@jaybankar07](https://github.com/jaybankar07)
