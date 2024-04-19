# Flask Starter

This repository is designed as a starter guide for developing web applications with Flask, a lightweight and flexible Python web framework. It covers the essentials such as setting up your environment, creating routes, rendering templates, and running a development server.

## Prerequisites

- Python installed on your machine
- Basic knowledge of Python programming

## Installation

### Set Up a Virtual Environment

1. **Create and activate a virtual environment**:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
   ```

### Install Flask

1. **Install Flask**:
   ```bash
   pip install flask
   ```

## Creating a Basic Flask Application

1. **Create a new Python script (`app.py`)**:
   ```python
   from flask import Flask, render_template

   app = Flask(__name__)

   @app.route('/')
   def home():
       return "Hello, Flask!"

   if __name__ == '__main__':
       app.run(debug=True)
   ```

2. **Run the Flask application**:
   ```bash
   python app.py
   ```
   - This will start a development server that you can access at `http://127.0.0.1:5000/`.

## Adding Routes and Templates

1. **Create a new route**:
   ```python
   @app.route('/about')
   def about():
       return "This is the about page."
   ```

2. **Render a template**:
   - First, create a directory called `templates`.
   - Inside `templates`, create an HTML file (`about.html`).
   - Modify the `about` function to render the template:
     ```python
     @app.route('/about')
     def about():
         return render_template('about.html')
     ```

## Contributing

Contributions to improve the guide, add new examples, or enhance functionality are welcome. Please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
