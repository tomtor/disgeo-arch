## Inrichting

### Inleiding

Dit hoofdstuk beschrijft de functionele inrichting van de Samenhangende Objectenregistratie op de applicatielaag van het NORA-vijflaagsmodel. Het doel ervan is om sturing te kunnen geven aan de transitie naar de Objectenregistratie en te dienen als kader voor technische inrichting van de Objectenregistratie. Ook biedt het een deel van de basis voor de organisatorische inrichting van de Objectenregistratie. 

Dit hoofdstuk beschrijft de onderdelen van de Objectenregistratie en de verbindingen daartussen en het wijst de functies van de Objectenregistratie toe aan deze onderdelen. 

<p style="color:blue">
Opm. Hfdst 3.1 en 3.2 geven nauwelijks richting, behalve wellicht de 10 gouden data rules, waar overigens (regel 6 en 8) nog wel wat op aan te merken is denk ik.
In 3.3 staan nog wat principes die op zich wel hout snijden.
</p>

### Functionele lagen in de inrichting

We onderscheiden drie lagen in de functionele indeling van de Objectenregistratie, zoals de afbeelding hieronder toont. Daarmee duiden we alleen het doel van de functies en doen we geen uitspraak over de de technische inrichting of de verdeling ervan over verschillende ICT-voorzieningen.

<figure id="inrichtinglagen">
    <img src="media/functionele-lagen-objectenregistratie.png" alt="functionele lagen">
    <figcaption>Functionele lagen in de inrichting van de Objectenregistratie</figcaption>
</figure>

De laag **Inzicht** bevat de functies die nodig zijn voor het beheren en gebruiken van gegevens over de gegevens, ofwel metagegevens. Deze laag wordt gebruikt door de andere lagen om de gegevensstructuur en de gegevensregels te kunnen toepassen in voorzieningen en om inzicht in de gegevenskwaliteit te verkrijgen.

De **Uitvoeringslaag** bevat de functies die nodig zijn voor het beheren en afnemen van objectgegevens, zoals voor het registreren en wijzigen van gegevens en voor het raadplegen ervan. Op deze laag maken we onderscheid tussen de functies ten behoeve van het beheren van objectgegevens door gebruikers in de rol van bronhouder en het afnemen van objectgegevens door gebruikers in de rol van afnemer. 

De **Ondersteuningslaag** bevat de functies die nodig zijn om bronhouders en afnemers te ondersteunen bij het beheren en afnemen van gegevens, zoals het beheren van machtigingen en het raadplegen van dienstencatalogi.

De functies in de drie lagen voor Inzicht, Uitvoering en Ondersteuning maken we zichtbaar in een **overzicht van capabilities**. In dit overzicht zijn clusters van functies gegroepeerd tot componenten. Deze vormen de inrichting van de voorzieningen. 

<figure id="Inzicht-inrichting-uitvoering">
    <img src="media/inrichting-inzicht-uitvoering-ondersteuning-objectenregistratie.png" alt="inrichting Inzicht uitvoering ondersteuning">
    <figcaption>De capabilities op de lagen Inzicht en Uitvoering en Ondersteuning</figcaption>
</figure>

    <p style="color:blue">
    Opmerking Lennart: Registreren lijkt ontkoppelt van ontsluiten/verstrekken. Ik denk dat dit "oud" denken is. Als je de keten kantelt, en data-gedreven werkt, dan is er "maar 1 database", waar alle processen in samenhang op werken. De inwinnende partij is verantwoordelijk voor de correctheid van de data, die verstrekt wordt - en wordt geacht zelf die data op orde te maken. Dan ligt de correctheid van de data ook bij de juiste partij, de partij met kennis, en die partij is zich bewust/sensitief van hoe de data gebruikt wordt. Kortom: inwinnen voor gebruik. 
    
    Nou kan je best er een aparte database van maken, bv. een real-time replica, desnoods een aparte database met deels een apart technisch datamodel, maar niet een apart informatiemodel. De informatie moet in de keten gelijk zijn, met dezelfde betekenis en ontsloten zodra dit kan. Ook mbt wanneer dit kan, beschikt alleen de inwinnende partij (over het algemeen) over de juiste kennis om dit in te schatten/te bepalen. Als je dus aparte technische datamodellen maakt, hou het informatiemodel deel dan 1 op 1 hetzelfde (!, dan kan dit wel, maar met behoud van consistentie). 
    
    Ik doel hier overigens nadrukkelijk niet op informatieproducten, of informatie op maat. Die onderwerpen zitten in een verlengstuk op de bron. Ik heb het uitdrukkelijk over de data in de bron. Zeg maar, de informatie waarmee de informatieproducten het moeten doen. Immers, alleen deze informatie uit de bron is er, er is verder niks (ook al wil je meer, er is niet meer, ook al wil je informatie met een andere betekenis, die is er niet, want het is niet zo ingewonnen).
    </p>


### Functies in de laag Inzicht

Op de laag **Inzicht** onderkennen we de volgende clusters voor inzien van de gegevensstructuur en het dienstenportfolio en inzicht in de gegevenskwaliteit: 

- *Toegang*: voor het bewaken van de toegang tot de diensten.
- *Gegevenscatalogus*: voor het kunnen beschrijven van de in de objectenregistratie beschikbare gegevens en informatieproducten en deze beschrijving te ontsluiten, zodat bronhouders, afnemers en andere betrokkenen hier kennis van kunnen nemen.
 - *Gegevenskwaliteit*: voor het vastleggen van de afgesproken kwaliteitsindicatoren en het meten en monitoren wat de waarde van deze indicatoren is en zowel de indicatoren als de gemeten waarden beschikbaar te stellen voor bronhouders, afnemers en andere betrokkenen, zoals toezichthouders en beleidsverantwoordelijken.
 - *Dienstencatalogus:* voor het beschrijven van de diensten van de objectenregistratie en om deze beschrijvingen (interactief) te ontsluiten, zodat betrokkenen hier makkelijk en goed kennis van kunnen nemen.


    <p style="color:blue">
    Opmerking Lennart: 

    Helemaal top natuurlijk zo'n gegevenscatalogus.

    Maar als ik me niet vergis kent een basisregistratie ook een semantische laag, waarin de semantiek beschreven is in gewone mensentaal, nog zonder dat er een catalogus is gemaakt van de gegevens/informatie zelf. De positionering daarvan lijkt me van belang om toe te voegen. Als aanvulling op wat er al staat (de quote hierboven).

    Wat dit betreft: ik ben er 100% voor om een informatiemodel te gebruiken als datgene waar de informatie in het stelsel zich aan conformeert. Immers, dat is het model van informatie (data/gegevens). Het model van de verdere semantiek is belangrijk en leuk, maar dat is niet informatie die wordt uitgewisseld. Dus inderdaad, het gegevensmodel moet centraal staan. Overigens noemen we die: informatiemodel in o.a. NEN3610. Zie ook MIM paragraaf 1.5 voor de betekenis van wat er onder een begrippen model en een informatiemodel wordt verstaan.
https://docs.geostandaarden.nl/mim/def-st-mim-20201023/#typen-informatiemodellen

    Merk op, er zijn wel eens mensen die informatiemodel definiëren als: de interne structuur in de database (MIM niveau 4), Dat bedoel ik expliciet niet. Ik doel op MIM niveau 2. 
    
    Waarom is het terecht om applicaties op het conceptuele informatiemodel te baseren:

    - De informatie is conform deze betekenis ingewonnen. Niet met een andere betekenis. Alle andere betekenissen zijn per definitie onduidelijk, want het is niet met die betekenis ingewonnen.

    - Standaardisatie en hergebruik en consistentie over 10-tallen API's heen begint met een gestandaardiseerde informatiestructuur. Al dan niet als onderlaag, die vertaalt wordt naar informatie op maat.

    - De data/gegevens conformeren zich niet aan het veel vrijere begrippenmodel, maar aan het informatiemodel.

    - De data/gegevens worden vaak wel in een 'informatie op maat' informatieproduct verder getuned. Dat is nuttig en belangrijk. Je hebt hier de vrijheid nodig om los te komen van het conceptuele informatiemodel, maar wel op een traceerbare wijze en met behoud van betekenis.

    Ik verwacht hier nog een inrichtingsprincipe: alle informatie die geleverd wordt, is qua betekenis conform het informatiemodel. Ofwel omdat de informatie 1 op 1 wordt geleverd, ofwel omdat informatie meer op maat wordt geleverd, maar dan is de betekenis traceerbaar naar het informatiemodel.
    </p>


### Functies in de laag Uitvoering

Op de Uitvoeringslaag onderkennen we de volgende clusters voor *beheer en afname van objectgegevens*:
- *Toegang*: voor het bewaken van de toegang van bronhouders en hun gemachtigden tot de beheerdiensten en van afnemers tot de afnamediensten. 
- *Registratie*: voor het creëren en wijzigen van objectgegevens door bronhouders en hun gemachtigden.
- *Opslag*: voor het duurzaam beschikbaar houden van objectgegevens.
- *Afname*: voor het afnemen van objectgegevens en daarvan afgeleide informatieproducten.
- *Notificatie*: voor het notificeren van afnemers van voor hen relevante gebeurtenissen die betrekking hebben op objectgegevens, zodat zij kunnen handelen naar die gebeurtenissen.
- *Terugmelding*: voor het in staat stellen van afnemers om meldingen over de juistheid van gegevens te kunnen registreren en deze beschikbaar te laten zijn voor bronhouders, zodat zij ze kunnen behandelen.

De component Terugmelding heeft als doel dat meldingen van afnemers over de juistheid van gegevens geregistreerd kunnen worden en beschikbaar zijn voor bronhouders, zodat zij ze kunnen behandelen

    <p style="color:blue">
    Opmerking Lennart: 
    Registreren lijkt ontkoppelt van ontsluiten/verstrekken. Ik denk dat dit "oud" denken is. Als je de keten kantelt, en data-gedreven werkt, dan is er "maar 1 database", waar alle processen in samenhang op werken. De inwinnende partij is verantwoordelijk voor de correctheid van de data, die verstrekt wordt - en wordt geacht zelf die data op orde te maken. Dan ligt de correctheid van de data ook bij de juiste partij, de partij met kennis, en die partij is zich bewust/sensitief van hoe de data gebruikt wordt. Kortom: inwinnen voor gebruik. Nou kan je best er een aparte (real-time replica t.b.v. load-spreiding) database van maken, maar niet een apart informatiemodel. De informatie moet in de keten gelijk zijn, met dezelfde betekenis en ontsloten zodra dit kan. Ook mbt wanneer dit kan, beschikt alleen de inwinnende partij (over het algemeen) over de juiste kennis om dit in te schatten/te bepalen.
    
    Ik doel hier met informatiemodel overigens nadrukkelijk niet op informatieproducten, noch op informatie op maat. Deze laatste onderwerpen zitten in een verlengstuk op de bron. Ik heb het uitdrukkelijk over de data in de bron en 1 op 1 afname vanuit deze bron via de algemene data-services. Zeg maar, de informatie waarmee de informatieproducten het moeten doen. Immers, alleen deze informatie uit de bron is er, er is verder niks (ook al wil je meer, er is niet meer, ook al wil je informatie met een andere betekenis, die is er niet, want het is niet zo ingewonnen).
    </p>


### Functies in de laag Ondersteuning

Op de **Ondersteuningslaag** onderkennen we de volgende clusters voor de ondersteuning van bronhouders en hun gemachtigden en afnemers:
- *Toegang*: voor het bewaken van de toegang van bronhouders en hun gemachtigden en afnemers tot de ondersteuningsdiensten.
- *Machtigingen*: voor het beheren van machtigingen voor diensten door bronhouders en afnemers. 
- *Abonnementen*: voor het kunnen registreren en beheren van abonnementen door bronhouders en afnemers op notificaties over gebeurtenissen die betrekking hebben op objectgegevens waarin ze geïnteresseerd zijn, en voor het kunnen registreren en beheren van abonnementen op Afname.
- *Betalingen*: voor het beheren van betalingen van betaalde diensten door de gebruikers van die diensten, indien sprake is van betaalde diensten. Betalen kan op verschillende manieren worden ingericht, zoals vooraf, bij afname van de dienst of achteraf, en is gekoppeld aan abonnementen.



### Algemene functies

In alle drie lagen onderkennen we *Toegang* voor het bewaken van toegang tot diensten. Deze functie wordt op een plek uitgewerkt onder Algemeen. 

Verder onderkennen we de behoefte aan *Interactie* om de diensten en de gegevens en producten van de objectenregistratie aan eindgebruikers (personen in de rol van bronhouder of afnemer) te presenteren en de mogelijkheden te bieden om er mee te interacteren.

De objectenregistratie zal naar verwachting verschillende generieke interactiecomponenten bieden, bijvoorbeeld een viewer voor het zoeken en raadplegen van objectgegevens (inzage), portalen voor het beheren van machtigingen en loketten voor het indienen van terugmeldingen en het beheren van abonnementen.

Uitwerking van eisen aan Interactie staan onder Algemeen.

### Niet-functionele eisen

Aan de componenten in de drie lagen voor Inzicht, Uitvoering en Ondersteuning, bestaan ook **niet-functionele eisen**. Deze benoemen we in algemene zin overkoepelend over de lagen en componenten.

<p class='note'>
Open vraag aan de reviewers: Welke niet-functionele eisen moeten opgenomen worden in deze Architectuurbeschrijving?
</p>


