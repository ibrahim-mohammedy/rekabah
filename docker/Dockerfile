FROM ubuntu:20.04

ENV NVM_DIR="$HOME/.nvm"
RUN apt update -y
RUN apt install curl  -y

WORKDIR /portal

RUN mkdir -p "/.nvm" && \ 
    curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash   && \ 
    export NVM_DIR="/.nvm"  && \ 
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"   && \ 
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  && \ 
    nvm install node && node -v && npm -v && \
    npm install -g @angular/cli 