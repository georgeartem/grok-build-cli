# Grok Build CLI

A share card is a tile. They are the same thing.

Do not return a share card with a build. Return it only when the user asks
with `/return-tile`, or explicitly asks to see the tile or the share card.

Writing `public/og.jpg` during a build is not returning the tile.
The workflow is `.grok/skills/return-tile/SKILL.md`.
