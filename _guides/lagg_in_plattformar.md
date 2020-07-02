### 

### Skapa plattformsobjektet med sprite<img src="./media/lagg_in_plattformar/media/image7.png" style="width:2.02018in;height:0.55729in" />

1\. Skapa ett gameobject plattform.go i objects

2\. Skapa en sprite och sätt dess Image och Default <img src="./media/lagg_in_plattformar/media/image2.png" style="width:1.45313in;height:0.69072in" />

Animation i properties enl. bilden nedan<img src="./media/lagg_in_plattformar/media/image6.png" style="width:4.61979in;height:0.60625in" />

Spriten är uppochned så sätt dess rotation runt z-axeln till 180 (grader) i dess properties  
  
  
  
<img src="./media/lagg_in_plattformar/media/image5.png" style="width:4.01976in;height:0.26042in" /><img src="./media/lagg_in_plattformar/media/image1.png" style="width:1.57813in;height:1.28678in" />

### Lägg till ett collisionobject

<img src="./media/lagg_in_plattformar/media/image8.png" style="width:1.40104in;height:2.06036in" />

Sätt Type till kinematic  
  
Group: **geometri** (viktigt: bestäms av spelarens fysik.script)

<img src="./media/lagg_in_plattformar/media/image4.png" style="width:2.40776in;height:1.44271in" />

Mask: spelare

Lägg till en box-shape och placera boxen på spriten

### Skapa världen i start.collection

<img src="./media/lagg_in_plattformar/media/image3.png" style="width:2.08944in;height:1.69271in" />

I start.collection högerklicka på Collection och Add Game Object, sätt id till världen, lägg in din plattform i världen<img src="./media/lagg_in_plattformar/media/image9.png" style="width:2.86557in;height:1.16146in" />
