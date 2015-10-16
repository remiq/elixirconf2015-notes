# ElixirConf 2015 notes

Notes from watching ElixirConf 2015 videos.

## Keynote: The Pendulum by Bruce Tate [40 min]

http://confreaks.tv/videos/elixirconf2015-keynote-the-pendulum

History of business applications, how they moved between
Server-Client and Stand-alone.

What problem are we solving? It does not scale.

Author says that Phoenix fixes the problem with handling sessions by
itself and having websocket channels. Then shows comparison with
Ruby.

It did not convinced me. 2/10

## What's next for Phoenix by Chris McCord [33 min]

http://confreaks.tv/videos/elixirconf2015-what-s-next-for-phoenix

New things:
- i18n with gettext will be in Phoenix 1.1
- user presence on channels (join/leave events)
- GraphQL

gettext - looks nice and almost ready.

User presence - for chat room apps only.

GraphQL - client specifies structure of data in JSON. If I would
compare it to module defining both client and server functions in Elixir,
this seems oposite to GraphQL.

GraphQL solves backend/frontend development synchronization by making backend
return anything frontend wants. This means that frontend and malicious
users may access more than you want.

Does moving structure to frontend is a correct way? Probably contracts would
be better way to do that.

Local GraphQL for server-side html templates? Hmmmm...

Server-side virtual DOM and pushing DOM changes to client?

GraphQL written as XML looks familiar...

GraphQL looks interesting, but not that much. 5/10

## Confident Elixir by Lance Halvorsen [32 min]

http://confreaks.tv/videos/elixirconf2015-confident-elixir

"Confident code tells clear, coherent story."

Story structure:
- gather data
- do work
- return values
- handle errors

GildedRose example of code to refactor: https://github.com/NotMyself/GildedRose

Pattern-matching usage basics. Pretty good.

Pretty good basics. 7/10
