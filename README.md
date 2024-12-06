# User Management System

This is a PHP-based user management system that provides functionality for user registration, login, profile management, and profile updates. The system features responsive design with a simple UI created using CSS. The backend uses MySQL for data storage and session handling for user authentication.

## Features

- **User Registration**: Allows users to create an account with a profile image.
- **User Login**: Secure login functionality with password encryption.
- **Profile Management**: Users can view their profile details, update their information, and upload a new profile picture.
- **Responsive Design**: A clean and mobile-friendly UI built with CSS and Google Fonts.
- **Session Management**: Ensures secure user authentication and prevents unauthorized access.

## Project Structure

```plaintext
project/
├── css/
│   └── style.css           # Custom styles for the user interface
├── uploaded_img/           # Folder to store uploaded profile images
├── config.php              # Database connection configuration
├── home.php                # User dashboard
├── login.php               # Login page
├── register.php            # Registration page
├── update_profile.php      # Profile update page
├── images/
│   └── default-avatar.png  # Default profile image
```

## Requirements

- **Server**: PHP-enabled web server (XAMPP)
- **Database**: MySQL
- **Browser**: Modern web browser

## Installation

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Set Up Database**:
   - Import the provided SQL file (if available) into your MySQL database.
   - Or create a `user_db` database and add a `user_form` table with the following fields:
     ```sql
     CREATE TABLE `user_form` (
       `id` INT(11) NOT NULL AUTO_INCREMENT,
       `name` VARCHAR(255) NOT NULL,
       `email` VARCHAR(255) NOT NULL,
       `password` VARCHAR(255) NOT NULL,
       `image` VARCHAR(255) NOT NULL,
       PRIMARY KEY (`id`)
     );
     ```

3. **Update Database Configuration**:
   - Open `config.php` and update the database credentials to match your local setup:
     ```php
     $conn = mysqli_connect('localhost', 'root', '', 'user_db') or die('connection failed');
     ```

4. **Run the Application**:
   - Start your PHP-enabled web server.
   - Open the application in your browser at `http://localhost/<project-folder>/`.

## Usage

1. **Register**:
   - Navigate to the registration page (`register.php`).
   - Fill in the details and upload a profile image to create an account.

2. **Login**:
   - Access the login page (`login.php`) to log in with your credentials.

3. **Profile Management**:
   - After logging in, you can view and update your profile details, including uploading a new profile picture.

4. **Logout**:
   - Use the logout button to end your session securely.

## Security Features

- Passwords are stored using MD5 encryption.
- Session handling ensures secure user authentication.
- Basic input validation to prevent SQL injection.

## Acknowledgments

- Google Fonts: [Poppins](https://fonts.google.com/)
- Icons: [FontAwesome](https://fontawesome.com/)

---
- **Author**: Ahmed M. Saad  
- **Email**: [ahmedm.saad005@gmail.com](mailto:ahmedm.saad005@gmail.com)
