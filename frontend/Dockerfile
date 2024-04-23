# This line specifies the base image for the Dockerfile. It instructs Docker to pull the official Node.js image tagged with
# version 14 from Docker Hub. This base image provides an environment with Node.js and npm (Node Package Manager) 
# installed, allowing you to build and run Node.js applications.
FROM node:14

# This line sets the working directory inside the Docker container to /app. The WORKDIR instruction is 
# used to define the directory where subsequent commands will be executed. In this case, it ensures that 
#all commands are executed relative to the /app directory.
WORKDIR /app     

# This line copies the package.json and package-lock.json files from the Docker host (the directory containing the Dockerfile)
# to the /app directory inside the Docker container. These files are typically used to define the dependencies and 
# scripts for the Node.js application.
COPY package*.json ./

# This line runs the "npm install" command inside the Docker container during build process. It installs the dependencies specified in the
# package.json file using npm, the package manager for Node.js applications. This step ensures that all required 
# dependencies are installed before proceeding with the build.
RUN npm install # This command will run in the '/app' directory

# This line copies the entire contents of the Docker host's directory (containing the Dockerfile and application 
# source code) to the current working directory (/app) inside the Docker container. 
COPY . .

# specifies the default command to run when the container starts. 
CMD ["npm", "start"]
