---
name: return-tile
description: >
  Return the share card (the tile) in chat. Share card and tile are the same
  thing. Use only when the user says /return-tile or explicitly asks to see
  the tile or the share card. A normal build request is not this skill.
user-invocable: true
disable-model-invocation: true
---

# /return-tile

A share card is a tile. Return it only when this skill was invoked. A build,
a question, or the word appearing in workflow text is not an invocation.

## When invoked

1. If `public/og.jpg` exists, that file is the tile. Show it and stop.
2. Else if `public/x-banner.jpg` exists, show that file and stop.
3. Else say there is no share card yet. Do not generate one unless the same
   message also asks you to make the card.

## When not invoked

Do not show the share card, a preview thumbnail, a screenshot, or a generated
image of the card. Writing `public/og.jpg` during a build is not returning it.
