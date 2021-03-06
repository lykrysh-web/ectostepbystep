# Ectostepbystep

## Reference

B. Barroso's [tutorial](https://www.toptal.com/elixir/meet-ecto-database-wrapper-for-elixir)


## Summary

`mix new ectostepbystep --sup` // set up a supervisor tree<br>
Add ecto and postgrex in mix.exs. mod: {Ectostepbystep.~~Application~~, []}<br>
`mix deps.get` // install dependencies<br>
Configure database in config/config.exs

    use Mix.Config
    config :cart, ecto_repos: [Cart.Repo]

`mix ecto.gen.repo`<br><br>

Add supervisor to the children list in lib/ectostepbystep.ex<br>
Set username and pw in config/config.exs<br>
`mix ecto.create`<br>
<br>
`mix ecto.gen.migration create_invoices`<br>
Create table in priv/repo/migration/20...._create_invoices.exs<br>
`mix ecto.migrate`<br>
<br>
Create table in priv/repo/migration/20...._create_items.exs<br>
`mix ecto.migrate`<br>
<br>
Create table in priv/repo/migration/20...._create_invoice_items.exs<br>
`mix ecto.migrate`<br>


## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `ectostepbystep` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:ectostepbystep, "~> 0.1.0"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/ectostepbystep](https://hexdocs.pm/ectostepbystep).


