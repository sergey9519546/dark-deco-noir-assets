# dark-deco-noir-assets

Public image host for the Dark Deco Noir Flow tool's picture cards.

Why this repo exists: the Flow tool's builder cannot faithfully reproduce
raster image bytes through its own text channel (inline base64 corrupts on
re-emission — proven 2026-11-09), and its sandboxed Preview will not fetch
from Muse's file storage. Package CDNs are the allowed origins, so card
pictures live here and are served by jsDelivr.

URL pattern (pin a release tag once the set is final; `main` while testing):

    https://cdn.jsdelivr.net/gh/<user>/dark-deco-noir-assets@main/cards/<name>.webp

## Layout

- `cards/` — one WebP per picture card, 320x180, q55. Naming:
  `<slot>-<name>.webp` (e.g. `detective-320x180.webp` is the Lead &
  Sidekick test card).
- Future batches (24 story frames, 6 zone plates, ~8 look frames,
  7 character-group portraits) land in `cards/` under the same naming
  once gate-checked and keep/kill-approved.

## Rules

- Only gate-passed exemplar images go here — nothing unreviewed.
- Never commit licensed characters as the face of an original archetype
  (character cards use original generated exemplars only).
- Do not rename a file once a tool build references its URL.
