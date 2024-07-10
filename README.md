# NoteApp

NoteApp is a simple note-taking web application. It allows users to create, view, and manage notes. The backend is built using Django and Django REST Framework, while the frontend is built using React.js. The application is containerized using Docker and orchestrated with Docker Compose.

## Features

- Create new notes
- View existing notes
- Responsive and user-friendly interface

## Prerequisites

- Docker
- Docker Compose

## Technologies Used

- **Backend**: Django, Django REST Framework
- **Frontend**: React.js
- **Database**: PostgreSQL
- **Containerization**: Docker, Docker Compose

## Getting Started

### Running Locally

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/noteapp.git
    cd noteapp
    ```

2. **Create environment files:**

    - **Backend Environment Variables**: Create a file named `.env` in the `backend` directory with the following content:

        ```bash
        POSTGRES_DB=noteapp
        POSTGRES_USER=noteapp_user
        POSTGRES_PASSWORD=noteapp_password
        DJANGO_SECRET_KEY=your_secret_key
        DJANGO_DEBUG=True
        DATABASE_URL=postgres://noteapp_user:noteapp_password@db:5432/noteapp
        ```

    - **Frontend Environment Variables**: Create a file named `.env` in the `frontend` directory with the following content:

        ```bash
        REACT_APP_API_URL=http://localhost:8000/api
        ```

3. **Build and run the containers:**

    Navigate to the root directory and run:

    ```bash
    docker-compose up --build
    ```

4. **Access the application:**

    - The frontend can be accessed at `http://localhost:3000`.
    - The backend AaPI can be accessed at `http://localhost:8000/api/notes/`.

