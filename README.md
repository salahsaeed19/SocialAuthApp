# My Django Project

This is a brief overview of my Django project, explaining the key modifications and features I've implemented.

## Introduction

My Django project is a web application that includes user authentication with Google login using the AllAuth library. Users can log in using their Google accounts and access various features of the application.

## Project Configuration

In `settings.py`, I made the following changes:

- Added the "users" app to the `INSTALLED_APPS` list.
- Configured Google authentication using the AllAuth library by adding the necessary settings in `SOCIALACCOUNT_PROVIDERS`.
- Set `DEFAULT_AUTO_FIELD` to use a BigAutoField for models.
- Added `AUTHENTICATION_BACKENDS` for AllAuth authentication.

## URL Configuration

In `urls.py`, I configured the following URL patterns:

- Admin interface: `admin/`
- AllAuth URLs for authentication: `accounts/`
- My custom app's URLs: `''` (the root URL)

## Custom App: "users"

I created a new Django app named "users" to handle user-related functionality.

- `templates/home.html`: This template includes a Google login link using AllAuth's `{% provider_login_url 'google' %}` template tag.
- `views.py`: Contains two views, one for rendering the home page and another for logging out users.

## Getting Started

To run this project locally, follow these steps:

1. Clone the repository.
2. Install the required dependencies.
3. Configure your database settings in `settings.py`.
4. Apply migrations and create database tables.
5. Run the development server.

Make sure to set up the necessary API keys and credentials for Google OAuth in your project settings.

## Dependencies

- Django
- AllAuth

## License

This project is licensed under the MIT License.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/salahsaeed19)
