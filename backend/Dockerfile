FROM node:10.23.3-alpine

RUN mkdir -p /app
WORKDIR /app
COPY package*.json ./
RUN apk --no-cache add --virtual builds-deps build-base python
RUN npm install
COPY . .
EXPOSE 4242
ENV NODE_ENV prod
ENTRYPOINT ["npm", "start"]