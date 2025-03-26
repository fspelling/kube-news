FROM node:20.10.0-alpine3.19
WORKDIR /app

RUN adduser -D fspelling
COPY --chown=fspelling:root --chmod=700 package*.json .
RUN npm install
COPY --chown=fspelling:root --chmod=700 . .

EXPOSE 8080
ENTRYPOINT [ "node", "server.js" ]
USER fspelling