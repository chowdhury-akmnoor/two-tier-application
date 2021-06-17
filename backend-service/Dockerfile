
FROM python:3.7.1

RUN mkdir /app
WORKDIR /app

RUN apt update -y
RUN apt install -y python-pip python-dev

COPY ./requirements.txt /app/requirements.txt

RUN pip3 install -r requirements.txt

ADD . /app
ENV FLASK_APP=app.py
EXPOSE 5000

CMD [ "flask", "run", "--host", "0.0.0.0"]

