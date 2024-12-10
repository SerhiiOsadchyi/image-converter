sudo apt-get install curl
sudo apt-get install nodejs
node -v
sudo apt-get install npm
npm -v
nvm -v
nvm install 14
nvm use 14

npm i
npm run build api
node dist/apps/api/main.js

docker build -f apps/api/Dockerfile -t mono:latest