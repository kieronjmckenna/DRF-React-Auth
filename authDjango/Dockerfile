FROM python:3.8.3

ENV PYTHONUNBUFFERED 1

RUN mkdir /api
WORKDIR /api
COPY requirements.txt /api/
RUN pip install -r requirements.txt
RUN python manage.py makemigrations
RUN python manage.py migrate

COPY . /api/
