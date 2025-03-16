# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript and enable type-aware lint rules. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.









# docker-commands

- docker pull hello-world
- docker run hello-world
- docker ps -a
- docker stop [container_id]
- docker remove [container_id]
- docker images
- docker rm [container]
- docker rm -f [container]
- docker [container] prune
- docker rmi [image_id]
- docker run -d busybox
- docker run -it ubuntu        (Interative mode)
- docker run --name [name] [image]
- docker run -p 8080:80 [image]
- docker run -v $(pwd):/app [image]
- docker exec -it [container_id] /bin/bash
- docker logs [container]
- docker attach [container]
- docker kill [container]
- docker stop $(docker ps -q)
- docker start [container]
- docker [container]  :/path_to_file





- root/dockerfile


FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 5173  

ENV PORT = 3000  (if env file is there)

CMD ["npm", "run", "dev"]



- docker build -t vite-test .     [Run everytime for each changes]
- docker run -p 5173:5173 vite-test / [id]
- docker run -p 5173:5173 [vite-test : [tag] / [id]]    OR   docker run -p 4000:3000 -e PORT=3000 --rm [image]    OR     docker run -p 4000:3000 --env-file .env --rm [image]



- changes in Dockerfile, .Dockerignore, vite.config.js
