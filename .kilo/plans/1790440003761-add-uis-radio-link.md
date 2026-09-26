# Add UIS Radio Link

## Goal
Insert a new "UIS Radio" link between X and WhatsApp in both the link cards and the social icon row.

## Current insertion points
- `data/links.js`: X entry ends at line 79; WhatsApp entry starts at line 80
- `index.html`: X anchor ends at line 87; Viber anchor starts at line 88; WhatsApp anchor starts at line 91
- `script.js`: ICONS map has no radio icon; closest existing icon is `globe`

## Decisions
- Use existing `globe` icon for the Radio entry; no new SVG needed
- Insert new link card in `data/links.js` after X, before WhatsApp
- Insert new social anchor in `index.html` after X, before Viber

## Tasks
1. Edit `data/links.js` and insert a new link object between X and WhatsApp with:
   - `title`: "UIS Radio"
   - `description`: "Listen Live from Internet"
   - `url`: "https://radio.unitedislamicsociety.org/"
   - `icon`: "globe"
   - `featured`: false
   - `enabled`: true
2. Edit `index.html` and insert a new social `<a>` between X and Viber with:
   - `href`: "https://radio.unitedislamicsociety.org/"
   - `aria-label`: "Radio"
   - inline SVG using the existing `globe` icon markup
3. Verify local `index.html` still loads and the new card/social link appear in the correct order
