# Pacman

A browser-based Pacman-style game built with JavaScript and served through a Django application.

This project combines a tile-based JavaScript game board with Django views, templates, user registration, icon selection, and high-score tracking. It was built as a full-stack practice project to connect front-end game logic with a Python/Django backend.

## Features

* Browser-playable Pacman-style maze
* Arrow-key movement controls
* Score tracking when Pacman collects coins and cherries
* Login and signup flow
* Selectable user icons
* High-score model connected to user accounts
* Django templates for login, signup, and gameplay pages
* Static game assets, including Pacman sprites, ghosts, coins, and cherries

## Tech Stack

* Python
* Django
* JavaScript
* HTML
* CSS
* bcrypt

## Project Structure

```text
Pacman/
├── pacman_app/
│   ├── migrations/
│   ├── static/
│   │   ├── icons/
│   │   ├── images/
│   │   ├── javascript/
│   │   │   └── game.js
│   │   └── styles/
│   ├── templates/
│   │   ├── game.html
│   │   ├── login.html
│   │   └── signup.html
│   ├── models.py
│   ├── urls.py
│   └── views.py
├── pacman_django/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── db.sqlite3
└── manage.py
```

## How It Works

The game board is represented as a JavaScript array, where each number corresponds to a different tile type such as a wall, coin, cherry, Pacman, ghost, or empty space. JavaScript renders the board into the browser and updates the board state when the player presses an arrow key.

The Django backend handles page routing, signup, login, session data, user records, selected icons, and high-score storage.

## Getting Started

### Prerequisites

Make sure you have Python and pip installed.

### Installation

Clone the repository:

```bash
git clone https://github.com/forrestgoryl/Pacman.git
cd Pacman
```

Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

On Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install django bcrypt
```

Apply database migrations:

```bash
python manage.py migrate
```

Run the development server:

```bash
python manage.py runserver
```

Then open the local development URL shown in your terminal, usually:

```text
http://127.0.0.1:8000/
```

## Current Status

This is a portfolio/practice project. The core Pacman movement, board rendering, scoring, user login/signup, and high-score model are implemented.

Potential future improvements include:

* Ghost movement and collision behavior
* Power-up logic
* Side-to-side teleportation
* Music and sound effects
* A smoother Pacman movement system
* Improved high-score updating
* Mobile-friendly controls
* Deployment-ready environment settings

## Portfolio Notes

This project demonstrates:

* JavaScript DOM manipulation
* Game-state management with arrays
* Keyboard event handling
* Django routing and template rendering
* Basic authentication flow
* Model relationships in Django
* Static asset organization
* Connecting front-end game logic with backend user data

## Author

Created by [Forrest Goryl](https://github.com/forrestgoryl).
