# Colour and design research for the proposal dashboard

Short notes behind the Phase 2 dark "cinematic" theme. Each claim is tagged with how strong the evidence is.

## Colour psychology (what the research does and does not support)

| Claim | Evidence | Source |
|---|---|---|
| Blue reads as **competence**; red as **excitement**. Colour shifts brand-personality perception and purchase intent. | Peer-reviewed, 4 experiments | Labrecque & Milne (2012), *J. Academy of Marketing Science* 40(5) 711–727, https://link.springer.com/article/10.1007/s11747-010-0245-y |
| Colour carries meaning that affects affect, cognition and behaviour, but effects depend on **context**, and the authors warn the field is "nascent" (no strong one-size-fits-all rules). | Peer-reviewed review | Elliot & Maier (2014), *Annual Review of Psychology* 65, https://pubmed.ncbi.nlm.nih.gov/23808916/ |
| People judge products/people within ~90 seconds, and colour is a large part of that first judgement. | Peer-reviewed review (the often-quoted "62–90 %" figure is **not** in this paper; we do not use it) | Singh (2006), *Management Decision* 44(6), https://www.emerald.com/insight/content/doi/10.1108/00251740610673332 |
| Dark, low-saturation and achromatic palettes raise perceived **status / premium**. | Mixed: one multi-study luxury paper on low saturation plus a review; packaging work is small-sample | https://biopen.bi.no/bi-xmlui/handle/11250/3108537 · https://core.ac.uk/download/212811698.pdf |
| For a CTA, **contrast and isolation** (one colour used only for the action) matter more than the specific hue. | Practitioner consensus, not peer-reviewed; specific % lifts quoted online are unverified | https://conversionxl.com/which-color-converts-the-best/ |

## MENA / Egypt specifics

- **Gold** is read as royalty, prestige and celebration in the region. Source is trade press, so treat it as weak evidence: https://www.zawya.com/en/business/colour-codes-lpt90rzi
- **Blue** is the most-preferred colour among Arab respondents in that same report, and blue/green/white are broadly liked across cultures.
- **Green** is positive and sacred in Islamic culture, and it is the WhatsApp colour Egyptian owners already associate with "message me". Product colour is a primary driver of Saudi consumer response (n = 625): https://digitalcommons.aaru.edu.jo/aja/vol40/iss3/3
- **Black** carries some negative idiomatic senses in Arabic (e.g. "black economy"). We therefore use a deep **navy-black**, not pure black.
- We found **no Egypt-specific peer-reviewed colour-marketing study**, so these roles are informed choices, not proven effects.

## Dark vs light mode

- NN/g's review of the studies: light mode gives better reading performance, especially for small text, and dark mode is harder for small text at night. NN/g ran no study of its own: https://www.nngroup.com/articles/dark-mode/
- **Tension:** the brief asks for a cinematic dark UI. Our mitigations:
  - body text ≥ 16.5 px at weight 400+ (thin weights "glow" on dark)
  - off-white text (#e9eff8), never pure white
  - long text never in low-contrast grey (≥ 7:1 for body, ≥ 4.5:1 for secondary)
  - generous line height (Arabic 1.85)
  - the **PDF/print stays light**

## Colour roles used

| Role | Colour | Why |
|---|---|---|
| Canvas | navy-black `#070d1a` | premium/dark without the negative "black" connotation |
| Trust/competence, structure, icons, links | blue `#5b9bff` / navy | Labrecque & Milne: blue = competence; most-liked hue in Arab samples |
| Premium: Business package, bonuses only | gold `#e2b85c` | gold = prestige in the region; scarcity keeps it meaningful |
| Action + money: Book a call, WhatsApp, savings result | green `#3ddc84` | isolation effect: the only green on the page is "act" or "you gain"; WhatsApp association |
| Loss: struck agency price only | red `#f26d6d` | excitement/alarm used once, to mark what the owner avoids |
| Form error | red | functional state, not decoration |

## 2026 benchmark (pages actually rendered and inspected)

- **Linear** https://linear.app/ — near-black canvas, product UI as the hero visual, very large tight headline, logo strip under the hero, muted grey body.
- **Raycast** https://www.raycast.com/ — black canvas with a single glowing colour object behind a centred headline; one primary button; glass panels.
- **Vercel** https://vercel.com/ — restrained monochrome, big type, logo row, bento-style feature cards.
- **Netflix Egypt** https://www.netflix.com/eg-en/ — dimmed poster wall behind the hero, ranked horizontal "Trending" row with big numerals, dark cards with soft gradients, one red CTA, accordion FAQ.
- **A24 (Awwwards Site of the Day, 26 Oct 2026)** https://a24.raviklaassens.com/ — one cinematic object as the hero, huge whitespace, motion as the main act.
- Awwwards Sites of the Day list (Nov 2026): https://www.awwwards.com/websites/sites_of_the_day/ (mostly WebGL showpieces, which are not appropriate for a proposal).

Techniques chosen for an SME sales proposal (impressive without hurting speed, mobile or readability):

1. Dark canvas with a slow aurora glow behind the hero (transform-only animation).
2. Video as the star, in a glowing card with subtle cursor tilt.
3. Kinetic headline (word-by-word rise) and count-up KPIs.
4. Netflix-style horizontal content row for the work, with hover zoom and a logo marquee.
5. Spotlight cursor light and an animated gold border on the recommended package.
6. Scroll reveals (transform only, readable at rest), section underline sweep, sidebar scrollspy.
7. A sticky mobile top bar with the single green action.

Rejected: WebGL/3D (weight, mobile battery), heavy glassmorphism everywhere (cost and contrast), autoplay sound.
