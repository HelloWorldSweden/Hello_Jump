
# För att skapa en ny värld / bana:

* Skapa en collection och ge den ett namn, typ: `"bana1.collection"`
* Gå in på main.collection och högerklicka på `"loader"`-objektet.
	- Välj `Add Component => Collection Proxy`
	- Tryck på den nyskapade `"Collection Proxy"`
	- Ändra id:t till något passande, t.ex. `"bana1"`
	- Tryck på knappen med 3 prickar `[...]` för att välja din collection.
* För att gå till den collection du vill, t.ex. `bana 1`, gör du såhär:
	- Från koden, kalla följande funktion:
```lua
msg.post("main:/loader", "ladda_värld", {till = "#namnet_på_din_collection_proxy"})
```

	- Klar!
