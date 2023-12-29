+++
title = "Zigbee"
date = "2023-12-29T14:29:16+01:00"
author = "villo"
authorTwitter = "" #do not include @
cover = ""
tags = ["domotica", "zigbee"]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++
15:12
Il protocollo Zigbee si differenzia dal normale protocollo wifi usato per esempio dai dispositivi Shelly in diversi aspetti, diciamo che di base con la tecnologia usata da shelly condivide solo la banda di frequenza utilizzata dei 2.4Ghz, del resto il sistema zigbee *per trasferimento di piccoli pacchetti di dati* è molto più efficente, di seguito alcune funzionalità:

- utilizzano un gateway per comunicare con il server, il che ha diversi pro, infatti il gateway può essere messo in diverse zone anche non per forza vicino al router wi-fi
- la trasmissione dei pacchetti avviene solo in funzione della necessità di comunicare uno stato(sensore) e quindi riduce l'inquinamento radio
- la funzione veramente più incredibile è quella della rete mesh, in pratica ipotizziamo di avere 3 dispositivi zigbee + il gateway, il dispositivo 1 è un sensore a batteria e si trova vicino al gateway, il dispositivo 2 è un attuatore per tapparelle alimentato a 220v e si trova a metà circa della portata del gateway e il dispositivo 3 è un sensore a batteria che rispetto al gateway si troverebbe troppo lontano, ma relativamente vicino al dispositivo 2 che # funge da router ripetitore # e permette di estendere la comunicazione anche fino al sensore 3.

