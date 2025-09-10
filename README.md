# Ubuntu Adagios Nagios Docker Script

This repository contains a simple shell script to deploy **Nagios** (with NagiosGraph support) using **Docker Compose** on Ubuntu.  
It automates the directory setup, generates the `docker-compose.yaml` file, and launches the Nagios container.

---

## 📌 Features
- One-click Nagios setup on Ubuntu
- Auto-create required directories (`nagiosetc`, `nagiosvar`, etc.)
- Preconfigured `docker-compose.yaml`
- Accessible via **http://localhost:8081/**
- Default login credentials included

---

## 🚀 Installation & Usage

### 1. Clone the repository
```bash
git clone https://github.com/rajibcse94/adagios-docker-script.git
cd adagios-docker-script
```
### 2. Make the script executable
```bash
chmod +x adagios-docker-script.sh
```
### 3. Run the script
```bash
./adagios-docker-script.sh
```
This will:
### Create required directories in /root/nagios-docker-03/

Generate a docker-compose.yaml

### Start the Nagios container

### 🔑 Default Credentials
```bash
Username: nagiosadmin
Password: nagios
```

### 🛑 Stop Nagios
To stop the container:
```bash
cd /root/nagios-docker-03
```

```bash
docker-compose down
```

### 🔄 Restart Nagios
```bash
cd /root/nagios-docker-03
```
```bash
docker-compose up -d
```
### 📂 Directory Structure
After running the script, the following structure is created:

```bash
/root/nagios-docker-03/
├── nagiosetc
├── nagiosvar
├── customplugins
├── nagiosgraphvar
├── nagiosgraphetc
└── docker-compose.yaml
```
### 🌍 Access Nagios
Open your browser and go to:
```bash
http://localhost:8081
```

---
### Notes
Make sure Docker and Docker Compose are installed before running the script.

Change environment variables in the script if you want custom credentials or timezone.

### 📜 License
This project is licensed under the MIT License.
