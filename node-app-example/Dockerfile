FROM soso/ubuntu
EXPOSE 3000
WORKDIR /usr/src/app
COPY package.json .
COPY app.js .
RUN pnpm install
CMD ["pnpm", "run:app"]

