FROM node:latest as build 
WORKDIR /usr/local/app
COPY ./ /usr/local/app/
RUN npm install 
RUN npm run build 

#Fase 2
FROM nginx:latest
COPY --from=build /usr/local/app/dist/review /usr/share/nginx/html 
EXPOSE 80 

