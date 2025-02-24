# Gas Utility Service - Django Application

## Overview
A gas utility company is experiencing a high volume of customer service requests, leading to long wait times and poor service. This Django application aims to streamline customer service by allowing users to submit and track service requests online while also managing customer accounts efficiently.

## Features

### 1. **Customer Service Requests**
- Customers can submit service requests online.
- Ability to select the type of service request.
- Provide details about the request and attach relevant files.

### 2. **Request Tracking**
- Customers can track the status of their requests.
- View the request submission date, time, and resolution updates.

### 3. **Customer Management**
- Store and manage customer details securely.
- Enable representatives to manage and respond to service requests.

### 4. **Admin Dashboard**
- View and manage all service requests.
- Assign and track request resolutions.

### 5. **User Authentication & Authorization**
- Secure login and registration system.
- Role-based access control (Customer, Admin, Support Representative).

## Tech Stack
- **Backend:** Django, Django REST Framework
- **Frontend:** Django Templates / React (optional)
- **Database:** PostgreSQL / SQLite (for development)
- **Authentication:** Django Authentication System
- **Deployment:** Docker, AWS/GCP (optional)

## Project Structure
```
├── gas_utility_service/
│   ├── manage.py              # Django management script
│   ├── config/                # Django project settings
│   │   ├── settings.py        # Project settings
│   │   ├── urls.py            # Root URL configuration
│   │   ├── wsgi.py            # WSGI entry point
│   │   ├── asgi.py            # ASGI entry point (optional)
│   ├── apps/
│   │   ├── users/             # User authentication and management
│   │   ├── requests/          # Service request handling
│   │   ├── support/           # Customer support features
│   ├── templates/             # HTML templates (if using Django templates)
│   ├── static/                # Static files (CSS, JS, images)
│   ├── requirements.txt       # Python dependencies
│   ├── Dockerfile             # Docker configuration
│   ├── README.md              # Project documentation
```

## Installation & Setup

### Prerequisites
- Python 3.x
- Django
- PostgreSQL (or SQLite for local development)

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/gas-utility-service.git
   cd gas-utility-service
   ```
2. Create and activate a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Apply migrations and start the server:
   ```sh
   python manage.py migrate
   python manage.py runserver
   ```

## API Endpoints (if using Django REST Framework)
| Endpoint | Method | Description |
|----------|--------|-------------|
| /api/auth/login/ | POST | User login |
| /api/auth/register/ | POST | User registration |
| /api/requests/ | GET, POST | List and create service requests |
| /api/requests/{id}/ | GET, PUT, DELETE | Retrieve, update, or delete a request |

## Deployment
- Use Docker for containerization:
  ```sh
  docker build -t gas-utility-service .
  docker run -p 8000:8000 gas-utility-service
  ```
- Deploy on AWS/GCP using services like Elastic Beanstalk or App Engine.

## Contributing
Feel free to fork the repository and submit pull requests.

## License
This project is licensed under the MIT License.

