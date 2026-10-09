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

A comprehensive, network-enabled IoT indoor environmental monitoring station powered by a **Raspberry Pi**, developed as a practical project (PIF 25/26)[cite: 1, 2, 14, 17]. The system measures various environmental parameters, processes them through a central database, and displays them in real-time via a dynamic kiosk dashboard[cite: 7, 10, 16, 48].

---

## 🛠️ Main Features & Architecture

### 1. Hardware & Workshop (Mechanics & Electronics)
* **Enclosure & Mount:** Custom-made PVC display bracket and base plate (manufactured, drilled, and deburred according to technical drawings) housed inside a painted wooden enclosure[cite: 23, 25, 33, 49].
* **Printed Circuit Board (PCB):** Hand-soldered interface board connecting the Raspberry Pi to sensors, actuators, and the power supply[cite: 26, 28].
* **Sensors:** 
  * **BME280:** Measures temperature, air pressure, and humidity[cite: 31, 33].
  * **BH1750:** Measures light intensity (Lux)[cite: 31, 33].
  * **MQ135 & ADS1115:** Measures air quality/gases via an external 16-bit analog-to-digital converter[cite: 29, 31].
* **Extras:** Indirect LED lighting integrated on the back of the bracket for visual status indication[cite: 37].

### 2. Software, Web Server & Database
* **OS & Kiosk Mode:** Raspberry Pi OS (64-bit) with automatic startup of a Chromium browser in kiosk mode via `labwc`[cite: 3, 7].
* **Web & Database Server:** Docker container running **PHP 8.4** and **Apache**, alongside a relational **MariaDB** database (including phpMyAdmin)[cite: 7, 14, 16].
* **API:** A Data Upload API (POST method) receives sensor data from the Raspberry Pi and stores it in the central database[cite: 18].
* **Dynamic Color-Coding System:** The dashboard visualizes metrics (temperature, humidity, air pressure, light, gas) in real-time and dynamically color-codes them based on threshold values (e.g., green for normal, yellow/red for critical)[cite: 48].

### 3. Network Security & Backup Server
* **Network & DNS:** Configured with static IPs, subnets, and a Pi-hole for local DNS resolution (`pif.local`)[cite: 5, 39].
* **Encryption:** HTTPS security for the web server using self-signed SSL certificates and enforced redirects[cite: 40].
* **Automated Backups:** A dedicated Ubuntu backup server creates daily dumps of the MySQL/MariaDB database via cron jobs (secured with `mysql_config_editor`) and automatically deletes backups older than 7 days[cite: 20, 21].
* **FTP Jail:** A secured FTP user (`ftpbackup`) with a restricted shell (`/bin/false`) and chroot jail enables secure access to backup files[cite: 20, 22, 46].

---

## 🚀 Technologies Used
* **Hardware:** Raspberry Pi 4, ADS1115, BME280, BH1750, MQ135[cite: 3, 29, 31, 33]
* **Operating Systems:** Raspberry Pi OS, Ubuntu Server[cite: 3, 14]
* **Servers & Containers:** Docker, Apache2, MariaDB, PHP 8.4, phpMyAdmin, vsftpd[cite: 7, 14, 16, 20]
* **Scripting & Networking:** Python 3, Bash, Git, Pi-hole, Cisco Packet Tracer[cite: 7, 21, 39, 41]

📊 GitHub Stats

📫 Let's Connect

LinkedIn: Your Name

Twitter/X: @yourhandle

Website: yourwebsite.com
