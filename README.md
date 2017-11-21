Python application with Heroku and Django



Setup
    download Heroku CLI
    
    heroku login

Prepare the app

    git clone https://github.com/heroku/python-getting-started.git

    cd python-getting-started


Depoly app

    heroku create
    git push heroku master
    
    heroku ps:scale web=1
    
    heroku open
    
    
View logs

    heroku logs --tail
    
Define a Procfile
-Use a Procfile, a text file in the root directory of your application, to explicitly declare what command should be executed to start your app.

    web: gunicorn gettingstarted.wsgi --log-file -
    
Scale the app
Right now, your app is running on a single web dyno. Think of a dyno as a lightweight container that runs the command specified in the Procfile.

    heroku ps:scale web=0
    
Heroku domains

    heroku domains
    
    heroku domains:add www.example.com
    

Declare app dependencies
Heroku recognizes an app as a Python app by the existence of a Pipfile or requirements.txt file in the root directory.

    start Postgres app

These are the app dependencies - install with CLI

    pipenv --three
    pipenv install
    pipenv shell

    

