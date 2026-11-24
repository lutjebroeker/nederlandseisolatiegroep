# Nederlandse Isolatie Groep – website

Statische website van nederlandseisolatiegroep.nl. Geen build-stap, geen framework: losse HTML-bestanden met inline CSS en JavaScript.

## Live zetten
- Elke push naar `main` gaat automatisch live via Vercel (project van Jelle, `lutjebroekers-projects`).
- De repo is openbaar; daardoor worden pushes zonder goedkeuring gedeployed. Wordt de repo weer privé, dan moet Jelle elke deploy goedkeuren.
- `vercel.json`: `cleanUrls` staat aan (`/subsidie.html` is ook bereikbaar als `/subsidie`). Bestanden in `img/` en `video/` worden een jaar gecachet: vervang je een foto of video, geef hem dan een nieuwe bestandsnaam en pas de verwijzing aan.

## Structuur
- 17 pagina's in de hoofdmap: `index.html`, de isolatiepagina's (spouwmuur, vloer, bodem, dak, isolatieglas), `subsidie`, `werkwijze`, `over-ons`, `contact`, `kennisbank` + 3 artikelen (`kosten-spouwmuurisolatie`, `kruipruimte-isoleren`, `wat-levert-isolatie-op`), en de juridische pagina's `privacy`, `voorwaarden`, `cookies`.
- Header, footer en het script onderaan staan in elke pagina apart. Pas je iets aan in de header, footer of het script, doe dat dan in alle 17 bestanden.
- Navigatie: elk menu-item en elke knop gaat naar een eigen pagina. Alleen de uitklapkopjes bij "Direct naar" op de homepage klappen open. "Isolatie", "Services" en "Over ons" zijn uitklapmenu's.
- Subsidiecheck: `subsidiecheck/index.html`, bereikbaar op `/subsidiecheck`. Losse landingspagina zonder menu (voor advertenties). Knoppen ernaartoe: menu (naast Subsidie), homepage-hero, blok op de subsidiepagina en de 5 isolatiepagina's, en een vaste knop onderin op mobiel (alle pagina's). Advertentielinks: `/subsidiecheck?bron=facebook`, optioneel `&type=tussenwoning|hoekwoning|twee-onder-een-kap|vrijstaand|appartement` en `&utm_campaign=...`.
- ISDE-bedragen in de subsidiecheck staan in `RATES` (bron: RVO, isolatiemaatregelen woningeigenaren, uitvoering 2025 of later). Gemiddelde oppervlaktes per woningtype in `AREA`. Controleer de bedragen bij een wijziging van de ISDE.
- Media: `img/` (6 foto's) en `img/isolatie/` (WebP-fotorijen op de 5 isolatiepagina's, 960×720, lazy loading; Unsplash/Pexels-licentie; bodem gebruikt voorlopig de vloerfoto's), `video/nig-5-stappen.mp4` (uitlegvideo met voice-over) en `video/poster.jpg`, `logo.svg`, `logo-icoon.svg`.

## Vaste gegevens
- Telefoon: +31 6 85235975 (`tel:+31685235975`). Bellen elke dag 08:00–20:00, WhatsApp 24/7 via https://wa.me/31685235975.
- E-mail: info@nederlandseisolatiegroep.nl
- KvK: 42106969
- Facebook: https://www.facebook.com/profile.php?id=61596782371164
- Instagram: https://www.instagram.com/nederlandseisolatiegroep/
- Footer: "© 2026 Nederlandse Isolatie Groep". De naam van de B.V. staat bewust nergens op de site.
- Huisstijl: navy #0F2A47, blauw #1B75BB, lichtblauw #8EC8F2, achtergrond #EAF3FB.

## Formulieren
- Aanvraagformulier (homepage en contact) en nieuwsbrief versturen via Web3Forms naar info@nederlandseisolatiegroep.nl. Zie `W3F_KEY` in het script onderaan elke pagina.
- De subsidiecheck verstuurt ook via Web3Forms: `w3fKey` in `CONFIG` in `subsidiecheck/index.html`.
- De Web3Forms-sleutel staat ingevuld (aangevraagd met info@nederlandseisolatiegroep.nl). Lukt versturen niet, dan opent als terugval het mailprogramma van de bezoeker. Pas je de sleutel aan, doe dat dan in alle 17 pagina's én in de subsidiecheck.

## Afspraken
- Geen cookies, analytics, Meta Pixel of andere tracking toevoegen zonder overleg met Daan. Anders kloppen de cookie- en privacyverklaring niet meer.
- Voeg je een externe dienst toe (zoals een formulierdienst of lettertypen), werk dan ook `privacy.html` bij.
- Teksten: u-vorm, rustig en feitelijk. Geen besparingsbedragen of subsidiepercentages zonder bron.
- Geen placeholders zoals [TELEFOONNUMMER] of [TIJD] live zetten.
- Controleer na een wijziging dat alle interne links en afbeeldingen nog naar bestaande bestanden wijzen.

## Nog open
- Echte reviews toevoegen zodra die er zijn (de reviewblokken zijn verwijderd).
