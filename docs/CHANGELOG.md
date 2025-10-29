# Changelog für Unimod LTE (BA MOD LTE)

Modem App der 3 Generation für LE910Cx-EUX und ME310G1 Modelle

--------------------------------------
# Version v18.2.0 - Release Version für ME310G1-WW/-W2
Datum: 23.05.2025

# Telit FW Versionen für ME310G1-WW/W2
keine Änderung zu Vorgänger

## Änderungen
HOTFIX - Bei Verwendung von Roaming SIM Karten und NB-IoT wurde die Registrierung fehlerhaft ausgewertet und wurde mit dieser Version behoben.

--------------------------------------
# Version v18.1.0 - Release Version für ME310G1-WW/-W2 und LE910C1-EUX
Datum: 08.04.2025

# Telit FW Versionen für ME310G1-WW/W2
keine Änderung zu Vorgänger

## Änderungen
HOTFIX - Es wurde bei der TCP Socketverbindung ein Fehler intern falsch behandelt. Dies führte dazu, dass das Modem über eine Socketverbindung nicht mehr zu erreichen war.

--------------------------------------
# Version v18.0.0 - Release Version für ME310G1-WW/-W2 und LE910C1-EUX
Datum: 12.02.2025

Dies ist das erste gemeinsame Release für ME310G1 und LE910C1-EUX Modelle
# Telit FW Versionen für ME310G1-WW/W2
siehe 17.15.0 - sind unterschiedlich!
ME310G1-WW - 37.00.216
ME310G1-W2 - 37.00.616

# Telit FW Version für LE910C1-EUX
siehe - 25.30.226-B035-P0F.225600, keine Änderung

## Änderungen
- Betrifft nur ME310G1 Modelle: Netzregistrierungsprobleme für NB-IoT eliminiert.
- Probleme bei nicht vorhandener PLMN behoben.
- Fehlersignalisierungen und Testausgaben werden jetzt dedizierter ausgeführt. Für die neuen Fehlersignalisierungen und entsprechenden Gegenmaßnahmen wurde ein Dokument erstellt.
- BUGFIX: Wenn das Debuglogging aktiviert war, konnte aufgrund eines internen Problems kein Reboot mehr angestoßen werden. In diesem Fall musste ein Hardware Neustart erfolgen, da der Watchdog noch weiter getriggert wurde.


--------------------------------------
# Version v17.15.0 - Release Version für ME310G1-WW/-W2
Datum: 14.09.2024

**Für die ME310G1 Modelle gibt es unterschiedliche Telit Firmwares!**

Die Applikation und MCU Version sind jedoch identisch.

## Zugehörige Versionen für ME310G1-WW
MCU Version:  umlte_aux_v4_20240905.hex
FW: Telit_ME310G1_NANVWWAU_37.00.226-P0C.220000_TFI_FH.exe<br>
**Hinweis: Die Meldung zeigt 37.00.216 obwohl das Package 37.00.226 heißt!**<br>
```c
// ME310G1-WW
37.00.216-P0C.210000
M0C.200005
P0C.210000
A0C.210000
```

## Zugehörige Versionen für ME310G1-W2 (450 MHz Modell)
ME310G1_W2_37.00.616-P0C.610001_TFI_FH.exe

```c
// ME310G1-W2
37.00.616-P0C.610001
M0C.600005
P0C.610001
A0C.610000
```

## Zugehörige Versionen für LE910C1-EUX
Wie bei 15.1.0 (25.30.226-B035-P0F.225600), keine Änderung
<br>

## Änderungen
- SIM Karten Wechsel Problem gefixt
- Registrierung Bug entdeckt und mit AT+CREG? Abfrage gefixt
- Registrierungs Prozessversuch hinzugefügt
- Signalsuche optimiert
- Netzwechsel erfordert nur noch einen Neustart

--------------------------------------
# Version v16.1.0 - Release Version
Datum: 06.08.2024
## Zugehörige Versionen
Wie 15.1.0, keine Änderung
<br>

## Änderungen
Zulässige Zeichenlängen für APN, URLs, Benutzernamen und Passwörter auf max. 128 Zeichen erweitert.<br>
<br>

--------------------------------------
# Version v15.1.0 - Release Version
Datum: 05.12.2023
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.226-B035-P0F.225600 | Beta Version - SPI Bus Fix Version<br> LE910C1-EUX_M_25.30.226-B035-P0F.225600_TFI_FH.exe |
| AUX MCU | 3 | Firmware für Atmel MCU |

[000:00:09:610]MOD INFO - ================================================================================<br>
[000:00:09:610]MOD INFO - MODULE INFO:<br>
[000:00:09:610]MOD INFO - ================================================================================<br>
[000:00:09:610]MOD INFO - MANUFACTURER:     Telit<br> 
[000:00:09:610]MOD INFO - SN# FACTORY:      354485412021052<br>
[000:00:09:610]MOD INFO - MODEL:            LE910C1-EUX<br>
[000:00:09:610]MOD INFO - PACKAGE VERSION:  25.30.226-B035-P0F.225600<br>
[000:00:09:610]MOD INFO - AZL VERSION:      252342<br>
[000:00:09:610]MOD INFO - SVN VERSION:      6<br>
[000:00:09:610]MOD INFO - SW VERSION:       25.30.226-B035-P0F.225600<br>
M0F.223006-B035<br>
P0F.225600<br>
A0F.223006-B035<br>
[000:00:09:610]MOD INFO - FW VERSION:       M0F.223006-B035<br>
[000:00:09:610]MOD INFO - HW VERSION:       1.30<br>
[000:00:09:610]MOD INFO - ================================================================================<br>

## Änderungen
### SPI-Initialisierungsanpassung
Mittels der aktuellen Telit Beta Firmware Version, wurde nun ein Low-Power-Umschaltproblem des SPI Interfaces gefixt. Durch den Low-Power Mode, wurde er SPI Bus (SPI-CLK) nicht auf den korrekten LOW-Pegel im IDLE Zustand belassen.
Hierdurch wurden Fehlkommunikationen verursacht. Dies ist nun mit der neuen Telit Firmware behoben und es

## Telit Info zu HW1.4
Laut Telit, kann die Beta Version auch für die neue HW1.4 verwendet werden!<br>
<br>
Ref: Email response on 24.11.2023<br>
Customer Baeris - LE910C1-EUX - SPI Communciation behaviour is different on newer modules | Case Number: 00475573<br>
Can we use this firmware version also for the new HW1.4 of the LE910C1-EUX?<br>
[Telit] Yes sure.<br>
<br>
Roberta Galeazzo<br>
EMEA Technical Support<br>
Telit Cinterion Application Engineering<br>

<br>

--------------------------------------



# Version v14.1.0 - Release Version
Datum: 13.04.2023
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.225-B008-P0F.225100 | Beta Version - UART FIFO Threshold Configuration Version<br> LE910C1-EUX_M_25.30.225-B008-P0F.225100_TFI_FH.exe |
| AUX MCU | 3 | Firmware für Atmel MCU |

## Änderungen
### Plausibilitätsprüfung für Ini-File und Autokorrektur
Da im Feld Probleme aufgetreten sind, wo im Ini-File in der ersten Zeile ein falscher Inhalt hineingeschrieben wurde und im Code aber keine Ursachen hierfür gefunden werden konnten, wurde nun eine Plausibilitätsprüfung für den Ini-Datei Inhalt hinzugefügt.
Es wird zunächst die Ini-Datei eingelesen, dann wird nach dem Schlüssel [BAER_Unimod] gesucht.
Wird dies nicht in der ersten Zeile gefunden, wo es stehen muss, so wird alles was vor dem Schlüssel steht gelöscht und eine neue param.ini erzeugt.

<br>

--------------------------------------

# Version v13.1.0 - Release Version
Datum: 15.12.2022
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.225-B008-P0F.225100 | Beta Version - UART FIFO Threshold Configuration Version<br> LE910C1-EUX_M_25.30.225-B008-P0F.225100_TFI_FH.exe |
| AUX MCU | 3 | Firmware für Atmel MCU |

## Änderungen
### FIP Mode
- Sollte der Port über die Settings auf 0 gesetzt werden, so wird der Default der Port 1234 verwendet. Dies ist somit eine Fallback Lösung, die den Verbindungsaufbau weiterhin gewährleistet, auch bei falschen Parametern. Im Testmode, wird dieser Fehler und entsprechende Behandlung ausgegeben:

  **BA_LOG_ALL("ERROR - Port is set to 0 in settings!!!"); <br>
  BA_LOG_ALL("ERROR - Set Port to 1234 (default)!!!");**

<br>

--------------------------------------

# Version v13.0.0 - Pre Release Version für Düsseldorfer Stadtwerke
Datum: 12.12.2022
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.225-B008-P0F.225100 | Beta Version - UART FIFO Threshold Configuration Version<br> LE910C1-EUX_M_25.30.225-B008-P0F.225100_TFI_FH.exe |
| AUX MCU | 3 | Firmware für Atmel MCU |

## Änderungen
### Probleme mit IPT Bridge Kommunikation behoben

- Bei der Anmeldung wurden aufgrund einer nicht korrekt initialisierten Variable, welche die Länge der zu versendeten Bytes definiert, zu viele Daten versendet. Die Baeris IPT Bridge toleriert das, andere IPT Bridges, wie z.B. die bei den Stadtwerken in Düsseldorf sind restrektiv und brechen die Verbindung sofort ab, wenn Daten an diese gesendet werden, diese über die erwartete Länge gehen.
- Ist die IPT Verbindung nur im LINK STATE, d.h. der IPT Server hat noch keinen Channel Open Request versendet, werden jetzt keine Daten mehr versendet.
- Reihenfolge der der Tasks Starts für IPT und Socket geändert. Hier kam es mit der Robotron IPT Bridge in Duesseldorf zu Timing Problemen.
- Fehlerbehandlung im Socket Modul überarbeitet/optimiert.
- Logging in IPT und Socket optimiert
- IPT Reconnect - Bevor ein IPT Reconnect nun initiiert wird, wird geprüft ob eine MODSET Kommunikation stattfindet. Hierzu am besten die Empfangfeldstärkeabfrage laufen lassen.
  Dann wird 5 min gewartet.
- IPT Reconnect - Max. Fehlversuche
  Dieses Feature war zwar bereits vorgesehen, wurde intern aber leider falsch behandelt. Details siehe Changelog im Git. 

### FIP Mode   
  - Aufgrund eines Parser Fehlers kann es passieren, dass der Port auf 0 gesetzt wird. Damit ist kein Verbindungsaufbau mehr möglich!!!  
  - Der Socket Timeout wurde nicht korrekt behandelt und daher ignoriert.
  
## Bekannte Probleme
- Wenn die Parametrierung über die lokale UART, bei einem offenen IPT Channel, durchgeführt wird, können IPT Server die Verbindung beenden, da unerwartet Daten empfangen werden. Das ist ein korrektes Verhalten eines IPT Servers, auch wenn die Baeri IPT Bridge in diesen Dingen fehlertoleranter ist. Wie auch immer, ist das kein Betriebsfall und verhält sich beim Vorgängermodell genauso.

<br>

--------------------------------------

# Version v12.12.0 - Release Version
Datum: 27.10.2022
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.225-B008-P0F.225100 | Beta Version - UART FIFO Threshold Configuration Version<br> LE910C1-EUX_M_25.30.225-B008-P0F.225100_TFI_FH.exe |
| AUX MCU | 3 | Firmware für Atmel MCU |

## Änderungen
- Testmode Parametrierungs Fix
  Punkt '.' zur Symbolisierung "Warte auf Parametrierung" über UART entfernt.
  Hintergrund: Bei aktivierten Testmode kann die Parametrierung über MODSET nicht durchgeführt werden, da jede Sekunde ein Punkt '.' zur Symbolisierung "Warte auf Parametrierung" auf der UART ausgegeben wurde. Diese verhindert die Kommunikation zu Modset.
- Der Versionseintrag bei der Vorgängerversion wurde durch einen Tippfehler falsch eingecheckt. Dadurch wird die Version v12.11.12 anstelle der v12.11.2 ausgegeben. 
  Um weitere Verwirrungen auszuschließen, wurde daher nun der Versionssprung auf die v12.12.0 durchgeführt.

## Bekannte Probleme
- Aktuell keine bekannt

--------------------------------------

# Version v12.11.2 - Release Version
Datum: 18.10.2022
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.225-B008-P0F.225100 | Beta Version - UART FIFO Threshold Configuration Version<br> LE910C1-EUX_M_25.30.225-B008-P0F.225100_TFI_FH.exe |
| AUX MCU | 3 | Firmware für Atmel MCU |

#Änderungen
- Baudrate für UART im Testmode von 38400 auf 9600 baud geändert. Anforderung aus Fertigung.
-

## Bekannte Probleme
- Aktuell keine bekannt

<br>

--------------------------------------

# Version v12.11.1 - Release Version
Datum: 17.10.2022
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.225-B006-P0F.225100 | Beta Version <br> LE910C1-EUX_M_25.30.225-B006-P0F.225100_TFI_FH.exe  |
| AUX MCU | 3 | Firmware für Atmel MCU |

- Telit FW: B008 (UART FIFO Threshold Configuration Version)
- AUX MCU: v3

## Bekannte Probleme
- Aktuell keine bekannt

<br>

--------------------------------------

# Version v12.10.10 - Pre Release
Datum: 05.10.2022
## Zugehörige Versionen
| Bezeichung | Version | Anmerkung |
| :--- | :--- | :--- |
| Telit FW | 25.30.225-B008-P0F.225100 | LE910C1-EUX_M_25.30.225-B008-P0F.225100_TFI_FH.exe |
| AUX MCU | 3 | Firmware für Atmel MCU |

## Bekannte Probleme
- UART FIFO Handling (4 kB Threshold) führt beim Zählerauslesen mit niedrigen Baudraten zu erheblichen Verzögerungen (ca. 20 s bei 1200 baud).

Mit der Pre Releas Version wurden 150 Geräte ausgeliefert
