# ~/docker_server/nginx/Dockerfile
FROM nginx:latest 
# 도커 개발자들이 만들어놓은 이미지 워낙 많이 쓰이니까 도커 개발자들이 엔진엑스 이미지를 만들어둠

COPY nginx.conf /etc/nginx/nginx.conf
COPY nginx-app.conf /etc/nginx/sites-available/

RUN mkdir -p /etc/nginx/sites-enabled/\
    && ln -s /etc/nginx/sites-available/nginx-app.conf /etc/nginx/sites-enabled/

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
