FROM        docker.io/ubuntu:latest

ENV         container docker

COPY        ./configCommander ./configCommander

RUN         apt update && \
            apt install -y build-essential python3 python3-pip && \
            cd ./configCommander && \
            make install && \
            cd config_commander_api

EXPOSE      8000/tcp

CMD         cd /configCommander/config_commander_api && uvicorn configCommanderAPI:app --host 0.0.0.0 --reload
