 +++
title = "Chromebook custome coereboot"
date = "2024-04-04T22:20:16+01:00"
author = "villo"
authorTwitter = "" #do not include @
cover = ""
tags = ["linux", "chromebook"]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++


Questo progetto è molto interessante e permette di cambiare il bios proprietario installato sui computer chromebook di moltissime marche e modelli per poter installare un altro sistema operativo, nel mio caso Arch linux tramite EndevorOS.
I chromebook sono macchine generalmente fatte per studenti o per utenti dalle necessità basiche di scrittura/lettura mail e navigazione, macchine basiche molto "plasticose" e con caratteristiche hardware basiche ma che poossono essere interessanti per alcuni aspetti..generalmente sono macchine poco potenti, con architettura X86 dual core con un TDP molto basso, questo permette di avere un pc a bassissimo consumo, quindi con una durata della batteria ottimale, un pc perfetto come seconda macchina di appoggio quando per esempio siamo in vacanza o fuori un weekend e non vogliamo portarci il nostro pc principale per paura di furti o di danneggiarlo.
Io ho trovato a 50 euro un chromebook lenovo 100e di seconda generazione, monito e tastiera pessimi ma del resto una macchinetta perfetta, fanless e consumi bassissimi, in sleep ha un consumo ridicolo e la la batteria sembra infinita..anche nell'utilizzo base di scrittura la batteria sembra non scendere mai, merito del  bassissimo tdp del processore e di Linux che ottimizza al massimo i processi. Nel mio caso posso ottendere tranquillamente 10 ore di utilizzo base.
Vediamo come fare per sostituire il bios, attenzione prima di acquistare un chromebook per questo progetto assicurarsi che sia compatibile, visitare la pagina ufficiale del progetto https://mrchromebox.tech/#devices
 
 # modello lenovo 100e 2nd gen

 celeron N4020 gemini lake disco 32Giga e 4g di ram


https://www.reddit.com/r/chrultrabook/comments/aufp1q/getting_started_read_this_first/

Per iniziare:


- Put your device into Developer Mode

- Disable the hardware firmware write protect, method varies by device

- Flash the UEFI Firmware

...
## developer mode

Con pc spento premere ESC + REFRESH(simbolo freccina che ruota) e power on
Enabling Developer Mode

Entering Developer Mode requires you to first boot into Recovery Mode. For Chromebooks, this means pressing [ESC+Refresh+Power]; On Chromeboxes, there is usually a physical recovery button (often a small hole above the SD card reader) which must be depressed when powering on. Once at the recovery screen, press [CTRL+D] to enable developer mode, then confirm when prompted. As a security measure, transitioning to/from Developer Mode will wipe out all ChromeOS user data, essentially powerwashing (resetting) the device. 
Dopo circa 5 minuti il pc si riavvia, *non toccare niente fino a che non senti doppio beep e si riavvia da solo*

Spengo, stacco la batteria(nel mio caso ), la lascion staccata poi attacco l alimentatore(attenzione con quello cinese non parte)
Accendo faccio partire e mi collego a una rete wifi
DOpo essersi riavviato parte in automatico un chromeos pulito, una volta partito premento ctrl+alt+F2 (simbolo freccia a dx) entro nella shell amministratore.
Utente :chronos
Non richiede password
Essendo connessi a internet:
cd; curl -LO mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh
QUando lo chiede confermare con Y, si riavvierà, ridare lo stesso comando dopo il riavvio
Selezionare 2 (complete UEFI) e lasciar andare.
Una volta finito fare un reboot


