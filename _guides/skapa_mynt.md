
# Skapa mynt

<u>Nivå</u>: Deltagare ska ha gått Defold 3 (Spelstudio By King)

Vad bra att du har kommit såhär långt. Nu ska vi skapa lite mynt som gör spelet lite mer interaktivt.

### Genomförande

<table><thead><tr class="header"><th><ul><li><blockquote><p>Vi har redan fixat så att det finns massor utav bilder på mynt som roterar. Du finner dom i <strong>graphics</strong> coin.atlas</p></blockquote></li><li><blockquote><p>Men nu ska vi skapa själva objekten som behövs.</p></blockquote><ul><li><blockquote><p>Börja med att skapa en mapp i object mappen namnge mappen: <strong>coin</strong> i mappen ska det finns två saker: coin.go och coin.script</p></blockquote></li></ul></li></ul><h2 id="myntet">Myntet</h2><h4 id="coin.go">coin.go</h4><ul><li><blockquote><p>Lägg till scriptet i game objectet</p></blockquote></li><li><blockquote><p>Lägg till en sprite</p></blockquote><ul><li><blockquote><p>Lägg till coin.atlas</p></blockquote><ul><li><blockquote><p>Välj coins animationen</p></blockquote></li></ul></li></ul></li><li><blockquote><p>Skapa ett kollisions object</p></blockquote><ul><li><blockquote><p>Lägg till en form på den, välj formen <strong>box</strong> och skala den så att den passar in på objektet</p></blockquote></li><li><blockquote><p>Ändra på mask och group</p></blockquote><ul><li><blockquote><p>Group: coin</p></blockquote></li><li><blockquote><p>Mask: player</p></blockquote></li></ul></li></ul></li></ul><h4 id="coin.script">coin.script</h4><ul><li><blockquote><p>När vi har våra mynt så vill vi att dom ska raderas när dom inte längre kan plockas upp av oss.</p></blockquote></li><li><blockquote><p>Börja med att plocka bort alla funktioner förutom <strong>function update()</strong> och <strong>function on_message()</strong></p></blockquote><ul><li><blockquote><p>i vår update vill vi kolla om myntet har ändrat på sin y position tillräckligt för att raderas. Vi får kolla om y position är mer än -500.</p></blockquote></li></ul></li></ul><blockquote><p><img src="./media/skapa_mynt/media/image8.png" style="width:5.08333in;height:1.21875in" /></p></blockquote><ul><li><blockquote><p>Okej nu raderas våra mynt när dom kommer till en viss position. Men inget händer om vi kolliderar med dom.</p></blockquote><ul><li><blockquote><p>i <strong>on_message</strong> kan vi kolla om vi kolliderar med något, i detta fall vill vi att om vi kolliderar med spelaren raderas och skapa poäng. (vi kommer till poängen senare)</p></blockquote></li><li><blockquote><p>Börja med att kolla efter en kollision</p></blockquote><ul><li><blockquote><p>Sedan kolla vad vi kollar med och jämför med vad vi vill kollidera med. alltså <strong>player</strong></p></blockquote><ul><li><blockquote><p>hint. Du jämför kollisions gruppen mellan 2 objekt med <strong>message.other_group</strong></p></blockquote></li><li><blockquote><p>Sedan är det bara att radera myntet för tillfället.</p></blockquote></li></ul></li><li><blockquote><p><img src="./media/skapa_mynt/media/image3.png" style="width:4.82292in;height:1.39063in" /></p></blockquote></li></ul></li></ul></li><li><blockquote><p>Testa att starta spelet, inga mynt dyker upp….</p></blockquote></li></ul><h4 id="factory.script">factory.script </h4><p>Skapa en ny funktion och namnge den create_coin()</p><ul><li><blockquote><p>Vi måste hämta positionen till vår fabrik att skapa mynten på.</p></blockquote><ul><li><blockquote><p>skapa en lokal variabel fö positionen i funktionen</p></blockquote><ul><li><blockquote><p>vi använder oss utav vmath.vector3(0, 0, 0) som innehåll i variabeln</p></blockquote></li></ul></li><li><blockquote><p>Vi måste även kolla på dom olika koordinataxlarna x, y och z.</p></blockquote><ul><li><blockquote><p>Eftersom att vi utvecklar ett 2D spel så behöver vi inte riktigt tänka på z axeln så mycket men x och y är våra viktigaste komponenter.</p></blockquote></li></ul></li><li><blockquote><p>hämta positionen av x axeln och säg att den är random mellan 35, 500 - 35</p></blockquote><ul><li><blockquote><p>math.random(35, 500 - 35)</p></blockquote></li></ul></li><li><blockquote><p>hämta också y positionen och säg att vi vill ha den vid latest_platforms y pos och att vi kör en random mellan 130, 150</p></blockquote><ul><li><blockquote><p><img src="./media/skapa_mynt/media/image1.png" style="width:4.77604in;height:0.20833in" /></p></blockquote></li></ul></li><li><blockquote><p>Nu ska vi skapa våra mynt.</p></blockquote><ul><li><blockquote><p>lägg till en factory.create() i den kommer vi skriva dom parametrana som saknas.</p></blockquote></li><li><blockquote><p><strong>factory.create(url, [position], [rotation], [properties], [scale])</strong></p></blockquote></li><li><blockquote><p>Vi har inte skapat vår fabrik ännu, men den kommer att heta <strong>coin_factory</strong></p></blockquote></li><li><blockquote><p>Nu ska vi ange vår position, skriv in variabel namnet för positionen som den andra parametern.</p></blockquote></li><li><blockquote><p>Det räcker nu för tillfället.<img src="./media/skapa_mynt/media/image6.png" style="width:6.375in;height:1.33333in" /></p></blockquote></li></ul></li></ul></li></ul><ul><li><blockquote><p>Nu är vi nästan klara</p></blockquote></li></ul><h4 id="factory.go">factory.go</h4><ul><li><blockquote><p>Lägg till en fabrik i game objektet.</p></blockquote><ul><li><blockquote><p>Id:et på fabriken ska vara <strong>coin_factory</strong></p></blockquote></li></ul></li></ul><p>Testa nu att starta spelet….</p><p>Vilka gigantiska mynt. Vi får ändra lite i vår kod för att ändra på skalan.</p><p>öppna factory.script igen. Gå ner till vår factory.create() där ska vi skriva lite till.</p><p><img src="./media/skapa_mynt/media/image5.png" style="width:6.375in;height:0.34722in" /></p><p>Vi måste lägga till skala, den är den 5:e parametern i factory create så vi säger att den ska ha. Först säger vi att vår rotations ska vara nil</p><ul><li><blockquote><p>Odentifierat tal eller saknar värde.</p></blockquote></li></ul><p>sedan säger vi att vi har en table</p><ul><li><blockquote><p>.</p></blockquote></li></ul><p>Nu skalan, du ändrar på den via att berätta vilka 3 axlar som ska ändras.</p><p>skriv då vmath.vector3(x, y, z) kolla bilden ovan så finner du siffrorna som du ska använda.</p><h2 id="gui">GUI</h2><p>Vi ska nu skapa GUI som har med myntet att göra. När vi är klara ska vi kunna få poäng kolla bilden</p><p><img src="./media/skapa_mynt/media/image2.jpg" style="width:1.69792in;height:1.07292in" /></p><h4 id="points.gui">points.gui</h4><p>Nu är det dags att skapa lite synlig text på skärmen så att vi vet hur många mynt vi har samlat.</p><p>Börja med att öppna guin där ‘ven våra poäng för höjden vi har kommit finns.</p><p>Lägg till en textur, du gör det genom att högertrycka på Textur mappen och välja en atlas. I detta fall så ska vi använda oss utav <strong>coin.atlas</strong></p><p><img src="./media/skapa_mynt/media/image4.png" style="width:2.8125in;height:0.58333in" /></p><p>För att vi ska kunna ha den i vårt spel och även att den ska kunna rotera så väljer vi att lägga till en nod</p><ul><li><blockquote><p>Högerklicka på Nodes</p></blockquote><ul><li><blockquote><p>välj först en box</p></blockquote><ul><li><blockquote><p>Den är till för vårt mynt.</p></blockquote><ul><li><blockquote><p>Flytta den nu till en bra position, vår ligger på X:396 Y: 702 Z: 0</p></blockquote></li></ul></li><li><blockquote><p>sätt en bra skala på den så att den får plats på skärmen och inte tar alldeles för mycket plats.</p></blockquote></li></ul></li><li><blockquote><p>Välj en text nod</p></blockquote><ul><li><blockquote><p>Denna är till för att visa “X” mellan bilden och våra coins.</p></blockquote><ul><li><blockquote><p>välj fonten som redan är inlaggd, kalas.</p></blockquote></li><li><blockquote><p>Skriv “X” i text rutan</p></blockquote></li><li><blockquote><p>Placera den bra, ex på position: X: 425 Y: 702 Z:0</p></blockquote></li></ul></li></ul></li><li><blockquote><p>Välj nu en till text nod</p></blockquote><ul><li><blockquote><p>Detta ska vara våran nod för att kunna räkna mynten.</p></blockquote></li><li><blockquote><p>ge den id:et - <strong>coin</strong></p></blockquote></li><li><blockquote><p>och sätt texten till 0 med en font.</p></blockquote></li></ul></li></ul></li><li><blockquote><p>Nu är vi klara i points.gui det borde se likande ut till denna:</p></blockquote></li><li><blockquote><p><img src="./media/skapa_mynt/media/image11.png" style="width:4.90104in;height:2.69792in" /></p></blockquote></li></ul><h4 id="points.gui_script">points.gui_script</h4><p>Nu ska vi skriva vår kod för att kunna få våra poäng.</p><p>Börja med att öppna points.gui_scriptet, där finner vi koden för själva nuvarande poängen och nu vill vi lägga till så att vi ändrar på coin noden.</p><ul><li><blockquote><p>Skapa en variablen som heter <strong>coins</strong> och ge den värdet 0 (coins = 0)</p></blockquote></li><li><blockquote><p>nu ska vi skapa en elseif sats för att kolla om meddelandet inte är “y_position” och istället “add_points”</p></blockquote><ul><li><blockquote><p>Vi kollar då om meddelandet är add points då ska vi lägga till ett mynt i vår variabel</p></blockquote><ul><li><blockquote><p>säg nu att coins är en mer än innan</p></blockquote><ul><li><blockquote><p>coins = coins + 1</p></blockquote></li></ul></li><li><blockquote><p>sedan måste vi hämta vår nod som vi ska visar sig.</p></blockquote><ul><li><blockquote><p>vi skrover därför att coin_node = gui.get_node(‘coin’) - OBS viktigt att denna stämmer överns med idet vi gav i points.gui annars kommer det inte att fungera.</p></blockquote></li></ul></li><li><blockquote><p>Det som är kvar att göra då är att sätta till den nya texten. Genom att använda gui.set_text(node, variabel) - OBS är endast exempel byt ut till rätt info</p></blockquote><ul><li><blockquote><p>kolla bilden så att det stämmer</p></blockquote></li></ul></li><li><blockquote><p><img src="./media/skapa_mynt/media/image10.png" style="width:4.63542in;height:2.99653in" /></p></blockquote></li></ul></li></ul></li></ul><ul><li><blockquote><p>Testa starta spelet, fungerar det?.....</p></blockquote><ul><li><blockquote><p>Vad kan vi ha glömt för något??</p></blockquote></li></ul></li></ul><ul><li><blockquote><p>Juste den får aldrig något meddelande om att lägga till points, öppna coin scriptet och skicka ett meddelande till vår GUI</p></blockquote><ul><li><blockquote><p><img src="./media/skapa_mynt/media/image9.png" style="width:4.88542in;height:2.04167in" /></p></blockquote></li><li><blockquote><p>function on message borde se ut såhär.</p></blockquote></li></ul></li><li><blockquote><p>Testa nu, fungerar det!</p></blockquote></li></ul><p>Ja! Bra jobbat! :) Det finns fler uppgifter som väntar, gör dom också och spelet kommer bli så coolt!</p></th></tr></thead><tbody><tr class="odd"><td></td></tr></tbody></table>

### Tips och trix

### Bilagor

-   Här finns en API med alla olika funktioner som spåret använder

    -   [<u>Defold/Lua API</u>](https://docs.google.com/document/d/1wNVHVbsEygRJ8ERMSRVUesvpo4vXKPuyI4MQwbsIepc/edit#heading=h.76i2mcbfv8w4)

### 