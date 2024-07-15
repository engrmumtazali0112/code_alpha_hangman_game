# Hangman Adventure Django

A responsive Hangman game built with Django.

## Features

- Responsive design for seamless play on any device
- Retro-style UI with atmospheric background
- Interactive SVG hangman drawing
- Real-time gameplay updates

## Installation

1. Clone the https://github.com/engrmumtazali0112/code_alpha_hangman_game
cd hangman-adventure-django

2. Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate

3. Install dependencies
pip install -r requirements.txt

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

![Capture](https://github.com/user-attachments/assets/0d9d693e-d963-402c-9c30-2390254cbc47)


## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)

Create a requirements.txt file:

Django==3.2.3
selenium==3.141.0

Contact:

Email : engrmumtazali01@gmail.com

Phone# : 03476338292

Link : ------------------

Linkedln : https://www.linkedin.com/in/mumtazali12/

Fiver : https://www.fiverr.com/s/6YzwedB

Upwork : https://www.upwork.com/nx/find-work/best-matches



Add your project files to the repository:

bashgit add .
git commit -m "Initial commit: Hangman Adventure Django project"
git push origin main

Create a .github/workflows/django.yml file for GitHub Actions:

yamlname: Django CI

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

bashgit add .github/workflows/django.yml
git commit -m "Add GitHub Actions workflow for Django CI"
git push origin main

link: 
