
docker pull nginx
# Run the first Nginx container
docker run --name myweb -p 7090:80 -d nginx
# docker run -d nginx creates and starts a detached Nginx container.
# Explanation:
# --name myweb: Sets the name of the container to "myweb."
# -p 7090:80: Maps port 7090 on the host to port 80 on the container.

# -d: Runs the container in detached mode (in the background).
# nginx: Specifies the Docker image to use, in this case, the official Nginx image.

# Run the second Nginx container with a custom name and image
docker run --name some-nginx -d -p 7090:80 some-content-nginx
# Explanation:
# --name some-nginx: Sets the name of the container to "some-nginx."
# -d: Runs the container in detached mode.
# -p 7090:80: Maps port 7090 on the host to port 80 on the container.
# some-content-nginx: Specifies the Docker image to use.

# Note: Using the same host port (7090) for both containers could lead to conflicts.
# If these commands are intended to be run simultaneously, consider choosing different host ports for each container.
# Ensure that the specified images are available on your system, or Docker will attempt to pull them from the Docker Hub.



# Navigate to the Docker data directory
cd /var/lib/docker/

# List the contents of the current directory
ls

# Navigate to the 'containers' directory
cd containers/

# List the contents of the 'containers' directory
ls

# Switch to the 'ubuntu' user
su - ubuntu

# List the contents of the home directory for the 'ubuntu' user
ls

# Navigate to a specific container's directory
cd a04783a6d7c028151eaf3216b2194a107bd46b4df5c9d7cfa3f39fe44740c894/

# List the contents of the container's directory
ls

# Navigate to the 'checkpoints' directory within the container's directory
cd checkpoints/

# List the contents of the 'checkpoints' directory
ls

# Move up one directory
cd ..

# Move up one directory
cd ..

# Display the disk usage of the container's directory
du -sh a04783a6d7c028151eaf3216b2194a107bd46b4df5c9d7cfa3f39fe44740c894/


# Navigate to the Docker data directory
cd /var/lib/docker/ 
# check for all the files and info what container have and all other config

# Start the Docker container named "myweb"
docker start myweb
# Explanation: Restarts the "myweb" container. If it was previously stopped, this command resumes its execution.

# List Docker images
docker images
# Explanation: Displays a list of locally available Docker images on the system.

# Execute the 'ls /' command inside the "myweb" container
docker exec myweb ls /
# Explanation: Runs the 'ls /' command inside the "myweb" Docker container, listing the contents of the root directory.


# Open an interactive Bash shell inside the "myweb" Docker container
docker exec -it myweb /bin/bash

# Explanation:
# - docker exec: Executes a command in a running Docker container.
# - -it: Allocates a pseudo-TTY and makes the command interactive, enabling interaction with the shell.
# - myweb: The name of the Docker container to execute the command in.
# - /bin/bash: The command to run inside the container, launching an interactive Bash shell.

### we ran it inside container 

apt update

apt install procps -y

root@bd8676faf4ac:/# ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 05:11 ?        00:00:00 nginx: master process nginx -g daemon off;
nginx         21       1  0 05:11 ?        00:00:00 nginx: worker process
root          35       0  0 05:14 pts/0    00:00:00 /bin/bash
root         225      35  0 05:16 pts/0    00:00:00 ps -ef


# Stop the Docker container named "myweb"
docker stop myweb
# Explanation: Stops the execution of the Docker container named "myweb."

# Remove the Docker container named "myweb"
docker rm myweb
# Explanation: Removes the Docker container named "myweb" from the system.
# Note: Ensure the container is stopped before removal.

# Remove the Docker image with the name "nginx"
docker rmi nginx
# Explanation: Removes the Docker image named "nginx" from the local image repository.
# Note: Ensure no containers are using the image before removal.




###########################################################################################


#Ubuntu image



docker pull ubuntu



# List all Docker containers
docker ps -a
# Explanation: Lists all Docker containers, including stopped ones.

# Remove Docker containers with specified IDs
docker rm ce157b84fed2 6ad0f0280735
# Explanation: Removes Docker containers with the specified IDs.

# List all Docker containers after removal
docker ps -a
# Explanation: Lists all Docker containers to verify removal.

# Remove a specific Docker container by its ID
docker rm 6ad0f0280735
# Explanation: Removes a specific Docker container by its ID.

# List all Docker images
docker images
# Explanation: Lists all Docker images on the system.

# Remove Docker images with specified names and tag
docker rmi ubuntu hello-world
# Explanation: Removes Docker images with the specified names and tag.

# List all Docker images after removal
docker images
# Explanation: Lists all Docker images to verify removal.

# Remove Docker image by name
docker rmi ubuntu
# Explanation: Removes the Docker image named "ubuntu."

# Forcefully remove Docker image by name
docker rmi -f ubuntu
# Explanation: Forcefully removes the Docker image named "ubuntu."

# List all Docker images after removal
docker images
# Explanation: Lists all Docker images to verify removal.

# Remove a non-existing Docker image (no action taken if the image does not exist)
docker rmi nonw
# Explanation: Attempts to remove a non-existing Docker image.

# Remove all Docker images
docker rmi $(docker images -q)
# Explanation: Removes all Docker images on the system.

# Remove a specific Docker image by ID
docker rmi c20060033e06
# Explanation: Removes a specific Docker image by its ID.
