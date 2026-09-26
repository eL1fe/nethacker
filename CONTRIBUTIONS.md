# Our contributions (eL1fe)

This build is Komershan's bot at `github.com/Komershan/nethacker@8e0e320501ad2b70f8d912e3e555d4f1e59f786e` (its `parents`) with eL1fe's all-role
fixes on top. Everything else, and the credit for it, belongs to Komershan and the bots listed in
`influences`.

Changes that originated in github.com/eL1fe/nethacker:

- Run AutoAscend with `panic_on_errors=True`: an assertion no longer kills the agent thread and
  stalls the episode until the no-progress timeout; errors go through AutoAscend's own panic recovery.
- Drop Sokoban instead of crashing when the solver's map desyncs from the real level.
- Forget a remembered altar the game says is not there instead of crashing.
- Parse singular `set of <color> dragon scales` (it crashed the item parser).
- Never touch a cockatrice or chickatrice bare-handed or kick it barefoot.
- Keep wand rays off peaceful monsters (shopkeepers, priests, watchmen).
- Never kick a door while a shopkeeper is in view (falling into a closed shop was fatal).
- Treat trees as unwalkable (the bot looped forever on the Monk quest home).
- Cure delayed stoning with a lizard or acid blob corpse, or by praying.
- Skip Elbereth against `@` and minotaurs, who ignore it.

First published on the `submit` branch of github.com/eL1fe/nethacker (crash fixes: 6585733;
the rest: ff8e491, 08db7c6, 02c405e).
