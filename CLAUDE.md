# CLAUDE.md

This file provides guidance to Claude Code when working with code in this repository.

## Project

**Firemni Diagnostika Landing Page** — marketing landing page for AB ANTE operational and economic diagnostics consulting product.

**Language:** Czech (cestina) for content, English for code.

## Stack

Static HTML/CSS/JS — no framework, no build step. Deployed on Vercel via GitHub auto-deploy.

## Design System

Identical to `krizova-diagnostika.vercel.app` (AB ANTE corporate brand).

- **Fonts:** Source Serif 4 (headings, weight 400), DM Sans (body text)
- **Colors:** Navy `#1A2E4A` (hero, CTA section), Copper `#D4722A` (accent, buttons), Cream `#FAFAF8` (background), Sand `#F4F2EE` (alt sections), White (nav, footer)
- **Nav & Footer:** White background with full-color logo (42px height), navy/muted text
- **Typography:** Fluid via `clamp()` — H1 scales 36–72px, H2 scales 28–42px
- **Container:** 1400px max-width (1600px for nav)
- **Pattern:** Trust & Authority — clean, minimal, professional B2B
- **Responsive:** 3 breakpoints (desktop, tablet 960px, mobile 640px)
- **CTA buttons:** Always white text (`#fff`) on copper background. Use `.nav-links a.nav-cta` (not just `.nav-cta`) to override `.nav-links a` specificity. This is a recurring bug — `.nav-links a` sets `color:var(--muted)` which overrides `.nav-cta` if specificity is not high enough.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Production landing page |
| `ab-ante-logo.png` | AB ANTE logo |

## Deploy

```bash
git push  # auto-deploys to Vercel
```

URL: `firemni-diagnostika.vercel.app`

## Content — Provozni a ekonomicka diagnostika firmy

Source document: `AB_ANTE_firemni diagnostika_260324_v2.docx`

### NAV

| Polozka | Anchor |
|---------|--------|
| Proc diagnostika | #problem |
| Co analyzujeme | #moduly |
| Jak to probiha | #jak-to-funguje |
| Vystupy | #vystupy |
| **Domluvit konzultaci** (CTA button) | #kontakt |

### HERO

- **Eyebrow:** Firemni diagnostika · AB ANTE
- **H1:** Ekonomika firmy neroste? *Ukazeme vam proc — a co s tim.*
- **Subheadline:** Nezavisla provozni a ekonomicka diagnostika pro majitele malych a strednich firem. Pojmenujeme priciny, zmapujeme rizika a navrhneme konkretni opatreni.
- **CTA:** Domluvit konzultaci → / Jak diagnostika probiha
- **Stats (4 boxy):** NDA (duvěrnost od prvniho kontaktu) | Data + expert (AI analyza, lidska interpretace) | Nezavisly pohled (diagnostika zvenčí, bez vazeb) | Bez sablon (kazda firma individualne)

### SEKCE: PROBLEM (id="problem")

- **H2:** Tusite to, ale nevidite priciny
- **3 karty:**
  1. Klesajici marze, rostouci naklady — a neni jasne proc
  2. Rozhodovani bez podkladu — chybi systematicky prehled
  3. Cas bezi — cim dele cekate, tim mene prostoru neco zmenit

### SEKCE: MODULY (id="moduly")

- **H2:** Pet modulu od provoznich dat po konkretni kroky
- **5 karet (A–E):**
  A. Provozni a ekonomicka analyza (jadro) — nakladove polozky, mzdovy fond, smlouvy, provozni zavislosti
  B. Obchodni diagnostika — sortiment, cilova skupina, trzni pozice, sezonnost, marze, konkurence
  C. Cash flow a zavazkova mapa — penezni toky, splatnosti, prioritizace veritelu
  D. Pravni a danova rizika — exekucni, danova a smluvni rizika, odpovednost jednatele
  E. Scenare a doporuceni — varianty postupu s konkretnimi kroky, predpoklady a cisly

### SEKCE: JAK TO PROBIHA (id="jak-to-funguje")

- **H2:** Od prvniho kontaktu k rozhodnuti
- **4 kroky** (kondenzovano ze 6 fazi):
  1. Briefing — uvodni schuzka, rozsah, NDA, seznam podkladu
  2. Sber dat a analyza — klient preda podklady, paralelne zajistime verejne zdroje, krizova kontrola
  3. Expertni review — senior konzultant overi zavery, formuluje scenare
  4. Spolecna schuzka — prezentace zaveru, diskuse variant, dohoda na dalsich krocich

### SEKCE: VYSTUPY (id="vystupy")

- **H2:** Rozhodovaci podklad, ne akademicka studie
- **4 karty (2x2):**
  1. Report — provozni a ekonomicka analyza, pojmenovane priciny, konkretni cisla
  2. Risk registr — pravni, danova a provozni rizika (kriticka / vyznamna / drobna)
  3. Scenare s konkretnimi kroky — kratkodobe, strednedobe, dlouhodobe
  4. Spolecna schuzka — zavery probereme osobne, dohodneme dalsi postup

### SEKCE: CENA (kratka zminka v ramci CTA)

Cenu stanovujeme individualne podle realneho rozsahu sluzeb a potreb. Vzdy predem, pred zahajenim prace.

### SEKCE: CTA / KONTAKT (id="kontakt")

- **H2:** Domluvit konzultaci
- **CTA:** mailto:info@ab-ante.cz

## Contact

**AB ANTE s.r.o.** · Perucka 61/13, 120 00 Praha 2 · [ab-ante.cz](https://ab-ante.cz)

- Vaclav Jankovsky · vaclav@ab-ante.cz · +420 775 262 645
- Jiri Zemlicka · jirka@ab-ante.cz · +420 602 162 043
