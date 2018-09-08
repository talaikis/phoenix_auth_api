# Phoenix API

Fork of [Phoenix-JWT-Auth-API](https://github.com/njwest/Phoenix-JWT-Auth-API)

## Start

```bash
mix deps.get
mix ecto.create
mix ecto.migrate
iex -S mix phx.server
```

## Secrets

1. Generate:

```bash
mix phoenix.gen.secret
```

2. Edit appropriate .env (.env.prod or .env.dev)

## Test

```bash
mix test
```

## Endpoints

```bash
# with header" "Authorization": "Bearer " + jwt:
GET http://localhost:4000/api/v1/user

POST http://localhost:4000/api/v1/sign_in
{
  "email": "foobar@email.com",
  "password": "some_password"
}

POST http://localhost:4000/api/v1/sign_up
{
  "user": {
    "email": "foobar@email.com",
    "password": "some_password",
    "password": "some_password"
  }
}
```

## TODO

* Fix failing tests inherited from original repo.
* Fisnih dotenv implementation.
* Other required routes.
