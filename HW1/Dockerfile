FROM python:3.8-slim-buster

RUN apt-get update
RUN apt-get install -y --no-install-recommends apt-utils

RUN apt-get -y install python3-pip

RUN pip3 install pyinstaller uvloop

COPY . .

RUN rm -rf build && rm -rf dist && pyinstaller -F src/main.py

EXPOSE 8080

CMD ./dist/main deploy
