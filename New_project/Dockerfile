FROM python:3.13.2-alpine3.21

WORKDIR /app

#install system dependencies required for psycopg2
RUN apk add --no-cache \
    postgresql-dev \ 
    gcc \
    musl-dev \
    libffi-dev \
    python3-dev

# copy project files
COPY requirements.txt .

#install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# expose for utilize the port with Django app
EXPOSE 8000