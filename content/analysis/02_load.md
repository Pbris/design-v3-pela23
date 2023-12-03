---
Title: Laddningstider
Description: En genomgång av tre webbplatsers laddningstid och användbarhet.
---


# Webbplatsers laddningstid och användbarhet
## En genomgång av tre webbplatser
*Detta är en rapport för en uppgift i kursen Design på BTH. Uppgiften går ut på att gå igenom tre webbplatser med avseende på deras laddningstid samt huruvida det finns förbättringsområden angående laddningstid och användbarhet.*
# Urval - valda webbplatser
Urvalet gjordes i en kategori webbplatser som identifierats som som personsidor av författarna.
I avgränsningen av tre webbplatser i kategorin valdes en amerikansk internationell kvinnlig artist, en svensk manlig skådespelare och regissör, samt en svensk kvinnlig f.d. idrottare.
Följande webbplatser undersöks, i ovan nämnda ordning:
* https://www.taylorswift.com/
* https://www.johanrheborg.se/
* https://charlotte-kalla.se/


# Metod
För att undersöka sidornas prestanda med avseende på laddningstider och användbarhet görs följande:
* Tar screenshot på webbplatsen.
* Gör mätningar av laddningstid, antal resurser som laddas samt sidans storlek med hjälp av Chrome DevTools samt Google Pagespeed [2].
** I Google PageSpeed görs tre mätningar i läget “Mobile” och “Desktop”. Genomsnittliga betyget för prestanda används. Betygen tolkas som bra om resultatet är över 90, medel / ok om resultatet är mellan 50 och 90, och dåligt om resultatet är under 50.
** I Chrome DevTools görs tre mätningar för inläsningstid, tiden det tar för DOM-content att laddas, totala sidans storlek samt antal resurser som laddas från webbplatsen. Cache inaktiveras för att få sidans totala storlek.
* För webbplatser med mer än en sida, testas tre sidor på samma sätt.
* Resultaten sammanställs i en tabell, och bifogas i rapporten som ett inbäddat kalkylark.
* För att ge förbättringsförslag på varje webbplats används Google PageSpeed Insights och mätningarna görs för mobil-läge. De 3 största förbättringsförslagen nämns i resultatet. Dessa mätningar görs bara en gång per sida då syftet främst är att få en fingervisning om hur webbplatsen kan förbättras.


Exempel från mätning av [johanrheborg.se](www.johanrheborg.se):


<figure>
<img src="%base_url%/image/laddningstider/dev_tools.png" title="Screenshot på Google Chrome's DevTools">
<figcaption>Figur 1: Resultat från en mätning av prestanda med avseende på nätverkstrafik och en webbplats rendering med hjälp av Google Chrome's DevTools</figcaption> 
</figure>


<figure>
<img src="%base_url%/image/laddningstider/page_speed.png" title="Page Speed mätning">
<figcaption>Figur 2: Page Speed mätning från Google Page Speed som visar på en webbplats prestanda.
Hämtad från [1]</figcaption> 
</figure>


# Resultat
Resultatet av mätningarna framgår av det inbäddade kalylarket nedan. Det ska poängteras att sidorna för Taylor Swift och Charlotte Kalla enbart består av en sida, det har alltså inte varit möjligt att mäta tre sidor på dessa, utan endas startsidan har mäts.


<iframe class='aspect-ratio-16-9' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTDd8MHKqMECdiXQafknjgWjQW27wB-s9Nz7d-72J1gxAtzN4CRHrWgcUrzxESe3jjY29npFF-AvGkS/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>


## Taylor Swift
<figure>
<img src="%base_url%/image/laddningstider/taylor_swift.png" title="Taylor Swifts webbplats, skärmavbild från slutet av november 2023">
<figcaption>Figur 3: TaylorSwift.com [2]</figcaption> 
</figure>


Stor webbplats med mycket rörlig media som tar lång tid att ladda in och överför mycket data. En sida som innehåller allt. Riktigt låga betyg i mobil-mätningen. De största förbättringsområdena som identifierats med hjälp av PageSpeed insights är att använda bättre format på bilderna (11.3 s) (serve image in next-gen formats), att använda rätt storlek på bilderna (11.2 s) (proberly size images) och att ta bort oanvänd JavaScript (7.1 s) (reduce unused JavaScript).


## Johan Rheborg
<figure>
<img src="%base_url%/image/laddningstider/johan_rheborg.png" title="Johan Rheborgs webbplats, skärmavbild från slutet av november 2023">
<figcaption>Figur 4: JohanRheborg.se [3]</figcaption> 
</figure>


Överlag en mindre webbplats, med närapå ok betyg i de olika mätningarna. Fotografi-sidan sticker ut med hela 122 mb som laddas in automatiskt, där finns 12 fotografier som är större än 4 MB, varav 5 är större än 7 MB. De största förbättringsområdena som identifierats med hjälp av PageSpeed insights för foto-sidan är att använda bättre format på bilderna (476.7 s) (serve image in next-gen formats), att komprimera bilderna mer effektivt utan att tappa kvalitet (414.8s) (efficiently encode images) och  att använda rätt storlek på bilderna (15.4s) (properly size images).  För själva startsidan, är förbättringsområdena att använda bättre format på bilderna (6.9s) (serve image in next-gen formats), att komprimera bilderna mer effektivt utan att tappa kvalitet (2.4s) (efficiently encode images) och att ta bort resurser som hindrar sidan från att laddas (1.07s) (eliminate render-blocking resources).


## Charlotte Kalla
<figure>
<img src="%base_url%/image/laddningstider/charlotte_kalla.png" title="Charlotte Kallas webbplats, skärmavbild från slutet av november 2023">
<figcaption>Figur 5: CharlotteKalla.se [4]</figcaption> 
</figure>


En sida som leverar allt i ett, dvs. finns bara en sida. Betyg som spretar mellan mobil och desktop. Indikeras som ok och dåligt, beroende på användarens enhet. De största förbättringsområdena som identifierats med hjälp av PageSpeed insights är att använda bättre format på bilderna (7.9 s) (serve image in next-gen formats), att använda rätt storlek på bilderna (5.2s) (properly size images) och  att komprimera bilderna mer effektivt utan att tappa kvalitet (2.6s) (efficiently encode images). 


# Analys
Av de fyra URL:er som granskades för förbättringsförslag och där laddningstider och prestanda mättes visas en sammanfattning i tabellen nedan. I tabellen kan vi se att webbplatserna har många gemensamma förbättringsområden, framför allt att alla skulle behöva jobba med sina bilder, och då framför allt att gå över till modernare bildformat såsom webp och att leverera rätt storlek på bilderna.


| Kategori | Charlotte Kalla | Johan Rheborg 1 | Johan Rheborg 2 | Taylor Swift | Summa  |
|----------|-----------------|-----------------|-----------------|--------------|--------|
| Serve image in next-gen formats | 7.9 s | 6.9 s | 476.7 s | 11.3 s | 502.8 s |
| Properly size images | 5.2 s | - | 15.4 s | 11.2 s | 31.8 s |
| Reduce unused JavaScript | - | - | - | 7.1 s | 7.1 s |
| Efficiently encode images | 2.6 s | 2.4 s | 414.8 s | 7.1 s | 426.9 s |
| Eliminate render-blocking resources | - | 1.07 s | - | - | 1.07 s |




# Referenser
* [1] (2023, November 28). Google Pagespeed [Online]. Tillgänglig: https://pagespeed.web.dev/
* [2] (2023, November 28). Taylor Swift [Online]. Tillgänglig: https://www.taylorswift.com/
* [3] (2023, November 28). Johan Rheborg [Online]. Tillgänglig: https://www.johanrheborg.se/
* [4] (2023, November 28). Charlotte Kalla [Online]. Tillgänglig: https://charlotte-kalla.se/


## Övrigt
Författare: Peter L,
Karl W
