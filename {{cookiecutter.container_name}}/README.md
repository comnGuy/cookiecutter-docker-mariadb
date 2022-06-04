# Notes

This folder is only for the dataset-db to mount the data of the DB.

## docker-compose

Add the following lines to docker-compose.

```
  {{cookiecutter.container_name}}:
    image: mariadb
    volumes:
      - ./{{cookiecutter.container_name}}/data:/var/lib/mysql
    restart: always
    env_file:
      - ./_env/{{cookiecutter.container_name}}.env
    ports: # TODO!
      - {{cookiecutter.port}}:3307
```
