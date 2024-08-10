
 
# Eventease

Eventease is a comprehensive platform that simplifies the process of creating, participating in, and sponsoring events. This repository houses both the frontend and backend codebases, enabling a seamless experience for all users involved.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
  - [Backend](#backend)
  - [Frontend](#frontend)
- [Configuration](#configuration)
  - [Frontend](#frontend-1)
  - [Backend](#backend-1)
- [API Endpoints](#api-endpoints)
- [Deployment](#deployment)
  - [Frontend](#frontend-2)
  - [Backend](#backend-2)
- [Contributing](#contributing)

## Overview

Eventease provides a seamless experience for users to create, participate in, and sponsor events. The platform is divided into two main parts:

- **Frontend:** Built with React, this part of the application provides a user-friendly interface for interacting with the platform.
- **Backend:** Powered by Django, this part of the application handles API requests, authentication, and data management.

## Features

### Frontend

- User-friendly interface for event management.
- Real-time feedback and notifications.
- Filtering events by categories.

### Backend

- Secure user authentication using JWT.
- Event creation, editing, and deletion.
- Participant and sponsorship management.
- Custom email verification for new users.
- API to support frontend interactions.

## Technologies Used

### Frontend

- React
- React Hook Form
- Toastify for notifications
- Vercel for deployment

### Backend

- Django
- PostgreSQL
- JWT for authentication
- Render for deployment

## Installation

### Backend

1. Clone the repository:

    ```bash
    git clone https://github.com/dipesh-db/Event_Ease.git
    cd Event_Ease/backend
    ```

2. Set up a virtual environment and activate it:

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up your PostgreSQL database and update `settings.py` with your database credentials.

5. Apply migrations:

    ```bash
    python manage.py migrate
    ```

6. Run the development server:

    ```bash
    python manage.py runserver
    ```

### Frontend

1. Install Dependencies:

    Ensure that Node.js and npm are installed on your computer, then run:

    ```bash
    npm install
    ```

2. Run the project locally:

    After the server is set up and running, execute:

    ```bash
    npm run dev
    ```

## Configuration

### Frontend

- Ensure that the API endpoints in your frontend are correctly pointing to your deployed backend.
- Update `vercel.json` if needed to handle routes properly for static hosting.

### Backend

- Update `settings.py` with your environment-specific settings.
- Ensure `ALLOWED_HOSTS` and `CORS_ALLOWED_ORIGINS` are configured properly for your deployment environment.
- Set up environment variables for sensitive information like `SECRET_KEY`, database credentials, and email configurations.

## API Endpoints

Key API endpoints include:

- **User Registration:** `/authentication/register/`
- **User Login:** `/authentication/login/`
- **Verify Email:** `/authentication/verify-email/`
- **Create Event:** `/events/create/`
- **Get Events:** `/events/get_events/`
- **Get User Created Events:** `/events/my_events/`
- **Delete Events:** `/events/delete_event/<int:event_id>/`
- **Edit Events:** `/events/edit_event/<int:event_id>/`
- **Participants:** `/participants/join/`
- **Sponsors:** `/sponsors/<int:event_id>/`

## Deployment

### Frontend

- The frontend is deployed on Vercel. Ensure that your `vercel.json` is configured correctly for routing.
- Push your code to the repository, and Vercel will automatically deploy your application.

### Backend

- The backend is deployed on Render. Push your code to the repository, connect to Render, and set up the necessary environment variables for deployment.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes. Make sure to write tests for any new features or bug fixes.

