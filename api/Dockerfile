FROM node:14 AS Production

WORKDIR /app

COPY package.json .
COPY package-lock.json .

RUN npm install

ENV NODE_ENV=production

COPY . .

RUN npm run build

CMD ["sh","-c", "npm run start:production"]

