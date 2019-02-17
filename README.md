<head>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>
**ESP8266 gateway The Things Network**
Ontwerp door de Haagse Makers. Openen JSON met <a href="http://easyeda.com" target="_blank">EasyEDA</a><br>
<br>
<h2><a href="https://www.tindie.com/products/VliegendeVogel/lora-gateway-ttn-for-beginners-esp8266/" target="_blank">BUY HERE</a> from tindie.com</h2>
<br>
<img src="https://github.com/pappavis/ESP8266-single-channel-lora-gateway/blob/master/plaatjes/IMG_6180%20Haagse%20Makers%20gateway_klein.jpg?raw=true" width="70%" height="70%">
<br><br>
<h1>**Setup Stappenplan**;</h1>
1. Download en Installeer GIThub client.<br>
2. Installeer Arduino IDE & ESP8266 boards.<br>
3. Open GIT Shell, en doen git clone https://github.com/things4u/ESP-1ch-Gateway-v5.0<br>
4. Open windows verkenner, kopieer de libs in de gedownload map naar &lt;Documents&gt;/Arduino/libraries<br>
5. Start ArduinoIDE, en open ESP-sc-gway.ino<br>
6. Kies tabblad ESP-sc-gway.h<br>
7. zoeken naar "fire", "water"<br>
8. Vervang fire met jouw WiFi naam, en water met jouw WiFi wachtwoord.<br>
<br>
Iets zoals dit:-<br>
<br>
wpas wpa[] = {<br>
	  { "" , "" },							// Reserved for WiFi Manager<br>
	  { "Volksrepubliek", "e1gen@volk@3igenland!!" },<br>
	  { "ape", "beer" }<br>
};<br>
<br>
9. Aansluiten gateway (incl wemos uiteraard!!) op jouw peecee, en kies in ArduinoIDE de jusite COM-poort.<br>
10. Upload naar arduino.<br>
11. Na upload, open debugscherm<br>
12. Druk resetknop op de wemos.<br>
13. Hij zou nu direct met WiFi moeten verbinden.<br>
<br>
en je ziet iets als deze:<br>
<br>
Host esp8266-66d093 WiFi Connected to MyWiFiNetwork on IP=192.168.2.82<br>
Local UDP port=1700<br>
Connection successful<br>
Gateway ID: 807D3AFFFFA7D093, Listening at SF9 on 868.10 Mhz.<br>
<br>
14. Open http://console.thethingsnetwork.org + maak een account als je die nog niet heb.<br>
15. Kies optie Register gateway, zet dan vinkje bij Legacy gateway.<br>
16. Invullen bovenvermelde gateway ID, plus optionle info zoals locatie en soort gateway.<br>
17. Opslaan. Je zou een connceted tekstje moeten zien.<br>
<br>
<img src="https://github.com/pappavis/ESP8266-single-channel-lora-gateway/blob/master/plaatjes/The_Things_Network_Console20190217.jpg?raw=true" title="The things network console">
<br>
Je gateway is nu online!!<br>
<br>
