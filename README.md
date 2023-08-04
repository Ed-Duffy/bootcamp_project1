Bootcamp Project 1 & 2 Documentation:

Planning:

Before I started this project I created a Trello which allowed me to identify all the tasks I had to complete in order to ensure the project was completed on schedule and met the mvp requirements. Additionally, this allowed me to update my progress and by utilising the 'Blocked' and 'Done' collums I was able to avoid duplicating my efforts. The below screenshot is an example of my working Trello board:

<img width="1470" alt="Screenshot 2023-08-04 at 14 39 24" src="https://github.com/Ed-Duffy/bootcamp_project1/assets/120494003/2c6776b7-afda-4b14-b223-7a42bcddbf8a">

After identifying the tasks I had to complete I was able to conduct a risk assesment which highlighted any challenges or difficulties I may face whilst completeing this project.


Project Work Method:

1.) The initial project required me to make an SQL database and subsequent table in which a python application could log data entrys each time the application was run. Below is an example of the SQL code that allowed me to create table in the schema myproject1 I created:

<img width="1470" alt="Screenshot 2023-08-04 at 14 47 50" src="https://github.com/Ed-Duffy/bootcamp_project1/assets/120494003/5b640471-a811-4b49-a697-1884bc57fedf">

2.) Once I had created a SQL schema and table, I created the python code that is located in this Git repo (app.py , backup.py and data.py). Once this was complete I could run the python code and it would create a log entry within my SQL table.

3.) After succesfully completing project one and creating the base code for this task, I focused my attention on automating the process utilising jenkins and docker. The first thing I did was config Nexus so that I could access a private repo to store my application data. To create the repo on Nexus I acessed localhost:8081 (port connection of container) and created a blob storage. Once this was complete I created a docker hosted repo and edited the Realms to ensure "Docker Bearer Token" was active. 

Nexus private repo:
<img width="1470" alt="Screenshot 2023-08-04 at 14 51 25" src="https://github.com/Ed-Duffy/bootcamp_project1/assets/120494003/24829d46-b57f-4bb4-b331-88f72d349990">

Nexus & python app running in Docker:
<img width="1470" alt="Screenshot 2023-08-04 at 14 50 33" src="https://github.com/Ed-Duffy/bootcamp_project1/assets/120494003/7d470881-1f50-4984-95bb-d3508f90dda8">

4.) Once Nexus and my private repo was set up with my python app, I was able to download and configure Jenkins. For this project I had to download Jenkins onto my local host utilising wsl command which allowed me to access bash from the terminal. Additionally, I had to amend the sudo controls for Jenkins to allow it to access my local data.

5.) After configuring and setting up Jenkins on my localhost I created a pipeline and a Jenkisfile which would automate my program.

Jenkisn pipeline successful build:
<img width="1470" alt="Screenshot 2023-08-04 at 14 50 52" src="https://github.com/Ed-Duffy/bootcamp_project1/assets/120494003/9c8490b8-2d78-4c8f-b3f3-b5f71cbe24bf">


6.) Once my pipeline was succesfully built I could check whether or not my build had been succesful by checking my localhost:5000/log and checking for '[]' . 
<img width="1470" alt="Screenshot 2023-08-04 at 14 51 08" src="https://github.com/Ed-Duffy/bootcamp_project1/assets/120494003/f93778ac-8953-4a6f-8bc6-9d708a2b801f">


7.)
Additionally to further test my build I added the below to my app.py file and then did localhost:5000/test:

@app.route('/test')
def test():
  return "Hey"




