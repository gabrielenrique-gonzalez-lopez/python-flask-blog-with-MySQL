# Use an official Python runtime as a parent image
FROM python:3.10.11-buster

# Set the working directory to /app
WORKDIR /flask-blog

RUN mkdir -pv app

# Copy the current directory contents into the container at /app
COPY . app/

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r app/requirements.txt

ENV FLASK_RUN_HOST=0.0.0.0

# Expose port 5000 for the Flask app
EXPOSE 5000

# Run the command to start the Flask app
CMD [ "flask", "--app", "app", "run"]
