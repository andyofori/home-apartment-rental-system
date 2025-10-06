# 🏠 Home & Apartment Rental System

A comprehensive web-based platform for property management and rental search in Ghana. This system connects landlords with potential tenants, streamlining the entire rental process from property listing to maintenance tracking.

## 📋 Project Information

**Course:** Software Engineering  
**Institution:** Valley View University  
**Lecturer:** Madam Rebecca Amponsah  
**Group:** Group 2  
**Project Duration:** 5 Weeks (5 Sprints)  
**Date Started:** September 24, 2025

## 📂 Project Structure

home-apartment-rental-system/
├── frontend/
│   ├── auth/              # Login & Registration pages
│   ├── dashboard/         # User dashboards
│   ├── properties/        # Property listing & search
│   ├── applications/      # Application forms
│   ├── maintenance/       # Maintenance requests
│   ├── messages/          # Messaging system
│   ├── css/               # Stylesheets
│   ├── js/                # JavaScript files
│   └── images/            # Static images
├── backend/
│   ├── api/               # API endpoints
│   ├── config/            # Configuration files
│   ├── includes/          # Helper functions
│   └── uploads/           # User uploaded files (gitignored)
├── database/
│   ├── schema.sql         # Database schema
│   └── migrations/        # Database migrations
├── docs/
│   ├── requirements.md    # Requirements documentation
│   └── api-docs.md        # API documentation
├── .gitignore
├── README.md
└── LICENSE


## 🚀 Getting Started

### Installation Steps

#### 1. Clone the Repository

```bash
# Clone via HTTPS
git clone https://github.com/YOUR-USERNAME/home-apartment-rental-system.git

# OR clone via SSH (if you have SSH keys set up)
git clone git@github.com:YOUR-USERNAME/home-apartment-rental-system.git

# Navigate into the project directory
cd home-apartment-rental-system
```

#### 2. Set Up Database

```bash
# Start XAMPP/WAMP and ensure MySQL is running

# Open phpMyAdmin in your browser
# http://localhost/phpmyadmin

# Create a new database named 'rental_system'
# Import the schema from database/schema.sql
```

**Or via command line:**
```bash
mysql -u root -p
CREATE DATABASE rental_system;
USE rental_system;
SOURCE database/schema.sql;
exit;
```

#### 3. Configure Database Connection

```bash
# Copy the example config file
cp backend/config/database.example.php backend/config/database.php

# Edit database.php with your credentials
```

Edit `backend/config/database.php`:
```php
<?php
$host = 'localhost';
$dbname = 'rental_system';
$username = 'root';        // Your MySQL username
$password = '';            // Your MySQL password
?>
```

#### 4. Start Local Server

# If using XAMPP/WAMP
# Move the project folder to htdocs/ (XAMPP) or www/ (WAMP)
# Access via: http://localhost/home-apartment-rental-system

# OR use PHP built-in server
cd frontend
php -S localhost:8000


## 🔄 Git Workflow

### Branch Strategy

- `main` - Production-ready code (protected)
- `develop` - Integration branch
- `feature/*` - Feature branches for each sprint task

### Daily Workflow

```bash
# 1. Pull latest changes
git checkout develop
git pull origin develop

# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Make changes and commit frequently
git add .
git commit -m "Descriptive commit message"

# 4. Push your branch
git push origin feature/your-feature-name

# 5. Create Pull Request on GitHub
# Request review from Scrum Master (Andrews)
```

### Commit Message Guidelines

# Good commit messages
git commit -m "Add user registration form with validation"
git commit -m "Fix login button alignment on mobile"
git commit -m "Update database schema for maintenance requests"

# Bad commit messages (avoid these)
git commit -m "changes"
git commit -m "update"
git commit -m "fix bug"



## 🤝 Contributing

### For Team Members

1. Never push directly to `main` branch
2. Always create a feature branch
3. Write clear commit messages
4. Test your code before pushing
5. Request code review via Pull Request
6. Keep your branch updated with `develop`

### Pull Request Process

1. Create a feature branch from `develop`
2. Make your changes and test thoroughly
3. Push your branch to GitHub
4. Create a Pull Request to `develop`
5. Add description of changes
6. Request review from Scrum Master
7. Address review comments if any
8. Merge after approval
