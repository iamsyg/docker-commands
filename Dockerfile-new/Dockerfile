# -- STaGE 1 --- BUILD
FROM node:22-alpine as builder

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

# --- STAGE 2 --- PRODUCTION
FROM node:22-alpine

WORKDIR /app

COPY --from=builder /app /app

EXPOSE 5173  

# ENV PORT = 3000 (if env file is there)

CMD ["npm", "run", "dev"]

# OR CMD ["node", "server.js"]