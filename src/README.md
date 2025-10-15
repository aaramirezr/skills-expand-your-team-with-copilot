# Mergington High School Activities

A comprehensive web application that allows students to view and register for extracurricular activities at Mergington High School, with teacher authentication for managing registrations.

## Features

### For Students
- **View Activities**: Browse all available extracurricular activities with detailed information
- **Advanced Filtering**: 
  - Filter activities by category (Sports, Arts, Academic, Community, Technology)
  - Filter by day of the week (Monday-Sunday)
  - Filter by time (Before School, After School, Weekend)
- **Search Functionality**: Search for activities by name or description
- **Activity Details**: View schedule, description, participant count, and maximum capacity for each activity

### For Teachers
- **Authentication System**: Secure login for teachers to manage student registrations
- **Sign Up Students**: Register students for activities (requires teacher authentication)
- **Unregister Students**: Remove students from activities (requires teacher authentication)
- **Session Management**: Maintain login sessions for seamless management

## Technology Stack

- **Backend**: FastAPI - Modern, high-performance Python web framework
- **Database**: MongoDB - Document database for storing activities and teacher accounts
- **Frontend**: Vanilla JavaScript with HTML/CSS
- **Authentication**: Password hashing with Argon2
- **Server**: Uvicorn ASGI server

## API Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| GET | `/activities` | Get all activities with optional filters (day, start_time, end_time) | No |
| GET | `/activities/days` | Get list of all days that have activities scheduled | No |
| POST | `/activities/{activity_name}/signup` | Sign up a student for an activity | Yes (Teacher) |
| POST | `/activities/{activity_name}/unregister` | Remove a student from an activity | Yes (Teacher) |
| POST | `/auth/login` | Login a teacher account | No |
| GET | `/auth/check-session` | Check if a session is valid | No |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
