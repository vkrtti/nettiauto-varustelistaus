# Varustelistaaja

Pudota auton varuste-PDF (tai kuva tai liitetty teksti), ja sivu palauttaa:

- Nettiauto-varustelistan suomeksi, järjestettynä ostajan kannalta tärkeimmästä alkaen
- Suomi-auto-tarkistuksen ja sen perusteet
- Myyntiväittämän (USP) 200 merkin kenttään. Merkit lasketaan koodilla, ja liian pitkä rivi lyhennetään.
- Listan asioista, jotka pitää tarkistaa itse (omistajat, huolto, renkaat…)

Sivu on yksi staattinen `index.html`, joka toimii GitHub Pagesissa.

## Käyttö

1. Avaa sivu ja klikkaa oikeasta yläkulmasta **Lisää API-avain**.
2. Liitä oma Anthropic API -avain ([console.anthropic.com](https://console.anthropic.com/settings/keys)) ja valitse malli.
3. Pudota PDF laatikkoon.

Avain tallentuu vain käyttäjän omaan selaimeen (localStorage), ja selain lähettää sen suoraan Anthropicille. Repossa ei ole avaimia.

## Ohjeen muokkaus

Mallin ohje on `index.html`:n sisällä `<script type="text/plain" id="systemPrompt">` -lohkossa. Ohje on sama kuin Clauden `nettiauto-varustelista`-skillissä, ja loppuun on lisätty sovelluksen JSON-muoto.
