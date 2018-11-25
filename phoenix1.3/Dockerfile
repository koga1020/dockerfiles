FROM elixir:1.6.5-slim

ARG APP_DIR=/app

RUN mkdir ${APP_DIR}
WORKDIR ${APP_DIR}

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y \
    sudo \
    curl \
    git \
    vim \
    wget \
    gnupg \
    gcc \
    g++ \
    make

RUN yes | mix local.hex
RUN yes | mix archive.install https://github.com/phoenixframework/archives/raw/master/phx_new-1.3.4.ez
RUN mix local.rebar --force

RUN curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
RUN apt-get install -y nodejs
RUN npm install -g yarn
RUN apt-get clean

CMD ["mix", "phx.server"]