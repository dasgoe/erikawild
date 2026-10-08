# Erika Wild — website (erikawild.be)

Statische site, 3 pagina's, pure HTML/CSS. Geen JavaScript, geen cookies, geen externe lettertypes.

```
index.html / nl.html                       → one-pager FR / NL
bon-cadeau.html / cadeaubon.html           → cadeaubon FR / NL
conditions.html / voorwaarden.html         → wettelijke vermeldingen + verkoopsvoorwaarden FR / NL
confidentialite.html / privacy.html        → privacy & cookies FR / NL
404.html                                   → tweetalige foutpagina
_headers                                   → Netlify: beveiligingsheaders + caching
css/style.css, img/, site.webmanifest, robots.txt, sitemap.xml (hreflang voor alle 8 pagina's)
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
- Geen logo: "ERIKA WILD" in systeemletters, kapitalen, gespatieerd. Favicon: "WILD" in de lichte bandeau op zwart. `img/favicon.svg` + `favicon-32.png` (oudere browsers), `apple-touch-icon.png` (bladwijzer/beginscherm iPhone), `icon-192/512.png` + `site.webmanifest` (Android).

## Boeken en prijzen
- Alle boekknoppen en de link "Réserver / Boeken" (kop, voet, contact) wijzen naar Cal. Plaatshouder `https://cal.com/CAL_ID` vervangen door de echte link (zoek op `CAL_ID` in alle html-bestanden).
- Individuele sessie: € 75 (1 uur). Groepssessie: € 35 per persoon (2 uur). Eén Cal-pagina voor beide. Staat in de slot-sectie, de feitenzin en de JSON-LD (makesOffer) — bij een prijswijziging alle drie aanpassen, FR én NL.

## Twee talen
- Elke pagina bestaat in FR en NL: `index.html` ↔ `nl.html`, `contact.html` ↔ `contact-nl.html`. Elke pagina linkt naar haar tegenhanger (taalknop), met `hreflang` fr/nl/x-default in de head en in `sitemap.xml`.
- Google toont in de zoekresultaten de versie in de taal van de zoeker. Wie rechtstreeks naar erikawild.be surft, krijgt altijd FR (x-default). Geen automatische doorverwijzing op browsertaal: dat sluit mensen op in één taal en hindert Google.
- Wijziging in één taal = ook in de andere, plus meta description, og-tags en JSON-LD.

## Inhoud one-pager (volgorde = rode draad)
hero (vraag) → lint (gedicht) → kernzin + film → [licht] één experiment → Experiment 01 + 4 activiteiten + beelden + plaats → [licht] wat er wakker wordt → brede foto → Ik ben Erika → [licht] stemmen deelnemers (enkel voornamen) → hoe het gaat + formules + FAQ → [licht] prijzen + boeken.

## Contrast (WCAG 2.1)
| Combinatie | Contrast | Norm |
|---|---|---|
| #F2EFE9 op #120E0C (tekst, knoppen) | 16,73:1 | AAA |
| #A9A49B op #120E0C (secundaire tekst) | 7,74:1 | AAA |
| #120E0C op #F2EFE9 (lichte vakken, labels) | 16,73:1 | AAA |

## Vóór livegang
1. Cal-links invullen: zoek `CAL_ID` (afspraaktypes /individueel, /koppel, /groep, /intake).
2. WhatsApp-link invullen: zoek `WHATSAPP_ID`.
3. In conditions/voorwaarden en confidentialite/privacy: alle gemarkeerde [VELDEN] invullen (naam, adres, KBO, btw-statuut, e-mail, verzekeraar).
4. Voorwaarden ook in Cal tonen vóór betaling.
5. Toestemming voor foto's en citaten.
6. Aparte GitHub-repo + Netlify-site.

## WhatsApp
Het gsm-nummer staat niet in de HTML. Alle WhatsApp-links gaan naar /whatsapp, /whatsapp-groupe of /whatsapp-groep; `_redirects` (Netlify) stuurt door naar wa.me. Nummer wijzigen of later een gebruikersnaam-link: enkel `_redirects` aanpassen.
