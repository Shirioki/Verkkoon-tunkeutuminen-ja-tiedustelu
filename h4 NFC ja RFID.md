# h4 NFC ja RFID

## 1. Tarkastele käytössäsi olevia RFID tuotteita, mieti miten hyvin olet suojautunut RFID urkinnalta?

RFID tuotteita jotka ovat omassa käytössäni ovat kotiavain, maksukortit ja matkakortti. Näitä vastaan en ole suojautunut sen ihmeellisemmin kuin, että säilytän lompakkoani ei näkyvällä paikalla. Mutta voisin suojautua näitä vastaan paremmin esimerkiksi RFID-suojakoteloilla tai korteilla.

## 2. Tutustu APDU komentojen rakenteeseen (voit käyttää tekoälyä tutustumiseen)

APDU (Application Protocol Data Unit) -komennot ovat viestintäyksiköitä, joita käytetään älykorttien ja kortinlukijoiden välillä. Ne koostuvat seuraavista osista:​

- CLA (Class byte): Määrittää komennon luokan.​

- INS (Instruction byte): Määrittää suoritettavan toiminnon.​

- P1 ja P2 (Parameter bytes): Tarjoavat lisäparametreja komennolle.​

- Lc (Length of command data): Ilmoittaa komennon datan pituuden.​

- Data: Sisältää itse komennon datan.​

- Le (Length of expected response data): Ilmoittaa odotetun vastausdatan pituuden.​

Vastaavasti, kun kortti vastaa komennon jälkeen, se lähettää Response APDU:n, joka sisältää:​

Data: Vastausdatan.​

SW1 ja SW2 (Status words): Kaksi tavua, jotka ilmaisevat komennon suorittamisen tuloksen.​

Tämä rakenne mahdollistaa monimutkaisten toimintojen suorittamisen älykorteilla ja on keskeinen osa korttien ja lukijoiden välistä viestintää.​

## 3. Tutki ja kerro minkä mielenkiintoisen RFID hakkerointi uutiset löysit. (Vinkki, useimmat liittyvät henkilökortteihin)

Elokuussa 2024 paljastui, että FM11RF08S-niminen MIFARE Classic -korttivariantti sisältää laitteistotakaportin, joka mahdollistaa kortin kaikkien avainten ohittamisen.
Tämä tarkoittaa, että hyökkääjä voi kloonata kortin ja saada pääsyn esimerkiksi hotellihuoneisiin tai toimistoihin ilman oikeaa avainta.

## Lähteet

Hardware Backdoor Discovered In RFID Cards Used In Hotels And Offices Worldwide: https://www.hacking.reviews/2024/08/hardware-backdoor-discovered-in-rfid.html

Smart card application protocol data unit: https://en.wikipedia.org/wiki/Smart_card_application_protocol_data_unit

