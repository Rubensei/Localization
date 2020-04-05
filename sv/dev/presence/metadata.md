---
title: Metadata.json
description: Innehåller grundläggande data om Presence
published: true
date: 2020-02-22T23:18:54.250Z
tags:
---

# Metadata.json

Om du vill publicera en närvaro i butiken och ladda den via tillägget bör du skapa `metadata. son` -filen i mappen `presence.js`.

Exemplet med den filen kan hittas nedan.

```javascript
{
  "författare": {
    "namn": "ANVÄNDAR",
    "id": "ID"
  },
  "bidragsgivare": [{
    "namn": "ANVÄNDAR",
    "id": "ID"
  }],
  "service": "TJÄNSTE",
  "description": {
    "sv": "DESCRIPTION"
  },
  "url": "URL",
  "regExp": "REGEXP",
  "iFrameRegExp": "REGEXP",
  "version": "VERSION",
  "logo": "URL",
  "thumbnail": "URL",
  "color": "#45A8FC",
  "taggar": ["CATEGORY", "TAG"],
  "category": "CATEGORY",
  "iframe": false
}
```

## Förstå metadata.json

Det exemplet ser verkligen konstigt ut, va? Oroa er inte, det är inte så svårt att förstå vad varje variabel är för.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Variabel</th>
      <th style="text-align:left">Beskrivning</th>
      <th style="text-align:left">Typ</th>
      <th style="text-align:left">Valfri</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>skapare</b>
      </td>
      <td style="text-align:left">Bör innehålla Objekt med <code>namn</code> och <code>id</code> av närvaroutvecklaren. Namnet är ditt Discord-användarnamn utan identifieraren (#0000). User <code>id</code> kan kopieras från Discord genom att aktivera utvecklarläget
        och högerklicka på din profil.</td>
      <td style="text-align:left"><code>Objekt</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>medverkande</b>
      </td>
      <td style="text-align:left">Bör innehålla Objekt med <code>namn</code> och <code>id</code> av närvaroutvecklaren. Namnet är ditt Discord-användarnamn utan identifieraren (#0000). User <code>id</code> kan kopieras från Discord genom att aktivera utvecklarläget
        och högerklicka på din profil.</td>
      <td style="text-align:left"><code>Array&lt;Object&gt;</code>
      </td>
      <td style="text-align:left"><code>Ja</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>tjänst</b>
      </td>
      <td style="text-align:left">Titeln på tjänsten som denna närvaro stödjer.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>beskrivning</b>
      </td>
      <td style="text-align:left">Liten beskrivning av närvaron, du kan använda beskrivning av tjänsten
        om du är utanför idéer. Din beskrivning måste innehålla nyckelparvärden som anger språket, och beskrivningen i det specifika språket. Gör beskrivningar med språken <i>som du känner</i>, våra översättare kommer att göra ändringar i din metadatafil. View the category for presence languages for a list. </td>
      <td style="text-align:left"><code>Objekt</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>URL</b>
      </td>
      <td style="text-align:left">URL of the service.<br><b>Example:</b><code>vk.com</code><br>
        <b>This url must match the url of the website as it will be used to detect wherever or not this is the website to inject the script to. This may only be used as an array when there are more than one urls.</b>
      </td>
      <td style="text-align:left"><code>Sträng, Array&lt;String&gt;</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>regExp</b>
      </td>
      <td style="text-align:left">En linjär uttryckssträng som används för att matcha webbadresser.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Ja</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>version</b>
      </td>
      <td style="text-align:left">Version av din närvaro.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>logotyp</b>
      </td>
      <td style="text-align:left">Länk till service&apos;s logotyp.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>thumbnail</b>
      </td>
      <td style="text-align:left">Länka till din närvaro miniatyr.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>färg</b>
      </td>
      <td style="text-align:left"><code>#HEX</code> värde. Vi rekommenderar att använda en primär färg på tjänsten
        som din närvaro stöder.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>taggar</b>
      </td>
      <td style="text-align:left">Array med taggar, kommer de att hjälpa användare att söka din närvaro på webbplatsen.</td>
      <td
      style="text-align:left"><code>Sträng, Array&lt;String&gt;</code>
        </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Kategori</b>
      </td>
      <td style="text-align:left">En sträng som används för att representera kategorin närvaron faller under.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Nej</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>iframe</b>
      </td>
      <td style="text-align:left">Anger om <code>iFrames</code> används</td>
      <td style="text-align:left"><code>Boolean</code>
      </td>
      <td style="text-align:left"><code>Ja</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>iFrameRegExp</b>
      </td>
      <td style="text-align:left">En reguljära uttrycksväljare som väljer iframes att injicera i.</td>
      <td style="text-align:left"><code>Sträng</code>
      </td>
      <td style="text-align:left"><code>Ja</code>
      </td>
    </tr>
  </tbody>
</table>

## Reguljära uttryck

Om du vill lära dig reguljära uttryck, här är några webbplatser.

#### Learning

• [RegexOne](https://regexone.com/) • [Regular Expressions Info](https://www.regular-expressions.info/tutorial.html)

#### Testing

• [Regexr](https://regexr.com/) • [Regex101](https://regex101.com/)

## Presence languages

PreMiD is a polygot service, meaning there are a multitude of languages involved to connect users around the globe. A full list of languages can be found with this [API endpoint](https://api.premid.app/v2/langFile/list).

## Presence categories

When making your presence, you must specify a category which the presence falls under. This is a compiled list of the categories that you can use.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Kategori</th>
      <th style="text-align:left">Namn</th>
      <th style="text-align:left">Beskrivning</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>anime</b></td>
      <td style="text-align:left"><b>Anime</b></td>
      <td style="text-align:left">Allt relaterat till anime, från forum till videoströmmande plattformar.</td>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>spel</b></td>
    <td style="text-align:left"><b>Spel</b></td>
      <td style="text-align:left">Alla webbplatser som har spelrelaterat innehåll, som <code>Kahoot</code> eller <code>Skribbl.io</code></td>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>musik</b></td>
    <td style="text-align:left"><b>Musik</b></td>
      <td style="text-align:left">Detta är webbplatser som erbjuder musikrelaterat innehåll, oavsett om det är streaming eller nedladdning.</td>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>socialt</b></td>
        <td style="text-align:left"><b>Socialt</b></td>
      <td style="text-align:left">Webbplatser som används för att skapa och dela innehåll eller för att delta i andra former av socialt nätverk.</td>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>videor</b></td>
        <td style="text-align:left"><b>Videor & Streams</b></td>
      <td style="text-align:left">Webbplatser som tjänar syftet att tillhandahålla videor och strömmar.</td>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>annat</b></td>
    <td style="text-align:left"><b>Annat</b></td>
      <td style="text-align:left">Allt som inte faller under en specifik kategori som anges ovan.</td>
      </td>
    </tr>
  </tbody>
</table>