# The players

- So let's create the player
- `mix phx.gen.html Football Player players name:string stars:integer`
  - Asks to add something on the router
  - Generates migration
  - Generates the schema (aka model)
    - WTF is `alias`, `import` and `use`
  - Generates the context
  - Generates the controller
    - WTF is `conn` and `plug`?
  - Generates the view
  - Generates the templates
- `mix ecto.migrate`
- Check out the results so far - [http://localhost:4000/players]()
- Add validations
  - Rank should be a 1 to 5 number
  - We use `Ecto.Changeset`s for that
    - WTF is `|>`
  - Let's try it using `validate_number/3` with `max` and `min`
  - Pan! No `max` option, let's find out the right name.

