# Full-Stack Portfolio Web Application

A containerized full-stack web application that dynamically displays portfolio information using a Python Flask REST API and a JavaScript frontend.

The project demonstrates frontend/backend integrations, REST API communication, Docker containerization, and reverse proxy configuration.

## Technologies Used
- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Python, Flask, REST API
- **Web Server:** Nginx
- **Containerization:** Docker, Docker Compose
- **Development Environment:** Linux, CloudLab

## Key Features
- Responsive portfolio interface displaying education, professional experience, and personal information.
- JavaScript-powered dynamic content retrieval from a Flask API.
- REST API providing structured JSON responses.
- Separate frontend and backend Docker containers.
- Nginx reverse proxy for routing API requests.
- Nginx reverse proxy for routing API requests.

## Application Architecture
The application consists of two independent services:
**Frontend -- Nginx + JavaScript**
Serves the portfolio website and retrieves data from the backend using HTTP requests.
**Backend -- Python + Flask**
Exposes a REST API that returns structured JSON data for the frontend to display.
**Request Flow**
Browser -> Nginx Frontend -> Flask REST API -> JSON Response -> Dynamic Page Rendering
Docker compose manages the services and provides internal networking between containers.

## Running the Application
[![Watch Demo](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://youtu.be/RwlQMWQInWk)

**Prerequisites:** Docker and Docker Compose.
Clone the repository:
```bash
git clone https://github.com/mclark-99/fullstack-portfolio-app.git
```

cd into project folder
```bash
cd fullstack-portfolio-app
ls
```

Run the setup script:
```bash
bash scripts/setup-cloudlab.sh
```

Build and start the containers:
```bash
sudo docker compose up --build
```

Verify the services in a new CloudLab terminal:
```bash
curl localhost:8000/api
curl localhost:3000
```

Find Cloudlab Hostname
```bash
hostname -f
```

Run in a new terminal (locally, not on CloudLab)
```bash
ssh -L 3000:localhost:3000 <your-username>@<your-cloudlab-hostname>
```

Open the application:
http://localhost:3000

## Technical Implementation
# Frontend Development
Built the user interface using HTML and CSS, with JavaScript responsible for retrieving and rendering data returned by the backend.

# Backend Development
Implemented a Flask API to provide structured data through HTTP requests.

# Containerization
Created separate Dockerfiles for the frontend and backend and used Docker Compose to coordinate service startup and networking.

# Reverse Proxy
Configured Nginx to serve static frontend assets and forward API requests to the Flask backend using Docker service-name resolution.


## Future Improvements
- Add interactive portfolio sections and project showcases.
- Implement automated testing for API endpoints.
- Introduce CI/CD workflows using GitHub Actions.
- Deploy the application to a publicly accessible hosting environment.

## Author
Maiti F. Clark
M.S. Computer Science -- West Chester University
Expected Graduation: December 2026
