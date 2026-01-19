------
# Arbeitsbericht ITSE-Labor
## 4AHITS Robin Dicker 19.01.2026
------

## Gemeinsame Übung (Metasploit)

- `msfconsole` um in die Metasploit shell zu kommen

### SSH Version:

-  `use auxiliary/scanner/ssh/ssh_version` um in die SSH Version umzusteigen
-  `set RHOSTS <target IP>` Ziel Host für Attacke festlegen
-  `run` ausführen 

![SSH](3.1.png)

<br>

### http Title:

- `use auxiliary/scanner/http/title` um in den http Title umzusteigen
- wieder set RHOSTS <> & run

![http](3.2.png)

<br>

## Übung (msf Basics)

### Cheatsheet:

search <begriff> – Module suchen <br>
use <modul> – Modul laden <br>
info – Infos zum Modul <br>
show options – Optionen anzeigen <br>
show payloads – verfügbare Payloads anzeigen <br>
set <option> <wert> – Option setzen <br>
unset <option> – Option löschen <br>
exploit oder run – Angriff starten <br>
exploit -j – im Hintergrund starten <br>
exploit -z – ohne Session-Interaktion starten <br>
setg - setzt globable Variable z.b.: setg LHOST <ip>

 <br>
 
### msfvenom

msfvenom kombiniert die früheren Tools msfpayload und msfencode.

-p – Payload auswählen <br>
-f – Ausgabeformat (exe, elf, raw, php, …) <br>
-e – Encoder <br>
-a – Architektur <br>
--platform – Zielplattform <br>
-l payloads – alle Payloads anzeigen <br>
--payload-options – Optionen eines Payloads anzeigen

 <br>

### Meterpreter

Meterpreter ist ein post‑exploitation Framework, das über eine Metasploit‑Payload geladen wird.

sysinfo – Systeminformationen <br>
getuid – aktuellen Benutzer anzeigen <br>
ps – Prozesse anzeigen <br>
migrate <pid> – in anderen Prozess wechseln <br>
upload <file> – Datei hochladen <br>
download <file> – Datei herunterladen <br>
shell – normale System-Shell öffnen <br>

 <br>


