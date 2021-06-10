FROM python:3.9
ENV PYTHONUNBUFFERED 1

RUN mkdir /code
WORKDIR /code

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y postgresql netcat

COPY requirements.txt /code/
RUN pip install --upgrade pip && \
	pip install -r requirements.txt

COPY . /code/

ENTRYPOINT ["./entrypoint.sh"]
