# Use the latest Nginx base image
FROM nginx:latest

# Set the working directory
WORKDIR /var/www/html

# Copy the front-end files
COPY ./softy-pinko-front-end /var/www/html

# Copy the Nginx configuration file
COPY softy-pinko-front-end.conf /etc/nginx/nginx.conf

# Expose the port
EXPOSE 9000

# Start Nginx and keep it running
CMD ["nginx", "-g", "daemon off;"]