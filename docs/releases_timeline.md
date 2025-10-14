# Relase Timeline - Kurzübersicht

# Alle Modelle
| Version | SW Release Datum | Fertigungsfreigabe | Anmerkungen |
|----|---|---|---|
v18.1.0 | 12.02.2025 | 14.02.2025 | HOTFIX - TCP Socket Problem / Nichterreichbarkeit behoben
v18.0.0 | 12.02.2025 | 14.02.2025 | <ul><li>ME310G1 Modelle: Netzwerkregistrierungsproblem bei NB-IoT gefixt.</li><li>Probleme bei nicht vorhandener PLMN behoben.</li><li>Fehlersignalisierungen und Testausgaben werden jetzt dedizierter ausgeführt. Für die neuen Fehlersignalisierungen und entsprechenden Gegenmaßnahmen wurde ein Dokument erstellt.</li><li>BUGFIX: Wenn das Debuglogging aktiviert war, konnte aufgrund eines internen Problems kein Reboot mehr angestoßen werden. In diesem Fall musste ein Hardware Neustart erfolgen, da der Watchdog noch weiter getriggert wurde. Da dies kein normaler Anwendungsfall ist, kann das Problem als unkritisch betrachtet werden.</li>



# ME310G1 Modelle
| Version | SW Release Datum | Fertigungsfreigabe | Anmerkungen |
|----|---|---|---|
v18.2.0 | 23.05.2025 | 23.05.2025 | HOTFIX - Registrierung schlägt fehl in Verbindung mit Roaming SIM Karten und NB-IoT. |
v18.0.0 | 14.09.2024 | 15.10.2024 | Initiales Release für die neuen ME310G1 Modelle<br>**BA MOD NB IOT**<br>**BA MOD 450** |


# LE910C1-EUX
| Version | SW Release Datum | Fertigungsfreigabe | Anmerkungen |
|----|---|---|---|
v16.1.0 | 06.08.2024 | 06.08.2024 | Aufgrund eines Kundenproblems mit einer sehr langen APN-URL Kennung wurden die zulässigen Zeichenlängen für APN, Usernames, Passwörter und URLs auf 128 Zeichen erweitert.
v16.1.0 | 06.08.2024 | 06.08.2024 | Aufgrund eines Kundenproblems mit einer sehr langen APN-URL Kennung wurden die zulässigen Zeichenlängen für APN, Usernames, Passwörter und URLs auf 128 Zeichen erweitert.
v15.1.0 | 05.12.2023 | 05.12.2023 | SPI IDLE Bus Problem gefixt (neue Telit FW und geänderte SPI Init)
v14.1.0 | 13.04.2023 | 30.05.2023 | Plausibilitätsprüfung und Autokorrektur für das Ini-File hinzugefügt (param.ini kann falsche Daten am Dateianfang enthalten) |
v13.1.0 | 12.12.2022 | 15.15.2022 | Wurde am 15.12.22 von den Stadwerken Düsseldorf freigegeben (Robotron IPT Bridge) und für die Fertigung aktualisiert bereitgestellt |
v12.12.0 | 27.10.2022 | 15.15.2022| Versionnummer wurde falsch im Code hinterlegt, daher wird die Version 12.1.0 angezeigt|
v12.11.2 | 18.10.2022 | 15.15.2022| Baudrate für Testmode wieder auf 9600 geändert |
v12.11.1 | 17.10.2022 | 17.10.2022 | Erstes Release mit optimierten UART FIFO (Telit FW) |