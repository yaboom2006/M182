# Hardening Ubuntu

## 1. Massnahmen

|   | Massnahme                            |   | Grund                                                 |   |   |
|---|--------------------------------------|---|-------------------------------------------------------|---|---|
|   | ------------------------------------ |   | ----------------------------------------------------- |   |   |
|   | Updates installieren                 |   | Schliesst Sicherheitslücken                           |   |   |
|   | Root Login deaktivieren              |   | Verhindert direkten Root-Zugriff                      |   |   |
|   | Rechte einschränken                  |   | Minimiert Risiko, dass Angreifer Root-Rechte erlangen |   |   |
|   | Firewall aktivieren                  |   | Blockiert unerwünschte Zugriffe                       |   |   |
|   | Logs aktivieren                      |   | Erlaubt die überwachung von Aktionen                  |   |   |
|   | Unnötige Dienste deaktivieren        |   | Weniger Möglichkeiten für Angriff                     |   |   |

---

## 2. Reflexion

### Adressierte Risiken

- Entfernung unnötiger Dienste und Pakete → verkleinert die Angriffsfläche  
- Deaktivierung des Root-Logins → verhindert direkten Vollzugriff  
- Aktivierung einer Firewall → erlaubt nur autorisierte Zugriffe  
- Einrichtung von Logging → ermöglicht die Nachverfolgung von Angriffen  

---

### Wirksamkeit der Massnahmen

- Sehr effektiv gegen bekannte Schwachstellen  
- Schützt insbesondere vor automatisierten Angriffen auf Container  
- Absolute Sicherheit ist nicht erreichbar (z. B. Zero-Day-Exploits oder Social Engineering bleiben ein Risiko)  

---

### Potenziale zur Verbesserung

- Container im Read-Only-Modus betreiben  
- Vermeidung von Secret-Speicherung innerhalb der Container  
- Einsatz von IDS/IPS zur Angriffserkennung  
- Einführung eines automatisierten Patch-Managements  

---

### Fazit

- Eine konsequente Systemhärtung reduziert die Angriffsfläche erheblich  
- Es wird klar, welche Schutzmassnahmen Priorität haben und wie ihre Wirksamkeit überprüft werden kann