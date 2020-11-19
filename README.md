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

Check the logs
```
docker-compose logs -f
```

Source activate command

```
source env/bin/activate
```

manage.py is in hello_django folder

# Notes in Postgress section =

To persist the data beyond the life of the container we configured a volume. This config will bind postgres_data to the "/var/lib/postgresql/data/" directory in the container.

### Running the migration command
```
docker-compose exec web python manage.py migrate --noinput
```

Database access command
```
docker-compose exec db psql --username=hello_django --dbname=hello_django_dev
```
### DB commands after accessing the DB on container
Look at the list of databases in the container after connecting to the db.
```
\l
```

Login as a user 
Note: hello_django_dev is the user name

```
\c hello_django_dev
```

Viewing the table rows

```
\dt
```
Quit the database

```
\q
```
