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


