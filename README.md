### Installation


# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Add the repository to Apt sources:
echo \
  "deb [arch=\"\$(dpkg --print-architecture)\" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  \"\$(. /etc/os-release && echo \"\$VERSION_CODENAME\")\" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

# Install Docker
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Verify Docker installation
sudo docker run hello-world

# Check Docker service status
systemctl status docker

# List Docker images
sudo docker images


# List Docker images
docker images

# Add the Ubuntu user to the 'docker' group (Option 1 - without sudo)
usermod -aG docker ubuntu
# Explanation: Adds the user 'ubuntu' to the 'docker' group. This allows the user to run Docker commands without sudo.

# Add the Ubuntu user to the 'docker' group (Option 2 - with sudo, recommended for Ubuntu)
sudo usermod -aG docker ubuntu
# Explanation: Same as the previous command, but using 'sudo' to ensure elevated privileges for modifying user groups.

# Display user information to confirm group membership
id ubuntu
# Explanation: Displays information about the user 'ubuntu', including group memberships. Verify that 'docker' is listed among the groups.


# Run the 'hello-world' Docker container
docker run hello-world
# Explanation: Downloads and runs the 'hello-world' Docker container. Used for testing Docker installation and connectivity.

# Run an interactive shell in a new Ubuntu container
docker run -it ubuntu bash
# Explanation: Creates a new container from the 'ubuntu' image and opens an interactive bash shell within the container.

# List Docker images
docker images
# Explanation: Displays a list of locally available Docker images on the system.

# (Note: Removed the incorrect 'docker pd' command)

# List running Docker containers
docker ps
# Explanation: Displays a list of currently running Docker containers.

# List all Docker containers (including stopped ones)
docker ps -a
# Explanation: Displays a list of all Docker containers, whether running or stopped.

# List running Docker containers
docker container ls
# Explanation: Lists the running Docker containers.

# List Docker images
docker images
# Explanation: Displays a list of locally available Docker images on the system.

# Run the 'hello-world' Docker container
docker run hello-world
# Explanation: Downloads and runs the 'hello-world' Docker container. Used for testing Docker installation and connectivity.

# List all Docker containers (including stopped ones)
docker ps -a
# Explanation: Displays a list of all Docker containers, whether running or stopped.

# Remove Docker image by its name
docker rmi ubuntu
# Explanation: Removes the Docker image with the specified name.


# Display system-wide information
docker info
# Explanation: Shows detailed information about the Docker system.

# Display detailed information about a container or image
docker inspect hello-world
# Explanation: Provides detailed information about the specified Docker container (in this case, 'hello-world').

# Run a Docker container
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
docker run -d --name cafewebsite -p 9080:80 cafeimg
# Explanation: Starts a new Docker container based on the specified image.

# Execute a command in a running container
docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
docker exec -it myweb /bin/bash
# Explanation: Runs a command inside a running Docker container.
