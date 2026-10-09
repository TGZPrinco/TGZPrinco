Hi there, I'm Princo 👋

🚀 Welcome to my GitHub profile!

I'm a passionate developer who loves building things for the web and exploring new technologies. Here you'll find a showcase of my latest projects, skills, and how to reach me.

🛠️ Tech Stack & Skills

Languages: JavaScript, PHP, Python, HTML/CSS

Frameworks & Libraries: React, Node.js, Express, Tailwind CSS

Tools & Platforms: Git, GitHub, Docker, VS Code

Databases: MYSQL, MariaDB

📂 Featured Projects

Here are some of the projects I've been working on recently:

Final Exam Project

# 🏡 Portable Indoor Feedback Station (PIF)

A comprehensive, network-enabled IoT indoor environmental monitoring station powered by a **Raspberry Pi**, developed as a practical project (PIF 25/26). The system measures various environmental parameters, processes them through a central database, and displays them in real-time via a dynamic kiosk dashboard.

---

## 🛠️ Main Features & Architecture

### 1. Hardware & Workshop (Mechanics & Electronics)
* **Enclosure & Mount:** Custom-made PVC display bracket and base plate (manufactured, drilled, and deburred according to technical drawings) housed inside a painted wooden enclosure.
* **Printed Circuit Board (PCB):** Hand-soldered interface board connecting the Raspberry Pi to sensors, actuators, and the power supply.
* **Sensors:** 
  * **BME280:** Measures temperature, air pressure, and humidity.
  * **BH1750:** Measures light intensity (Lux).
  * **MQ135 & ADS1115:** Measures air quality/gases via an external 16-bit analog-to-digital converter.
* **Extras:** Indirect LED lighting integrated on the back of the bracket for visual status indication.

### 2. Software, Web Server & Database
* **OS & Kiosk Mode:** Raspberry Pi OS (64-bit) with automatic startup of a Chromium browser in kiosk mode via `labwc`.
* **Web & Database Server:** Docker container running **PHP 8.4** and **Apache**, alongside a relational **MariaDB** database (including phpMyAdmin).
* **API:** A Data Upload API (POST method) receives sensor data from the Raspberry Pi and stores it in the central database.
* **Dynamic Color-Coding System:** The dashboard visualizes metrics (temperature, humidity, air pressure, light, gas) in real-time and dynamically color-codes them based on threshold values (e.g., green for normal, yellow/red for critical).

### 3. Network Security & Backup Server
* **Network & DNS:** Configured with static IPs, subnets, and a Pi-hole for local DNS resolution (`pif.local`).
* **Encryption:** HTTPS security for the web server using self-signed SSL certificates and enforced redirects.
* **Automated Backups:** A dedicated Ubuntu backup server creates daily dumps of the MySQL/MariaDB database via cron jobs (secured with `mysql_config_editor`) and automatically deletes backups older than 7 days.
* **FTP Jail:** A secured FTP user (`ftpbackup`) with a restricted shell (`/bin/false`) and chroot jail enables secure access to backup files.

---

## 🚀 Technologies Used
* **Hardware:** Raspberry Pi 4, ADS1115, BME280, BH1750, MQ135
* **Operating Systems:** Raspberry Pi OS, Ubuntu Server
* **Servers & Containers:** Docker, Apache2, MariaDB, PHP 8.4, phpMyAdmin, vsftpd
* **Scripting & Networking:** Python 3, Bash, Git, Pi-hole, Cisco Packet Tracer
