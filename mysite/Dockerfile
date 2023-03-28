# # Dockerfile
# FROM python:3.7-windowsservercore

# WORKDIR /app

# RUN python -m pip install --upgrade pip

# COPY requirements.txt requirements.txt
# RUN python -m pip install -r requirements.txt

# COPY . .


# # runs the production server
# # ENTRYPOINT ["python", "mysite/manage.py"]
# CMD ["python","/manage.py","runserver","0.0.0.0:8000"]


# Pull base image
FROM python:3.10.2-slim-bullseye

# Set environment variables
ENV PIP_DISABLE_PIP_VERSION_CHECK 1
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work directory
COPY . code
WORKDIR /code

# Install dependencies
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# Copy project
COPY . .

# EXPOSE 8000

# CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]






