FROM ubuntu:22.04

LABEL APP="StudentappFE"
LABEL DevopsEngg="Mayur"

# Set non-interactive mode to avoid prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Update the system and install Apache
RUN apt update && apt install -y apache2 && apt clean

# Set the working directory
WORKDIR /var/www/html

# Copy your frontend files to the container
COPY index.html .

# Expose port 80 for HTTP
EXPOSE 80

# Start Apache in the foreground
CMD ["apachectl", "-D", "FOREGROUND"]

