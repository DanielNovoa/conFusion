conFusion - total conFusion put into code
=========================================

Installation
-----------------------------------------

* Hämta hem ramverket via git clone https://github.com/DanielNovoa/conFusion.git`
* Konfigurera .htaccess
  Editera .htaccess och byt ut webbadressen för RewriteBase till din installations url
  Om RewriteBase ej behövs på din webbserver kan du enkelt inaktivera det genom att sätta ett `#` framför
* Ladda upp ramverket till din webbserver
* Sätt chmod 777 på katalogen `site/data`
* För att initiera databasen, peka webbläsaren på följande underkatalog `module/install`


Personifiera/anpassa conFusion
-----------------------------------------

### Logotyp
För att byta ut logotypen byter du ut filen `logo_80x80.png` till valfri bild med måttet 80x80 pixlar
Bilden hittar du i följande undermapp `site\themes\mytheme`


### Titel
För att byta tilel på ramverket editerar du följande fil `site/config.php`
Längst ner finner du ett kodstycke innehållande 'header' och 'slogan'
Byt ut 'conFusion' och 'Total conFusion put into code' till valfri titel och slogan


### Navigeringsmenyn
För att anpassa navigeringsmenyn editerar du följande fil `site/config.php`
Leta reda på koden `$ly->config['menus']`
Här hittar du huvumenyns länkas som är uppbyggda på följande sätt
`'namn' => array('label'=>'titel', 'url'=>'funktion'),`
`namn` är din valfriga beskrivning av länken och kommer ej vara synlig för dina besökare
`titel` är den text som kommer synas i navigeringsmenyn, tex Blogg
`funktion` är den funktion som kommer anropas, tex blog


### Footern
För att anpassa footern editerar du följande fil `site/config.php`
Längst ner i koden hittar du följande `'footer' => '<p>conFusion &copy; by Daniel Novoa</p>',`
Byt ut texten `conFusion &copy; by Daniel Novoa` till valfritt innehåll

### Anpassa ramverkets utséende (färger, teckensnitt mm)
Gå till `site\themes\mytheme` och editer filen `style.css`
Här kan du lägga in egen "styling" enligt CSS (http://en.wikipedia.org/wiki/Cascading_Style_Sheets)


Komma igång med innehåll
-----------------------------------------

När initierade databasen, som en del av installationen, skapades några exempelposter
Du kan kika på dessa för att få en uppfattning om vilka funktioner som finns i bloggen
Bloggverktyget kan tex användas både för att skapa blogg-poster (post) och statiska sidor (page)
Du kan även anrop olika filter såsom bbcode (http://en.wikipedia.org/wiki/BBCode) och htmlpurifier (http://htmlpurifier.org)

### Skapa en blogg
För att skapa en blogg pekar du din webbläsare på följande undermapp `/content`
Skriv in rubrik, key (detsamma som slug: http://en.wikipedia.org/wiki/Clean_URL#Slug) och content
Ange Type som `post`

### Skapa en sida
Samma som för ovan, men ange Type som `page`

### Filter
Tillgängliga filter är:
plain - vanlig text
bbcode - när du använder bbcode i texten
htmlpurify - när du använder html-taggar i texten






