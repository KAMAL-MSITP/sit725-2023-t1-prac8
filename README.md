#Refer Commands File for Docker commands

#Refer Dockerfile for the dockerization details

For eloborade explanation on DockerFile, see below:
1.	FROM node:
•	This command specifies the foundational image for the Docker container, utilizing the official Node.js image from Docker Hub. The specific version of Node.js is not explicitly mentioned, implying the use of the latest available version.
2.	WORKDIR /app:
•	This directive establishes the working directory inside the container as /app. All subsequent actions will be performed within this directory.
3.	COPY . .:
•	This instruction copies the contents of the current directory (where the Dockerfile resides) into the /app directory within the container. This assumes that the application code and essential files are co-located with the Dockerfile.
4.	EXPOSE 3000:
•	This statement notifies Docker that the application inside the container will employ port 3000. However, it does not explicitly expose this port to the host machine; port binding needs to be specified when running the container.
5.	RUN npm install:
•	Executed during the build process, this command installs the Node.js dependencies for the application. It presupposes the presence of a package.json file in the current directory, delineating the application's dependencies.
6.	CMD ["npm", "start"]:
•	This sets the default command to execute when the container is initiated. In this case, it launches the Node.js application using the npm start command. This assumes that the start script is defined within the scripts section of the package.json file.
