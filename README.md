# Secure File Sharing Application

Project Overview

Purpose
The Secure File Sharing Application is a Django-based web application designed to provide a secure and user-friendly platform for file management and sharing. The primary goal is to ensure file confidentiality, integrity, and controlled access through robust encryption and authentication mechanisms.

# Key Objectives
Provide secure user registration and authentication.<br>
Enable encrypted file uploads and downloads.<br>
Implement secure file sharing between users.<br>
Ensure file integrity through cryptographic hashing.<br>
Protect against common web vulnerabilities.<br>

# Features

User Authentication<br>
Secure user registration.<br>
Login/logout functionality.<br>
Password protection for user accounts.<br>

File Upload<br>
Supports multiple file types: txt, pdf, docx, jpg, png, zip.<br>
Files are automatically encrypted before storage.<br>
File type validation to prevent unsupported file uploads.<br>

File Encryption<br>
Uses Fernet symmetric encryption for secure file encryption.<br>
Generates and manages encryption keys.<br>
Files are encrypted before being stored and decrypted only during download.<br>

File Sharing<br>
Users can share files with specific individuals.<br>
Keeps track of file sharing history.<br>
Prevents unauthorized access to shared files.<br>

File Integrity Checks<br>
SHA256 hash generation for each file.<br>
File integrity is verified during both upload and download.<br>
Detects file tampering to ensure the file’s authenticity.<br>

# Setup & Installation
Software Requirements ( Clone the repository and install the required dependencies:) <br>
Python 3.8+<br>
Django 3.2+<br>
pip package manager<br>

Required Dependencies<br>
Django<br>
python-dotenv<br>
cryptography<br>

Clone my Repo:<br>
``` git clone https://github.com/DhruvChotalia/Secure-File-Sharing-Application.git ```

# Installation Dependencies
To install the required dependencies, run the following command:<br>
``` pip install django cryptography python-dotenv ```

Apply Database Migrations<br>
To set up the database, run the following commands:<br>
```
python manage.py makemigrations
python manage.py migrate
```
3. Create a Superuser<br>
To access the Django admin panel, create a superuser account:<br>
```
python manage.py createsuperuser
```
Follow the prompts to enter your admin credentials.

# Usage Guide
User Registration

Go to the registration page.<br>
Enter your details (username, email, password) and submit.<br>
Login to the application with your new credentials.<br>

Uploading Files<br>
After logging in, navigate to the file upload page.<br>
Select the file you want to upload.<br>
Confirm the upload.<br>

Sharing Files<br>
Select the file you want to share from your file list.<br>
Enter the recipient's username and confirm sharing.<br>

Managing Files<br>
View your uploaded files in the dashboard.<br>
Download, share, or delete files as needed.<br>

Demo Videos:
Link - [AllTests Demo Videos are Here](https://drive.google.com/drive/folders/1MTmJ6h-gwPTzYnGDZ4U_R2KTLom0IOCK?usp=drive_link)


# Security and Encryption
Fernet Encryption: Files are encrypted using the Fernet symmetric encryption method before being stored.<br>
SHA-256 Hashing: Each file is assigned a SHA-256 hash for integrity verification during upload and download.<br>

Error Handling<br>
Error messages are displayed through Django’s messaging framework if issues arise (e.g., authentication failures, file not found, file sharing errors).
Users are redirected to the relevant pages after errors.<br>

Testing<br>
The application includes unit tests to verify its core functionality, validate security features, and ensure proper behavior under different scenarios.

Prerequisites<br>
Ensure you have the following installed:<br>

Python 3.x <br>
Django<br>
pytest-django<br>
pytest-cov<br>
Cryptography<br>
python-dotenv<br>

Run Tests<br>

# Running Tests and Generating Reports
Generating Test Report <br>
To run the tests for the File Sharing & Encryption Web Application and generate a test report, follow these steps: <br>
Navigate to the app directory of the project (where fileapp is located). <br>

Run the following command to execute the tests: <br>

```
pytest --cov=fileapp tests/
```

After executing the command, pytest will generate a report in the terminal, showing the status of each test and the overall coverage for the fileapp directory.<br>

Acknowledgments<br>
Django for the web framework.<br>
Cryptography for secure file encryption.<br>
pytest for the testing framework.<br>
