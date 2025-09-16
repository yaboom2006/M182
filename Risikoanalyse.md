# Risikoanalyse in einem fiktiven Unternehmensumfeld

## Risikoanalyse

| System | Bedrohung | Schwachstelle | Eintritts- wahrscheinlichkeit | Schweregrad | Betroffene Schutzziele (C/I/A) | Risiko |
| ------ | --------- | ------------- | ----------------------------- | ----------- | ------------------------------- | ------ |
| Webserver | DDoS-Angriff legt Shop lahm | Kein DDoS-Schutz (WAF/CDN) | gelegentlich | hoch | A | hoch |
| Datenbankserver | Zugriff auf Kundendaten | Veraltete Software, fehlende Patches | gelegentlich | kritisch | C, I | kritisch |
| Notebook Support | Gerät gestohlen → Datenabfluss | Keine Verschlüsselung | häufig | hoch | C, I | hoch |

---

## Massnahmendefinition

| System | Risiko | Massnahme | Wirkung |
| ------ | ------ | --------- | ------- |
| Datenbankserver | Zugriff auf Kundendaten | Updates, Systemhärtung, Zugriff einschränken | Wahrscheinlichkeit sinkt stark |
| Notebook Support | Datenabfluss bei Diebstahl | Festplattenverschlüsselung, MFA | Schweregrad sinkt, Daten geschützt |

---

## Diskussion und Bewertung

1. Grösster Handlungsbedarf:
   Beim Datenbankserver, da sensible Kundendaten betroffen sind. Folgen wären rechtlich und finanziell sehr schwerwiegend.  

2. Schwachstelle behoben:
   Eintrittswahrscheinlichkeit sinkt stark, Risiko wird deutlich geringer, auch wenn Bedrohung bleibt.  

3. Organisatorische Massnahmen:
   Menschen sind oft die Schwachstelle. Schulungen und klare Prozesse sorgen dafür, dass Technik richtig genutzt wird.  
