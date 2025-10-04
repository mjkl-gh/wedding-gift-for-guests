# Testen en Afstellen

Nu alle onderdelen in elkaar zitten kunnen we de opstelling gaan testen en uiteindelijk gaan afstellen.

!!!! warning
    Het werkt het beste als je de instructies voor het testen eerst volledig doorleest. En dan pas de stappen uitvoert

## Testen

Als je dat nog niet gedaan had, kan je nu het schuifje op de batterijhouder omzetten. De ESP32 zou nu tot leven moeten komen. Als tijdens het flashen alles is goed gegaan, verbind hij met je wifi netwerk en is het dashboard bereikbaar. Er is een zeer goede kans dat vrij snel na het opstarten het pompje begint te pompen. Deze zal kort pompen en dan een periode wachten. Dan zal hij weer pompen en wachten, etc etc. Dit hoort en komt omdat de sensor droog is. Als dit gebeurt kan je beter eerst de batterij weer uitzetten en een schaaltje water halen.

Leg vervolgens de sensor in het schaaltje water, maar NIET de pomp. Dit is om te voorkomen dat de pomp aan gaat terwijl we eerst wat andere dingen testen. Zet nu het schuifje weer aan. De pomp zal als het goed is niet starten. Start hij wel let dan goed op het kleine printplaatje tussen de sensor en de micro controller. Hier zit een potmeter op (blauw met wit) en een ledje. Als het ledje brand dan is, ondanks het water, de sensor nog steeds te droog. Dat klopt natuurlijk niet. We kunnen de sensor inregelen door met een kruiskopschroevendraaier de potmeter te verdraaien. Rechtsom maakt hem gevoeliger. Linksom, minder gevoelig. Draai de potmeter naar links tot het ledje uitgaat. De sensor is nu niet meer hoog

Nu de pomp niet meer draait. Kunnen we het dashboard bezoeken. Bezoek het adres uit de [programmeren](01-flashing-firmware.md) stap.

Weet je die niet meer? Je kan ook de batterij loskoppelen. Dit is erg belangrijk om schade aan je laptop te voorkomen! En dan microcontroller met usb met je laptop te verbinden. Als je vervolgens op de [flash](../flash.md) pagina op `connect` klikt kan je voor `Logs` kiezen en dan zal je de logs te zien krijgen. Klik vervolgens `Reset device` en het apparaat zal opnieuw opstarten, Tussen de logging komen de wifi instellingen te staan. 1 hiervan is het "ip adres". Als je deze in de browserbalk intikt zal je naar het dashboard gaan.

Of zie de [programmeren](01-flashing-firmware.md) stap voor de andere mogelijkheden.

## Afstellen

Zoals je ondertussen misschien gemerkt hebt reageert het pompje op de vochtigheid van de sensor. Draai eerst de sensor naar minst gevoelig. Maak de sensor eerst helemaal droog en draai dan totdat het lampje uitgaat. Draai dan terug zodat het lampje net aan is gegaan. De sensor is nu afgesteld om de plant helemaal droog te houden.

Nu kan je de sensor in de plant plaatsen. Stop ook het slangetje bij de plant. Zorg dat deze goed vastgeklemd zit. Je kan hier de bonus [druppelaar](../bonus/dripper.md) voor gebruiken. Kijk ook bij de andere bonus dingen voor inspiratie! Als de pomp losschiet kan hij namelijk water op plaatsen dumpen waar dat niet gewenst is. Het beste werkt als de slang tot de bodem van de pot in de grond zit, als je de druppelaar niet gebruikt

Hang nu de pomp in een waterreservoir. Bijvoorbeeld een bierblikje. Je kan een blikopener gebruiken om het bierblikje te openen en vervolgens de pomp hierin te laten zakken. Zorg dat het gedeelte met de krimpkous boven water blijft. Bijvoorbeeld met wat tape. De rest kan prima onder water.

Je kan de plant nu water geven door de sensor iets gevoeliger te maken. Draai de potmeter totdat het lampje (en de pomp) weer aanspringt. De pomp zal nu een aantal pompcyclussen uitvoeren. Tot de plant nat genoeg is. Laat het water intrekken, en controleer later weer. Bijvoorbeeld de volgende dag.

Doordat de pomp de plant nu op een constant waterniveau houdt, is het makkelijk teveel of te weinig water te geven. Laat de pomp zijn werk doen voor een langer tijdsbestek. Blijft de grond erg droog, en krijgt de plant zichtbaar te weinig water? schroef dan elke dag de potmeter ietsje op zodat de pomp vaker en meer water geeft. Als de plant het erg zwaar heeft, kan je ook even tijdelijk handmatig bewateren terwijl je het proces verder inregelt. Via het dashboard kan je de pomp handmatig activeren. Of kan je natuurlijk een handgieter gebruiken.

Het dashboard heeft ook een analoge vochtigheidsmeter. Weet je de juiste theoretische vochtigheid voor jouw plant? Dan kan je die gebruiken om het systeem sneller in te regelen. Let er wel op dat de meter de huidige waarde aangeeft, en niet de gemiddelde waarde. Het uiteindelijke gemiddelde kan dus lager (of hoger) liggen, en dat is waar je plant vooral om zal geven.

## Troubleshooting

!!! Question "Verbind de esp32 niet meer met wifi?"
    Bezoek de [programmeer](01-flashing-firmware.md) pagina en flash de esp32 opnieuw. Doorloop alle stappen om met wifi verbinding te maken daarna


