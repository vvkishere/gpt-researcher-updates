# Step 1: Use an official Python runtime as the base image
FROM python:3.11

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy the current directory contents into the container at /app
COPY . /app

# Step 4: Install any system dependencies (e.g., gcc, etc.)
RUN apt-get update && apt-get install -y --no-install-recommends \
    gcc \
    && rm -rf /var/lib/apt/lists/*

# Step 5: Install Python dependencies
RUN pip install --upgrade pip \
    && pip install -r requirements.txt

# Step 6: Expose the port the app runs on (if needed)
EXPOSE 11435

# Step 7: Set environment variables (if the application requires them)
# ENV ENV_VAR_NAME=value

# Step 8: Command to run the application
CMD ["python", "main.py"]
