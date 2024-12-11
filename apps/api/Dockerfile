FROM node:14-alpine AS build
WORKDIR /opt/app
ADD *.json ./
RUN npm install
ADD . .
RUN npm run build api

FROM node:14-alpine
WORKDIR /opt/app
ADD package.json ./
RUN npm install --production
COPY --from=build /opt/app/dist/apps/api ./dist/
CMD ["node", "./dist/main.js"]