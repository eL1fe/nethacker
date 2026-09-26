# Our contributions (eL1fe)

This bot builds on AutoAscend and on daglar-dragomirov's dive bot (see `parents` and
`influences` in `nethackers.solution.json`). These changes originated here:

**All roles**
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

- Never offer a same-race corpse on an altar: a chaotic character summons a demon lord that way
  (the "poisoned by Juiblex" deaths on Dlvl 1). Found by our `nethackers evolve` run (Opus 5.5),
  kept after a 60-seed check.
- Remember doorways that refuse a diagonal step instead of retrying the same move forever.
  Found by the same run.

**Monk**
- Cast the healing spell a third of Monks start with.
- Grind to Xp 8 before the Mines pick hunt and digging (Xp 5 Monks died to Mines packs).
- Rest to 90% HP before exploring when nothing hostile is in sight.
- Pray when Weak from hunger once the prayer timeout has surely expired (the pet eats most corpses on the long Dlvl 1 grind).

The `submit` branch of github.com/eL1fe/nethacker records when each change was first published
(Monk healing and the cockatrice guard: ff8e491; crash fixes: 6585733).
