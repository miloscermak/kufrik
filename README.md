# Kufřík

**47 AI promptů od Senty a Miloše Čermákových.** Dva pohledy, jeden cíl: aby AI nebyla hračka ani strašák, ale nástroj, který šetří čas a rozšiřuje, co dokážete.

🌐 **Live:** [kufrik.inspiruj.se](https://kufrik.inspiruj.se)

---

## Co je uvnitř

| Kufřík | Doména | Promptů | Jazyk |
|--------|--------|---------|-------|
| **Sentin** | Byznys, leadership, strategie | 17 | CZ + EN |
| **Milošův** | Psaní, čtení, kreativita, život s AI | 30 | CZ |

Sourozenecké, ne konkurenční. Některé techniky se překrývají (OSINT, multiperspektiva) — a to je vlastnost, ne chyba. Stejná metoda funguje strategicky i kreativně.

## Soubory

```
kufrik/
├── index.html                ← rozcestník
├── sentin-kufrik.html        ← Sentin CZ
├── sentin-kufrik-en.html     ← Sentin EN
├── milosuv-kufrik.html       ← Milošův CZ
├── _redirects                ← Netlify: /en.html → /sentin-kufrik-en.html
├── netlify.toml              ← publish = "."
├── README.md
├── CLAUDE.md                 ← konvence projektu
└── .gitignore
```

Plochá struktura. Žádné podsložky, žádné dependencies, žádný build step.

## Technika

- **Single-file HTML** — každý kufřík je jeden soubor s vloženým CSS i JS
- **Vanilla** — žádný framework, žádný Tailwind
- **Inter font** z Google Fonts (jediná externí závislost)
- **Responsive** — flexbox + grid, mobile-first
- **Print-friendly** — všechny kufříky mají `@media print` styling
- **Kopírovací tlačítka** u každého promptu — kopírují čistý text bez HTML značek

## Deploy

- **Netlify** auto-deploy z `main` větve
- Publish directory: `/` (root, viz `netlify.toml`)
- Custom doména `kufrik.inspiruj.se` nastavená v Netlify

## Autoři

**Senta Čermáková** — ex-Deloitte, ex-korporát. Sedm a půl roku v Big4. Dnes lektorka AI Masterclass pro top management.

**Miloš Čermák** — novinář, autor, AI lektor. Píše pro [novinky.inspiruj.se](https://novinky.inspiruj.se). Stavbu aplikací bez programátora bere jako řemeslo, ne magii.

Společně: **[Inspiruj.se](https://inspiruj.se)** — rodinný vzdělávací startup, ~14 000 proškolených lidí.

## Licence

Obsah je dostupný k osobnímu i firemnímu používání. Pokud z něj děláte vlastní školení, uveďte zdroj. Pro komerční přeprodej kontaktujte autory.
