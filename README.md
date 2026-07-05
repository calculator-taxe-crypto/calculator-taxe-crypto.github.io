# Calculator Taxe Crypto România (2026)

Mini aplicație web **mobile-first**, fără dependențe de build, care te ajută să estimezi cât impozit și CASS ai de plătit la ANAF pentru câștigurile din criptomonede — și cât ar trebui să pui deoparte lunar ca să nu te prindă nepregătit la Declarația Unică.

🔗 **Live**: [calculator-taxe-crypto.github.io](https://calculator-taxe-crypto.github.io/)

## Ce face

- **Două moduri de calcul**, printr-un toggle:
  - **Anual** — introduci câștigul estimat pe tot anul fiscal; aplicația calculează impozitul + CASS-ul total și suma lunară de economisit (împărțită la 12).
  - **Lunar** — introduci doar câștigul din luna curentă; aplicația proiectează anul (× 12) pentru a estima pragurile, apoi îți arată cât să pui deoparte din luna asta **și** cât poți cheltui liniștit din rest.
- Calculează **impozitul pe venit (16%)**, cu regula de scutire totală pentru câștiguri sub 600 lei/an.
- Calculează **CASS-ul pe trepte fixe** (6 / 12 / 24 salarii minime brute anuale), cumulând câștigul din crypto cu alte venituri din "alte surse" (chirii, dobânzi, dividende) dacă le adaugi.
- **Salariul minim brut e editabil** — alegi una din valorile presetate pentru 2026 sau introduci manual orice altă valoare.
- Totul se recalculează live, fără reload.

## Reguli fiscale folosite (valabile la data scrierii, 2026)

| Regulă | Valoare |
|---|---|
| Impozit pe câștig din criptomonede | 16% din 1 ianuarie 2026 (10% pentru câștigurile realizate în 2025) |
| Scutire totală | sub 600 lei/an, cu condiția ca fiecare tranzacție să fie sub 200 lei — peste prag se impozitează *toată* suma, nu doar diferența |
| CASS | 10%, pe trepte fixe (nu proporțional): sub 6 salarii minime anuale → 0 lei · 6–11,99 → CASS la nivelul a 6 salarii minime · 12–23,99 → la 12 · peste 24 → la 24 |
| Bază CASS | crypto + alte venituri din "alte surse" (chirii, dobânzi, dividende, investiții), cumulate |
| Salariu minim brut 2026 | 4.050 lei (ianuarie–iunie) · 4.325 lei (din iulie) |
| Termen Declarație Unică | 25 mai, anul următor celui în care ai realizat câștigul |

Temei legal: art. 116 din Codul fiscal (Legea 227/2015), modificat prin Legea 239/2025.

> ⚠️ **Legislația se poate schimba**, iar unele zone rămân neclare — de exemplu, ce valoare a salariului minim se folosește exact pentru pragul anual de CASS, dat fiind că salariul minim crește la jumătatea anului 2026. Instrumentul e orientativ, nu consultanță fiscală. Verifică sumele finale cu ANAF sau cu un contabil înainte de a declara.

## Structură

```
.
├── index.html   # aplicația (HTML + CSS + JS, un singur fișier)
└── README.md
```

> Fișierul se numește `index.html` (nu `calculator-taxe-crypto.html`) pentru că acest repo e o pagină GitHub de tip *user page* (`calculator-taxe-crypto.github.io`) — GitHub Pages caută automat `index.html` la rădăcină ca să-l servească direct la domeniul principal.

## Rulare locală

Nu are dependențe — deschizi fișierul direct în browser.

```bash
git clone https://github.com/calculator-taxe-crypto/calculator-taxe-crypto.github.io.git
cd calculator-taxe-crypto.github.io
open index.html   # sau dublu-click pe fișier
```

## Publicare cu GitHub Pages

Acest repo e deja configurat corect ca pagină de tip *user page*:

- **Repo**: [github.com/calculator-taxe-crypto/calculator-taxe-crypto.github.io](https://github.com/calculator-taxe-crypto/calculator-taxe-crypto.github.io)
- **Live**: [calculator-taxe-crypto.github.io](https://calculator-taxe-crypto.github.io/)

Ca să rămână public, verifică doar **Settings → Pages → Source**: branch `main`, folder `/ (root)`.

## Tehnologii

HTML + CSS + JavaScript vanilla, fără framework-uri sau pași de build. Fonturi: Fraunces, IBM Plex Sans, IBM Plex Mono (Google Fonts, încărcate prin CDN).

## Licență

Nespecificată momentan — adaugă un fișier `LICENSE` (de ex. MIT) dacă vrei să clarifici termenii de utilizare/reutilizare a codului.

## Disclaimer

Acest instrument are scop informativ și educațional, nu constituie consultanță fiscală sau juridică. Sumele afișate sunt estimări bazate pe legislația în vigoare la momentul realizării aplicației — verifică întotdeauna cu sursele oficiale ANAF sau cu un contabil autorizat înainte de a-ți declara veniturile.
