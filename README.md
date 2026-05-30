# Payroll Management System

A PHP/MySQL payroll management web application for managing employees, attendance, allowances, deductions, payroll processing, and payslip printing.

## Features

- User login and access control
- Employee management
- Department and position management
- Attendance tracking and time logs
- Allowances management
- Deductions management
- Payroll generation and calculation
- Payroll history and payslip printing
- User administration and settings

## Requirements

- Apache web server (XAMPP, WAMP, or similar)
- PHP 7.x / 8.x
- MySQL / MariaDB
- Web browser

## Installation

1. Copy the `Payroll-Management-System` folder into your web server document root (for example, `C:\xampp\htdocs\`).
2. Start Apache and MySQL services.
3. Open phpMyAdmin at `http://localhost/phpmyadmin`.
4. Create a new database named `payroll`.
5. Import the provided SQL schema if available (`payroll.sql`).
6. Update database settings in `db_connect.php` if your MySQL credentials differ:

```php
$conn= new mysqli('localhost','root','','payroll') or die("Could not connect to mysql".mysqli_error($con));
```

7. Open the application in your browser:

```text
http://localhost/Payroll-Management-System/login.php
```

## Default Login

If the database includes default credentials, use:

- Username: `admin`
- Password: `admin123`

If no user exists yet, create an administrator account using the `users` table or the user management page after installing the database schema.

## Important Notes

- The repository does not include the SQL schema file itself. If you have the original package, import the `payroll.sql` file to create the database structure.
- Ensure the database name in `db_connect.php` matches the created database.
- The main backend logic is handled in `admin_class.php`, and AJAX actions are dispatched through `ajax.php`.

## Main Pages

- `login.php` — login screen
- `index.php` — main dashboard after login
- `employee.php` — manage employees
- `attendance.php` — manage attendance logs
- `allowances.php` — manage allowance types
- `deductions.php` — manage deduction types
- `manage_payroll.php` — payroll creation and processing
- `manage_user.php` — user administration

## License

Use and modify this project for learning and internal development.

