## Skapa fiende<img src="./media/skapa_fiende/media/image5.png" style="width:2.2066in;height:0.64063in" />

Skapa fiendeobjektet, lägg på sprite och collisionobject

Sätt group till ‘fiende’ och mask till ‘spelare,geometri’

Fäst fysik-scriptet på fiendeobjektet. Sätt type till ‘kinematic’.

<img src="./media/skapa_fiende/media/image6.png" style="width:2.56771in;height:1.11355in" />

Skapa fiende.script och fäst det på fiendeobjektet, i fiende.script, skriv update-funktionen och gör så att fienden rör sig åt vänster

i fabrik.script, lägg till en variabel monster time som kollar om ett monster ska komma. I update, minska monster time med dt.<img src="./media/skapa_fiende/media/image4.png" style="width:3.34896in;height:0.97869in" />

<img src="./media/skapa_fiende/media/image3.png" style="width:6.27083in;height:1.22222in" />

Efter att vi skapat en plattform, kolla om det är dags att skapa ett monster

<img src="./media/skapa_fiende/media/image1.png" style="width:2.4982in;height:1.11458in" />

Lägg till fienden på plattformen och spelarens kollisionsobjekt

<img src="./media/skapa_fiende/media/image2.png" style="width:3.57813in;height:1.20658in" />

Uppdatera on_message i spelare-scriptet så att spelaren dör om man nuddar ett monster

(detta kan senare bytas ut mot att vi laddar gameover.collection eller startar om spelet)
