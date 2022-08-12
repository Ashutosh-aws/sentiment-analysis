FROM node:14 as build
COPY . /opt/
WORKDIR /opt/
RUN  npm install
RUN  npm run-script build

FROM nginx
COPY --from=build /opt/build/ /usr/share/nginx/html
