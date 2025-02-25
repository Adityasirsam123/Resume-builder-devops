# Use an official Python runtime as a parent image
FROM python:3.11-alpine3.18

# Set the working directory in the container
WORKDIR /app

# Copy the application files to the container
COPY . /app/

# Install dependencies
RUN pip install --upgrade pip \
    && pip install -r requirements.txt

# Expose the port on which the app runs
EXPOSE 8000

# Run migrations and start the server
CMD ["sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]
