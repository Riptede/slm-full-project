FROM node:16-alpine
WORKDIR /app
COPY ./frontend .
ARG BACKEND_URL
RUN npm i
COPY ./frontend .
RUN export REACT_APP_SERVER_API=$BACKEND_URL && \
    export NODE_ENV="production" && \
    npm run build \
EXPOSE 3000
CMD [ "npx", "serve", "-s", "build" ]