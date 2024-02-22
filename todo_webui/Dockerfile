FROM node:20-bookworm-slim

WORKDIR /app

COPY . .
RUN npm ci
RUN npm run build --location=project

CMD ["npm", "start"]
