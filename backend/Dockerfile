FROM rasa/rasa:1.10.3
USER root
WORKDIR /app
COPY . /app
COPY ./data /app/data

RUN  rasa train

VOLUME /app
VOLUME /app/data
VOLUME /app/models

CMD [ "run","-m", "-port","9000", "/app/models","--enable-api","--cors","*","--debug" ]
