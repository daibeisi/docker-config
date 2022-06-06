# syntax=docker/dockerfile:1
FROM python:3
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
WORKDIR /Django
COPY requirements.txt /Django/
RUN python -m pip install --upgrade pip
RUN pip install -r requirements.txt
COPY . /Django/