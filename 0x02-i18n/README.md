# i18n Project README

## Overview
This project focuses on internationalization (i18n) using Flask and Flask-Babel. The goal is to create a multilingual Flask application that can handle different locales, display translated messages, and localize timestamps.

## Learning Objectives
- Parametrize Flask templates to display different languages.
- Infer the correct locale based on URL parameters, user settings, or request headers.
- Localize timestamps.

## Requirements
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7).
- All files should end with a new line.
- A README.md file at the root of the project is mandatory.
- Code should use the pycodestyle style (version 2.5).
- The first line of all files should be `#!/usr/bin/env python3`.
- All `.py` files should be executable.
- All modules, classes, functions, and methods should have documentation.
- All functions and coroutines must be type-annotated.

## Setup and Installation
1. **Clone the repository:**
    ```bash
    git clone https://github.com/your_username/alx-backend.git
    cd alx-backend/0x02-i18n
    ```

2. **Install dependencies:**
    ```bash
    pip3 install flask flask_babel==2.0.0 pytz
    ```

3. **Run the Flask app:**
    ```bash
    export FLASK_APP=app.py
    flask run
    ```

## Project Structure
```
0x02-i18n/
├── README.md
├── babel.cfg
├── templates/
│   ├── 0-index.html
│   ├── 1-index.html
│   ├── 2-index.html
│   ├── 3-index.html
│   ├── 4-index.html
│   ├── 5-index.html
│   ├── 6-index.html
│   ├── 7-index.html
│   └── index.html
├── translations/
│   ├── en/
│   │   └── LC_MESSAGES/
│   │       ├── messages.mo
│   │       └── messages.po
│   └── fr/
│       └── LC_MESSAGES/
│           ├── messages.mo
│           └── messages.po
├── 0-app.py
├── 1-app.py
├── 2-app.py
├── 3-app.py
├── 4-app.py
├── 5-app.py
├── 6-app.py
└── 7-app.py
```

## Tasks
### Task 0: Basic Flask App
Create a basic Flask app with a single route `/` and an `index.html` template that outputs "Welcome to Holberton" as the page title and "Hello world" as the header.

### Task 1: Basic Babel Setup
- Install Flask-Babel.
- Instantiate Babel in the app.
- Configure available languages (`["en", "fr"]`).
- Set default locale and timezone.

### Task 2: Get Locale from Request
Create a `get_locale` function to determine the best match with supported languages using `request.accept_languages`.

### Task 3: Parametrize Templates
- Use `_` or `gettext` to parametrize templates.
- Create a `babel.cfg` file.
- Initialize translations and dictionaries.
- Provide translations for `home_title` and `home_header`.
- Compile dictionaries.

### Task 4: Force Locale with URL Parameter
- Implement locale selection via `locale` URL parameter.
- Update `get_locale` to handle the `locale` parameter.

### Task 5: Mock Logging In
- Mock user login with a user table.
- Define `get_user` and `before_request` functions.
- Display welcome messages based on login status.

### Task 6: Use User Locale
- Update `get_locale` to use user’s preferred locale if supported.
- Priority: URL parameter > user settings > request header > default.

### Task 7: Infer Appropriate Time Zone
- Define `get_timezone` to determine the timezone from URL parameters, user settings, or default to UTC.
- Validate timezones using `pytz`.

### Task 8: Display the Current Time
- Display the current time on the home page based on the inferred timezone.
- Provide translations for `current_time_is`.

## License
This project is licensed under the MIT License.

## Author
ALX, 2024

---

This README provides a comprehensive guide to setting up and running the project, along with details of each task and requirements.
