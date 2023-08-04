Bootcamp Project 1 & 2 Documentation:

1.) The initial project required me to make an SQL database and subsequent table in which a python application could log data entrys each time the application was run.

2.) In order to complete these task I created a SQL database using the below commands:

CREATE DATABASE myproject1;

USE DATABASE myproject1;

CREATE TABLE log(
id INT PRIMARY KEY AUTO_INCREMENT,
date TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
action VARCHAR(100),
parameter VARCHAR(1000),
status VARCHAR(100)
);

3.) Once I had created a SQL schema and table, I created the python code that is located in this Git repo (app.py , backup.py and data.py). Once this was complete I could run the python code and it would create a log entry within my SQL table.

4.) After succesfully compleeting project one and creating the base code for this task, I focused my attention on automating the process utilising jenkins and docker. The first thing I did was config Nexus so that I could access a private repo to store my application data.

5.) After completeing this I build a NEXUS container and a specific image for my application. In order to do this I used the command: "docker build -t localhost:8083/pythonapp .". 

6.)

7.) In order to automate this process I created a Jenkins pipeline and added a Jenkinsfile to the Git Repo. 

8.) Once my pipeline was succesfully built I could check whether or not my build had been succesful by checking my localhost:5000 and checking for '[]' . Additionally to further test my build I added the below to my app.py file:

@app.route('/test')
def test():
  return "Hey"




