


# 
# View logs for a Docker container (incorrect command)
docker logs
# Explanation: Incorrectly used 'docker logs' without specifying a container. Corrected in the next command.

# Pull the Nginx image from Docker Hub
docker pull nginx
# Explanation: Downloads the Nginx image from the official Docker Hub repository.

# List all Docker images (incorrect command)
dcoker images
# Explanation: Incorrectly spelled "docker" as "dcoker." Corrected in the next commands.

# List all Docker images
docker images
# Explanation: Lists all Docker images on the system.

# List all Docker containers
docker ps -a
# Explanation: Lists all Docker containers, including stopped ones.

# Inspect Docker image (incorrect command)
dcoker inspect nginx
# Explanation: Incorrectly spelled "docker" as "dcoker." Corrected in the next command.

# Inspect Docker image
docker inspect nginx
# Explanation: Displays detailed information about the Nginx Docker image.

# View logs for a Docker container named "nginx"
docker logs nginx
# Explanation: Displays the logs for the Docker container named "nginx."

# Run Nginx container in detached mode and map ports dynamically
docker run -d -P nginx
# Explanation: Runs the Nginx container in detached mode and maps ports dynamically.

# List all Docker containers (incorrect command)
dcoker ps -a
# Explanation: Incorrectly spelled "docker" as "dcoker." Corrected in the next commands.

# List all Docker containers
docker ps -a
# Explanation: Lists all Docker containers, including stopped ones.

# View logs for a Docker container with an incorrect name (contains space and missing quotes)
docker logs Product Support Engineer)
# Explanation: The command is incorrect; it seems like an attempt to view logs for a container with a problematic name.

# View logs for a Docker container with a specific ID
docker logs 5a51c3c5aea8
# Explanation: Displays the logs for the Docker container with the specified ID.

# Run Nginx container, mapping ports dynamically
docker run -P nginx
# Explanation: Runs the Nginx container and maps ports dynamically.

# Run Nginx container in detached mode
docker run -d nginx
# Explanation: Runs the Nginx container in detached mode.

# List all Docker images
docker images

# List all Docker containers (incorrect command)
dcoker ps -a
# Explanation: Incorrectly spelled "docker" as "dcoker." Corrected in the next commands.

# List all Docker containers
docker ps -a

# Clear the terminal screen
clear

# Run MySQL 5.7 container in detached mode, mapping ports dynamically
docker run -d -P mysql:5.7
# Explanation: Runs the MySQL 5.7 container in detached mode and maps ports dynamically.

# List all Docker containers
docker ps -a

# List running Docker containers
docker ps

# View logs for a specific Docker container named "heuristic_jang"
docker logs heuristic_jang

########################## not running ###############3

#  docker logs heuristic_jang
2023-11-15 06:23:21+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 5.7.44-1.el7 started.
2023-11-15 06:23:22+00:00 [Note] [Entrypoint]: Switching to dedicated user 'mysql'
2023-11-15 06:23:22+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 5.7.44-1.el7 started.
2023-11-15 06:23:22+00:00 [ERROR] [Entrypoint]: Database is uninitialized and password option is not specified
    You need to specify one of the following as an environment variable:
    - MYSQL_ROOT_PASSWORD
    - MYSQL_ALLOW_EMPTY_PASSWORD
    - MYSQL_RANDOM_ROOT_PASSWORD


# Run MySQL 5.7 container in detached mode, map ports dynamically, and set the root password
docker run -d -P -e MYSQL_ROOT_PASSWORD=mypass mysql:5.7
# Explanation:
# - -d: Run the container in detached mode.
# - -P: Publish all exposed ports to random ports on the host.
# - -e MYSQL_ROOT_PASSWORD=mypass: Set the environment variable for the MySQL root password.
# - mysql:5.7: Specifies the Docker image to use (MySQL version 5.7).

# List all Docker containers
docker ps -a
# Explanation: Lists all Docker containers, including the newly created MySQL container.

# View logs for a specific Docker container named "loving_pascal"
docker logs loving_pascal
# Explanation: Displays the logs for the Docker container with the specified name "loving_pascal."


################ working now ###################3


# ubuntu@ip-172-31-27-243:~$ docker logs loving_pascal
2023-11-15 06:38:48+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 5.7.44-1.el7 started.
2023-11-15 06:38:48+00:00 [Note] [Entrypoint]: Switching to dedicated user 'mysql'
2023-11-15 06:38:48+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 5.7.44-1.el7 started.
2023-11-15 06:38:49+00:00 [Note] [Entrypoint]: Initializing database files
2023-11-15T06:38:49.182717Z 0 [Warning] TIMESTAMP with implicit DEFAULT value is deprecated. Please use --explicit_defaults_for_timestamp server option (see documentation for more details).
2023-11-15T06:38:50.033986Z 0 [Warning] InnoDB: New log files created, LSN=45790
2023-11-15T06:38:50.269668Z 0 [Warning] InnoDB: Creating foreign key constraint system tables.
2023-11-15T06:38:50.340770Z 0 [Warning] No existing UUID has been found, so we assume that this is the first time that this server has been started. Generating a new UUID: a2fa77a6-8381-11ee-90dc-0242ac110005.
2023-11-15T06:38:50.343386Z 0 [Warning] Gtid table is not ready to be used. Table 'mysql.gtid_executed' cannot be opened.
2023-11-15T06:38:50.755924Z 0 [Warning] A deprecated TLS version TLSv1 is enabled. Please use TLSv1.2 or higher.
2023-11-15T06:38:50.756178Z 0 [Warning] A deprecated TLS version TLSv1.1 is enabled. Please use TLSv1.2 or higher.
2023-11-15T06:38:50.760206Z 0 [Warning] CA certificate ca.pem is self signed.
2023-11-15T06:38:50.775474Z 1 [Warning] root@localhost is created with an empty password ! Please consider switching off the --initialize-insecure option.
2023-11-15 06:38:53+00:00 [Note] [Entrypoint]: Database files initialized
2023-11-15 06:38:53+00:00 [Note] [Entrypoint]: Starting temporary server
2023-11-15 06:38:53+00:00 [Note] [Entrypoint]: Waiting for server startup
2023-11-15T06:38:53.575123Z 0 [Warning] TIMESTAMP with implicit DEFAULT value is deprecated. Please use --explicit_defaults_for_timestamp server option (see documentation for more details).
2023-11-15T06:38:53.577137Z 0 [Note] mysqld (mysqld 5.7.44) starting as process 125 ...
2023-11-15T06:38:53.590967Z 0 [Note] InnoDB: PUNCH HOLE support available
2023-11-15T06:38:53.591115Z 0 [Note] InnoDB: Mutexes and rw_locks use GCC atomic builtins
2023-11-15T06:38:53.591242Z 0 [Note] InnoDB: Uses event mutexes
2023-11-15T06:38:53.591361Z 0 [Note] InnoDB: GCC builtin __atomic



















