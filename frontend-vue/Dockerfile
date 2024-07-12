FROM nginx:latest

ENV TZ Asia/Seoul
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone 

COPY ./frontend-vue/nginx.conf /etc/nginx/nginx.conf
COPY ./frontend-vue/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]