<h1 align="center">API ONLY RAILS APP</h1>

<p align="center">
  <a href="https://github.com/antoniojking/rails_api_only_app/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/mental-health-org/mental_health_be?style=for-the-badge" alt="contributors_badge">
  </a>
  <a href="https://github.com/antoniojking/rails_api_only_app/issues">
    <img src="https://img.shields.io/github/issues/mental-health-org/mental_health_be?style=for-the-badge" alt="issues_badge">
  </a>
  <a href="https://github.com/antoniojking/rails_api_only_app/network/members">
    <img src="https://img.shields.io/github/forks/mental-health-org/mental_health_be?style=for-the-badge" alt="forks_badge">
  </a>
  <a href="https://github.com/antoniojking/rails_api_only_app/stargazers">
    <img src="https://img.shields.io/github/stars/mental-health-org/mental_health_be?style=for-the-badge" alt="stars_badge">
  </a>
</p>

<h4 align="center">Learn.Apply.Grow.</h4>

<p align="center">
The Rails API Only App is a RESTful API to demonstrate proficiency with various rails features and helpful gems. Endpoints may be accessed through an http request helper such as Postman.
</p><br>

<p align="center">
  <a href="#about-the-project">About The Project</a> •
  <a href="#technologies">Technologies</a> •
  <a href="#local-setup">Local Setup</a> •
  <a href="#testing">Testing</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#endpoints">Endpoints</a> •
  <a href="#database-schema">Database Schema</a> •
  <a href="#contributors">Contributors</a> •
  <a href="#acknowledgements">Acknowledgements</a>
</p>


## About The Project



### Learning Goals

* Use an agile process to turn well defined requirements into deployed and production ready software
* Implement professional git workflow
* Build a RESTful API with Ruby on Rails
* Implement TDD


## Technologies

<p align="center">
  <b>Framework</b><br>
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" />
</p>

<p align="center">
  <b>Languages</b><br>
  <img src="https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-4169E1.svg?style=for-the-badge&logo=SQL&logoColor=white" />
</p>

<p align="center">
  <b>Tools</b><br>
  <img src="https://img.shields.io/badge/Atom-66595C.svg?&style=for-the-badge&logo=atom&logoColor=white" />  
  <img src="https://img.shields.io/badge/git-F05032.svg?&style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-181717.svg?&style=for-the-badge&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Heroku-430098.svg?&style=for-the-badge&logo=heroku&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1.svg?&style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" />
</p>

<p align="center">
  <b>Processes</b><br>
  <img src="https://img.shields.io/badge/OOP-b81818.svg?&style=for-the-badge&logo=OOP&logoColor=white" />
  <img src="https://img.shields.io/badge/TDD-b87818.svg?&style=for-the-badge&logo=TDD&logoColor=white" />
  <img src="https://img.shields.io/badge/MVC-b8b018.svg?&style=for-the-badge&logo=MVC&logoColor=white" />
  <img src="https://img.shields.io/badge/REST-33b818.svg?&style=for-the-badge&logo=REST&logoColor=white" />  
</p>

<div align="center">

| Development | Testing       | Dependencies          |
|:-----------:|:-------------:|:---------------------:|
| Python 3.9.7| unittest      | djangorestframework   |
| Django 3.2.8| coverage      | dotenv                |
| Circle CI   |               | psycopg2              |
| Git/Github  |               |                       |
| Heroku      |               |                       |

</div>


## Local Setup

1. Create and invoke your virtual environment in your local project directory
   ```
   $python3 -m venv <env>

   $source <env>/bin/activate
   ```

2. Fork and clone this repo into your local project directory

4. Install dependencies
   ```
   $python3 -m pip install -r requirements.txt
   ```

5. Setup the database
   ```
   $psql

   $CREATE DATABASE <db_name>;
   ```

6. Add PostgreSQL database info to `settings.py`
   ```py
   DATABASES = {
     'default': {
         'ENGINE': 'django.db.backends.postgresql_psycopg2',
         'NAME': '<db_name>',
         'USER': '<username>',
         'PASSWORD': '<password>',
         'HOST': 'localhost',
         'PORT': '',
     }
   }
   ```

7. Migrate database tables
   ```
   $python3 manage.py migrate`
   ```

8. Run server
   ```
   $python3 manage.py runserver`
   ```

## Testing

- To run the test suite:
  ```
  $python3 manage.py test
  ```

- To assess test coverage:
  ```
  $coverage run --source='.' manage.py test

  $coverage report
  ```

## Getting Started

The `base path` of each endpoint is:

```
https://developer-mental-health-org.herokuapp.com/api/v1
```

- For `GET` requests, you can simply send the endpoint requests through your internet browser.  
- For any other requests (i.e. `POST`, `PATCH`, `DELETE`), you will need to use an API client to provide the request body and access the endpoints.

## Endpoints

The following table presents each API endpoint and its documentation.  

HTTP Verb | Endpoint          | Description                                    | Docs
----------|-------------------|------------------------------------------------|------
GET       | /things           | Get all things                                 | [doc](./docs/things_endpoint.md)
GET       | /things/:id       | Get one thing                                  |
POST      | /things           | Create a new thing                             |
PATCH     | /things/:id       | Update a thing                                 |
PUT       | /things/:id       | Update a thing                                 |
DELETE    | /things/:id       | Delete a thing                                 |


## Database Schema
![Database Schema](/docs/storage/images/schema.png)


## Contributors

<div align="center">

![](https://avatars.githubusercontent.com/u/81713591?s=150)
 :--:    
 **Antonio King**
 [GitHub](https://github.com/antoniojking)  
 [LinkedIn](https://www.linkedin.com/in/antoniojking/)

</div>

## Acknowledgements
```
"You are under no obligation to remain the same person you were a year ago, a month ago, or even a day ago. You are here to create yourself, continuously."
- Richard Feynman
```
