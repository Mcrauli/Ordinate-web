---
name: Ordinate
description: Laserkeilattu pistepilvi puhtaaksi, mitattavaksi IFC/DXF-arkkitehtimalliksi.
colors:
  bg: "#0a0e14"
  bg-2: "#0f1620"
  panel: "#121a26"
  line: "#1e2a3a"
  ink: "#e6edf5"
  muted: "#8194a8"
  dim: "#7589a0"
  laser-lime: "#c6f24e"
  point-cyan: "#39d0d8"
  warn: "#ffb454"
typography:
  display:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: "clamp(46px, 8.2vw, 94px)"
    fontWeight: 800
    lineHeight: 1.04
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: "clamp(32px, 4.6vw, 52px)"
    fontWeight: 800
    lineHeight: 1.04
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: "23px"
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Spline Sans, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "normal"
  label:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: "12.5px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.08em"
rounded:
  sm: "8px"
  md: "11px"
  lg: "14px"
  pill: "100px"
spacing:
  xs: "12px"
  sm: "18px"
  md: "26px"
  lg: "48px"
  xl: "84px"
components:
  button-primary:
    backgroundColor: "{colors.laser-lime}"
    textColor: "{colors.bg}"
    rounded: "{rounded.md}"
    padding: "14px 26px"
  button-ghost:
    backgroundColor: "{colors.bg-2}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "14px 26px"
  panel:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.ink}"
    rounded: "{rounded.lg}"
    padding: "30px"
---

# Design System: Ordinate

## 1. Overview

**Creative North Star: "The Scan Bay"**

Ordinaten sivu on pimeä keilaushalli. Tausta on lähes musta, sinertävä tila (#0a0e14), jonka päällä leijuu hienovarainen pistepilvitekstuuri — kuin keilaimen näkemä huone ennen kuin siitä on mitattu mitään. Tähän tilaan tuodaan kaksi mittaavaa valoa: **laser-lime** (#c6f24e) on aktiivinen säde, joka osoittaa tärkeimmät teot ja tulokset; **point-cyan** (#39d0d8) on data itse, pisteet ja tekniset merkinnät. Kaikki muu on kalibroitua harmaata.

Systeemi on **rohkea ja erottuva** ammattilaistyökaluksi: vahva typografinen hierarkia ja committed-väristrategia kantavat sen, eivät lisätyt efektit. Se torjuu tietoisesti geneerisen SaaS-startup-lookin (violetti-sini-gradientit, pyöreät kortit kortin sisällä), kuluttajamaisen leikkisyyden ja raskaan enterprise-harmaan. Tumma teema ei ole "cool dark by default" vaan domain-perusteltu: laserkeilaus tapahtuu fyysisesti pimeässä mitatussa tilassa, ja sivu elää samassa maailmassa.

Sävy on mittaava, ei mainostava: jokainen väite näytetään konkretialla (mm-tarkkuus, QA-poikkeama, oikeat IFC-objektit).

**Key Characteristics:**
- Tumma, sinertävä "keilaushalli" -pohja + pistepilvitekstuuri
- Yksi terävä lime-aksentti teoille ja tuloksille; cyan datalle/merkinnöille
- Vahva display-typografia (Bricolage Grotesque 800), editoriaalinen rytmi
- Hiusviivat (#1e2a3a) jakajina — ei laatikoita laatikoiden sisään
- Mitattu, faktapohjainen ääni; ei hypeä

## 2. Colors

Tumma sinertävä neutraalipohja, jossa kaksi kylläistä aksenttia kantavat koko identiteetin — kaikki muu on kalibroitua harmaaskaalaa.

### Primary
- **Laser Lime** (#c6f24e): Aktiivinen säde. Ensisijaiset CTA:t ("Lataa"), avainsanojen korostus otsikoissa, numerot sekvenssissä, payoff-paneelin reuna. Käytön niukkuus on sen voima.

### Secondary
- **Point Cyan** (#39d0d8): Data ja tekniset merkinnät — mono-labelit, `tag-mono`-leimat, koodin korosteet. Erottuu limestä roolina: lime = teko, cyan = data.

### Neutral
- **Scan Black** (#0a0e14): Sivun pohja — pimeä mitattu tila.
- **Bay Surface** (#0f1620) & **Panel** (#121a26): Kohotetut pinnat (alt-osiot, paneelit, taulut).
- **Grid Line** (#1e2a3a): Hiusviivat, reunat, jakajat.
- **Ink** (#e6edf5): Pääteksti ja otsikot.
- **Muted** (#8194a8) & **Dim** (#7589a0): Leipäteksti ja toissijainen teksti tummalla (≥4.5:1).

### Tertiary
- **Signal Amber** (#ffb454): Vain varoituksille. Ei koristekäyttöä.

### Named Rules
**The One Beam Rule.** Lime on aktiivinen säde — sitä käytetään korkeintaan ~10 % näkyvästä pinnasta. Jos kaikki hehkuu limellä, mikään ei ohjaa. **The Two Lights Rule.** Lime ja cyan eivät ole vaihtoehtoisia: lime = teko/tulos, cyan = data/merkintä. Älä sekoita rooleja.

## 3. Typography

**Display Font:** Bricolage Grotesque (fallback sans-serif)
**Body Font:** Spline Sans (fallback sans-serif)
**Label/Mono Font:** JetBrains Mono

**Character:** Bricolage Grotesque on omaääninen, hieman epäsovinnainen groteski — antaa rohkeuden ilman koristeellisuutta. Spline Sans on neutraali humanisti, joka pitää leipätekstin luettavana. JetBrains Mono tuo teknisen, "mittalaite"-tunnun labeleihin ja koodiin. Pari toimii kontrastiakselilla: ekspressiivinen display vs. neutraali humanisti vs. mono — ei kahta samanlaista groteskia.

### Hierarchy
- **Display** (800, clamp 46–94px, lh 1.04, ls -0.035em): Vain hero. `text-wrap: balance`.
- **Headline** (800, clamp 32–52px, lh 1.04, ls -0.02em): Osioiden h2-otsikot.
- **Title** (600, 23px): Korttien/sekvenssin/FAQ:n otsikot.
- **Body** (400, 17px, lh 1.65): Leipäteksti, max ~62–68ch. `text-wrap: pretty`.
- **Label** (600, 12.5px, ls 0.08em, UPPERCASE): Mono-leimat, `tag`, taulun otsikot. Cyan-värisenä.

### Named Rules
**The Mono-as-Instrument Rule.** JetBrains Monoa käytetään vain teknisinä merkintöinä (labelit, koodi, optioluettelo) — ei leipätekstinä eikä "dev-tool"-koristeena. **The Display-Ceiling Rule.** Hero enintään 94px; ei yli, ettei sivu huuda.

## 4. Elevation

Systeemi on lähtökohtaisesti **litteä**. Syvyys tehdään tonaalisella kerrostuksella (bg → bg-2/panel) ja hiusviivoilla (#1e2a3a), ei varjoilla. Ainoa poikkeus on tarkoituksellinen, brändinmukainen hehku.

### Shadow Vocabulary
- **Payoff Glow** (`box-shadow: 0 24px 64px -30px rgba(198,242,78,.28)`): Vain before/after-osion "ulos"-paneelissa korostamassa lopputulosta (StructuralModel). Tämä on tietoinen "rohkea & erottuva" -valinta, ei oletus.
- **Tag Dot Glow** (`box-shadow: 0 0 10px var(--accent)`): Hero-tagin pieni pistevalo.

### Named Rules
**The Flat-Bay Rule.** Pinnat ovat litteitä levossa; syvyys tulee sävystä ja viivasta. Hehku on poikkeus, joka varataan yhdelle fokuspisteelle (payoff). Älä lisää geneerisiä drop-shadow'ta kortteihin.

## 5. Components

### Buttons
- **Shape:** Pehmeästi pyöristetty (11px, `{rounded.md}`).
- **Primary:** Lime-tausta (#c6f24e), tumma teksti (#0a0e14), padding 14×26px, Bricolage 600. Hover: `translateY(-2px)`. Active: takaisin 0.
- **Ghost:** bg-2-tausta, ink-teksti, line-reuna. Hover: lime-reuna + lime-teksti.
- **Focus:** näkyvä `:focus-visible` — 2px lime-ääriviiva, offset 3px.

### Cards / Containers
- **Corner Style:** 14px (`{rounded.lg}`).
- **Background:** panel (#121a26).
- **Border:** 1px line (#1e2a3a).
- **Shadow Strategy:** litteä (ks. Elevation); poikkeus payoff-paneeli.
- **Internal Padding:** 24–30px.
- Käytetään säästeliäästi: output-kortit ja before/after-paneelit. **Ei** identtisiä ikoni+otsikko+teksti -ruudukoita.

### Navigation
- **Style:** sticky, blur-tausta (rgba(10,14,20,.72)), 1px alareuna. Linkit muted → ink hoverissa.
- **Mobile (<760px):** hampurilaisnappi (44×40px); valikko avautuu pudotuksena. Linkin klikkaus sulkee.

### Tables (optio-luettelo)
- Hiusviivarivit, mono-otsikot (cyan, uppercase), `td:first-child` lime-mono nowrap. Ei solujen reunoja, vain vaakaviivat.

### Signature: Editorial "Why" Row
Iso väittämä (Bricolage 800, clamp 27–42px) avainsana limellä korostettuna, hiusviivalla erotettu rivi — ei kortti. Kantaa "rohkea & erottuva" -linjan ilman laatikoita.

### Signature: Before/After Scan Slider
Heron pääkuva: sama kohde samasta kamerakulmasta pistepilvenä (cyan) ja mallina (valkoinen, lime-yläreunat), vedettävä erotin (lime). Kuvat renderöidään `data/_web_render3d.py`:llä vain omasta tai markkinointiin lisensoidusta datasta. Näppäimistö: `input[type=range]`.

### Signature: Pipeline Overview Strip (poistettu 28.9.2026, korvattu sliderilla)
Kompakti vaakarivi: `Lataus → Segmentointi → Semantiikka → Malli → Export`, lime-nuolet. Yleiskuva herossa; numeroitu detalji vain "Miten"-osiossa (01–04).

### Motion
Reveal-animaatiot vahvistavat jo näkyvää oletusta (`.js`-gated), staggered IntersectionObserverilla. `prefers-reduced-motion` kunnioitettu kaikkialle. Easing pehmeä ease-out, ei bounce.

## 6. Do's and Don'ts

### Do:
- **Do** käytä limeä aktiivisena säteenä ≤10 % pinnasta (CTA, avainsana, tulos); cyan datalle ja merkinnöille.
- **Do** rakenna syvyys sävyllä (bg → panel) ja hiusviivoilla, ei varjoilla.
- **Do** pidä display-typografia rohkeana (Bricolage 800) ja hierarkia jyrkkänä.
- **Do** perustele väitteet konkretialla (mm, QA, IfcWall/IfcDoor), älä superlatiiveilla.
- **Do** varmista ≥4.5:1 kontrasti ja näkyvät `:focus-visible`-tilat.

### Don't:
- **Don't** tee geneeristä SaaS-startup-lookia: ei violetti-sini-gradientteja, ei pyöreitä kortteja kortin sisällä, ei hero-metric-templatea.
- **Don't** lisää eyebrow-kickeriä joka osioon eikä identtisiä ikoni+otsikko+teksti -korttiruudukoita (AI-grammar).
- **Don't** käytä leikkisää/kuluttajamaista sävyä — ei emojeita otsikoissa, ei sarjakuvakuvitusta.
- **Don't** valu raskaaseen enterprise-harmaaseen tai lomakeviidakkoon.
- **Don't** myy hypellä ("vallankumouksellinen tekoäly"); pitäydy mitattavissa hyödyissä.
- **Don't** levitä lime-hehkua ympäri sivua — se on varattu yhdelle fokuspisteelle.
