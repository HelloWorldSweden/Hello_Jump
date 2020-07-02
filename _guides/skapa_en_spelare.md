# Skapa en spelare

### Skapa spelarobjektet med script

<img src="./media/skapa_en_spelare/media/image13.png" style="width:1.98116in;height:1.90104in" />

1.  Skapa en mapp objects som ska ha era Game Objects och deras scripts i sig

2.  I mappen, skapa ett Game Objects: spelare

3.  Skapa även ett spelare.script i samma mapp

###  Lägg till spelarbilden i b.atlas (i mappen /grafik) och skapa en sprite<img src="./media/skapa_en_spelare/media/image8.png" style="width:2.77773in;height:1.32813in" /><img src="./media/skapa_en_spelare/media/image9.png" style="width:1.5191in;height:0.98438in" />

4\. Gå till b.atlas i grafik-mappen

5\. I Outline högerklicka på Atlas och välj “Add Images”  
  
  
6. Om ni inte lagt upp en egen bild i /grafik/bilder sök på “alien” och välj en alien med kul färg.<img src="./media/skapa_en_spelare/media/image6.png" style="width:1.52083in;height:1.65226in" /><img src="./media/skapa_en_spelare/media/image11.png" style="width:2.08854in;height:1.1494in" />

7\. Nu ska er atlas se ut såhär

<img src="./media/skapa_en_spelare/media/image2.png" style="width:1.70313in;height:1.88535in" />

8\. Nu välj spelare.go i /objects och högerklicka på Game Objects, välj Add Component och skapa en ny sprite. Sett dess Image till b.atlas och dess DefaultAnimation till bilden ni la in ovan

### Lägg till collisionobjects<img src="./media/skapa_en_spelare/media/image12.png" style="width:2.02604in;height:0.84309in" /><img src="./media/skapa_en_spelare/media/image5.png" style="width:1.94271in;height:2.2731in" />

9\. Lägg till ett collisionobject

10\. Sätt typen till Kinematic

11\. Sätt grupp till **spelare**

12\. Sätt mask till **geometri  
**- **viktigt**: ‘geometri’ är fördefinierat i fysik.script

<img src="./media/skapa_en_spelare/media/image4.png" style="width:1.24479in;height:1.57293in" /><img src="./media/skapa_en_spelare/media/image1.png" style="width:1.60938in;height:1.49233in" />

13\. Lägg till en box-shape till din collisionobject

14\. Placera boxen vid spritens fötter

### Lägg till alla scripts som behövs

<img src="./media/skapa_en_spelare/media/image3.png" style="width:1.76889in;height:2.05729in" /><img src="./media/skapa_en_spelare/media/image7.png" style="width:1.80198in;height:1.84547in" />

15\. Gör följande för:  
spelare.script

fysik.script

sensor.script

15.1 Välj Add Component File

15.2 Välj scriptet

### Lägg in spelaren i start.collection i /main - mappen

<img src="./media/skapa_en_spelare/media/image10.png" style="width:3.32589in;height:1.48438in" />
