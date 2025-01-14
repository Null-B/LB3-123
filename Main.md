# Static IP and Time zone
Noting Here bc its a place holder

## Host Name anderen
Wir mussen unsere Host name andere so das wir in der zufkunf unsere server einfach erkkerne konnen. Das ist auch wichtig wenn wir nacher eine domain erstellen was wird von der Host name ubernommen.

### Process
1. Auf das linke seite drucken auf das "Local Server"
![alt text](image.png)

Dann in der server properties seihst du die "Computer Name"
2. Drucke auf das "Computer Name"
![alt text](image-1.png)
![alt text](image-2.png)

3. Drucke auf "change"
![alt text](image-3.png)

Und heir wirds du Eien eigene name wahlen fur deine Server, es ist epholen eine name nach der Firma Names konzept zu gehen, aber das ist nicht zwangshaft
![alt text](image-4.png)
4. Gebe das Name euren server ein
5. Drucke Auf "OK"
![alt text](image-5.png)
Um die andereungne zu ubernehmen muss du deine gerat neu starten
6. Drucke auf Ok
![alt text](image-6.png)

Du werdest auch nochmal informiert das du musst deine pc neu starten
![alt text](image-7.png)

7. Wahle "restrart now"
![alt text](image-8.png)

Warte Bis deine Server Neu Startet

### Teste
Um zu sehen ob unsere Server Mit der Neue Name konfiguriert ist mussn wir es in der local server properties Uberprufen.

Wenn der server hochgeafhren ist
8. Offnen sie Server Manager.
9. Gehen sie auf Local Server
![alt text](image.png)

Und unter "Properties" Wrist du sehehn das der server mit der neuen name konfiguriert ist.
![alt text](image-9.png)

wenn das nicht der fall ist, machen sie die schritte nochmal

# AD DS
Active Directory (AD) ist eine weit verbreitete Windows-Software, die Administratoren ermöglicht, ein gesamtes Netzwerk zentral zu verwalten. Mit Active Directory gehören die Zeiten der Vergangenheit an, in denen jedes einzelne Gerät wie PCs, Laptops und mobile Geräte manuell konfiguriert werden musste.
AD bietet eine zentrale Plattform zur Verwaltung von Benutzern, Geräten, Gruppenrichtlinien, Sicherheitsrichtlinien und Zugriffsrechten. Dadurch wird die Verwaltung großer Netzwerke effizienter, sicherer und konsistenter.

## Installation
1. Starte eure VM, und logge euch ein
2. Offnen Serve Manager

3. Auf Der Dashboard druchke auf add roles and Feautres (Das Nummmer 2)
![alt text](image-10.png) 

4. Lessen sie die einleitung durhc, und drucken sie OK
![alt text](image-11.png)

5. Wahle Role Based Installation und Drucke OK
![alt text](image-12.png)

6. Wahle Deine Server, Pass Gut auf das es Deine Server ist.
![alt text](image-13.png)
Sie konen heir auch die IP uberprufen und das computer name, wenn diese paratmetre nicht stimmen ich ephele das sie es heir abrechen und die parameter anderen

7. Finde "Active Directory Domain Serveces" In das Liste
![alt text](image-14.png)

8. Selectire die Modul
9. Drucke auf Add Feautres
![alt text](image-15.png)

Uberpruffe das es Selektirert ist
![alt text](image-16.png) 

10. Drucke auf next
11. Schau das "Group Polices Management" ausgewahlt ist
![alt text](image-17.png)
Wenn das nicht der fall wahre, selektiren sie es maneuel
12. Drucke auf next

Der serve wird dir informacion ubder das AD geben, wenn sie wollen Lessen sie es druch.

13. Drucke auf next

Heir wirds du eine uberblick von die modulen bekommen die instaliert werden. Bitte sahuen sie an, nutze deiser photo als eine beispliel
![alt text](image-18.png)
14. Drucke auf Install

Lassen sie der Installation Laufen bis es Fertig ist
![alt text](image-19.png)

Wenn es fertig wird,
![alt text](image-20.png)
15. Drucken sie auf "Close"

Sie haben jetz geschaft die AD DS moudl zu instaliren, Es fehlt noch der Modul zu konfiguriert

## Configuration
Es ist notig fur das Funkzionalitat der Active Directory zu konfiguriert, Ohne eine richtigen konfiguration wird der AD DS Nicht fukzioniren.

Nahc der Installation wird Die flagge in das obbere Rehcte ecke mit eine warn sybole sein, das ist sozusagen eine signal das etwas muss getan werden um die Installation feritg zu stellen.

1. Drucken sie auf das flagge
![alt text](image-21.png)

Sie werden sehen das es eine "Post deplomyent Configuration" Gibts
![alt text](image-22.png)

2. Drucken Sie auf "Promote the Server to Domain Controler"
![alt text](image-23.png)

Du wirds dieser menu bekommen, wie der Installtions menu das ist anlich und wrids gelich ablaufen.
![alt text](image-24.png)


3. Drucke auf Add new forest

Was ist eine Forest?
/////////////////

gebe Deine Domain eine Domain name. Das wird spatter von der DNS verwalten.
Der AD Modul benotigt eine FQDN, und wrid keine einfache name in der domain name.
Du must eine TLD haben, ohne eine TLD wird der Server der name Ncith akzeptiren. 

4. Schreibe deine Domain Name rein
![alt text](image-25.png)

wenn sie verscheiden servern und forst haben auf eine server es kann dazu fuhren das die auf verschidene Infrascrucutre funkzioneiren. Deswegen ist es jetz nicht so wichtig in unsere fall aber sie nacher auf eine andere infracscurete eine Forest erstellen wollen. Mussen sie enschprechend wissen weche aus zuwahlen

5. Wahle die Windwos Server 2025
![alt text](image-26.png)

Welche funkzionen soll diesr dns server haben. Du hast die auswahl das zu bestimmen.

6. Wahle DNS
![alt text](image-27.png)

Dieses password musen sie merken wegen es wird wichtig spatter, wenn wir die clients einloggen und mir Der AD verbinden.

7. Schreibe eine Passoword rein, Und Drucke Weiter

![alt text](image-28.png)

Wir Brauchen keine DNS delegation zone, Wegen das wird eine simplen AD + DNS Setup.

8. Drucke Weiter

![alt text](image-29.png)

Das Netbios ist das name was die Cleint Gareten werden sehen wenn die mit der AD verbunden sind, das ist die name von der server das wird zu das end user sehebar

9. Schribe die Name rein, Durkce weiter

![alt text](image-30.png)

Hier kannst du die Phaden zu das data an der server andren. Das ist wichtig wenn du willst das die data auf eine andre disk oder dirve geschpeichertwerden soll. Wir nutzen die Default wengen wir haben nur eine dirive.

10. Drucke weiter

![alt text](image-31.png)


Heir gibts eine revwei, sher epholen die settings an zu schauen bevor du weiter gehst. Nutze meine Screenshots als eine Template.

![alt text](image-32.png)

![alt text](image-33.png)

11. Drucke weiter

Lass Windows server 2025 Die Settigns einstellen und die ubernehmen. Es wird auch shaeun das der Server hat die benotigte resurcen und Modulen dieser weiter zu mahcen.

Es ist nicht eine grosses problem wenn eineige warnunge heir auftacuhen, wir benotigen weinger modulen als die normal auf eine serve sich befinden

![alt text](image-34.png)

Heir in unsere fall tauchen zb einige Probleme mit der Netwrok adapter wengen das eine VM ist. WIr konnen die Ignoriren fur der ziet wegen es wird nicht viel andere sein als waren wir auf einer echten server.

12. Drucke auf Install

![alt text](image-36.png)

![alt text](image-37.png)

Nahc diser Opertaiton wrid der Server selber Neustarten. 

Mit Der erste tiel der instalation von Das Active Directoy sind wir feritg. Wir werden mit der Grupen und Unsern Nacher weiter machen. Aber bvor das bentoige wir einige Modulen.

# DNS
Siro is doing this

# DCHP
Noting here




# Groups and Users AD

Wir haben die DNS Und Das DCP konfiguriert, jetz so das unsere AD Mit Unser Gefuhlt werden kann schauen wir uns an wie mann Unser und Organistaion Units machet in AD.

*Grund Begreife* 

Organistoan Untis sind wie abtielungen, die sind da um usern Directorys und sontstiges zu behalten. Mann kann meherere usern und Directorys uber eine organistational unti verwalten. 

Usern an der AD, Usern sind die Besntand teil der AD wir konenn die nutzetn um leute in der AD zu verbinden und zusamnen zu bringen. Die konnen eine veilatligkeit an Moglichkeiten zur verwaltung haben wie: Cloud Hoems, Cloud Storange, VMs um ins netz zu arbeiten und auch configuraitosn so das auf jeder comptuer konenn die gelich und einfahc arbeitenn.

Folder, an der AD konenn wir foldern erstellen wo wir data und Inforamtionenn reinmachen konnen, die nutuzen uns wie File Shares aber afu eine bessere nuvea

----

1. Von der Server Maneger In der Obberen Ecke Drucke auf "Active Directoy User and Servicecs"
![alt text](image-38.png)
![alt text](image-39.png)

an der linken seite befindent sich die active domains in diene Network
![alt text](image-40.png)

Heir ist das Domain kemal.com die wir vorher gemacht haben.

2. Drucke auf Der Main Domain
![alt text](image-41.png)

Heir befinden sich die utnere Direcotrs fur das AD. Heir findete man 

3. 

## Cleitn Tests

## Conectivity




# Printing Server
