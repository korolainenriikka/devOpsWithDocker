FROM ubuntu:16.04
EXPOSE 8000

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

COPY . /home/app/
WORKDIR /home/app

RUN npm install
CMD FRONT_URL=http://localhost:5000 npm start
