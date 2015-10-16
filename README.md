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
  - enforce data types with guards
- do work
  - module logic should be in module, not functions using it
- return values
  - returned value should be meaningful
- handle errors

GildedRose example of code to refactor: https://github.com/NotMyself/GildedRose

Pattern-matching usage basics. Pretty good.

I have expected more about error handling, but I got only:
"Use supervisors, unless you want to return error to user."

Pretty good basics. 7/10

## Release Management with Exrm and Conform by Paul Schoenfelder  [34 min]

http://confreaks.tv/videos/elixirconf2015-release-management-with-exrm-and-conform

How to release your code:
- without releases
  - can use sftp or git
  - build is slow
  - no upgrade / downgrade
  - unstable
  - usable, but not best
- with release
  - self contained
  - easy to deploy
  - easy to reproduce - similar to Docker idea

Live release upgrade of phoenix chat demo.

Warning: configuration is evaluated during build, so you can't use System.env,
nor change them in production.

Creating new release:
- either have config stuff (ie. passwords) on dev machine
- or build release on CI
- or use Conform to read from production files.

Do you run integration tests from release? Docker would say `yes`.

Conform part is rather boring and heavy handed.

DevOps stuff, interesting. 7/10

## Building a visual programming tool using Elixir by Josh Adams [29 min]

http://confreaks.tv/videos/elixirconf2015-building-a-visual-programming-tool-using-elixir

Creating business rule engine.

Visually creating big `if` block in Bootstrap? I don't like it. Creating
"programming aids" for non-programmers always ends with programmers
writing non-programmers pseudo-programs. Why bother?

Code looks messy, uses smart hacks and then it is rendered in Angular. Sigh.

Skipped the rest. 0/10
