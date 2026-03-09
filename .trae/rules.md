# Trae Project Rules

## Objective
Build a scalable, maintainable application named **Organizapp** designed for seamless deployment to Hostinger via GitHub.

## Core Principles
1.  **Hostinger Compatibility**: The stack must run natively on Hostinger (standard PHP/MySQL environment).
2.  **GitHub Deployment**: Code changes are pushed to GitHub. Deployment should be automated via GitHub Actions or Hostinger's Git integration.
3.  **Modularity**: The app must be modular to support evolving features (Tasks, Finance, Automation).
4.  **Scalability**: Database schema and logic designed for growth.

## Tech Stack
-   **Backend**: PHP 8.2+ (Laravel 11).
-   **Frontend**: Blade + Livewire / Alpine.js.
-   **Database**: MySQL / MariaDB.
-   **Queue/Jobs**: Database driver (for Hostinger compatibility).

## Architecture Guidelines
-   **Modular Structure**:
    -   Use `app/Services` for business logic (e.g., `TaskService`, `FinanceService`).
    -   Use `app/Repositories` for complex data access if needed.
    -   Keep Controllers thin; delegate logic to Services.
-   **Database**:
    -   Use Migrations for all schema changes.
    -   Use Seeders for initial data.
-   **Configuration**:
    -   All environment-specific config in `.env`.
    -   Never commit secrets.

## Deployment Workflow
1.  Develop locally.
2.  Commit and push to GitHub `main`.
3.  GitHub Action triggers deployment (FTP/SFTP) to Hostinger.
4.  Run `php artisan migrate --force` on production if needed (via SSH or route).
