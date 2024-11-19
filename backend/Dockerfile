FROM python:3.11-buster
LABEL authors="Sobhan Moghimi"
RUN apt -y update && apt -y install net-tools vim telnet curl

# set environment variables
# Avoid .pyc files to be created:
ENV PYTHONDONTWRITEBYTECODE=1
# No cache for python output in terminal:
ENV PYTHONUNBUFFERED=1
# Upgrade pip  to the latest version (Optional)
RUN pip3 install --upgrade pip

RUN mkdir /app
WORKDIR /app


COPY requirements.txt .
RUN pip3  install --no-cache-dir -r ./requirements.txt

COPY sample_app ./sample_app

EXPOSE 8100