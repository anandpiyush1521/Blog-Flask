# Flask Blog Application

<p align="center">
  <img src="https://img.shields.io/badge/Powered_by-Flask_and_SQLAlchemy-blue?style=for-the-badge&logo=flask" alt="Powered by Flask">
  <img src="https://img.shields.io/badge/Powered_by-SQLite-green?style=for-the-badge&logo=sqlite" alt="Powered by SQLite">
</p>


## Overview

This project is a simple blog application built using the Flask framework. It provides functionality for viewing blog posts, as well as an admin dashboard for managing posts, uploading files, and handling user contact forms. The application uses SQLAlchemy for database management and Flask-Mail for sending email notifications.

## Features

- **Home Page**: Displays a paginated list of blog posts.
- **Blog Post Page**: View the content of a specific blog post.
- **About Page**: Static page with information about the blog.
- **Admin Dashboard**: Manage blog posts, including adding, editing, and deleting posts.
- **File Upload**: Upload files to the server.
- **Contact Form**: Send messages to the admin via email.
- **User Authentication**: Secure admin access with a username and password.

## Setup and Installation

### Prerequisites

- Python 3.x
- Virtual Environment (recommended)
- SQLite (default, included with Python)
- Flask-Mail Configuration (Gmail account)

### Backend Setup

1. **Clone the Repository**

    ```bash
    git clone https://github.com/yourusername/flask-blog-app.git
    cd flask-blog-app
    ```

2. **Create and Activate a Virtual Environment**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Dependencies**

    ```bash
    pip install -r requirements.txt
    ```

4. **Set Up Configuration**

    - Open the `config.json` file and update the following fields with your own information:
        - `local_uri`: Local database URI (e.g., `sqlite:///site.db`).
        - `prod_uri`: Production database URI (optional).
        - `upload_location`: Path where uploaded files will be stored.
        - `gmail-user`: Your Gmail username for sending emails.
        - `gmail-password`: Your Gmail password.
        - `admin_user`: Admin username for accessing the dashboard.
        - `admin_password`: Admin password for accessing the dashboard.

5. **Run the Application**

    ```bash
    python app.py
    ```

    The application will run in debug mode and can be accessed at `http://127.0.0.1:5000/`.

### Usage

1. **Access the Application**

    Open your browser and navigate to `http://127.0.0.1:5000`.

2. **Admin Dashboard**

    - Navigate to `/dashboard` to log in as an admin.
    - Use the credentials specified in `config.json`.
    - From the dashboard, you can add, edit, or delete blog posts.

3. **File Uploads**

    - Navigate to `/uploader` as an admin to upload files. Files will be saved in the directory specified in `config.json` under `upload_location`.

4. **Contact Form**

    - Navigate to `/contact` to send a message to the admin. The message will be emailed to the admin's Gmail account.

### Screenshots

<p align="center">
  <img src="path_to_your_image/dashboard_screenshot.png" width="1000" alt="Admin Dashboard">
</p>

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request if you have any suggestions, bug fixes, or improvements.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
