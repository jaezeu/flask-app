## Introduction

Note that this repository is only used for running a sample flask app

## Environment setup for running locally

Ensure that you have the following installed on your system:

- python 3.x
- pip

Create a virtual environment as this prevents package conflicts and keeps your setup clean:

```bash
cd flask_app
python3 -m venv venv
source venv/bin/activate

#Once the virtual environment is active, proceed with the following:
pip install --upgrade pip
pip install flask
```

You can then run your app within your virtual environment:

```bash
python app.py
```