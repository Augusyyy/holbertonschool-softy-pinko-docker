# Use the latest Ubuntu base image
FROM ubuntu:latest

# Update and upgrade the package lists
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install flask

# Set the working directory
WORKDIR /app
# Copy the Flask application file
COPY api.py /app

# Set the FLASK_APP environment variable
ENV FLASK_APP=api.py

# Expose the port the app runs on
EXPOSE 5252

CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=5252"]
