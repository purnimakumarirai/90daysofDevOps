
We are going to set up a pipeline for a Django application.
#Configuring Jenkins

1. Create a new item and choose a free-style project.
2. In the General setting provide the project descriotion. 
3. Now, go to source code to Jenkins.
3. management to configure GitHub to Jenkins. Provide the GitHub URL where the code exists. Use the secret text option to provide credentials
4. Now, go to Build Steps and choose the execute shell build option.
5. Guess, you have already written the docker file to containerize the application.
6. Provide the docker commands to build an image from the docker file and build the container.
7. docker build -† node-todo-anr
   docker run -p 8000:8000 node-todo-app
8. Finallv. click on build now to execute the project.
9. Navigate to the URI now.

#Initiallising Webhook
1. Let's automate the build process with the integration of webhook in GitHub.
2. You need to have ssh key and GPG key from the id rsa.pub in server and save it to GitHub.
3.Go to the code repository and navigate to the settings. Then provide the details in Webhook section.
4. The payload URL is the Jenkins URL.
5. It should be configured now.
#Configure project in WebHook
1. Make changes to the file in GitHub for the project and commit it.
2. Monitor the build in Jenkins that must have triggered automatically by webhook.
3. Navigate to the URL to see the changes that you had made in the code in GitHub.
#Configuring tasks using Docker-Compose
1. Write a Docker Compose file for the application.
2. Now, go to Jenkins and navigate to the build steps of the project. Provide the docker-compose commands. $ docker-compose down
$ docker-compose up -d
3. Now, build the project and check if the build is successfully completed. Finally navigate to the URL.
