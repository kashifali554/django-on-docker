#Testing Django with Docker

### Docker commands

Build command

```
docker-compose build
```

run the container
```
docker-compose up -d
```

logs
```
docker-compose logs -f
```

Source activate command

```
source env/bin/activate
```

manage.py is in hello_django folder

If docker build is failed to locate the docker file. Specify where the Dokcerfile is located.
look at this snippit of code in docker-compose.yml

```
    build:
      context: .
      dockerfile: Dockerfile
```