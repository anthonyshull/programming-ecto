# Usage

```
%> brew install postgresql
%> docker run --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=postgres -d postgres
%> iex -S mix
```

```elixir
iex> alias MusicDB.Repo
iex> query = from a in "albums", select: a.title, order_by: [:title]
iex> Repo.all(query)
```