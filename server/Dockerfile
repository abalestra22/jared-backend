FROM node:9

# Create app directory
WORKDIR /usr/src/app

COPY . .

# Install app dependencies
RUN yarn --prod && yarn cache clean

ADD https://github.com/ufoscout/docker-compose-wait/releases/download/2.3.0/wait /wait
RUN chmod +x /wait

EXPOSE 3000
CMD /wait && yarn start


