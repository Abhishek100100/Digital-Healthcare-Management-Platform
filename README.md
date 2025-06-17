# Digital Healthcare Management Platform

A comprehensive hospital management system with a graphical user interface, built using Python, Tkinter, and MySQL. This platform streamlines the management of patients, doctors, appointments, beds, staff, and emergency duties for healthcare institutions.

---

## Features

- **Admin Login & Registration**: Secure authentication for administrators.
- **Patient Management**: Register, update, and manage patient records.
- **Doctor Management**: Register, update, search, and manage doctor profiles and appointments.
- **Appointment Scheduling**: Book, cancel, and search appointments between patients and doctors.
- **Bed Management**: Add, allot, and manage hospital beds, including cost and ward assignment.
- **Staff Management**: Register, update, and manage hospital staff.
- **Emergency Duty Scheduling**: Assign and reschedule emergency duties for doctors.
- **Search & Filter**: Powerful search and filter options for all modules.
- **GUI**: Intuitive, multi-window interface using Tkinter and PIL for images.
- **MySQL Database**: All data is stored and managed in a MySQL database (`hms`).

---

## System Architecture

- **Frontend**: Python Tkinter GUI
- **Backend**: MySQL database (`hms`)
- **ORM/DB Access**: `mysql-connector-python`
- **Image Handling**: PIL (Pillow)

---

## Project Structure

```
Digital-Healthcare-Management-Platform/
├── main.py                  # Main application entry point (Tkinter GUI)
├── LICENSE
├── 21535001_poolb_5_report.pdf
├── README.md
├── .idea/                   # IDE settings (optional)
├── env/                     # Python virtual environment (optional)
├── images/                  # All GUI images (backgrounds, icons, etc.)
```

---

## Getting Started

### 1. Prerequisites

- Python 3.7+
- MySQL Server (tested with MySQL 5.7+)
- [Pillow](https://pypi.org/project/Pillow/) (`pip install pillow`)
- [mysql-connector-python](https://pypi.org/project/mysql-connector-python/) (`pip install mysql-connector-python`)

### 2. Database Setup

1. **Create the database and tables**  
   - Start your MySQL server.
   - Create a database named `hms`.
   - Create the required tables (`admin`, `doctor`, `patient`, `appointment`, `bed`, `staff`, `emergency`, etc.) as referenced in the code.
   - Example for `admin` table:
     ```sql
     CREATE DATABASE IF NOT EXISTS hms;
     USE hms;
     CREATE TABLE admin (
         email VARCHAR(255) PRIMARY KEY,
         passwd VARCHAR(255),
         SecurityQ VARCHAR(255),
         SecurityA VARCHAR(255)
     );
     -- Repeat for other tables as per your schema.
     ```

2. **Set MySQL credentials**  
   - The code expects MySQL user: `root`, password: `0000`, database: `hms`.
   - Update these in [`main.py`](main.py) if your credentials differ.

### 3. Install Dependencies

```sh
pip install pillow mysql-connector-python
```

### 4. Place Images

- Put all required images (backgrounds, icons, etc.) in the `images/` directory.
- Update image paths in [`main.py`](main.py) if your directory structure differs.

### 5. Run the Application

```sh
python main.py
```

---

##  Usage

- **Login**: Start the app and log in as admin (or register a new admin).
- **Navigate**: Use the menu to manage patients, doctors, appointments, beds, staff, and emergencies.
- **CRUD Operations**: Each module supports create, read, update, and delete/search operations via the GUI.
- **Emergency & Bed Management**: Assign beds to patients, schedule/reschedule emergency duties for doctors.

## Configuration

- **Database**: MySQL (`hms`)
- **Image Paths**: Update image paths in [`main.py`](main.py) if needed.
- **MySQL Credentials**: Change in code if not using `root/0000`.

---

## Notes

- The application is designed for local/offline use in a hospital or clinic environment.
- All data is stored in the local MySQL database.
- For deployment or multi-user access, consider enhancements for security and networking.

---

## References

- [Tkinter Documentation](https://docs.python.org/3/library/tkinter.html)
- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)
- [mysql-connector-python Docs](https://dev.mysql.com/doc/connector-python/en/)
