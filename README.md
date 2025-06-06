# Hostel Management System

## Introduction/Overview

This project is a web-based application designed to manage various aspects of a hostel. It provides a platform for students to apply for rooms, for hostel managers to manage room allocations, student records, and overall hostel operations, and for administrators to oversee the system.

## Features

*   **User Registration and Login:** Separate login portals for Students, Hostel Managers, and Admin/Subwardens.
*   **Student Application:** Students can apply for hostel rooms through an online application form.
*   **Room Allocation:** Hostel Managers can allocate rooms to students.
*   **Room Management:** View status of rooms (e.g., empty, allocated).
*   **Student Management:** Admins/Managers can view and manage student details.
*   **Messaging System:** Communication between users (e.g., students and managers).
*   **Profile Management:** Users can view and update their profiles.
*   **Admin Dashboard:** For overall management of the system, users, and hostel operations.

## Technology Stack

*   **Backend:** PHP
*   **Database:** MySQL
*   **Frontend:** HTML, CSS, JavaScript

## Installation Instructions

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    ```
    (Replace `https://github.com/your-username/your-repository-name.git` with the actual repository URL)

2.  **Move the project to your web server directory:**
    - For XAMPP/WAMP, usually `htdocs` or `www`.

3.  **Database Setup:**
    - Create a new database in your MySQL server (e.g., via phpMyAdmin).
    - Import the SQL files located in the `database/` directory. You will likely need to import them in a specific order if there are dependencies, or import the main application schema first. See the "Database Setup" section below for more details on the files.
    - (Example: `database/hostel_management_system_Application.sql`, `database/hostel_management_system_Hostel.sql`, etc.)

4.  **Configure Database Connection:**
    - Locate the database configuration file(s) (usually in a file like `includes/config.inc.php` or similar).
    - Update the database host, username, password, and database name with your local settings.

5.  **Access the application:**
    - Open your web browser and navigate to the project's URL (e.g., `http://localhost/your-project-directory-name/`).

## Usage (User Roles)

The system typically has the following user roles:

*   **Student:**
    *   Can register and log in to their accounts.
    *   Can fill out and submit hostel application forms.
    *   Can view their application status.
    *   Can manage their profile.
    *   Can communicate with the hostel management.

*   **Hostel Manager:**
    *   Can log in to the manager portal.
    *   Can view and manage student applications.
    *   Can allocate rooms to students.
    *   Can manage room details (e.g., view empty/allocated rooms, mark rooms for maintenance).
    *   Can view and manage student records.
    *   Can communicate with students and administrators.
    *   Can manage their profile.

*   **Administrator/Subwarden:**
    *   Can log in to the admin/subwarden portal.
    *   Has an overview of the entire system.
    *   Can manage student accounts and records.
    *   Can manage hostel manager accounts.
    *   Can oversee room allocations and hostel status.
    *   May have access to system settings and configurations.
    *   Can generate reports.

Access the respective login pages to use the system:
*   Student Login: (e.g., `index.php` or a specific student login page)
*   Hostel Manager Login: `login-hostel_manager.php`
*   Admin/Subwarden Login: `login-hostel_subwarden.php` or an admin login page like `admin/`

## Database Setup

The database schema and initial data are provided in the `database/` directory.

1.  **Create a database:** Create a new database in your MySQL server (e.g., using phpMyAdmin or SQL commands). Let's assume you name it `hostel_management_system_db`.
2.  **Import SQL files:** Import the following SQL files into your newly created database. It's generally a good practice to import them in an order that respects table dependencies (e.g., tables that are referenced by foreign keys should be created first). If a specific order is required, it should be determined by examining the file contents.
    *   `database/hostel_management_system_Application.sql`
    *   `database/hostel_management_system_Hostel.sql`
    *   `database/hostel_management_system_Hostel_Manager.sql`
    *   `database/hostel_management_system_Message.sql`
    *   `database/hostel_management_system_Room.sql`
    *   `database/hostel_management_system_Student.sql`

    (Note: You might need to adjust the database name within these SQL files if they contain `CREATE DATABASE` statements or `USE` statements that you wish to override.)

3.  **Verify Connection:** Ensure your PHP configuration file (e.g., `includes/config.inc.php`) points to the correct database name, host, username, and password.

## Contributing

Contributions to the Hostel Management System are welcome! If you have suggestions for improvements or find any issues, please feel free to:

1.  **Fork the repository.**
2.  **Create a new branch** for your feature or bug fix:
    ```bash
    git checkout -b feature/your-feature-name
    ```
    or
    ```bash
    git checkout -b fix/issue-description
    ```
3.  **Make your changes** and commit them with clear and descriptive messages.
4.  **Push your changes** to your forked repository.
5.  **Create a Pull Request** to the main repository, detailing the changes you've made.

Please ensure your code adheres to any existing coding standards and include relevant tests if applicable.

## License

This project is currently not under any specific license.
Please add a `LICENSE` file to the repository to specify the terms under which this software is provided.

Consider using a common open-source license such as:
*   [MIT License](https://opensource.org/licenses/MIT)
*   [GNU General Public License v3.0 (GPLv3)](https://www.gnu.org/licenses/gpl-3.0.en.html)
*   [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
