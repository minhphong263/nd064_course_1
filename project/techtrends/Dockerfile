# Use a Python base image in version 3.8
FROM python:3.8

# Set the working directory
WORKDIR /app

# Copy the requirements.txt file to the working directory
COPY requirements.txt .

# Install the packages defined in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code to the working directory
COPY . .

# Expose the application port
EXPOSE 3111

# Ensure that the database is initialized with the pre-defined posts
RUN python init_db.py

# Command to run the application
CMD ["python", "app.py"]