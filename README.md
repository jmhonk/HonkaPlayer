# HonkaPlayer

Kaikkien tarpeisiin sopiva musiikkisoitin Windowsille. Toimii kansiosta ilman asennusta:
käynnistä `HonkaPlayer.exe`.

Tehty Electronilla (HTML, CSS ja JavaScript) ja Web Audio API:lla.

---

## Ominaisuudet

### Soitin
- Toisto ja tauko, edellinen ja seuraava, kelaus edistymispalkista
- Äänenvoimakkuus ja mykistys
- **Sekoita** – satunnainen järjestys
- **Toistotila** (klikkaus vaihtaa): *Toista kaikki* → *Toista yksi* → *Ei toistoa*
- **Pienennä / Laajenna** – piilottaa kirjaston ja jonon, jolloin ikkuna kutistuu pelkäksi
  soittimeksi. Soitin aukeaa aina laajennettuna.
- **EQ** – taajuuskorjain omassa ikkunassaan: 10 kaistaa, esivahvistus ja esiasetukset
  (Rock, Pop, Basso…). Tuplaklikkaus nollaa kaistan. Oletuksena pois päältä; EQ-nappi
  korostuu, kun taajuuskorjain on päällä.
- Klikkaus kellonaikaan (Klassikko-teema) vaihtaa kuluneen ja jäljellä olevan ajan.

### Kirjasto
- **+ Lisää kansio** lisää kansion alikansioineen. Soitin muistaa lisätyt kansiot.
- Tiedostoja ja kansioita voi myös **raahata** ikkunaan.
- **⟳ Päivitä** etsii muistetuista kansioista uudet kappaleet, poistaa koneelta poistetut
  (myös soittolistoilta ja jonosta) ja lukee muuttuneiden tiedostojen tiedot uudelleen.
  Sama tarkistus tehdään automaattisesti käynnistyksessä. Jos kokonainen kansio puuttuu
  (esim. irrotettu ulkoinen levy), sen kappaleita ei poisteta.
- Kirjastosta itse poistetut kappaleet eivät palaa päivityksessä. Jos kansiosta poistetaan
  kaikki kappaleet, soitin unohtaa koko kansion. Kansion lisääminen uudelleen palauttaa
  poistetut kappaleet.
- Samaa tiedostoa ei lisätä kahdesti.
- Kappaleiden tiedot (nimi, esittäjä, albumi, genre, vuosi, kappalenumero) luetaan
  tiedostoista taustalla.
- **Taulukko**: Kappale, Esittäjä, Albumi, Genre, Vuosi, Kesto
  - otsikon klikkaus järjestää, toinen klikkaus kääntää järjestyksen
  - sarakkeen leveyttä muutetaan vetämällä otsikon reunasta (tuplaklikkaus = oletus)
  - hiiren oikea nappi otsikkoriviin: näytettävät sarakkeet (Kappale ja Esittäjä aina näkyvissä)
  - lista rullaa myös sivuttain
- **Ryhmät** vasemmalla (valintalaatikko): *Esittäjä*, *Albumi*, *Genre*, *Soittolistat*
  - klikkaus suodattaa, Ctrl-/Shift-klikkaus valitsee useita
  - tuplaklikkaus vaihtaa jonoksi ryhmän kappaleet ja aloittaa soiton
- **Haku** suodattaa sekä kappaleita että ryhmälistaa (nimi, esittäjä, albumi, genre, vuosi).
- **Tuplaklikkaus kappaleeseen**: jonoksi vaihtuu se, mitä kirjasto näyttää, ja soitto alkaa
  klikatusta kappaleesta.
- **Hiiren oikea nappi** kappaleeseen tai ryhmään: *Toista valinta*, *Lisää jonoon*,
  *Lisää soittolistaan ▸*, *Poista kirjastosta*.

### Soittolistat
- *Soittolistat*-näkymässä **+ Uusi soittolista**.
- Kappaleita lisätään hiiren oikealla → *Lisää soittolistaan ▸*.
  ✓ = kappale on jo listalla (klikkaus poistaa), – = osa valituista on listalla.
- Hiiren oikea nappi listaan: toista, lisää jonoon, nimeä uudelleen, poista.

### Jono
- Oikeassa reunassa näkyy, mitä soitetaan nyt.
- Järjestystä voi muuttaa vetämällä, ja kappaleita voi raahata kirjastosta jonoon.
- Hiiren oikea nappi: *Toista*, *Lisää soittolistaan ▸*, *Poista jonosta*.
- **Tyhjennä jono** jonon alla.

### Asetukset (⚙)
- **Teema**: Moderni (oletus) tai Klassikko
- **Korostusväri**: Smaragdi, Yösini, Meripihka, Neon, Paperi
- **Tasapaino**: vasen / oikea kanava (tuplaklikkaus = keskelle)
- **Ristihäivytys**: 0–12 s, kappaleet liukuvat toisiinsa (oletuksena pois)
- **Tasaa äänenvoimakkuus**: kappaleet soivat suunnilleen yhtä kovaa (oletuksena päällä).
  Äänekkyys mitataan soiton aikana (LUFS, tavoite −14) ja tallennetaan kirjastoon.
  Rajoitin estää säröytymisen.
- **Kansiot → Hallitse…**: lista lisätyistä kansioista ja niiden kappalemääristä. Kansion voi
  poistaa, jolloin sen kappaleet poistuvat kirjastosta (tiedostot jäävät koneelle). Samasta
  ikkunasta voi myös lisätä kansion.
- **Pikanäppäimet → Muokkaa…**: omat pikanäppäimet (oletuksena ei yhtään)

### Näppäimistö
- **Mediapainikkeet** (toista/tauko, seuraava, edellinen) toimivat aina, myös kun soitin on
  taustalla. Soiva kappale näkyy Windowsin mediapaneelissa.
- Omia pikanäppäimiä ei ole oletuksena; ne asetetaan asetuksista.
- Listoissa: **Delete** poistaa valitut, **Ctrl+A** valitsee kaikki, **Enter** soittaa
  valitut, **Ctrl+F** siirtyy hakuun, **Esc** sulkee valikot ja ikkunat.

### Muistaa käynnistysten välillä
- Kirjaston, soittolistat, jonon ja lisätyt kansiot
- Toistokohdan (sama kappale samasta kohdasta, ei ala soida itsestään)
- Ikkunan koon, paikan, näytön ja suurennustilan
- Kaikki asetukset

Tiedot ovat kansiossa `%APPDATA%\HonkaPlayer` (kirjasto: `library.json`).

### Suorituskyky
- Listoista piirretään vain näkyvät rivit, joten kymmenetkin tuhannet kappaleet toimivat
  sujuvasti.
- Kansioiden läpikäynti ja tietojen luku tehdään taustalla.

### Tuetut tiedostomuodot
MP3, FLAC, OGG, Opus, WAV, M4A/AAC, WebM
