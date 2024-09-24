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

The `www` folder only contains a copy of a standard set of files to mount. To store and mount these files, save them into the `bahmni-web` folder in your docker folder, and use a docker-compose config as above. You will also need to place a copy of `bahmniapps` and `bahmni_config` into this folder, or mount them as seperate volumes *after* mounting `bahmni-web`.