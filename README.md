## Personal Blog – Flask Web Application

##Overview

**Personal Blog** is a full‑stack web application built with **Python and Flask**, developed as part of the course **“100 Days of Code – The Complete Python Pro Bootcamp” by Angela Yu**.

The project demonstrates the design and implementation of a complete blog platform, including **user authentication**, **role‑based access control**, **CRUD operations**, **database modeling**, and **comment management**. It is designed to showcase practical backend and full‑stack development skills relevant for junior / graduate software engineering roles.

---

## Project Goals

* Build a real‑world Flask web application from scratch
* Implement secure user authentication and authorization
* Design and manage a relational database using an ORM
* Apply role‑based access control (admin vs regular user)
* Practice clean project structure and separation of concerns
* Gain hands‑on experience with form handling and validation

---

## Technologies & Tools

* **Python 3**
* **Flask** – backend web framework
* **Flask‑SQLAlchemy** – ORM for database modeling
* **SQLite** – default database (easily replaceable)
* **Flask‑Login** – user authentication & session management
* **Flask‑WTF / WTForms** – form handling and validation
* **Flask‑Bootstrap5** – UI styling
* **Flask‑CKEditor** – WYSIWYG editor for blog posts
* **Flask‑Gravatar** – user avatars for comments
* **Werkzeug Security** – password hashing
* **HTML5 / CSS3 / Jinja2** – frontend templates

---

## Project Structure

```
Personal-Blog/
│
├── static/
│   └── css/
│       └── styles.css
│
├── templates/
│   ├── index.html
│   ├── post.html
│   ├── about.html
│   ├── contact.html
│   ├── login.html
│   ├── register.html
│   └── make-post.html
│
├── forms.py          # WTForms definitions
├── main.py           # Application entry point
├── posts.db          # SQLite database
├── requirements.txt
└── README.md
```

---

## Core Features

### User Authentication

* User registration with hashed passwords
* Secure login and logout using Flask‑Login
* Session management

### Role‑Based Authorization

* Admin‑only routes protected with decorators
* Only the admin user (ID = 1) can:

  * create new blog posts
  * edit existing posts
  * delete posts

### Blog Management

* View all posts on the homepage
* Dynamic routing for individual blog posts
* Rich‑text post creation using **CKEditor**

### Comment System

* Authenticated users can add comments
* Each comment is linked to:

  * a specific user
  * a specific blog post
* Automatic user avatars via **Gravatar**

### Static Pages

* About page
* Contact page

---

## Database Design

The application uses **SQLAlchemy ORM** with the following models:

* **User** – registered users
* **BlogPost** – blog articles
* **Comment** – user comments linked to posts

Relationships:

* One‑to‑many: User → BlogPost
* One‑to‑many: User → Comment
* One‑to‑many: BlogPost → Comment

The default database is **SQLite**, but the app supports other databases via environment configuration.

---

## Running the Application Locally

### Environment Variables

```
export FLASK_KEY=your_secret_key
export DB_URI=sqlite:///posts.db
```

Windows (PowerShell):

```
setx FLASK_KEY "your_secret_key"
setx DB_URI "sqlite:///posts.db"
```

### Installation & Execution

```
git clone https://github.com/DimaIoan-Andrei/Personal-Blog.git
cd Personal-Blog

python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate     # Windows

pip install -r requirements.txt
python main.py
```

Access the app at:

```
http://127.0.0.1:5002
```

---

## Key Learning Outcomes

* Building production‑style Flask applications
* Implementing authentication & authorization
* Secure password handling
* Designing relational data models with SQLAlchemy
* Applying decorators for access control
* Handling user input with validated forms
* Integrating third‑party Flask extensions

---

## Possible Future Improvements

* User profile pages
* Multiple user roles (editor / admin)
* Reply threads and likes for comments
* Image upload & cloud storage
* Deployment with Docker / Render / Railway

---

## Author

**Ioan‑Andrei Dima**
Built as part of *100 Days of Code – The Complete Python Pro Bootcamp (Angela Yu)*

---
## *This project is intended as an educational and portfolio application, demonstrating practical Flask and backend development skills.*
