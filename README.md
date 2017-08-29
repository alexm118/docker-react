Docker React

Simple app to show an easy scaffold for hosting a react up with nginx inside a docker container

Command to run

```
docker run --name docker-nginx -p 3000:3000 -v ~/Code/docker-react/docker-app/build:/usr/share/nginx/html -v ~/Code/docker-react/docker-app/default.conf:/etc/nginx/conf.d/default.conf  nginx
```