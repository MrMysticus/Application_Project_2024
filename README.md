# Application Project Sprottenflotte

This repository consists of the work for the Application Project Sprottenflotte.

<div style="border: 2px solid red; padding: 10px; border-radius: 5px;">
  <strong>⚠️ Warning:</strong> 
  Do not change the Master_Document.ipynb without team agreement!
</div>



---

Structure:

```
Data
└──
Informations
└──
Master_Document.ipynb
requirements.txt
README.md
```

## Git commands

- `git status`
- `git add —all`
- `git add <filename>`
- `git commit -am "..."`
- `git push`
- `git pull`

## Create a .env file

You can create the following .env file in the project directory.

This .env file will store sensitive information such as passwords, client secrets, and access tokens securely. The .env file is not under version control and therefore secure, because it is added to the .gitignore file.

**Note:** You can use the `sample.env` file, which serves as a template, for creating your own `.env` file.

```
# password for keycloak
PASSWORD="*************"

# client_secret
CLIENT_SECRET="fP81XZ5OTt5iRJ7qhyyTCv4eQtpGqc5i"

# access token
ACCESS_TOKEN='eyJhbGcxN6MIceG82CRo73uugB4gCbbKgofF3UFJLeFcILi0vPV46Og'

```

You can access the variables inside the .env file with:

```
import dotenv

# .env
config = dotenv.dotenv_values(".env")

PASSWORD = config["PASSWORD"]

CLIENT_SECRET = config["CLIENT_SECRET"]

ACCESS_TOKEN = config["ACCESS_TOKEN"]
```

## Installation:

### 1. Clone the repository from GitHub

Clone the repository to a nice place on your machine via:

```
git clone git@github.com:MrMysticus/Application_Project_2024.git
```

### 2. Create a new environment

#### 2.1 Virtual environment

Make a new virtual .venv environment with python version 3.12 or an conda environment.

#### 2.2 Conda environment

Create a new Conda environment for this project with a specific version of Python:

```
conda create --name application_project_2024 python=3.12
```

Initialize Conda for shell interaction:

To make Conda available in you current shell execute the following:

```
conda init
```

### 3. Install packages from requirements.txt

Install packages in environment:

```
pip install -r requirements.txt
```
