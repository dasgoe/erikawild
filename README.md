# Erika Wild — website (erikawild.be)

Statische site, 3 pagina's, pure HTML/CSS. Geen JavaScript, geen cookies, geen externe lettertypes.

```
index.html     → one-pager FR (Expérience 01 · sans la vue)
nl.html        → one-pager NL (Experiment 01 · zonder zicht)
contact.html   → tweetalig contactformulier (Formspree)
css/style.css  → design tokens + componenten
img/           → favicon (svg), portret (webp 480/720/1080), og-afbeelding
robots.txt / sitemap.xml (met hreflang FR/NL)
```

## Stijl (v3 — zwart-wit, maar warm)
- Zwart-wit: warm zwart toneel #120E0C, gebroken wit #F2EFE9. Geen andere kleur.
- Warmte zonder kleur: warm zwart, warm getoonde zwart-witfoto (barietafdruk), zacht toneellicht achter de titel, zachtere filmkorrel.
- Signatuur "le bandeau" (de blinddoek): lichte band als schuin label (cursieve serif), als bedekt woord in de titel ("la vue" / "het zicht"), en als schuin lopend lint.
- Koppen en bandeau-teksten: grote cursieve Didot/Bodoni (Mac) of Georgia (Windows). Lopende tekst: systeemletters.
- Lichte vakken (#F2EFE9) enkel om iets te laten poppen, compact, nooit 2 na elkaar.
- Het lint beweegt traag; staat bij bezoekers met "minder beweging" stil.
- Experimenten: een nieuw experiment = label, lint, titel en lijst in sectie `#experience` (FR) / `#experiment` (NL) vervangen.

## Merknaam
- Geen logo: "ERIKA WILD" in systeemletters, kapitalen, gespatieerd. Favicon `img/favicon.svg` = EW in kapitalen.

## Boeken en prijzen
- Alle boekknoppen en de link "Réserver / Boeken" (kop, voet, contact) wijzen naar Cal. Plaatshouder `https://cal.com/CAL_ID` vervangen door de echte link (zoek op `CAL_ID`, 16 plekken in 3 bestanden).
- Individuele sessie: € 75 (1 uur). Groepssessie: € 35 (2 uur). Staat in de slot-sectie, de feitenzin en de JSON-LD (makesOffer) — bij een prijswijziging alle drie aanpassen, FR én NL.

## Contrast (WCAG 2.1)
| Combinatie | Contrast | Norm |
|---|---|---|
| #F2EFE9 op #120E0C (tekst, knoppen) | 16,73:1 | AAA |
| #A9A49B op #120E0C (secundaire tekst) | 7,74:1 | AAA |
| #120E0C op #F2EFE9 (lichte vakken, labels) | 16,73:1 | AAA |

## Vóór livegang
1. `CAL_ID` vervangen door de echte Cal-link (16 plekken in 3 bestanden) en 1x testboeken.
2. `FORMSPREE_ID` in `contact.html` vervangen door de ID van een apart erikawild.be-formulier, en 1x testen.
3. Mentions légales: naam, adres en KBO-nummer van de aanbieder (vzw of eenmanszaak?).
4. Nakijken of deze beloftes kloppen: "aucune expérience en danse ou en musique", "tu peux retirer le bandeau à tout moment", "tu choisis ton moment dans l'agenda en ligne".
5. Aparte GitHub-repo en Netlify-site voor erikawild.be.
