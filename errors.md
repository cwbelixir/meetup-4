# Common errors

## Error:

When `mix ecto.create` gets exception:

** (Mix) The database for Socker.Repo couldn't be created:
an exception was raised:
  ** (DBConnection.ConnectionError) tcp connect (localhost:5432):
  connection refused - :econnrefused

### Solution:

- Remove `/usr/local/var/postgres/postmaster.pid` and restart postgres
- If it does not work, remove `/usr/local/var/postgres/` and reinstall postgres

## Error:

When `mix ecto.create` gets exception:

** (Mix) The database for Socker.Repo couldn't be created:
FATAL 28000 (invalid_authorization_specification): role
"postgres" does not exist

### Solution:

- `sudo -u kelvinst psql postgres`
- `CREATE USER postgres SUPERUSER;`
- `CREATE DATABASE postgres WITH OWNER postgres;`
