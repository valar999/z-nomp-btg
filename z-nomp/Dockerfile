FROM node

RUN apt-get update && apt-get install -y libsodium-dev
RUN git clone https://github.com/z-classic/z-nomp
WORKDIR /z-nomp
RUN npm install n -g
RUN n stable
RUN npm update
RUN npm install
ADD btg_coin.json coins/btg.json
ADD btg_pool.json pool_configs/btg.json
ADD config.json .
CMD sleep 60; npm start
