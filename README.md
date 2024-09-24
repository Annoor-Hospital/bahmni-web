# Bahmni Web Docker

This project sets up a simple web server using Apache (httpd) to serve Bahmni front-end files. Docker image exposes port 8091.

Files and folders can be mounted in the docker-compose, file:

``` yaml
services:
  bahmni-web:
    image: annoor-docker/bahmni-web:1.0.0
    volumes:
      - "./bahmni-web:/usr/local/apache2/htdocs:ro"  # Mount contents of bahmni-web folder for serving.
    restart: always
```