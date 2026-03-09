# Organizapp

A scalable, modular application for managing tasks, finances, and automation.

## Project Overview
**Organizapp** is built with Laravel 11 and designed for seamless deployment to Hostinger via GitHub Actions.

### Core Features
-   **User Authentication**: Secure login/registration.
-   **Task Management**: Calendar-based task tracking.
-   **Finance Module**: Money movements and tracking.
-   **Automation**: Integration with n8n/webhooks.
-   **File Management**: Upload and organize files.

## Tech Stack
-   **Backend**: Laravel 11 (PHP 8.2+)
-   **Frontend**: Blade Templates + Alpine.js / Livewire
-   **Database**: MySQL
-   **Deployment**: GitHub Actions (FTP/SFTP)

## Project Rules & Architecture
See [.trae/rules.md](.trae/rules.md) for detailed coding standards and architectural guidelines.

## Setup Instructions

1.  **Install Dependencies**
    ```bash
    composer install
    npm install
    ```

2.  **Environment Setup**
    -   Copy `.env.example` to `.env` (already configured for MySQL).
    -   Create a MySQL database named `organizapp`.
    -   Run migrations:
        ```bash
        php artisan migrate
        ```

3.  **Run Development Server**
    ```bash
    php artisan serve
    npm run dev
    ```

## Deployment
Push to the `main` branch to trigger deployment (requires GitHub Actions configuration).
