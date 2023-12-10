# Persistent store

Persitent store will be generated in the persist directory that is created upon running the container.

# Initial database

An initial database that will become populated into the maindb database can be stored in this directory.
Don't forget to uncomment:

    - ./mysql/maindb.sql:/docker-entrypoint-initdb.d/maindb.sql

and check if the names are accordingly ('maindb.sql'). The name does not require to have the same name as the database.
