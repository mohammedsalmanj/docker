# Use the official Ubuntu base image
FROM ubuntu

# Metadata as defined above
LABEL author="salman" \
      project="cafe"

# Set non-interactive mode during installation
ENV DEBIAN_FRONTEND=noninteractive

# Update package list and install necessary packages
RUN apt-get update && \
    apt-get install -y git apache2

# Set the default command to start Apache in the foreground
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]

# Expose port 80 for incoming web traffic
EXPOSE 80

# Set the working directory to /var/www/html
WORKDIR /var/www/html

# Create a volume for Apache logs
VOLUME /var/log/apache2

# Add the contents of barista.tar.gz into the container
ADD barista.tar.gz /var/www/html/

# 
COPY barista.tar.gz /var/www/html/
