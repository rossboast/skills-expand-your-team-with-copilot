# Mergington High School Activities

A FastAPI web application that allows teachers to manage extracurricular activities and register students for them.

## Features

### Activity Management
- View all available extracurricular activities with details
- Browse activities by multiple categories (Sports, Arts, Academic, Community, Technology)
- Filter activities by day of the week (Monday-Sunday)
- Filter activities by time slot (Before School, After School, Weekend)
- Search activities by name or description

### Teacher Authentication
- Teacher login/logout system
- Secure authentication required for student registration actions

### Student Registration
- Teachers can register students for activities (via email)
- Teachers can unregister students from activities
- View current participant counts for each activity
- Prevent duplicate registrations

## API Endpoints

| Method | Endpoint                                                          | Description                                                         |
| ------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Get all activities with optional filters (day, start_time, end_time) |
| GET    | `/activities/days`                                                | Get list of all days that have activities scheduled                 |
| POST   | `/activities/{activity_name}/signup?email=student@mergington.edu&teacher_username=username` | Sign up a student for an activity (requires teacher authentication) |
| POST   | `/activities/{activity_name}/unregister?email=student@mergington.edu&teacher_username=username` | Remove a student from an activity (requires teacher authentication) |
| POST   | `/auth/login?username=username&password=password`                 | Login as a teacher                                                  |
| GET    | `/auth/check-session?username=username`                           | Check if a teacher session is valid                                 |

> [!IMPORTANT]
> All data is stored in memory, which means data will be reset when the server restarts.

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
