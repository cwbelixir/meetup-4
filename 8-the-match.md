# The match

- Let's generate the match!
- `mix phx.gen.html Football Match matches date:date`
- But wait! We only have the match date! We need each team players!
- `mix phx.gen.html Football MatchPlayer match_players match_id:references:matches player_id:references:players team:integer`
- Let's add the match players selector on match creation
  - Add `player_ids` to the `templates/match/form.html.eex` with the list of players
  - Do not show the list on match edit
  - Load the list of players on the controller and send it to new templates
  - We should send the player's name and id, and not the whole player
    - Introducing `Enum` and anonymous functions
- And now let's create the match players
  - Introducing `Ecto.Repo` and `Ecto.Query`
  - Load all selected players
  - Create the `MatchPlayer`s
- Balance the players in the teams!!
  - The business logic
  - Show the match, player name and stars on match_players list
