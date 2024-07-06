# Dockerizing frontend: Dockerfile for building react + chakra-ui app
FROM node:18-alpine

WORKDIR /frontend

COPY package.json .

RUN npm install

COPY . .

RUN npm run build

EXPOSE 3000

CMD ["npx", "vite", "preview", "--port", "3000"]
