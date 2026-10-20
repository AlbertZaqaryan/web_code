FROM python:3.12-alpine

RUN apt-get update && apt-get install -y build-essential libpq-dev

WORKDIR /app

COPY requirements.txt /app/

RUN python -m pip install --upgrade pip
RUN pip install django
COPY . /app/

EXPOSE 8000
CMD [ "python", "manage.py", "runserver", "0.0.0.0:8000" ]