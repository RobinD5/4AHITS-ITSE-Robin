------
# Arbeitsbericht ITSE-Labor
## 4AHITS Robin Dicker 17.11.2025
------

# Übung (nmap cheat sheet)

## Nmap Cheat Sheet

## Grundlegende Scans
- `nmap <IP>` -> Standard-Scan  
- `nmap -A <IP>`-> Aggressiver Scan (OS, Version, Skripte)  
- `nmap -Pn <IP>` -> Host-Erkennung überspringen  

## Ports
- `nmap -p 80 <IP>` -> Nur Port 80  
- `nmap -p- <IP>` -> Alle Ports  
- `nmap -F <IP>` -> Schneller Scan (häufige Ports)  

## Scan-Techniken
- `nmap -sS <IP>` -> SYN-Scan (Stealth)  
- `nmap -sT <IP>` -> TCP Connect  
- `nmap -sU <IP>` -> UDP-Scan  
- `nmap -sV <IP>` -> Service-/Versions-Erkennung  
- `nmap -O <IP>` -> OS-Erkennung  

## Timing
- `nmap -T4 <IP>` -> Schnell  
- `nmap -T5 <IP>` -> Sehr schnell (riskant)  

## Output
- `nmap -oN scan.txt <IP>` -> Normal Output  
- `nmap -oA results <IP>` -> Alle Formate  

## NSE (Skripte)
- `nmap --script=default <IP>` -> Standard-Skripte  
- `nmap --script=vuln <IP>` -> Schwachstellen-Scan  

---
Tipp: Kombiniere Optionen für detaillierte Ergebnisse, z. B.:  
```bash
nmap -sS -sV -O -p- -T4 <IP>
