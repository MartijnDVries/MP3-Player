Mp3-speler
====

De opdracht was om een mp3-speler te maken in Small Basic. Dit was een team opdracht en is \
met twee mensen gemaakt. De mp3-speler moest een aantal functies hebben zoals bijvoorbeeld het \
aanmaken van een playlist en het printen van deze playlist. 

Opdracht
----

* Mooie, nette GUI
* Een mp3-bestand kunnen afspelen, pauzeren en stoppen
* Voor- en achteruit kunnen bladeren
* Eenvoudig kunnen angeven in welke map zich de af te spelen mp3's zich bevinden
* Een lijst kunnen  printen met de aanwezige muziekbestanden in deze map
* Vastlegeen hoe vaak een nummer wordt afgespeeld in een top 10
* Top 10 kunnen afspelen
* Zelf een playlist kunnen samenstellen
* Een shuffle-functie
* Muziekbestanden importeren uit een specifieke folder
* Een nummer of een complete playlist verwijderen
* Volume regeling

Werkwijze
----

Taal: Small Basic\
Libraries: LitDev

=== Ontwerp ===

Eerst is de GUI ontworpen. De images die gebruikt zijn, zijn gemaakt in Word, omdat je hier mooie simpele vormen \
kan maken die te gebruiken zijn voor buttons. Deze images zijn vervolgens online gehost zodat het niet afhaneklijk \
is van een folder op een pc. \
Sommige buttons roepen over de layout van het scherm andere schermen op waarop bijvoorbeeld de nummers van een \
bepaalde playlist staan. Omdat het niet mogelijk is om lagen te maken in de layout moest hier een oplossing voor \
komen aangezien de mouseklikken afhanekelijk zijn van de x- en y-positie. Dit hebben we opgelost door wanneer er \
een scherm over het layout verschijnt deze te binden aan een letter met een waarde. Bijvoorbeeld wanneer het scherm \
verschijnt voor het naam invoeren van een nieuwe playlist dan c = 1. De rest van de buttons is zo geprogrammeerd dat \
wanneer c = 1 er niks gebeurt bij deze buttons. \

=== Muziek Afspelen ===

LitDev heeft een functie om de muziekfolder aan te roepen als de folder waar muziekbestanden vanuit kunnen worden \
afgespeeld. Er is voor gekozen om van deze functionaliteit gebruikt te maken om het simpel te houden. \
LitDev heeft ook de mogelijkheid om mp3-files af te spelen, te pauzeren of te stoppen. Deze hebben we ook gebruikt \
voor dit project. De functies zijn gebonden aan de images die deze functies representeren. \
Wanneer mp3-files worden aangeroepen uit de folder worden deze in een array gestopt. Daardoor \
kunnen we makkelijk voor en achteruit bladeren door de index + 1 of -1 aan te roepen en de huidige file te stoppen \
met afspelen. Shuffle is gemaakt door een random number generator een nummer te laten kiezen tussen 1 en het aantal \
files in de folder en deze vervolgens af te spelen. \
Door op de button musiclist te klikken verschijnt er een kader met daarin in een lijst met alle nummer die zich in \
de folder bevinden. Vanuit dit kader is het ook mogelijk om te navigeren en af te spelen door de pijltjes in dit \
kader te gebruiken. Wanneer je buiten het kader gebied gaat met de muis zal de kader weer verdwijnen. 

=== Playlists ===

De playlists kunnen worden aangemaakt en naam worden gegeven. Deze worden opgeslagen in "PlayData.txt". \
Door op de knop playlists te drukken verschijnt er een dropdown menuutje, met als laatste button "make a new playlist" \
Druk je hierop dan verschijnt er een scherm waarop je de gewenste naam van de playlist kan invoeren. \
Eenmaal de naam ingevoerd zal de playlist verschijnen in het dropdown menuutje. Hierop kan deze aangeklikt worden \
Door op de knop musiclist te drukken verschijnt er een lijst met de muziekfiles uit de muziekfolder. Afhaneklijk 
van het aantal playlists  dat is aangemaakt verschijnt onderaan deze lijst een aantal buttons gekoppeld aan deze playlists. \
Als de button  eenmaal wordt ingedrukt (wordt hij groen) en is het nummer toegevoed aan de playlist. Wordt de button \
nogmaals ingedrukt, dan wordt hij weer zwart en is het nummer uit de playlist verwijderd. De playlist is een aparte \
array, daardoor kunnen de shuffle functie en voor- en achteruit bladeren op dezelfde manier worden toegespast. \
Wanneer je in het dropdown menu op een playlist klikt zal deze verschijnen op de derde button op het hoofdscherm. \
En wanneer je hier met de linkermuisknop op klikt kan je het kader zien met de lijst van nummers die in deze playlist \
staan. Ook het afspelen en navigeren binnen de ze lijst is wederom mogelijk. Door op de rechtermuisknop op de playlist \
te klikken ontstaat er een optie om de playlist te verwijderen. Wanneer de playlist verwijdert wordt verdwijnt deze uit \
het drop-down menuutje. 

=== Top 10 ===

De opdracht was om een top 10 bij te houden. Wanneer er een nummer wordt afgespeeld, gaat er een timer lopen. Wanneer er \
vijf seconden verstreken is(tick), wordt het nummer in een array gestopt als deze nog niet in deze array zit, met daarachter een \
cijfer. Wanneer een nummer wordt afgespeeld die al wel in deze array zit, wordt er 1 bij dit cijfer opgeteld. Zo ontstaat er \
een array met de nummers die het vaakst worden afgespeeld. Door de 10  nummer weer te geven op het scherm is er zo een top 10 \
gecreëerd. Deze top 10 wordt dus live bijgehouden. Wat hiermee in het gedrang kwam was het afspelen van de nummer. Omdat er \
slechts 1 timer tegelijk kan lopen in Small Basic konden we niet de lengte van de nummers bepalen. Daarmee zouden we als het \
nummer afgelopen was automatisch door kunnen gaan naar het volgende nummer. Dit is dus niet het geval en er zal opnieuw op play \
moeten worden geklikt. 

=== Volume regeling ===

Ervoor gekozen om een slider te gebruiken als volume regeling. Relatie aan hoeveel pixels deze omhoog of omlaag gaat zal het \
volume aangepast worden. De functionaliteit wordt geregeld door een LitDev functie. De volume van windows wordt hiermee aangepast, \
een andere mogelijkheid was hier niet. 

=== Lijst printen === 

Rechtsonderaan het programmaatje is een print icon te vinden. Afhaneklijk van welke playlist is geselecteerd vanuit het drop- \
down menuutje zal deze playlist worden geprint (pdf in dit geval maar zou ook naar hardware kunnen).  Door de bestandslocatie \
en bestands naam van de files van de array (playlist of complete  muzieklijst) aan te roepen kan hiervan een lijst worden gemaakt.
De strings van deze lijst worden zo aangepast dat het deze indeling heeft: "Arties - Nummmer.mp3". 


Reflectie
----

Een belangrijk onderdeel van dit project was samenwerken. Alhoewel de initiele deadline niet gehaald is, heeft het project  \
nooit echt stil gelegen. Dit was meer een onderschatting van de groote het project.  \
De samenwerking zelf ging goed. Er was goed overleg en de taken waren verdeeld. Verder vind ik samenwerken leuk want je komt \
samen tot een resultaat waar je individueel nooit opgekomen zou zijn. \
Online was de taakverdeling te vinden op Trello \
Versiebeheer is bijgehouden in Github. 











