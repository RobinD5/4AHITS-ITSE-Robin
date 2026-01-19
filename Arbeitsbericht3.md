------
# Arbeitsbericht ITSE-Labor
## 4AHITS Robin Dicker 19.01.2026
------

# Gemeinsame Übung (Metasploit

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
