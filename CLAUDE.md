# Kufřík — Sentin + Milošův

## O projektu
Statický miniweb na `kufrik.inspiruj.se` (deploy z Netlify). Dva sourozenecké kufříky AI promptů:

- **Sentin kufřík** — byznys, leadership, strategie (17 promptů, CZ + EN)
- **Milošův kufřík** — psaní, čtení, research, kreativita, život s AI, tvorba (30 promptů v 7 blocích, zatím jen CZ)

Plus **rozcestník** na kořeni domény.

## Technický stack
- Čisté HTML + CSS + vanilla JavaScript (vše inline v každém souboru)
- Font: Inter (Google Fonts)
- Hosting: Netlify
- GitHub repo: `miloscermak/kufrik`
- Doména: `kufrik.inspiruj.se` (custom domain) + `kufrik.netlify.app`

## Struktura

```
kufrik/
├── index.html                ← rozcestník (purple→teal gradient)
├── sentin-kufrik.html        ← Sentin CZ
├── sentin-kufrik-en.html     ← Sentin EN
├── milosuv-kufrik.html       ← Milošův CZ (EN zatím není)
├── _redirects                ← Netlify redirect (legacy /en.html → /sentin-kufrik-en.html)
├── netlify.toml              ← publish = "."
├── README.md                 ← GitHub front page
├── CLAUDE.md                 ← tento soubor
└── .gitignore
```

## Vizuální styl

CSS custom properties v `:root` každého HTML:

| | Hex | Použití |
|---|---|---|
| Sentin accent | `#6B4C9A` (deep `#4A3470`) | Sentin CZ + EN |
| Milošův accent | `#2C6E7F` (deep `#1B4A57`) | Milošův CZ |
| Rozcestník | gradient `#6B4C9A` → `#2C6E7F` | index.html hero |
| Tip box | `#FFF8E7` / `#F0D060` | žlutý, oba kufříky |

Při ručních úpravách barev **měň proměnnou v `:root`**, ne jednotlivé hex hodnoty.

## Přepínač jazyka

Pouze v Sentinu (CZ ↔ EN). HTML element `.lang-switch` vpravo nahoře, fixní, blur. Pokud upravuješ styl, **synchronizuj obě jazykové verze**.

Linky:
- `sentin-kufrik.html`: CZ aktivní, EN → `/sentin-kufrik-en.html`
- `sentin-kufrik-en.html`: EN aktivní, CZ → `/sentin-kufrik.html`
- `milosuv-kufrik.html`: bez přepínače (EN neexistuje)
- `index.html` (rozcestník): bez přepínače (zatím není EN rozcestník)

## Deploy

- Netlify auto-deploy z `main` větve
- Publish directory: `/` (root, viz `netlify.toml`)
- Žádný build step — čistě statický web
- Custom doména `kufrik.inspiruj.se` v Netlify nastavená přes CNAME

## Pracovní prostor

**Toto repo je publikační artefakt.** Velké změny (nové prompty, nový kufřík, nová jazyková verze) dělej v pracovní složce `~/cowork/eon-prirucky/`. Až je obsah hotový a schválený, **zkopíruj sem** finální HTML a commit.

Drobné opravy (překlep, link, CSS tweak) můžeš dělat přímo tady.

## Formát promptů (kanonický)

Každý prompt má v HTML přesně tuto strukturu:

```html
<div class="prompt-card" id="pN">
  <div class="prompt-card-header">
    <h3><span class="prompt-number">N</span> Název <span class="tag tag-*">domena</span></h3>
    <p class="prompt-situation">1–2 věty kurzívou, kdy se to hodí.</p>
  </div>
  <div class="prompt-box">
    <button class="copy-btn" onclick="copyPrompt(this)">Kopírovat</button>
    <pre>... prompt s <span class="placeholder">[PLACEHOLDERY]</span> ...</pre>
  </div>
  <div class="story-box">
    <strong>Ze Sentiných zkušeností / Z Milošovy praxe:</strong> ...
  </div>
  <div class="tip-box">
    <strong>Tip:</strong> ...
  </div>
</div>
```

**Nevymýšlej nové sekce.** Když přidáš nový prompt, drž tuto strukturu.

## Údržba

- Při úpravě obsahu Sentina vždy synchronizuj CZ + EN verzi
- Při změně CSS přepínače jazyků (.lang-switch) sahám do obou Sentinů
- README.md aktualizuj, když se mění hlavní fakta (počet promptů, struktura)
- Tento CLAUDE.md aktualizuj, když se mění workflow nebo struktura

## Související

- Pracovní složka (návrhy, markdown verze, podklady, E.ON workshopy): `~/cowork/eon-prirucky/`
- Globální Milošovy preference: `~/.claude/CLAUDE.md`
- Sentin staré artefakty (PPTX, PDF): `~/cowork/senta-kufrik-*`
