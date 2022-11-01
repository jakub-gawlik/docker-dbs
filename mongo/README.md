# What is it?

Dockerised bundle that includes [MongoDB](https://www.mongodb.com/) server and web database management interface [Mongo Express](https://github.com/mongo-express/mongo-express)

# Running

Make sure you have [Docker]() and [Docker compose]() installed on your machine.

Run `docker-compose up`. It will install the bundle.

Mongo express will be available on `http://localhost:8081`. If you want to secure this interface with a password, uncomment those lines in `docker-compose.yml`:

```
ME_CONFIG_BASICAUTH_USERNAME=admin
ME_CONFIG_BASICAUTH_PASSWORD=admin
```

and adjust the login details respectively.
