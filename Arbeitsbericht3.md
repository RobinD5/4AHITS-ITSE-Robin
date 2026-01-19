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
<br>

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
<br>

sysinfo – Systeminformationen <br>
getuid – aktuellen Benutzer anzeigen <br>
ps – Prozesse anzeigen <br>
migrate <pid> – in anderen Prozess wechseln <br>
upload <file> – Datei hochladen <br>
download <file> – Datei herunterladen <br>
shell – normale System-Shell öffnen <br>

 <br>

 ## Übung (nmap FTP scan)

nmap scan mit:
<br>
nmap --script=vuln -p 21 <ip> 
<br>

![nmapvuln](3.3.png)
<br>

- "vsftpd 2.3.4 backdoor vulnerability" gefunden
<br>

CVE‑2011‑2523 – vsFTPd 2.3.4 Backdoor:
<br>
Ein Angreifer kann sich mit einem Benutzername anmelden, der ein :) enthält.
<br>
Dadurch öffnet der Server eine Backdoor‑Shell auf Port 6200.
<br>
Diese Backdoor wurde absichtlich in die veröffentlichte Version eingebaut
<br>

Recherchiere warum diese Skripte als intrusive bezeichnet werden, warum werden diese bei -sC oder -A nicht ausgeführt?
<br>
Sie sind intrusive weil sie:
- Senden speziell präparierte Pakete
- Versuchen Exploits auszulösen
- Testen Login‑Versuche
- Provozieren Fehlerzustände
- Können Dienste zum Absturz bringen
  <br>


## Übung (msf FTP Version herausfinden)

- search type:auxiliary scanner ftp -> auxiliary/scanner/ftp/ftp_version

- use auxiliary/scanner/ftp/ftp_version

- set RHOSTS <ip> -> run

![ftp](3.4.png)

- "Banner: 220 (vsFTPd 2.3.4)" bestätigt die Version 2.3.4

<br>

## Übung (msf vsftpd exploit)

![in shell](3.5.png)

![youhavebeenhacked](3.6.png)


![youhavebeenhacked2](3.7.png)

![youhavebeenhacked3](3.8.png)


