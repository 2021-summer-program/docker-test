FROM ubuntu:20.04

#작업디렉토리 
WORKDIR /usr/src/app

RUN apt-get update -y && \
    apt-get install -y python3-pip python3-dev \
    build-essential libssl-dev libffi-dev python3-setuptools \
    python3-venv mongodb-clients

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

#현재 디렉토리 경로에 req.txt 복사 
COPY /backend/requirements.txt /usr/src/app
#-r 옵션은 파일(requirement.txt)에 적혀있는 라이브러리를 설치하라는 의미
RUN pip3 install -r requirements.txt 
RUN pip3 install flask-restx

EXPOSE 5000

CMD [ "python3", "app.py" ]