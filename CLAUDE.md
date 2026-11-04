# Betuwse Bron: website

Verhuurwebsite voor chalet 56 op Resort Rivierendal in Ochten (Betuwe): een vrijstaand vakantiechalet voor 4 personen met 2 slaapkamers, een eigen hottub en ligging aan een bomenlaan. Het merk is bedoeld voor gasten. Investeerders moeten het via de professionele uitstraling oppikken, niet via rendementsclaims op deze site. Later komen er meer chalets op hetzelfde park bij.

## Wat er staat

- `index.html`: de volledige pagina als één statisch bestand, met inline stijlen. Er is geen bouwstap nodig: open hem in de browser.
- `assets/img/`: hero (`chalet-droom.jpg`), hottub-uitsnede, drie interieurfoto's en de plattegrond (`plattegrond-rivierendal-56.svg`).
- `assets/logo/`: het horizontale logo in kleur (voor op creme) en in creme (voor op donker).
- Het volledige brandbook (merkverhaal, beeldtaal, tokens en alle logovarianten) staat buiten de repository in de map `../brandbook/`. Het hoort niet in de webmap, want alles in de hoofdmap is publiek.

## Huisstijl (zie `../brandbook/tokens.json`)

- Kleuren: creme `#faf5ec` (achtergrond), boomgaard `#2f4a36` (merkkleur, koppen, knoppen), boomgaard-diep `#1f3325`, linnen `#f1e8da`, blad `#dce5d5`, bloesem `#f2d4d0`, appel `#b4412f` (alleen kleine accenten), honing `#c8902e` (alleen iconen), inkt `#2a2420`, inkt-gedempt `#6b5f55`.
- Lettertypen: Fraunces (koppen, gewicht 480 tot 500) en Figtree (tekst), beide via Google Fonts.
- Knoppen zijn pillen (radius 999px), foto's krijgen radius 28px en kaarten 14px.
- Labels en bovenregels in hoofdletters met letterafstand 0.14em.

## Schrijfregels

- Alles in het Nederlands, ook geen Engelse vaktermen.
- Spreek de lezer aan met u, in een iets formele en rustige toon. Gebruik korte zinnen.
- Geen gedachtestreepjes (em-dashes): gebruik komma's, punten of dubbele punten.
- Geen uitroeptekens, geen schaarste-druk, geen superlatieven.
- Verzin geen feiten. Ontbrekende gegevens blijven als [PLACEHOLDER] staan.

## Eerlijkheid over beeld

- `chalet-droom.jpg` en `chalet-hottub.jpg` zijn AI-bewerkingen van de echte woning. De hottub, de lichtslingers en de beplanting bestaan (nog) niet. Ze dragen daarom het label "Sfeerimpressie" en dat label blijft staan.
- Vervang ze door echte foto's zodra de hottub geplaatst is.
- De plattegrond is schematisch en overgetrokken van Google Maps. Chalet 56 is gemarkeerd. Nieuwe aankopen krijgen dezelfde donkergroene markering.

## Nog open

- Placeholders in `index.html`: prijs per nacht, telefoon en hoe de sleutel wordt overgedragen.
- Placeholders op de subpagina's: temperatuur en huisregels van de hottub (`wellness/`), afstanden en drie tips (`omgeving/`), bedden, sleutel, roken, geluid, annulering en betaling (`praktisch/`). Zoek op `[` om ze te vinden.
- Te controleren teksten in het blok Ligging: "geen doorgaand verkeer" en "alles binnen loopafstand".
- De boekingsbalk doet nog niets. Koppel hem aan een boekingssysteem of laat hem doorlinken naar Airbnb of Booking.
- Zodra de prijs bekend is: ook toevoegen aan de gestructureerde gegevens (JSON-LD) en `llms.txt`.

## Vindbaarheid (SEO en AI-zoekers)

- Pagina's: `index.html`, `wellness/`, `omgeving/` en `praktisch/` (elk met een eigen `index.html`). Kop, voet en stijlblok staan in elke pagina apart: wijzig ze op alle pagina's tegelijk. Subpagina's verwijzen met `../` naar `assets/`.
- `robots.txt`, `sitemap.xml` en `llms.txt` staan in de hoofdmap. Werk `lastmod` in de sitemap bij en voeg nieuwe pagina's toe.
- In `index.html` staan gestructureerde gegevens (`VacationRental` en `FAQPage`). Houd die gelijk aan de zichtbare tekst: elke vraag in `FAQPage` staat ook op de pagina. Geen placeholders in de gestructureerde gegevens.
- Foto's op de pagina zijn WebP. De JPG-originelen blijven staan voor deelvoorbeelden (Open Graph).
- `.htaccess` stuurt www door naar betuwsebron.nl en blokkeert `CLAUDE.md` en `README.md` voor bezoekers.

## Werkafspraken en publicatie

- Dit is een statische site: HTML, CSS, afbeeldingen en eventueel JavaScript. Er is geen bouwstap en geen Node. PHP kan wel.
- Repository: `rubenkraan-droid/betuwse-bron`, tak `main`.
- De hoofdmap van de repository is de webmap. `index.html` staat in de hoofdmap. Alle links naar bestanden zijn relatief (`assets/...`).
- Plesk (Cloud86) publiceert automatisch: bij elke push naar `main` wordt de repository één op één gekopieerd naar de webmap van betuwsebron.nl. Een push is dus direct live.
- Zet nooit wachtwoorden, sleutels of `.env`-bestanden in de repository.
- Laat elke publicatie (push naar `main`) eerst bevestigen.
- Vraag het voordat bestaande bestanden in de repository worden verwijderd of overschreven.
