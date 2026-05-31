# Covid-TMS — COVID-19 Test Management System

A web-based application for managing COVID-19 testing end to end — user registration, test result tracking, and reporting. Built to streamline operations for clinics and health authorities through centralized test data management.


## Overview

During the COVID-19 pandemic, clinics and health authorities needed a reliable way to register people for testing, record results, and report on testing activity. Covid-TMS provides a centralized web platform that brings these workflows together — reducing manual paperwork and giving administrators a single place to manage test data.

## Problem

- Test registration and result tracking were often handled manually or across disconnected systems.
- Clinics and health authorities lacked a centralized view of testing data for reporting.
- Distributing and recording results reliably was slow and error-prone.

Covid-TMS addresses these by centralizing registration, result tracking, and reporting in one web application.

## Key Features

- **User registration** — Register individuals for COVID-19 testing.
- **Test result tracking** — Record and update test results against registered users.
- **Reporting** — Generate reports on testing activity for clinics and health authorities.
- **Centralized data management** — A single platform for managing test data across operations.
- **Web-based access** — Accessible through a browser for staff and administrators.

## System Architecture

A classic server-rendered web architecture with a PHP application layer and a SQL database, hosted on AWS.

```
        +-------------------+
        |      Users        |
        | (Clinic staff /   |
        |  administrators)  |
        +---------+---------+
                  |  HTTPS
                  v
        +-------------------+
        |   Frontend        |
        |  HTML, CSS/SCSS,  |
        |  JavaScript       |
        +---------+---------+
                  |  Request / Response
                  v
        +-------------------+
        |   Application     |
        |   Layer (PHP)     |
        +---------+---------+
                  |  SQL queries
                  v
        +-------------------+
        |   SQL Database    |
        +---------+---------+
                  |
                  v
        +-------------------+
        |   Hosting: AWS    |
        +-------------------+
```

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | HTML, CSS, SCSS, JavaScript |
| Backend | PHP |
| Database | SQL |
| Hosting / Cloud | AWS |

## Getting Started

### Prerequisites

- PHP (with a local server such as XAMPP, or PHP's built-in server)
- A SQL database (e.g. MySQL)
- A modern web browser

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/kulkarni1973onkar/Covid-TMS-Covid-Test-Management-System-.git
   cd Covid-TMS-Covid-Test-Management-System-
   ```

2. **Set up the web server**

   Place the project in your web server's root directory (e.g. `htdocs` for XAMPP), or run PHP's built-in server from the project root:

   ```bash
   php -S localhost:8000
   ```

3. **Create and import the database**

   - Create a new SQL database.
   - Import the provided SQL schema file (if included in the repository).

4. **Configure the database connection**

   Update the database credentials in the project's configuration file to match your environment (host, database name, username, password).

5. **Run the application**

   Open the app in your browser:

   ```
   http://localhost:8000
   ```

## Project Structure

> A representative structure — adjust to match the actual repository.

```
Covid-TMS/
├── assets/            # CSS, SCSS, JavaScript, images
├── config/            # Database connection / configuration
├── includes/          # Shared PHP includes
├── pages/             # Application pages (registration, results, reports)
├── sql/               # Database schema / seed files
├── index.php          # Entry point
└── README.md
```

## Usage

1. Open the application in a browser.
2. Register users for COVID-19 testing.
3. Record and update test results for registered users.
4. Generate reports on testing activity for clinics or health authorities.

## Roadmap

> Suggested enhancements for future versions.

- Role-based access for staff, lab technicians, and administrators.
- Automated result notifications (email/SMS).
- Dashboard with testing trends and analytics.
- Export of reports to PDF/CSV.

## Disclaimer

This application was built to manage COVID-19 testing operations and data. It does not provide medical advice or diagnosis. Always follow official public-health guidance and consult qualified professionals for medical concerns.

---

> **Note:** This README is based on the project's stated stack and purpose. Update the database setup steps, configuration file names, and project structure to match your actual codebase before publishing.
