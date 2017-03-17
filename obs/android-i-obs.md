---
related:
  - obs/iphone-i-obs.md
---

# Streame fra Androiden telefonen over trådløst nett

Vi har ikke fått sett på muligheten for å streame fra telefonene over kabel, bør være mulig. men dette må vi se mer på.

Det er mulig å sette opp android telefonene som et IP kamera som deler video med nettverket rundt seg, også kan man gå i OBS og si at du skal hente dataene fra kameraet. Fordelen med dette er at du ikke trenger kabel. Ulempene er at det er litt forsinkelse og kvaliteten vil ikke være den samme som via kabel. Det suger også endel batteri, så du bør nok ha i en strømlader selv om du ikke trenger en kabel mellom pc og telefon.

## Step by Step - forklaring

Du må først installere en app på telefonene din. [IP Webcam](https://play.google.com/store/apps/details?id=com.pas.webcam&hl=en),

Når denne er installert må du Åpne appen

Det første vi vil gjøre er å finne meny valget `Video Preferences` her er alle valgene hvor du kan stille på kvalitett.

Våre anbefalte instillinger er:

`Video resolution` - 1280 \* 720

`Main camera` - Primary camera

`Video orientation` - Landscape

Det er mange flere settings, men vi har ikke utforsket alle. Er du misfornøyd med kvaliteten på bildet, så er det verdt og nevnte at det er en `Quality` innstilling som man kan prøve skru opp. Men dette er ikke prøvd.

Gå så tilbake til hovedmenyen, scroll helt nederst og velg `Start server`

Du vil da få et opp et bilde som kanskje ligner litt på dette:

TODO: komprimer bilde som ligger i \#sass på slack og last opp

Her ser du at du får opp en IPv4 addresse nederst midt på skjermen som kan ligne litt på denne: `192.168.1.217:8080`

\(for avanserte brukere: se action oppe i høyre hjørne, kan være ting av interresse der\)

Denne IP addressen skal du nå legge inn i OBS.

Hvis ikke OBS er åpnet, så gjør du det nå.

![](/assets/sources-obs.png)

Velg så `+` under sources.

![](/assets/media-source.png)

\(din dropdown meny vil ha litt andre valg\)

Og velg Media Sources, og gi den et fornufig navn. F.eks `Samsung Galaxy` eller  `Telefonen min`

![](/assets/medie-source-url-from-phone.png)

Du vil da få opp vinduet vist over, legg nå på urlen som vi fant på mobilen i input feltet.

her er det endel ting som fort kan bli feil.

1. Du må ha `http://` før ipen
2. Du må ha `/video` bak
3. input format feltet må ha verdien `mjpeg` og ikke noe space til sluttt.

PS1: Previewen virket ikke med en gang du la inn riktige verdier, så når man tror man har riktige verdier. Trykk OK,  
også prøve så å trykke på innstillinger \(tannhjuelet\), da skal preview funke.

PS2: Hvis den blir feilkonfiurert så vil du se et kjempeliten rødt firkant oppe i venstre hjørne, da har noe blitt feil og selv med riktige verdier så vil du ikke se at det skulle ha fungert, fjern da konfigurasjonene fra `sources` og start så på nytt.

PS3: Husk at du må ha trykket ``start server` og denne må gå for at du skal finne kameraet over.``

Forhåpentligvis fikk ikke du noen av problemene nevnt over og du ser nå en stream fra mobilen din i OBS.

Det er nok da tid for å [legge inn et overlay i obs](/overlay/hva-er-en-stream-overlay.md)

## Mer Problemer?

Denne guiden er fornorsket og vi har prøvd og gjøre den litt bedre enn den orginale tråden vi tok utgangspunkt i, men sjekk ut den orginale tråden - [https://obsproject.com/forum/threads/android-smartphone-as-a-webcam-tutorial.6957/](https://obsproject.com/forum/threads/android-smartphone-as-a-webcam-tutorial.6957/) kanskje den kan hjelpe deg på vei. eller send mail til post@volleystream.no så skal vi se om vi klarer å hjelpe deg.

