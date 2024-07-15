# Hangman Adventure Django

A responsive Hangman game built with Django.

## Features

- Responsive design for seamless play on any device
- Retro-style UI with atmospheric background
- Interactive SVG hangman drawing
- Real-time gameplay updates

## Installation

1. Clone the repository
git clone https://github.com/your-username/hangman-adventure-django.git
cd hangman-adventure-django

2. Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate
Copy
3. Install dependencies
pip install -r requirements.txt
Copy
4. Run migrations
python manage.py migrate
Copy
5. Start the development server
python manage.py runserver
Copy
6. Open your browser and navigate to `http://localhost:8000`

## Testing

Run the tests with:
python manage.py test
Copy
## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)

Create a requirements.txt file:

CopyDjango==3.2.3
selenium==3.141.0

Add your project files to the repository:

bashCopygit add .
git commit -m "Initial commit: Hangman Adventure Django project"
git push origin main

Create a .github/workflows/django.yml file for GitHub Actions:

yamlCopyname: Django CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    strategy:
      max-parallel: 4
      matrix:
        python-version: [3.7, 3.8, 3.9]

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python ${{ matrix.python-version }}
      uses: actions/setup-python@v2
      with:
        python-version: ${{ matrix.python-version }}
    - name: Install Dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt
    - name: Run Tests
      run: |
        python manage.py test

Commit and push the workflow file:

bashCopygit add .github/workflows/django.yml
git commit -m "Add GitHub Actions workflow for Django CI"
git push origin main
