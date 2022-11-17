FROM ubuntu:22.04

# install dependencies
RUN apt update && \
    apt upgrade -y && \
    apt install -y \
    git \
    npm \
    nodejs

# install amcat4client (the web client)
RUN git clone https://github.com/ccs-amsterdam/amcat4client /srv/amcat4client && \
    cd /srv/amcat4client && \
    npm install && \
    npx update-browserslist-db@latest  && \
    npm run build

EXPOSE 5000

WORKDIR /srv/amcat4client

CMD ["npm", "start"]
