FROM node:7.8.0

ENV NPM_CONFIG_LOGLEVEL warn

COPY . .

RUN npm run build

# Update
RUN apt-get update

# Install NGINX
RUN apt-get install -y nginx


# Remove the default Nginx configuration file
RUN rm -v /etc/nginx/nginx.conf

# Copy a configuration file from the current directory
ADD nginx.conf /etc/nginx/

# Copy build directory to Nginx
Add ./build /usr/share/nginx/html

# Append "daemon off;" to the configuration file
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

EXPOSE 3000

# Set the default command to execute when creating a new container
CMD service nginx start