
# Build Image

https://www.tooplate.com/zip-templates/2137_barista_cafe.zip

![Alt text](image-4.png)

### install.sh file and start deployment 

# Download the webpage source code in a zip file from the specified URL
wget https://www.tooplate.com/zip-templates/2137_barista_cafe.zip

# Unzip the downloaded zip file
unzip 2137_barista_cafe.zip

# List the contents of the extracted directory
ls 2137_barista_cafe/

# Change into the directory containing the extracted files
cd 2137_barista_cafe/

# Create a compressed tar archive (tar.gz) of all files in the directory
tar czvf barista.tar.gz *

# Move the tar archive to the parent directory
mv barista.tar.gz ../

# List the contents of the parent directory
ls ../

# Change to the home directory
cd

# Copy the tar archive to the specified directory (assumes 'images/cafe/' exists)

cp barista.tar.gz images/cafe/

# Change into the target directory
cd images/cafe/

# Edit the Dockerfile to specify the image configuration (e.g., dependencies, commands)
vim Dockerfile

# /images/cafe# ls
Dockerfile  barista.tar.gz

# Build a Docker image with the specified tag 'cafeimg' using the current directory as the build context
docker build -t cafeimg .

# List the currently running Docker containers
docker ps

# List all Docker containers (both running and stopped)
docker ps -a

docker images

# Run a Docker container in detached mode (-d) named 'cafewebsite,' mapping host port 9080 to container port 80
docker run -d --name cafewebsite -p 9080:80 cafeimg
