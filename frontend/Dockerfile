FROM node:14-alpine
WORKDIR /src
COPY package*.json ./
RUN npm install
#ADD nvm.tar.gz ./
ADD https://github.com/nvm-sh/nvm/archive/refs/tags/v0.39.1.tar.gz /tmp/nvm.tar.gz
COPY . ./
#RUN tar -xf nvm.tar.gz -C /tmp/
CMD [ "npm", "start" ]