# Ordinate

Laserkeilattu pistepilvi sisään, muokattava IFC4-arkkitehtimalli ulos.

**[Lataa Windowsille](https://github.com/Mcrauli/scan2bim-web/releases/latest/download/Ordinate-Setup.exe)**  ·  **[Verkkosivu](https://rekolalauri.fi/scan2bim-web/)**  ·  [Kaikki versiot](https://github.com/Mcrauli/scan2bim-web/releases)

## Mitä se tekee

Keilain antaa kymmeniä miljoonia pisteitä: kaiken mitä tilassa sattui olemaan.
Mallintaja piirtää niiden päälle seinät käsin. Ordinate tekee sen osan
automaattisesti ja **tarkistaa oman työnsä pistepilveä vasten.**

1. **Lataus.** E57, LAS/LAZ, PTS/XYZ, PLY/PCD — useampi tiedosto kerralla.
   Isot E57:t luetaan lohkoittain, jottei koko pilvi mene muistiin.
2. **Kalusteet pois.** Neuroverkko (PointNet) luokittelee jokaisen pisteen ja
   poistaa kalusteet, johdot ja LVI:n. Jäljelle jää runko.
3. **Rakenne esiin.** Seinät, laatat, pilarit, palkit, oviaukot ja tilat.
   Seinädetektori valitaan kohteen mukaan: vapaan tilan ääriviiva tavallisessa
   tilassa, tiheyshistogrammi paljaassa betonirungossa.
4. **Karsinta mittaamalla.** Seinä jonka pinnalla ei ole pisteitä poistetaan,
   väärässä paikassa oleva napsautetaan mitatulle pinnalle, ja evidenssin yli
   venytetty pää leikataan takaisin. Myös seinä joka jäi toisen taakse etsitään
   erikseen, koska ääriviiva näkee vain ensimmäisen pinnan.
5. **Vienti.** IFC4 millimetreissä, täysi hierarkia, materiaalit, Pset ja Qto.
   Ovet ja ikkunat leikkaavat seinän aidosti. Mukana QA-raportti.

## Kuinka tarkka se on

Nämä luvut on **mitattu**, ei arvioitu.

| | |
|---|---|
| Seinäpinnan sijaintivirhe | **0.04 mm** mediaani, 13/14 seinää alle 1.5 mm |
| Keilaimen oma kohina samoilla pinnoilla | 3–24 mm RMS |
| Kattavuus (aidoista seinäpisteistä mallissa) | **81–89 %** |
| Tarkkuus (mallin pinnan alla aitoa seinää) | **92–98 %** |

Sijaintiluvut ovat asuntoskannauksesta, mitattuna raakapilveä vasten. Kattavuus
ja tarkkuus on mitattu julkista **Rohbau3D**-vertailuaineistoa vasten
([doi:10.60776/ZWJFI4](https://doi.org/10.60776/ZWJFI4), MIT) viidellä eri
työmaakohteella — se on per-piste-luokiteltua dataa, joten mallia voi verrata
todelliseen seinään pisteen tarkkuudella.

Malli on siis kohinatason sisällä siellä missä se on, mutta **se ei löydä
kaikkea**: pahiten katveeseen jäävät pinnat joita keilain ei nähnyt. QA-raportti
kertoo tämän kohteittain, seinä seinältä, eikä piilota sitä.

## Käyttö

Asenna, avaa, raahaa skannitiedostot ikkunaan, vie IFC. Pythonia ei tarvita.
Sovellus päivittää itsensä tästä reposta.

## Tästä reposta

Julkinen jakelurepo: verkkosivu (GitHub Pages) ja Windows-asennusohjelma
Releases-välilehdellä. Lähdekoodi on yksityisessä `Mcrauli/scan2bim`-repossa.
