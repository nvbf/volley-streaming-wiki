---
title: Legge inn overlay
parent: Open Brodcast Software
---

Si at du har fått en nettadresse som du vil legge inn som overlay i OBS.

Her bruker vi et eksempel fra scoreboard-plugingen vår, og vi bruker følgende adresse: [http://volleystream.no/scoreboard?matchId=dragvoll](http://volleystream.no/scoreboard?matchId=dragvoll).

* Først så må du åpne OBS.

![OBS Studio](./images/obs-program.png)

* Under **Sources**, klikk på "+"-tegnet, som er nederst til venstre.

![OBS Sources](./images/obs-sources.png)

* Klikk deretter på **BrowserSource**.

![OBS Add Browser Source](./images/obs-add-browser-source.png)

* Lag en ny source, og gi den et valgfritt navn. Vi har her kalt den "Overlay".

![OBS New Browser Source](./images/obs-new-browser-source.png)

* I feltet "URL", fyll inn **adressen** du har fått.
* I feltet "Width", fyll inn **1280**.
* I feltet "Height", fyll inn **720**.
* I feltet "FPS", fyll inn **30** hvis du streamer i 30FPS eller 60 hvis du streamer i 60FPS.

![OBS browser source settings](./images/obs-browser-source-settings.png)

* Klikk på **OK**.

Nå skal overlayet være klar til bruk i OBS.
