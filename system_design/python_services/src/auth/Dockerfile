FROM python:3.10-slim-bullseye

RUN apt-get UPDATE \
&& apt-get install -y --no-install-recommends --no-install-suggests \
build-essential default-libmysqlclient-dev \
&& pip install --no-cache-dir --upgrade pip

WORKDIR /app
COPY ./reqirements.txt /app
RUN pip install --no-cache-dir --requirement /app/requirement.txt
COPY . /app

EXPOSE 5000

CMD [ "python3", "server.py" ]
