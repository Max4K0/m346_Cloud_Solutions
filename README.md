# m346_Cloud_Solutions

### KN01:

#### A:
Ein Hypervisor selber ist ja eine Software, die verschiedene virtuelle Maschinen auf einem System bereitstellen kann. 
Dadurch können verschiedene Hosts systeme getrennt voneinander Arbeiten.

Der Hypervisor allerdings besteht auch aus 2 varianten.

Den Bare Metal Hypervisor oder hier Typ 1 läuft direkt auf der Hardware. 
Ein System, welches direkt auf der Hardware seperat funktioniert bietet meistens immer eine gute geschwingigkeit
HyperV wäre so eine VM, welche das bietet.

Den Hosted Hypervisor oder hier typ 2 laufen direkt auf dem Betriebsystem und sind wie ein normales Programm.
Vmware oder auch Virtualbox funktionieren so.

Hauptunterschied der beiden Varianten sind also worüber sie laufen. Direkt die Hardware oder über das OS.

#### B:

- 12 Logische Prozessoren - 32gb Ram.

Wenn ich bei Vmware die CPU cores einstelle, so darf ich bei den "Total Prozessor cores" nicht über meine Logischen Prozessoren cores gehen.
Ansonsten kann ich diese Einstellungen nicht bestätigen.

![image](https://github.com/user-attachments/assets/c75b3b1a-2b44-45f3-b513-5b5af4ea20e5)

![image](https://github.com/user-attachments/assets/10c115e8-67be-4b18-9a7f-1f58e7b0e71e)

Beim Ram ist das Ähnlich. Hier kommt noch dazu, weil ich ja noch ein OS am laufen habe, so muss ich dem System auch einen gewissen Ram freiraum geben.
In der Teorie ist es möglich den Ram deutlich zu erhöhen über seinen normalen Ram wert.
Der Ram würde dann den Festplattenspeicher benutzen.
Ich habe dieses Feature allerdings begrenzt. Daher habe ich ein direktes Limit.

![image](https://github.com/user-attachments/assets/0f9be2c7-4419-4a7a-ba27-5be18c3c5efe)

![image](https://github.com/user-attachments/assets/287f537a-ecb7-4f1a-bb59-d5d47010c9af)

Die VM lässt sich also garnicht erst starten, wenn meine Werte zu hoch sind.


Den  Befehl "lscpu | grep "CPU(s)"" gab es nicht auf meiner Windows VM, da dies ein Linux Befehl war.
Ich habe stattdessen "wmic cpu get NumberOfCores,NumberOfLogicalProcessors" genutzt.
![image](https://github.com/user-attachments/assets/14f0b56e-e84d-4970-bc9c-ef3cd4806897)

Beim ram war es statt "free -h" bei mir auch "Get-ComputerInfo | Select-Object CsTotalPhysicalMemory".


![image](https://github.com/user-attachments/assets/8817767f-538f-4a1f-9897-7501bcb06f79)


