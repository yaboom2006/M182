# Monitoring mit Wazuh

## Installation

1. ### System vorbereitet
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. ### Repository hinzufügen
   ```bash
   curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH | sudo apt-key add -
   echo "deb https://packages.wazuh.com/4.x/apt stable main" | sudo tee /etc/apt/sources.list.d/wazuh.list
   sudo apt update
   ```

3. ### Wazuh-Manager installieren
   ```bash
   sudo apt install wazuh-manager -y
   ```

4. ### Wazuh-Agent installieren
   ```bash
   sudo apt install wazuh-agent -y
   sudo systemctl enable wazuh-agent
   sudo systemctl start wazuh-agent
   ```
   Konfiguration:  
   Datei `/var/ossec/etc/ossec.conf` bearbeiten und Manager-IP eintragen.

---

## Systemhärtung

- ### Unnötige Dienste entfernen
  ```bash
  sudo apt autoremove -y
  ```

- ### Root-Login über SSH deaktivieren
  Datei `/etc/ssh/sshd_config` anpassen:
  ```
  PermitRootLogin no
  ```
  Danach:
  ```bash
  sudo systemctl restart ssh
  ```

- ### Firewall einrichten (ufw)
  ```bash
  sudo ufw allow 22/tcp
  sudo ufw allow 5601/tcp
  sudo ufw allow 1514/tcp
  sudo ufw enable
  ```

- ### Fail2ban installieren
  ```bash
  sudo apt install fail2ban -y
  ```

- ### SSH-Absicherung
  - Nur Key-Auth in `/etc/ssh/sshd_config` aktivieren:
    ```
    PasswordAuthentication no
    ```
  - SSH-Port ändern, z. B.:
    ```
    Port 2222
    ```

- ### Automatische Updates aktivieren
  ```bash
  sudo apt install unattended-upgrades -y
  sudo dpkg-reconfigure unattended-upgrades
  ```

---

## Fazit

Wazuh ist mega praktisch, um ein System zu überprüfen, ob es genug gehärtet ist.

**Ich habe gelernt:**  
- Wie man ein Wazuh installiert und einrichtet  
- Wie wichtig Systemhärtung zusätzlich zur Installation ist  

**Meine Meinung:**  
Wazuh ist komplex in der Einrichtung, bietet aber sehr viele Möglichkeiten, um Systeme sicherer zu machen und Angriffe schneller zu erkennen.
