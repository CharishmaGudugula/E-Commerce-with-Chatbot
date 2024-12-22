The E-Commerce with Chatbot repository is a project that integrates a chatbot into an e-commerce platform to enhance customer interaction and support.

Purpose
The project aims to provide a smarter shopping experience by using an AI-powered chatbot to assist users with:

Product information.
Order tracking.
Customer service inquiries.
Key Features
Product Assistance: Customers can ask questions about product specifications, availability, and pricing.
Order Status Updates: The chatbot provides real-time updates about ongoing orders.
Customer Support: Handles common questions, such as return policies, shipping information, and account-related issues.
Technology Stack
Backend: Python
Frontend: HTML, CSS, JavaScript
AI Chatbot Framework: Rasa, a framework for building conversational AI.
Setup Overview
Clone the repository.
Install dependencies via pip.
Set up the database with configuration files.
Train the chatbot using Rasa.
Run the application server and access the chatbot-enabled platform.
Contributing and License
The repository is open for contributions and is licensed under the MIT License, making it freely available for use and modification.
# E-Commerce Platform with Integrated Chatbot

This project is a simple e-commerce platform built using **Flask**. It features a chatbot to assist users, providing information about products, handling inquiries, and enhancing the overall user experience.

---

## Features

- **User Authentication:**
  - Register, log in, and manage user profiles.
  - Change passwords and update profile information.

- **Product Management:**
  - Admin can add, remove, or update products.
  - Products are organized into categories.

- **Shopping Cart:**
  - Users can add products to their cart.
  - View cart contents and calculate the total price.
  - Remove items from the cart.

- **Chatbot Integration:**
  - Chatbot assists users by answering questions or providing product details.
  - Uses a custom implementation for chatbot responses.

- **Order Management:**
  - Simple checkout flow for users to place orders.

---

## Technology Stack

- **Backend:** Flask (Python)
- **Frontend:** HTML, CSS, Jinja2 templates
- **Database:** SQLite
- **Chatbot Framework:** Custom implementation with Python

---

## Getting Started

### Prerequisites

- Python 3.6 or higher
- SQLite

### Installation

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_directory>
Install required dependencies
pip install -r requirements.txt
Set up the database:

Create an SQLite database named database.db.
Populate the database with necessary tables (users, products, categories, kart).
Configure the upload folder:

Ensure the static/uploads directory exists for image uploads.
Run the application:
python app.py
Access the platform:

Enter localhost:5000 in the browser.
Project Structure
├── app.py                 # Main Flask application file
├── static/
│   ├── uploads/           # Directory for uploaded images
│   └── ...                # Static assets (CSS, JS, images)
├── templates/             # HTML templates for the application
├── requirements.txt       # List of required Python packages
└── database.db            # SQLite database file (to be created)
# E-Commerce Platform with Flask

This project is a basic e-commerce platform developed using **Flask**. It includes user management, product catalog, shopping cart functionality, and category-based product organization. The database schema is designed using SQLite.

---

## Features

- **User Management:**
  - Register, login, and manage user profiles.
  - Update personal details and change passwords.

- **Product Management:**
  - Admin can add and remove products.
  - Products are categorized for easier browsing.

- **Shopping Cart:**
  - Users can add products to their cart.
  - View cart and checkout.

- **Database Design:**
  - **Users Table**: Stores user details.
  - **Categories Table**: Organizes products into categories.
  - **Products Table**: Holds product details.
  - **Kart Table**: Tracks user-cart relationships.

---

## Technology Stack

- **Backend:** Flask (Python)
- **Database:** SQLite
- **Frontend:** HTML, CSS, Jinja2 Templates

---

## Database Schema

The SQLite database is structured as follows:

```sql
CREATE TABLE IF NOT EXISTS users (
    userId INTEGER PRIMARY KEY, 
    password TEXT,
    email TEXT,
    firstName TEXT,
    lastName TEXT,
    address1 TEXT,
    address2 TEXT,
    zipcode TEXT,
    city TEXT,
    state TEXT,
    country TEXT, 
    phone TEXT
);

CREATE TABLE IF NOT EXISTS categories (
    categoryId INTEGER PRIMARY KEY,
    name TEXT
);

CREATE TABLE IF NOT EXISTS products (
    productId INTEGER PRIMARY KEY,
    name TEXT,
    price REAL,
    description TEXT,
    image TEXT,
    stock INTEGER,
    categoryId INTEGER,
    FOREIGN KEY(categoryId) REFERENCES categories(categoryId)
);

CREATE TABLE IF NOT EXISTS kart (
    userId INTEGER,
    productId INTEGER,
    FOREIGN KEY(userId) REFERENCES users(userId),
    FOREIGN KEY(productId) REFERENCES products(productId)
);
Getting Started
Prerequisites
Python 3.6 or higher
SQLite

Here’s a README.md file tailored to your project with the database schema creation script included:

markdown
Copy code
# E-Commerce Platform with Flask

This project is a basic e-commerce platform developed using **Flask**. It includes user management, product catalog, shopping cart functionality, and category-based product organization. The database schema is designed using SQLite.

---

## Features

- **User Management:**
  - Register, login, and manage user profiles.
  - Update personal details and change passwords.

- **Product Management:**
  - Admin can add and remove products.
  - Products are categorized for easier browsing.

- **Shopping Cart:**
  - Users can add products to their cart.
  - View cart and checkout.

- **Database Design:**
  - **Users Table**: Stores user details.
  - **Categories Table**: Organizes products into categories.
  - **Products Table**: Holds product details.
  - **Kart Table**: Tracks user-cart relationships.

---

## Technology Stack

- **Backend:** Flask (Python)
- **Database:** SQLite
- **Frontend:** HTML, CSS, Jinja2 Templates

---

## Database Schema

The SQLite database is structured as follows:

```sql
CREATE TABLE IF NOT EXISTS users (
    userId INTEGER PRIMARY KEY, 
    password TEXT,
    email TEXT,
    firstName TEXT,
    lastName TEXT,
    address1 TEXT,
    address2 TEXT,
    zipcode TEXT,
    city TEXT,
    state TEXT,
    country TEXT, 
    phone TEXT
);

CREATE TABLE IF NOT EXISTS categories (
    categoryId INTEGER PRIMARY KEY,
    name TEXT
);

CREATE TABLE IF NOT EXISTS products (
    productId INTEGER PRIMARY KEY,
    name TEXT,
    price REAL,
    description TEXT,
    image TEXT,
    stock INTEGER,
    categoryId INTEGER,
    FOREIGN KEY(categoryId) REFERENCES categories(categoryId)
);

CREATE TABLE IF NOT EXISTS kart (
    userId INTEGER,
    productId INTEGER,
    FOREIGN KEY(userId) REFERENCES users(userId),
    FOREIGN KEY(productId) REFERENCES products(productId)
);
To create the database schema, you can use the provided Python script initialize_database.py:

python
Copy code
import sqlite3

# Open database
conn = sqlite3.connect('database.db')

# Create tables
conn.execute('''CREATE TABLE IF NOT EXISTS users 
    (userId INTEGER PRIMARY KEY, 
    password TEXT,
    email TEXT,
    firstName TEXT,
    lastName TEXT,
    address1 TEXT,
    address2 TEXT,
    zipcode TEXT,
    city TEXT,
    state TEXT,
    country TEXT, 
    phone TEXT
    )''')

conn.execute('''CREATE TABLE IF NOT EXISTS categories
    (categoryId INTEGER PRIMARY KEY,
    name TEXT
    )''')

conn.execute('''CREATE TABLE IF NOT EXISTS products
    (productId INTEGER PRIMARY KEY,
    name TEXT,
    price REAL,
    description TEXT,
    image TEXT,
    stock INTEGER,
    categoryId INTEGER,
    FOREIGN KEY(categoryId) REFERENCES categories(categoryId)
    )''')

conn.execute('''CREATE TABLE IF NOT EXISTS kart
    (userId INTEGER,
    productId INTEGER,
    FOREIGN KEY(userId) REFERENCES users(userId),
    FOREIGN KEY(productId) REFERENCES products(productId)
    )''')

# Close connection
conn.close()
Getting Started
Prerequisites
Python 3.6 or higher
SQLite
Installation
Clone the repository:
git clone <repository_url>
cd <repository_directory>
Install dependencies:


pip install -r requirements.txt
Set up the database:

Run the initialize_database.py script to create the tables.
Use a database management tool or custom scripts to populate the categories and products tables with sample data.
Run the application:
python app.py
├── app.py                  # Main Flask application file
├── initialize_database.py  # Script to create database schema
├── static/
│   ├── uploads/            # Directory for uploaded product images
│   └── ...                 # Other static files (CSS, JS, etc.)
├── templates/              # HTML templates for the app
├── requirements.txt        # List of Python dependencies
└── database.db             # SQLite database file (created at runtime)
Contribution :
1.Fork the repository.
2.Create a branch:
git checkout -b feature-name
3.Make your changes and commit:
git commit -m "Description of changes"
4.Push to your branch :
git push origin feature-name
5.Open a pull request.




