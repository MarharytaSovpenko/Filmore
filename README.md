# Cinema Service

An API service for cinema management written with DRF

## Feauters:

- JWT-based authentication for secure access
- An admin panel located at /admin/ for easy management
- Comprehensive documentation available at /api/doc/swagger/
- Efficient management of orders and tickets
- Media files for movie images stored in Docker
- Creation of movies with actors and genres
- Convenient filtering of movies and movie sessions
- A custom command to start the Docker app only when the database is available

### Install using GitHub:
1. Run the command below in your terminal
    - `git clone git@github.com:MarharytaSovpenko/Cinema-service.git`
2. Open the project folder in your IDE
3. If you are using PyCharm - it may propose you to automatically create venv for your project and install requirements
   in it, but if not:
    - python -m venv venv
    - source venv/Scripts/activate (on Windows/Git Bash)
    - venv\Scripts\activate (on Windows/PowerShell)
    - source venv/bin/activate (on macOS)
    - pip install -r requirements.txt
4. Create .env file and fill it with variables from .env.sample.
5. Don't forget to do migrations
    - `python manage.py migrate`
6. Run your server using the command below
    - `python manage.py runserver`


### Run with Docker:
- Install Docker https://www.docker.com/
- Run `docker-compose up` command and check with `docker ps` that 2 services are up and running
- Go to `127.0.0.1:8000/api/` and check the project endpoints via DRF interface


### Getting access:
- Create a new user via /api/user/register/
- Obtain a user token via /api/user/token/
- Install the ModHeader extension and create a request header with the value "Bearer <Your access token>"
- Go to /api/doc/swagger/