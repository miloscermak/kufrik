# Sentin Kufřík — Příručka AI promptů pro manažery

## O projektu
Statická jednostránková webová příručka AI promptů pro manažery, vytvořená pro Sentin. Obsahuje praktické prompty, tipy a příběhy z praxe. Dostupná ve dvou jazycích — česky (hlavní) a anglicky.

## Technický stack
- Čisté HTML + CSS + vanilla JavaScript (vše inline v jednom souboru)
- Font: Inter (Google Fonts)
- Hosting: Netlify (statický deploy)
- GitHub repo: miloscermak/kufrik

## Struktura
- `index.html` — česká verze (hlavní)
- `en.html` — anglická verze
- Přepínač jazyka (CZ / EN) je vpravo nahoře, fixní, s blur efektem
- Oba soubory obsahují vše inline (CSS i JS)

## Deploy
- Netlify deploy z main větve
- Publish directory: `/` (root)
- Žádný build step — čistě statický web

## Údržba
- Při úpravách obsahu vždy synchronizovat obě jazykové verze
- Přepínač v obou souborech používá stejný CSS blok (`.lang-switch`) — pokud se upravuje styl, upravit na obou místech
