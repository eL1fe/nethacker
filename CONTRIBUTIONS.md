# Our contributions (eL1fe)

This build is Komershan's bot at `github.com/Komershan/nethacker@f8a5821` (its `parents`) with
eL1fe's fixes on top. Everything else, and the credit for it, belongs to Komershan and the bots
listed in `influences`.

Changes that originated in github.com/eL1fe/nethacker:

- Stop retrying armor that a welded two-handed weapon blocks ("You cannot do that while holding
  your weapon" looped forever without passing a turn; a Ranger stood on Dlvl 1 at Xp 8).
- Remember doorways that refuse a diagonal step (the retry loop stalled a Knight on Dlvl 18).
  Found by our `nethackers evolve` run.
- Never offer a same-race corpse on an altar: a chaotic character summons a demon lord that way
  ("poisoned by Juiblex" on Dlvl 1). Found by our `nethackers evolve` run.
- Keep healing potions for real crises (below a third of max HP or at 5 HP, and only when a
  prayer would not fix it now); the old "HP < 8" rule drank both starting potions on scratches.
  Found by our `nethackers evolve` run.
- Never set off a gas spore next to a pet or a peaceful: killing the pet angers the god and every
  later prayer fails. Found by our `nethackers evolve` run.
- Stop at "Nothing happens" when zapping an empty wand: the direction key was sent anyway and
  became a move (one walked into a peaceful shopkeeper), and the dud wand kept being chosen in
  fights. Tag it and never zap it again. Found independently by two of our `nethackers evolve` runs.
- Run AutoAscend with `panic_on_errors=True`, so an assertion goes through AutoAscend's own panic
  recovery instead of killing the agent thread and stalling the episode.
- Drop Sokoban when the solver's map desyncs; forget phantom altars; parse singular
  `set of <color> dragon scales`.
- Never touch a cockatrice bare-handed or kick it barefoot; cure delayed stoning with a lizard or
  acid blob corpse or by praying.
- Keep wand rays off peaceful monsters; never kick a door while a shopkeeper is in view.
- Treat trees as unwalkable; skip Elbereth against `@` and minotaurs.
- The Xp 8 grind before diving (this base already grinds to Xp 8 for most roles) was first found
  for the Monk in eL1fe/nethacker@ff8e491.

The `submit` branch of github.com/eL1fe/nethacker records when each change was first published.
