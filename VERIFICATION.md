# Verification

Checked **21 October 2026**, with **Chromium 153** via Playwright. The profile has not been published to GitHub during this task; these are local SVG-document and GitHub-style image-embedding checks.

| Check | Result |
| --- | --- |
| All five SVGs at 0, 2, 5, 9 and 13 seconds | Rendered and visually inspected at exact SVG/CSS timeline positions |
| Image embedding | All five also rendered as `<img>` resources and inspected through the requested sampling window |
| Animation removed | SMIL nodes removed; all CSS animations disabled; readable base layouts remain |
| Reduced motion | All five rendered with `prefers-reduced-motion: reduce`; zero running CSS animations and no visible animated SMIL groups |
| Portrait identity and alpha | Embedded PNG bytes match supplied originals by SHA-256; original RGBA alpha retained |
| Typography | Font outlines keep visible typography consistent in SVG-document and image modes; base64 WOFF2 display and mono fonts included in every SVG |
| Clipping and spacing | No horizontal text overflow; orbit badges remain spaced apart; entrances reveal within intended clip regions |
| Mobile | 375 px image and preview widths checked; no horizontal overflow. SVGs scale as images; descriptive README alt text preserves the essential content |
| External asset requests | **Zero** HTTP(S) requests during standalone SVG and image-mode rendering, including the offline preview |
| SVG structure | Valid XML; unique, namespaced IDs; no JavaScript, `foreignObject`, external styles, external font/image references or externally requested assets |
| Animation conventions | SMIL begins at `0s`; delayed foil sweep uses keyTimes; CSS entrances use fill-mode `both`; base attributes remain readable |
| Hero | Discrete character-width typing, rising clipped name reveal, four roles in a 16-second cycle |
| About | Three interest slides, four seconds each, with segment progress bars; reduced motion lists all interests |
| Stack | Correctly labelled brand paths and chips; three tilted elliptical tracks, spaced badges and animated orbit tracers |
| ID | Drop and damped settling sequence, then continuous ±1.7° swing; metal clasp, decorative barcode, subtle light sweep |
| Connect | Exact pointing PNG; genuine platform marks; visible arrows; real external links below the SVG in README |
| README | Exactly five relative SVG paths ending `?v=1`, projects table, supplied clickable social links, no contribution-city section |

## Link checks

- GitHub profile, GUIDAR repository and weather-station repository: HTTP 200; repository data also verified with the GitHub plugin.
- YouTube, Topmate and `https://signodes.netlify.app`: HTTP 200.
- LinkedIn returned HTTP 999; Medium returned HTTP 403 to automated access. Their exact supplied URLs were retained. These responses do not establish whether a logged-in visitor can access the profiles, so their destination content was not independently validated.
- Bail Reckoner and AI Vision Reader are intentionally unlinked at the user's choice.

## Evidence and implementation decisions

The separate verification archive contains renders, contact sheets, byte hashes and browser/link results. Direct SVG snapshots use deterministic timeline positions. Image-mode samples use real elapsed time to confirm actual embedded-image animation; capture overhead means those sample filenames are approximate elapsed timestamps.

The first visual pass exposed moving-label collisions and browser font substitution in image mode. The final stack uses spaced, correctly labelled badges on each ellipse with travelling tracers. Visible typography is outlined from the licensed source fonts. Every SVG still embeds both WOFF2 fonts, and source licences are included.

Only dated GitHub repository metadata appears on the dashboard. The undated 17+ hackathon wins and 5000+ reach are omitted. Project descriptions and event-year claims are supplied by the user; they are not presented as externally audited dashboard metrics. No employment, contact details, project URLs or unknown counts were inferred.

Browser and GitHub rendering policies can change. The included static layouts remain useful without animation, and SVG anchors are deliberately not used for navigation.
