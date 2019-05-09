**Using celery with Flask**

This repository is an example of using Celery 

1. Send Asynchronous Email
2. Long running task with progress update

![alt text](Screenshots/celery.png?raw=true "Title")

**Quick Setup**

 Clone the repository.

->create virtualenv

  $ virtualenv venv   // this command to create virtual environment
   
->activate the virtual environment 

  $ source venv/bin/activate
  
->Install the requirements 

  $ pip install -r requirements.txt
  
 
 Install the redis from https://redis.io/download .
    
  
**How to run the project**

_You need to run three terminals_

In first terminal, 

$ cd <Project-Folder>

$ ./run-redis.sh

In second terminal.

$ cd <Project-Folder>

$ export MAIL_USERNAME=<your-gmail-username>

$ export MAIL_PASSWORD=<your-gmail-password>

$ source venv/bin/activate

(venv) $ celery worker -A app.celery --loglevel=info

In third terminal,

$ source venv/bin/activate

(venv) $ python app.py


**Finally,**

Go to http://localhost:5000/ and enjoy this application!






