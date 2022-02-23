FROM node:16

# Create app directory
RUN mkdir -p /usr/app
WORKDIR /usr/app

COPY . .

ENV REACT_APP_DOORS_BACKEND_URL "http://localhost:8080"
ENV NODE_ENV production

RUN npm install
RUN npm run build

FROM nginx
RUN mkdir -p /usr/share/nginx/html
COPY --from=0 /usr/app/build /usr/share/nginx/html

