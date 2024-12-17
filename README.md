# Application Project Sprottenflotte

This repository consists of the work for the Application Project Sprottenflotte.

## Structure:

```
Data
 ├── 				- Folder for data files
 └── 
Informations
 ├── 				- Folder for general Informations
 └── 
Model_training
 ├── model_training_rf.pth	- Notebook for Random Forest model training
 ├── model_rf.joblib		- Serialized Random Forest model for making predictions
 ├── scaler_rf.joblib		- Scaler for Random Forest data used in predictions
Results
 ├── 				- Folder for results and diagrams
 └── 

app_functions.py		- Collection of helper functions for data manipulation and UI functions
app.py				- Main application script to launch the Streamlit app
data.py				- Manages data fetching from external APIs and synchronization with GitHub
predictions_dl.py		- Manages deep learning model predictions
predictions_rf.py		- Manages random forest model predictions

AUTHORS				- Lists the contributors to the repository
poetry.lock			- Contains the exact versions of all dependencies used in the project to ensure consistency across different environments
pyproject.toml			- Specifies the project metadata and dependencies. Functions as a configuration file for the Poetry dependency manager
README.md
.gitignore
```

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
ACCESS_TOKEN='eyJhbGcxN6MIceG82CRoi0vPV46Og'

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
