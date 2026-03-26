# Project Mandaten: Peninei Halakha - Pesach Website Project

Dit document bevat de afspraken en instructies voor het project "Peninei Halakha - Nederlands".

## 1. Project Doelstelling
Het creëren van een uitgebreide Nederlandstalige website gebaseerd op het boek "Peninei Halakha: Pesach" van Rabbijn Eliezer Melamed. De website dient als een digitaal naslagwerk en leesplatform.

## 2. Website Richtlijnen
*   **Design:** Warm, academisch en overzichtelijk. Gebruik van het 'Libre Baskerville' lettertype voor een klassieke boek-uitstraling.
*   **Gebruiksvriendelijkheid:** De site moet 'responsive' zijn (goed leesbaar op zowel laptop als mobiel).
*   **Navigatie:** Een duidelijke hoofdpagina (`website/index.html`) met links naar alle hoofdstukken en secties.

## 3. Vertaling & Inhoud Richtlijnen
*   **Bron:** [Peninei Halakha - Laws of Pesah](https://ph.yhb.org.il/en/category/pesah/)
*   **Stijl:** Volledige, onverkorte en verhalende vertalingen van de Engelse brontekst naar het Nederlands.
*   **Terminologie:** Cruciaal is het behoud van de Hebreeuwse/Joodse terminologie (zoals *Chametz*, *Matzah*, *Kezajit*, *Sjechina*). Deze woorden worden **dikgedrukt** of in hun originele context gebruikt.
*   **Nauwkeurigheid:** Geen samenvattingen; de volledige diepgang en alle citaten van de brontekst moeten behouden blijven.

## 4. Workflow Afspraken
1.  **Extractie:** Ophalen van de volledige Engelse tekst per sectie van de officiële website.
2.  **Vertaling:** Volledige Nederlandse vertaling met focus op terminologie en leesbaarheid.
3.  **Opslag:** Vertalingen worden als Markdown opgeslagen in `/translations/` (naamgeving: `04-XX-XX_Titel.md`).
4.  **Publicatie:** De vertaling wordt direct omgezet naar een HTML-pagina in `/website/sections/chXX/`.
5.  **Index:** De hoofdpagina (`website/index.html`) wordt bijgewerkt met links naar de nieuwe secties.

## 5. HTML Template
Elke sectie-pagina volgt dit patroon:
```html
<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Sectienummer]. [Titel]</title>
    <link rel="stylesheet" href="../../style.css">
    <link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville:wght@400;700&family=Source+Sans+Pro:wght@400;600&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <div class="container">
            <h1>Peninei Halakha: Pesach</h1>
            <p class="subtitle">Hoofdstuk [N]: [Hoofdstuktitel]</p>
        </div>
    </header>
    <main class="container">
        <a href="../../index.html" class="back-link">&larr; Terug naar overzicht</a>
        <article class="content-section">
            <h2>[Sectienummer]. [Sectietitel]</h2>
            <!-- inhoud -->
        </article>
    </main>
    <footer>
        <div class="container">
            <p>&copy; 2026 Pesach Project - Peninei Halakha in het Nederlands</p>
        </div>
    </footer>
</body>
</html>
```
*Let op: voor H1-secties (in `/website/sections/` direct) is het pad naar style.css `../style.css` en naar index.html `../index.html`.*

---
*Overgedragen van Gemini naar Claude op: 26 maart 2026. Alle 16 hoofdstukken (H1–H16) zijn compleet vertaald en gepubliceerd.*
