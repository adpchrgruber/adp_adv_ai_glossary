# A Working Grammar of Machine Intelligence

**76 terms, derived in seven layers** — an interactive glossary of AI for architecture, art, and design research.

Companion volume to [A Working Glossary of Making, from Analogue to Digital](https://adpchrgruber.github.io/adp_adv_26_glossary/), growing out of its §8 · Artificial Intelligence & Data.

**Live page:** https://adpchrgruber.github.io/adp_adv_ai_glossary/

---

## The idea

The first volume ordered the vocabulary of making by domain and by curated thread. This volume cannot be ordered that way, because its terms are not siblings — they are **derivations**. A diffusion model is unintelligible without the latent space it runs in; an agent is a language model with tools and goals; every critique term points back at a training decision made three layers down.

So the ordering principle here is **dependency**, written as a grammar. One master production rule opens the page:

```
⟨intelligence⟩ ::= ⟨data⟩ → ⟨model⟩ → ⟨learning⟩
                   → ( ⟨generation⟩ | ⟨capture⟩ | ⟨agency⟩ )
                   ⊣ ⟨critique⟩
```

Each non-terminal expands into one of seven layers, and each layer is only allowed to use what the layers beneath it have already defined:

| # | Layer | Gloss |
|---|-------|-------|
| 1 | `⟨data⟩` | the raw material |
| 2 | `⟨model⟩` | the machine that learns |
| 3 | `⟨learning⟩` | the education |
| 4 | `⟨generation⟩` | the making of image & form |
| 5 | `⟨capture⟩` | the scene, reconstructed |
| 6 | `⟨agency⟩` | the working partner |
| 7 | `⟨critique⟩` | the reckoning |

## Three views

- **Derivation** — the seven layers as a diagram. Click any term to trace its full ancestry to the ground (violet lines), with a panel showing what it *builds on* and what it *leads to*, both clickable.
- **Grammar** — each layer written as a BNF production rule; the whole field on one screen as text.
- **Index** — A–Z with live search, the familiar view from the first volume.

Every term carries a one-line, design-inflected definition and an **Example images ↗** link with a hand-tuned query — architectural where the term can show itself in buildings (GAN → generated facades, NeRF → building reconstructions), diagrammatic where it is a mechanism (transformer, RLHF, RAG).

Terms shown **dashed** already appear in the first volume's §8 and are included here as ground; **solid** terms are what this volume adds.

## One rule kept the list durable

*Name the concept, not the product.* No model names, no version numbers, no tools of the season. Every headword is a research concept with a citation trail — the layer beneath the churn. Terms were verified against the research literature, 2024–26.

## Editing

Everything lives in `index.html`. The corpus is a single JavaScript array near the top of the `<script>` block:

```js
{ id:"splat", t:"3D Gaussian splatting", l:4, p:["radiance"],
  d:"A radiance field made explicit — millions of soft, coloured blobs in space, rendered in real time." }
```

- `id` — short unique key
- `t` — the headword as displayed
- `l` — layer index, `0`–`6`
- `p` — parent ids (what the term builds on; drawn as derivation edges)
- `base: 1` — marks a term already defined in the Glossary of Making, §8
- image queries live in the `IMGQ` map, keyed by `id`

Add, reorder, or reparent terms there; the derivation, grammar, and index views rebuild themselves on load. No build step, no dependencies.

## Publishing

1. Create a repository named `adp_adv_ai_glossary`
2. Commit `index.html` and `README.md` to the `main` branch
3. Settings → Pages → Deploy from a branch → `main` / `(root)`
4. The page appears at `https://<username>.github.io/adp_adv_ai_glossary/`

## Colophon

Digital vocabulary after the *Atlas of Digital Architecture* (Hovestadt, Hirschberg & Fritz, eds.; Birkhäuser, 2020).
Type: Helvetica Neue for reading text, IBM Plex Mono for terms and rules.
Flush left, ragged right · One typeface · One violet.
