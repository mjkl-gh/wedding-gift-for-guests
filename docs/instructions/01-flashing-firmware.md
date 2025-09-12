# De firmware flashen

## Flashen

Om de firmware naar de microcontroller te flashen moeten we de microcontroller via usb aansluiten op onze computer. Haal de microcontroller uit de verpakking en sluit hem direct aan op je computer zoals in onderstaande foto

![Hoe sluit je de usb aan](../img/flashing.jpg)

Het is hierbij belangrijk dat je de usb-c connector op de micro controller zelf gebruikt en niet die op het proto-board er onder.

Vervolgens ga je naar de [flash-pagina](../flash.md) en klik je op connect om te verbinden met de micro controller. Installeer dan de laatste versie van mjkl-gh.plant-waterer.

De firmware is gebaseert op esphome. Hierdoor is het supermakkelijk om een configuratie te schrijven en deze te compileren. Of om deze configuratie aan te passen. De configuratie van deze firmware vind je [hier](https://github.com/mjkl-gh/wedding-gift-for-guests/blob/main/firmware/plant-waterer.yaml)

## Verbinding maken met wifi

Nu de microcontroller geflasht is kan deze verbonnden worden met je wifi netwerk. Deze stap is optioneel, maar door dit te doen kan je onder andere updaten via wifi. De sensor waarden uitlezen en de pomp handmatig activeren.

Dit kan op meerdere manieren. Namelijk:

### Home assistant

 Voor mensen die al een [Home assistant](../about/home-assistant.md) installatie hebben met bluetooth proxy of de app gebruiken. Home assistant detecteert het nieuwe apparaat automatisch. Open de app en ga naar Settings->Integrations&Devices en hier zal een nieuw apparaat ontdekt zijn. Voeg dit apparaat toe (Home assistant zal om je wifi wachtwoord vragen) en alles zou moeten werken vanaf hier

### Improv serial

Als je op de[flash-pagina](../flash.md) nog verbonden bent of opnieuw verbind, zal de pagina automatisch detecteren dat het zogenaande "Improv serial" protocol actief is op de micro controller. Door op "Configure Wi-Fi" te klikken en het wifi netwerk en wachtwoord naar keuze in te vullen. Zal de micro-controller verbinding maken met het lokale wifi netwerk.

### Improv Ble

Een andere optie is het Improv bluetooth protocol te gebruiken. Door naar de [improv website](https://www.improv-wifi.com/) te gaan op een apparaat met bluetooth. Kan je de micro-controller verbinden met je wifi netwerk.

Klik op de grote knop "Connect device to wifi." Je apparaat zal nu via bluetooth scannen naar apparaten die het Improv Ble protocol ondersteunen. Zoals de zojuist geflashte microcontroller.  Je apparaat zal nu onder andere een apparaat vinden genaamt "plant-waterer-xxxx" waarbij xxxx staat voor een uniek id wat gegenereert is.

Klik op plant-waterer-xxxx en vul je wifi gegevens in om het te laten verbinden