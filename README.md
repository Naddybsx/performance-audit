# Performance audit – Byenti.com

## Wat is een Performance Audit?

Een performance audit is een onderzoek naar de snelheid en laadtijd van een website. Het doel is om te ontdekken of een website goed presteert op verschillende apparaten, zoals mobiele telefoons en desktops. Tijdens deze audit kijk ik naar technische knelpunten, zoals zware afbeeldingen, trage scripts of een te grote HTML structuur (DOM). Zo leer je hoe je de gebruikerservaring kunt verbeteren en je website sneller kunt maken.

## Geteste Website

Voor deze audit heb ik de website [Enti.com](https://www.byenti.com) getest. Dit is een online modestore gericht op moderne en bescheiden kledingstijlen. Ik werk hier zelf, dus het was interessant om te onderzoeken hoe de site technisch presteert.

## Gebruikte tools

Ik heb de website getest met de volgende tools:

- [Lighthouse(in DevTools van Chrome) ](https://developer.chrome.com/docs/lighthouse/overview?hl=nl) 
- [Google PageSpeed Insights](https://pagespeed.web.dev/)
- [WebPageTest](https://www.webpagetest.org/)

Elke tool geeft op een andere manier inzicht in de prestaties van een website. Zo krijg je een volledig beeld van wat er technisch goed gaat, en wat er beter kan.

## Screenshots van de testresultaten

### Lighthouse
- Mobile testresultaat
  <img width="1000" alt="Scherm­afbeelding 2025-04-15 om 20 10 59" src="https://github.com/user-attachments/assets/d348da77-07d6-4071-9bee-d4953e9daa0c" />

- Desktop testresultaat
<img width="1000" alt="Scherm­afbeelding 2025-04-16 om 00 22 15" src="https://github.com/user-attachments/assets/fb54ed13-50d3-4985-823d-25c5a5082aa7" />


### PageSpeed Insights (PSI)
- Mobile score en Core web vitals
<img width="1000" alt="Scherm­afbeelding 2025-04-16 om 01 07 21" src="https://github.com/user-attachments/assets/529860a2-473b-4477-ba45-39bd9353cd82" />
  
- Desktop score en Core web vitals
<img width="1000" alt="Scherm­afbeelding 2025-04-16 om 01 42 36" src="https://github.com/user-attachments/assets/a2ccc23e-a907-44d7-bb23-9055a6148023" />

### WebPageTest
- Waterfall chart


## Samenvatting van de bevindingen

### Mobiele prestaties
- De **mobiele score was laag (38/100)**.
- Grote afbeeldingen en veel scripts zorgen voor lange laadtijden.
- De HTML structuur is erg groot (DOM = veel elementen).
- Niet-gebruikte code vertraagt de eerste weergave van de pagina.

### Desktop prestaties
- Lighthouse gaf een **score van 99/100 op desktop**, maar dat is misleidend.
- PageSpeed Insights laat zien dat de pagina nog steeds zwaar is, vooral door:
  - Overbodige scripts
  - Grote netwerkbestanden
  - Veel third-party scripts zoals TikTok

### WebPageTest
- De waterfall chart laat zien **welke bestanden vertraging veroorzaken**.
- Veel externe scripts worden vroeg geladen.
- Render-blocking bronnen zorgen ervoor dat de pagina pas later zichtbaar is.
- Grote afbeeldingen vertraagt de LCP

## Wat kan er beter?

- Afbeeldingen comprimeren (bijv. WebP gebruiken)
- Lazy loading toepassen op niet zichtbare afbeeldingen
- Niet-gebruikte CSS/JS verwijderen
- JavaScript opdelen en pas laden als het nodig is
- DOM optimaliseren (minder elementen)
- Cachebeleid instellen voor statische bestanden
- Externe scripts beperken of verplaatsen naar het einde van de laadtijd

## Link naar mijn volledige documentatie

👉 [Klik hier voor de volledige wiki](https://github.com/Naddybsx/performance-audit/wiki)

In de wiki vind je:

- Een analyse van de Lighthouse en PSI resultaten
- Vergelijkingen tussen mobiel en desktop
- Uitleg over hoe je een waterfall chart leest
- Concrete aanbevelingen en oplossingen

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
