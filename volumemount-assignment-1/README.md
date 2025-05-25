# Docker commands for this:

## 1. `docker container run -d --name psql174 -e POSTGRES_HOST_AUTH_METHOD=trust  -v psql:/var/lib/postgresql/data postgres:17.4`

## 2. `docker container run -d --name psql175 -e POSTGRES_HOST_AUTH_METHOD=trust  -v psql:/var/lib/postgresql/data postgres:17.5`

- Same Volume is mounted to both containers.
- "Mounts": [
            {
                "Type": "volume",
                "Name": "psql",
                "Source": "/var/lib/docker/volumes/psql/_data",
                "Destination": "/var/lib/postgresql/data",
                "Driver": "local",
                "Mode": "z",
                "RW": true,
                "Propagation": ""
            }
        ],
