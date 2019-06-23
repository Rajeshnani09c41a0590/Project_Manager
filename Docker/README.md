# Docker Commands to execute the program


* dockerx pull mysql:latest

* dockerx run --name taskmanagerdb -e MYSQL_ROOT_PASSWORD=password -e  MYSQL_DATABASE=taskmanager -e MYSQL_USER=fsduser -e MYSQL_PASSWORD=password -d mysql:latest

* dockerx build ./backend -t taskmanagerbackend

* dockerx run -p 8080:8080 --name taskmanagerbackend --link taskmanagerdb:mysql -d taskmanagerbackend

* dockerx build -t taskmanagerweb  ./webapp

* dockerx run -d --name taskmanagerweb -p 4200:4200 taskmanagerweb:latest

Ensure that the Docker file mentioned in the folder have been copied to the UI(webapp) folder and backend folder before executing the docker commands

**Note:** Docker compose was not applied to the project, as the same was not in the current scope of the BRD for Project Manager application 
