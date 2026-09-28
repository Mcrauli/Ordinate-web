# Product

## Register

brand

## Users

Ordinaten jakelu- ja markkinointisivu. Kohderyhmä on rakennusalan ammattilaiset, jotka tarvitsevat olemassa olevasta rakennuksesta mitattavan BIM-mallin:

- **BIM-mallintajat ja arkkitehtitoimistot** — tekevät IFC-malleja laserkeilausdatasta; Ordinate poistaa käsin jäljittämisen tunnit.
- **Rakenne- ja rakennussuunnittelijat** — tarvitsevat mitatun rungon (seinät, laatat, pilarit) saneeraus- ja korjaussuunnitteluun.
- **Insinööri- ja konsulttitoimistot** — scan-to-BIM osana laajempaa suunnittelu-/saneerausprojektia.

Myös **rakennuttajat, kiinteistönomistajat ja keilauspalvelut**, joille pistepilvi on vieras käsite (28.9.2026 laajennus).

Konteksti: kävijä päättää lataako ohjelman. Sivun pitää olla ymmärrettävä myös ilman alan jargonia: selitä mitä keilaus ja malli ovat, ja käytä teknisiä termejä (IFC, E57) vain tarkenteina. Ammattilaiselle yksityiskohdat löytyvät kysymyksistä.

## Product Purpose

Ordinate muuntaa laserkeilatun pistepilven (E57/LAS/LAZ/PTS) puhtaaksi, mitattavaksi arkkitehtimalliksi: seinät, laatat, pilarit, ovet ja ikkunat tunnistettuna oikeina IFC-objekteina, kalusteet ja LVI suodatettuna pois. Vienti IFC2X3 + DXF, jotka avautuvat Solibrissa, Revitissä ja ArchiCADissa. Kaupallinen Windows-työpöytäsovellus (GUI + CLI), ladattava asennusohjelma + automaattipäivitys.

Sivun tehtävä: vakuuttaa että automaatti tuottaa luotettavan, mitatun mallin — ja ohjata lataamaan asennusohjelma. Onnistuminen = lataus.

## Brand Personality

**Rohkea & erottuva.** Kolme sanaa: *mitattu, terävä, omaääninen.* Insinöörimäinen luotettavuus ilman tylsyyttä — uskaltaa näyttää erilaiselta kuin geneerinen BIM-/CAD-ohjelmisto. Ääni: suora, faktapohjainen, ei myyntipuhetta. Tunne jonka pitää syntyä: *"tämä on tehty ammattilaiselle ja se osaa asiansa."* Estetiikka on blueprint/pistepilvi-henkinen (tumma pohja, lime + cyan aksentit, editoriaalinen typografia) — tietoinen, committed valinta, ei refleksi.

## Anti-references

- **Ei geneeristä SaaS-startupia** — ei violetti-sini-gradientteja, ei pyöreitä kortteja kortin sisällä, ei "AI-slop" -kaavaa (eyebrow joka osiossa, identtiset korttiruudukot, hero-metric-template).
- **Ei leikkisä/kuluttajamainen** — ei sarjakuvakuvituksia, emojeita otsikoissa eikä kepeää sävyä; tämä on ammattityökalu.
- **Ei raskas enterprise** — ei tukkoinen harmaa lomakeviidakko, ei "yritysohjelmiston" jäykkyys.
- **Ei ylimyyty / hypeä** — ei "vallankumouksellinen tekoäly" -mainoskieltä; pitäydytään mitattavissa hyödyissä ja faktoissa.

## Design Principles

1. **Mittaa, älä mainosta.** Väitteet perustellaan konkretialla (mm-tarkkuus, QA-poikkeama, oikeat IFC-objektit), ei superlatiiveilla.
2. **Näytä lopputulos.** Pistepilvi → puhdas malli -muunnos on tuote; sen pitää näkyä, ei vain lukea (before/after, payoff-fokus).
3. **Erotu harkiten.** Rohkeus tulee vahvasta hierarkiasta, typografisesta rohkeudesta ja committed-väristrategiasta — ei lisätyistä efekteistä.
4. **Selkokieli ensin, tarkkuus perässä.** Jokainen väite ymmärrettävä ilman alan sanastoa; tekniset yksityiskohdat tarkenteina, eivät otsikoissa.
5. **Yksi selkeä toiminto.** Sivun jokainen osio palvelee yhtä päämäärää: lataa Ordinate.

## Accessibility & Inclusion

WCAG 2.1 AA tavoite: tekstikontrasti ≥4.5:1, näkyvät `:focus-visible`-tilat, `prefers-reduced-motion` kunnioitettu (reveal + sileä vieritys), kosketuskohteet ≥44px, toimiva mobiilinavigaatio. Sisältö näkyy myös ilman JS:ää (reveal vain progressiivinen parannus).
