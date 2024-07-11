
# Flask CI/CD Pipeline with Docker

This repository contains a simple Flask application that is set up with a CI/CD pipeline using GitHub Actions and Docker. The pipeline installs dependencies, runs tests, builds a Docker image, and deploys the application.

## Project Structure

```
flask-ci-cd/
│
├── app.py                  # The main Flask application
├── requirements.txt        # Python dependencies
├── Dockerfile              # Dockerfile to containerize the Flask application
├── test_app.py             # Test file for the Flask application
├── .github/
│   └── workflows/
│       └── ci-cd.yml       # GitHub Actions workflow configuration
└── README.md               # This README file
```

## Getting Started

### Prerequisites

- Python 3.12
- Docker
- Git

### Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/elbachir-salik/flask-ci-cd.git
   cd flask-ci-cd
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**:
   - On Windows:
     ```bash
     .\venv\Scripts\activate
     ```
   - On macOS and Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

1. **Run the Flask application**:
   ```bash
   python app.py
   ```

2. **Access the application**:
   Open your web browser and go to `http://localhost:5000`.

### Running Tests

1. **Run the tests**:
   ```bash
   pytest
   ```

### Docker

1. **Build the Docker image**:
   ```bash
   docker build -t flask-docker-ci-cd .
   ```

2. **Run the Docker container**:
   ```bash
   docker run -d -p 8080:5000 --name flask_container flask-docker-ci-cd
   ```

3. **Access the application in Docker**:
   Open your web browser and go to `http://localhost:8080`.

### CI/CD Pipeline

The CI/CD pipeline is set up using GitHub Actions. It performs the following steps:
1. Checks out the code.
2. Sets up the Python environment.
3. Installs dependencies.
4. Runs tests.
5. Builds the Docker image.


The pipeline is triggered on every push to the `master` branch and on pull requests to the `master` branch.

### Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes.

### License

This project is licensed under the MIT License.
