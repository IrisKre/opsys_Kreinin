Praktikum 4 lahendus:

|Küsimus|Linux|Windows|Linuxis kasutatud käsklus|Windowsis kasutatud tööriist|
|---|---|---|---|---|
|Mitu protsessi kokku arvutis käib?|214|227|ps -aux l (asendab kriipsu) wc -l|Tegumihaldur - > Jõudlus -> Protsessid|
|Milline on kõige esimesena käivitatud protsess?|/sbin/init splash|smss.exe|ps axo pid,cmd,comm,etime|Process Explorer -> Start Time|
|Mitu ja milliste kasutajate protsesse arvutis käib?|USER, root, systemd-oom, systemd-resolve, systemd-timesync, avahi, messagebus, syslog, kernoops, rtkit, colord, iris|irisk, LOCAL SERVICE, NETWORK SERVICE, SYSTEM, UMFD-0, DWM-5|ps -eo user|Tegumihaldur - > Üksikasjad -> Kasutajanimi|
|Kui kaua on arvuti järjest töötanud (up time) ? (Alternatiivselt võib vastata ka millal (kuupäev ja kellaaeg) arvuti viimati käima pandi?)|24min|0:23:17:38|uptime|Tegumihaldur - > Jõudlus -> Tööaeg|
|Milline protsess käivitati kõige hiljem (viimasena)?|update-notifier|chrome.exe|ps -ef|Process Explorer -> Start Time|
|Milline on kõige rohkem protsessoriaega võttev protsess|/usr/bin/gnome-shell|System Idle Process|ps -aux --sort -pcpu|Process Explorer -> CPU time|
|Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess?|/usr/bin/gnome-shell|msedge.exe|ps -aux --sort -vsz|Process Explorer -> Virtual Size|
|Milline on kõige rohkem füüsilist mälu (working set) võttev protsess?|/usr/bin/gnome-shell|SearchApp.exe|ps -aux --sort -pcpu|Process Explorer -> Working Set|
|Kui palju füüsilisest mälust (Physical Memory) on vaba|201Mi|8.5GB|free -h|Tegumihaldur - > Jõudlus -> Mälu|
|Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt?|12G ja 47%|280.61GB ja 59%|df -h|Arvutihaldus -> Mäluseade -> Kettahaldus -> Vaba ruum/% vaba|
|Milline on kõige suurem kõvakettal olev fail ja kõige suurem kaust?|fail:/var/lib/snapd/seed/snaps/gnome-3-38-2004_112.snap ja kaust:/usr|fail: OS-Kreinin.vdi (16.2 GB) ja kaust:Windows|sudo du -a / l (asendab kriipsu) sort -n -r l (asendab kriipsu) head|WinDirStat -> Size|
|Võrrelge terminali käskude: sha1sum /dev/zero l (asendab kriipsu) sha1sum /dev/zero  ja  sha1sum /dev/urandom l (asendab kriipsu) sha1sum /dev/urandom protsessori nõudlust. Avage teine terminaliaken ja top samaaegseks käivitamiseks. Uurige millisele CPU alamtegevusele us, sy, id, wa, st jne kulub enim protsessori aega ja mitu protsenti kulub kummagi käsu korral? (Ainult Linuxis) Lisa ka ekraanipilt aruande juurde näiteks pärast tabelit.|Esimese käsu korral kulub us peale kõige rohkem, 97.0%, ja teise käsu korral sy peale 52.7%.|-|top|-|
|Milline protsess kõige rohkem salvestusseadmele kirjutab, kõige rohkem salvestusseadmelt loeb? Millisesse faili antud protsess kõige rohkem kirjutab, millisest failist kõige rohkem loeb? (Ainult Windowsis)|-|kirjutab:System, C:\$Mft (NTFS Master File Table); loeb: chrome.exe, C:\Users\irisk\AppData\Local\Google\Chrome\User Data\Profile 1\Cache\Cache_Data\data_|-|Resource Monitor -> Disk -> Disk Activity -> Write/Read|
|Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? Vali antud protsessi poolt kasutatavatest ühendustest üks ning kirjuta välja järgnev: kohalik IP-aadress, kohalik port, ühenduse teise poole IP-aadress, port, latents ja antud ühenduse poolt kasutatav võrguliikluse kogumaht. (Ainult Windowsis) Lisa ka ekraanipilt aruande juurde näiteks pärast tabelit.|-|Chrome.exe; 192.168.3.6; 64114; 13.64.73.29; 443; 176ms; 4,518,986|-|Resource Monitor -> Network|
|Sõber kurdab, et tema arvuti on oluliselt aeglasem kui varasemalt. Millise programmiga ja millise parameetrite abil saate tuvastada milline protsess või teenus muudab arvuti aeglaseks?|Vaatame, mis tekkinud tabelis veerus %CPU kõige esimene tulemus on/suurima protsendiga on ja selle protsessi peaks sulgema.|Selles aknas olevat tabelit tuleb sorteerida Protsessori % järgi. Suurima protsendiga protsess/protsessid tuleks peatada.|top|Tegumihaldur -> Protsessid|


Iris Kreinin Oktoober 6, 2022, at 23:14

12. küsimuse pildid:
<img width="461" alt="12 1 küsimus_IK" src="https://user-images.githubusercontent.com/60475987/194409560-67da37dc-dbad-4326-90cd-f421f4b22921.png">
<img width="461" alt="12 2 küsimus_IK" src="https://user-images.githubusercontent.com/60475987/194409564-9923eb24-69a0-487a-a2ce-ff7eb6ea31db.png">

14. küsimuse pilt:
<img width="960" alt="14 küsimus_IK" src="https://user-images.githubusercontent.com/60475987/194409584-cb60fb7c-a3a6-449e-a98a-97ec82a4d082.png">

