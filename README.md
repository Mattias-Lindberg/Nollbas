# Nollbas – Solna

> Solnas kommunala ekonomi granskat från grunden. Öppen data, öppen debatt.

Livedata från [Kolada / SKR](https://www.kolada.se) — ingen backend, ingen databas, ingen kostnad.

---

## Teknik

- Ren HTML / CSS / JS — inget ramverk
- [Chart.js](https://www.chartjs.org) för visualiseringar
- [Kolada API](https://api.kolada.se) — gratis, ingen nyckel krävs
- [Giscus](https://giscus.app) för kommentarer via GitHub Discussions
- PWA — installerbar på mobil och dator

---

## Publicera på GitHub Pages (30 minuter)

### 1. Skapa repot

1. Gå till [github.com](https://github.com) → New repository
2. Namnge det `nollbas`
3. Sätt till **Public**
4. Klicka **Create repository**

### 2. Ladda upp filerna

```bash
git init
git add .
git commit -m "lansering: nollbas"
git branch -M main
git remote add origin https://github.com/mattiaslindberg/nollbas.git
git push -u origin main
```

### 3. Aktivera GitHub Pages

1. Repot → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / `/ (root)`
4. Klicka **Save**

Din sida blir live på:
`https://mattiaslindberg.github.io/nollbas`

---

## Aktivera Giscus-kommentarer

1. Aktivera **Discussions** på repot (Settings → Features → Discussions ✓)
2. Gå till [giscus.app](https://giscus.app)
3. Ange ditt repo: `mattiaslindberg/nollbas`
4. Välj **Pathname** som mappning
5. Välj temat **dark**
6. Kopiera `<script>`-taggen
7. Ersätt `<div class="giscus-placeholder">` i `index.html` med script-taggen

---

## Egen domän (valfritt)

1. Köp `nollbas.se` — troligen ledig
2. Repot → Settings → Pages → Custom domain
3. Lägg till en `CNAME`-fil i repots rot med domännamnet

---

## Kolada-nyckeltal som används

| Diagram | KPI | Beskrivning |
|---------|-----|-------------|
| Nettokostnad jämförelse | N07403 | Nettokostnad totalt, kr/inv |
| Skola trend | N15033 | Nettokostnad grundskola, kr/elev |
| Politisk organisation | N03007 | Kostnad politisk organisation, kr/inv |
| Äldreomsorg | N17006 | Nettokostnad äldreomsorg, kr/inv 65+ |
| Befolkning | N01951 | Folkmängd totalt |

Hitta fler nyckeltal på [kolada.se](https://www.kolada.se/verktyg/kolada)

---

## Lägg till innehåll

Redigera `index.html` direkt. Varje analysartikel är ett `.post-card`-block.
För tvåspråkigt innehåll, använd `data-lang="sv"` och `data-lang="en"` på parallella element.

---

*All data är offentlig. All kod är öppen.*
