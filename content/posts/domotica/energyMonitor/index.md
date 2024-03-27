+++
title = "HomeAssistant-EnergyDashboard"
date = "2024-03-21T23:20:16+01:00"
author = "villo"
authorTwitter = "" #do not include @
cover = ""
tags = ["domotica", "zigbee", "hass"]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++

22:19 del 21/03/24

Finalmente nei giorni scorsi ho terminato la sostituzione del vecchio quadro elettrico con uno nuovo più grande
dove poter fare alloggiare il nuovo sensore/interuttore "intelligente" che andrà a pilotare il caricatore dell'auto elettrica (Dacia Spring) e il sensore di corrente a doppia pinza sempre zigbee.

I due prodotti sono questi:

| ![Fit Image](power1.jpg?fit=500x500)   | ![Fit Image](power2.jpg?fit=500x500)  |
| -------- | ------- |

Il sensore tuya di sinistra non è altro che un interruttore zigbee con misurazione della potenza istantanea, inoltre ha
alcune funzioni "intelligenti" di protezione con soglie programmabili, ad esempio può staccare il carico se superata una certa corrente o soglia di voltaggio, molto utile se si vuole prevenire danni.
Possiede inoltre un piccolo pulsante tattile sul fronte per attivare o disattivare il carico.

Il secondo sensore è solo un sensore di potenza istantanea misurata questa volta tramite pinza amperometrica che andrà posizionata sulla fase che ci interessa misurare facendo attenzione anche al verso col quale posizioniamo la pinza, perchè questi sensori forniscono non solo la potenza istantanea in Kw ma anche la *direzione* della corrente, in questo modo è possibile stabilire se il valore riportato è potenza prodotta per esempio dall'impianto fotovoltaico oppure potenza prelevata dalla rete.
Nel mio caso ho posizionato una pinza sulla fase subito dopo il contatore e l'altra sulla fase di ritorno dall'inverter fotovoltaico.

Dopo aver alimentato le due unità sono subito state riconosciute all interno di zigbee2mqtt e ho potuto fare i primi test proprio tramite la piattaforma zigbee2mqtt che permette di vedere i valori in tempo reale:
![Float Start](zigbee2mqttPower.png?fit=500x500) In questo caso i nomi dei due canali a e b non sono modificabile, sono istanze ancora all interno solo di zigbee2mqtt, le potremmo rinominare dentro a homeassistant.
In questo caso il canale A è collegato alla fase del contatore quindi misura sostanzialmente la corrente che prendo e quella che cedo alla rete. B invece è collegato alla fase dell'impianto fotovoltaico.

27/03/24
Una volta collegate le due pinze come detto, posso verificare immediatamente dentro a



