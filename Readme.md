# LMS API Backend

This is a robust backend service for a Learning Management System (LMS) built with Django and Django REST Framework (DRF). It provides a secure API to manage educational content, track student progress, and handle interactive quizzes.

## Key Features

- **Educational Content Management**: Create and manage Courses, Lessons, and Quizzes with custom ordering and prerequisite tracking.
- **User Progress Tracking**: Monitor student engagement, lesson completions, and quiz attempts with detailed score reporting.
- **Secure Authentication**: Built-in JSON Web Token (JWT) authentication for secure access.
- **Cross-Origin Support**: Pre-configured CORS settings for seamless integration with frontend applications (e.g., React, Vue, Next.js).

## Tech Stack

- **Framework**: Django, Django REST Framework
- **Authentication**: `djangorestframework-simplejwt`
- **Database**: SQLite (Development) / PostgreSQL-ready
- **CORS Management**: `django-cors-headers`

## Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AbdlKabeer/lms-api-backend.git
   cd lms-api-backend
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run database migrations:**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional):**
   ```bash
   python manage.py createsuperuser
   ```

6. **Start the development server:**
   ```bash
   python manage.py runserver
   ```

## Core Models

- **Course**: The main educational module containing lessons.
- **Lesson**: Individual sections within a course. Supports content, summaries, and prerequisites.
- **Quiz / Question / Option**: Assessment tools linked to lessons.
- **UserProgress**: Tracks completed lessons and current status for users.
- **QuizAttempt / QuizResponse**: Records user scores and answers for quizzes.

## API Architecture

The application is structured into key modular apps:
- `api`: Contains the core learning and tracking logic.
- `account`: Manages user authentication, profiles, and permissions.

## License

This project is licensed under the MIT License.