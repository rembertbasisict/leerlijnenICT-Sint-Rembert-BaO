# Leerlijnen ICT – Op.stap

Doorlopende leerlijnen ICT van de 2de kleuter tot het 6de leerjaar voor de scholen van Scholengroep Sint-Rembert.

- **Live:** https://rembertbasisict.github.io/leerlijnenICT/
- **Bronnen:** de 86 leerplandoelen ICT van Op.stap (leerplanversie V1.3, 15/10/2026), de Leerlijn mediawijsheid van Mediawijs, de minimumdoelen ICT (Onderwijsdoelen – Lager onderwijs, versie 2.0) en de schooleigen AI-leerlijn van de scholengroep.
- **Contact:** basis.ict.pedagogisch@sint-rembert.be

De site is een naslagpagina. Ze bewaart geen gegevens, vraagt geen aanmelding en bevat geen persoonsgegevens.

---

## 1. De bestanden

| Bestand | Wat staat erin | Wie past het aan |
| --- | --- | --- |
| `index.html` | De volledige site: leerdoelen, leerlijnen, minimumdoelen, AI-leerlijn, dekkingscheck | Alleen bij een nieuwe versie van de site (vervangen door uploaden) |
| `suggesties.js` | De **aanvulling van onze scholen** bij elk leerdoel | ICT-coördinator, met het potloodje op GitHub |
| `sharepoint-links.js` | De links naar het **lesmateriaal in SharePoint** | ICT-coördinator, met het potloodje op GitHub |
| `README.md` | Deze handleiding | – |

De bestandsnamen moeten **exact** zo heten. Een bestand met `(1)` of `.html.html` in de naam wordt door de site niet gebruikt.

---

## 2. Hoe de site is opgebouwd

Het menu links opent telkens één pagina:

- **Inleiding:** "Zo gebruik je deze site" en, uitklapbaar, de achtergrond (bronnen, niveaus, codes).
- **Per leerjaar:** voor leerkrachten. Kies een leerjaar en je ziet de leerdoelen van de vier leerlijnen. De pagina stopt bij het laatste leerdoel van dat leerjaar.
- **1 · Computationeel denken**, **2 · Digitale informatieveiligheid**, **3 · Mediawijsheid:** de leerlijnen met overzichtsmatrix en groeipad per spoor.
- **4 · AI:** de schooleigen AI-leerlijn voor de 3e graad, met de leeftijdsgrens voor AI-chatbots.
- **Minimumdoelen:** de 25 minimumdoelen ICT en de leerplandoelen die ernaartoe werken.
- **Dekkingscheck:** controle dat alle 86 leerplandoelen aan bod komen, plus de versiecontrole.

Bij elk leerdoel (61 in totaal) staan:
- **Suggesties voor in de les** (uitklapbaar): eerst de voorbeelden **uit het leerplan**, daaronder de **aanvulling van onze scholen** uit `suggesties.js`;
- de knop **Lesmateriaal in SharePoint ↗**, als er in `sharepoint-links.js` een link is;
- de knop **✎ Idee doorgeven**: opent een e-mail aan basis.ict.pedagogisch@sint-rembert.be, met het leerdoel en de codes ingevuld.

**Weergave voor leerkrachten en voor de ICT-coördinator.** Standaard zijn leerplancodes en minimumdoelen verborgen. Met de schakelaar **Toon leerplancodes en minimumdoelen** (bij Per leerjaar) verschijnen ze, samen met de filter op minimumdoel en de aantallen. De browser onthoudt die keuze.

**Rechtstreeks linken** kan met een stukje achter het adres:
- `#yr-5de-leerjaar` (of `#yr-2de-kleuter`, `#yr-1ste-leerjaar` …) opent een leerjaar;
- `#ll1`, `#ll2`, `#ll3`, `#ll4` opent een leerlijn;
- `#md` opent de minimumdoelen.

---

## 3. Een aanvulling (lessuggestie) wijzigen of toevoegen

1. Open op GitHub `suggesties.js` en klik op het **potloodje**.
2. Zoek het leerdoel. De regels staan per leerjaar, met boven elke regel het spoor en de leerplancodes, bijvoorbeeld:
   ```
   // 2B · Informatiegeletterdheid · 8.2.GL5.6
   "5de-leerjaar_8-2-GL5-6": "Een website beoordelen met drie vragen: …",
   ```
3. Pas alleen de tekst **tussen de aanhalingstekens** aan.
4. Klik **Commit changes**. Na een minuut staat de aanvulling op de site.

**Regels**
- Geen rechte aanhalingstekens (`"`) in de tekst. Gebruik ‘ ’ of “ ”.
- Laat de komma op het einde van de regel staan.
- De sleutel links (bv. `"5de-leerjaar_8-2-GL5-6"`) niet veranderen.
- Een lege tekst (`""`) toont geen aanvulling. De voorbeelden uit het leerplan blijven staan.

**Een klikbare link toevoegen:** schrijf de naam met het adres tussen haakjes erachter. Op de site wordt de naam klikbaar.
```
Lesmateriaal van Mediawijs: Kritikat (https://www.mediawijs.be/nl/kritikat).
```
Het adres moet met `https://` beginnen.

---

## 4. Een SharePoint-link wijzigen of toevoegen

1. Kopieer in SharePoint de link van de map: **Delen > Link kopiëren**.
2. Open op GitHub `sharepoint-links.js` en klik op het **potloodje**.
3. Zoek het leerdoel. Achter elke regel staan de codes en de leerdoeltekst als commentaar.
4. Plak de link tussen de aanhalingstekens:
   ```
   "5de-leerjaar_8-2-GL5-6": "https://sintrembert.sharepoint.com/…",
   ```
5. Klik **Commit changes**.

- Per leerjaar is er ook een regel `"map:5de-leerjaar"` voor de map van het hele leerjaar. Die knop staat bovenaan het leerjaar bij Per leerjaar.
- Een lege regel (`""`) geeft geen knop.
- Collega's hebben in SharePoint zelf toegang tot de map nodig. De links zijn zichtbaar op de openbare site, maar de mappen openen alleen voor wie toegang heeft.

---

## 5. Een nieuwe versie van index.html uploaden

1. Controleer dat het bestand exact `index.html` heet. Zet in Verkenner de bestandsnaamextensies zichtbaar (**Weergeven > Weergeven > Bestandsnaamextensies**).
2. Kies op GitHub **Add file > Upload files**, sleep het bestand erin en klik **Commit changes**. Het oude bestand wordt vervangen.
3. Wacht op het groene vinkje bij **Actions**.
4. Open de site en herlaad met **Ctrl + F5** (Mac: Cmd + Shift + R), of zet `?v=` met een nieuw getal achter het adres.

`suggesties.js` en `sharepoint-links.js` upload je **niet** opnieuw, tenzij dat uitdrukkelijk gevraagd wordt, bijvoorbeeld wanneer leerdoelen opgesplitst of toegevoegd worden. Anders overschrijf je je eigen aanvullingen en links.

**Een vorige versie terugzetten:** open het bestand op GitHub, klik op **History**, kies de gewenste versie en kopieer of herstel die.

---

## 6. Insluiten in SharePoint

1. Een SharePoint-beheerder voegt `github.io` toe aan de toegelaten domeinen: **Site-instellingen > HTML-veldbeveiliging**. Anders blijft het venster leeg.
2. Bewerk een sitepagina, voeg het webonderdeel **Insluiten** toe en plak het adres van de site.
3. Plaats het webonderdeel in een sectie op volle breedte en maak het zo hoog mogelijk. Een knop of link die de site in een nieuw tabblad opent, werkt ook altijd.

---

## 7. Onderhoud

**Leerplan Op.stap**
- Kijk regelmatig het [wijzigingsoverzicht op PRO.](https://pro.katholiekonderwijs.vlaanderen/aanpassingen-aan-leerplan-sinds-1-september-2026-1) en de pagina [Leerplan ICT](https://pro.katholiekonderwijs.vlaanderen/leerplan-ict) na.
- Bij een nieuwe versie moeten in `index.html` mee aangepast worden: de leerdoelen, de officiële teksten in de tooltips, de voorbeelden uit het leerplan, de dekkingscheck en het versienummer (bovenaan, bij Versiecontrole en in de voettekst).

**Minimumdoelen**
- Bron: [Onderwijsdoelen – Lager onderwijs, versie 2.0](https://onderwijsdoelen.be/doelen/LO_V2_0).
- Verandert het versienummer in dat adres, dan moeten de minimumdoelen op de site mee aangepast worden.
- De koppeling tussen leerplandoelen en minimumdoelen is een eigen, voorlopige koppeling van de scholengroep.

**AI-leerlijn**
- Bron: AI-leerlijn leerlingen en leerkrachten, Scholengroep Sint-Rembert.
- Leerlingen van de lagere school gebruiken zelf geen AI-chatbot (leeftijdsgrens 13 jaar, zie [Kenniscentrum Digisprong](https://www.vlaanderen.be/kenniscentrum-digisprong/themas/innovatie/artificiele-intelligentie/vanaf-welke-leeftijd-kunnen-of-mogen-je-leerlingen-generatieve-ai-gebruiken)). Houd site en document op dit punt gelijk.

---

## 8. Problemen oplossen

| Wat zie je | Oorzaak | Oplossing |
| --- | --- | --- |
| De site toont nog de oude versie | Opgeslagen kopie in de browser, of publicatie nog bezig | Wacht op het groene vinkje bij **Actions**, herlaad met **Ctrl + F5** |
| Een wijziging verschijnt niet | Bestand heet `index (3).html`, `index.html.html` … | Bestand hernoemen naar exact `index.html` en dubbele bestanden verwijderen |
| Donkerblauwe melding onderaan: "suggesties.js bevat een fout" | Rechte aanhalingsteken in een tekst, of een ontbrekende komma of `};` | Regel nakijken in `suggesties.js` |
| Melding: "deze sleutels bestaan niet op de pagina" | Een sleutel is veranderd of hoort bij een oude versie | Sleutel herstellen zoals in de lijst |
| Een link in een aanvulling is niet klikbaar | Oude `index.html` op GitHub, of het adres begint niet met `https://` | Nieuwste `index.html` uploaden, adres controleren |
| Menu reageert niet in SharePoint | Oude `index.html` | Nieuwste `index.html` uploaden |
