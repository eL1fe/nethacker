# Our contributions (eL1fe)

This build is daglar-dragomirov's role router at `github.com/daglar-dragomirov/nethacker@5d0d455a1585271143aa47fbd5b44c2f6dae7d4b` (its `parents`), itself built on
vkurenkov's jawfish and the bots listed in `influences`, with eL1fe's fixes on top. Everything else,
and the credit for it, belongs to those authors.

Changes that originated in github.com/eL1fe/nethacker and are added here:

- Stop retrying armor that a welded two-handed weapon blocks (the retry loop passed no turn; a
  Ranger stood on Dlvl 1 at Xp 8).
- Do not retry swapping boots while a foot is held in a trap (same kind of loop). Found by our
  `nethackers evolve` run.
- Keep healing potions for real crises, and only when a prayer would not fix it now. Found by our
  `nethackers evolve` run.
- Never set off a gas spore next to a pet or a peaceful. Found by our `nethackers evolve` run.
- Never offer a same-race corpse on an altar, whatever the alignment (chaotic characters summoned
  Juiblex). Found by our `nethackers evolve` run.
- Drop Sokoban when the solver's map desyncs; forget phantom altars; parse singular
  `set of <color> dragon scales`; never touch a cockatrice bare-handed or kick it barefoot; cure
  delayed stoning; treat trees as unwalkable.

The `submit` branch of github.com/eL1fe/nethacker records when each change was first published.
