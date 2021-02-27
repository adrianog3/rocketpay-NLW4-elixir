# Commands

```bash
# Install mix CLI
mix archive.install hex phx_new 1.5.7

# Create project
mix phx.new rocketpay --no-webpack --no-html

# Add this line into mix.exs on deps section 
{:credo, "~> 1.5", only: [:dev, :test], runtime: false}

# Install dependencies
mix deps.get

# Check credo syntax analyser
mix credo gen.config

# Run project
mix phx.server

# interactive elixir
iex -S mix

# create migration
mix ecto.gen.migration create_user_table

# execute migration
mix ecto.migrate
```

## Testing modules

```elixir
# iex -S mix
params = %{name: "Adriano Souza", password: "123456", email: "adriano@domain.com", nickname: "adrianog3", age: 25}
Rocketpay.Repo.all(Rocketpay.User) |> Rocketpay.Repo.preload(:account)
```
