Put the following into "stack.yml":

# Use postgres/example user/password credentials
#8080:8080 for outside:inside

version: '3.1'

services:

  db:
    image: postgres
    restart: always
    environment:
      POSTGRES_PASSWORD: example

  adminer:
    image: adminer
    restart: always
    ports:
      - 8080:8080


Then run 

docker-compose -f stack.yml up

In adminer, export and save.
