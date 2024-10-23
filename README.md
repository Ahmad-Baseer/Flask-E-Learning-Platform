# E-learning Platform

This E-learning Platform provides a fully functional backend built with Flask, using MySQL for data storage and Bootstrap for the frontend. The main focus of the platform is user management, course management, and content delivery, with various features to handle user authentication, session management via cookies, and course-related functionalities.

### Core Functionalities:
- User Authentication: The system generates and manages user sessions with secure cookies and validates user login state before providing access to resources.
- File Uploads: The platform allows users to upload files (images, PDFs, etc.) for courses, leveraging secure file handling and storage in a specific directory (static/img).
- Database Interaction: MySQL is used to store user data, session cookies, and other application-specific data. The backend connects to the MySQL database using credentials loaded from a configuration file (config.json).
- HTML Content Parsing: The platform utilizes BeautifulSoup to handle and sanitize HTML input/output, ensuring the removal of unwanted HTML tags before rendering content.
- Image Handling: There is functionality to manage images, using the Pillow library for image processing (e.g., adding text or drawing on images).
### Key Libraries:
- Flask: Provides the web framework and session management.
- MySQL: Used for persistent data storage.
- Pillow: Handles image manipulation tasks.
- BeautifulSoup: Used for HTML parsing and sanitizing user inputs.
- CV2: Likely used for advanced image processing related to course content.

# Steps to run this project

## Prerequisites
- Python 3.x
- MySQL server
- MySQL Workbench (optional for managing the database)
- A virtual environment (recommended)
- Flask and required Python dependencies

## 1. Clone the Project Repository
Clone this repository to your local machine using Git:
```bash
git clone https://github.com/Ahmad-Baseer/Flask-E-Learning-Platform.git
cd Flask-E-Learning-Platform
```
## 2. Set Up Virtual Environment
```bash
python3 -m venv venv
#on windows
venv\Scripts\activate
#on linux
source venv/bin/activate
```
## 3. Install Python Dependencies
```bash
pip install -r requirements.txt
```
## 4. Set Up the Database
You’ll need to set up the MySQL database before running the project.
### 4.1 Start MySQL Server
Ensure your MySQL server is running.
### 4.2 Create the Database
Login to MySQL shell by providing your username and password.
```bash
mysql -u root -p
```
Once in the MySQL shell, create the database and import the SQL file:
```bash
CREATE DATABASE teach_me;
USE teach_me;
SOURCE /path_to/teach_me.sql;
```
## 5. Configure the Flask App
Put your credentials in config.json.
## 6. Run the Application
```bash
python main.py
```





