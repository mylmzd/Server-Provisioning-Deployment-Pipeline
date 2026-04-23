# Automated Server Provisioning & Web Deployment Pipeline

## 📌 Project Overview
This project focuses on automating Linux server administration and establishing a custom, local CI/CD deployment pipeline. By utilizing advanced Bash scripting, it automates code deployments from GitHub to an Apache web server, handles user permission management securely, and includes a log analysis tool for web traffic monitoring.

> **Note:** The web assets (CSS/JS/HTML) in this repository are sample files used to test the automated deployment pipeline and dynamic manipulation scripts.

## 🚀 Technologies & Tools
- **Scripting & Automation:** Bash Scripting
- **System Administration:** Linux User Management, systemd
- **Web Server:** Apache HTTP Server
- **Version Control:** Git & GitHub (Branch Protection, PR Workflows)

## ⚙️ Key Features & Implementations

### 1. Secure Linux Server Configuration
- Implemented advanced user management by creating specific user accounts with customized home directories.
- Configured secure, passwordless `sudo` privileges to streamline automation scripts without compromising base system security.

### 2. Automated Bash Deployment Pipeline
- Developed a robust Bash script that handles the end-to-end deployment process:
  - **Git Automation:** Conditionally clones the repository or pulls the latest changes if the repo already exists.
  - **Dynamic Content:** Dynamically manipulates HTML content (e.g., injecting variables) before serving.
  - **Automated Deployment:** Seamlessly syncs updated assets to the Apache `DocumentRoot`.

### 3. GitHub Workflow & Branch Protection
- Enforced industry-standard version control best practices.
- Configured **Branch Protection Rules** on the `main` branch.
- Mandated successful **Pull Request (PR)** reviews before merging to prevent direct pushes to production (Demonstrated via the `backgroundfeature` branch workflow).

### 4. Apache Log Analysis Script
- Created a custom Bash utility to parse `/var/log/httpd/access_log`.
- Extracts, sorts, and isolates unique visitor IP addresses to monitor traffic and identify potential anomalous behavior.

## 📂 Repository Structure
- `main` branch: Production-ready code and pipeline destination.
- `backgroundfeature` branch: Used to demonstrate feature development, isolated testing, and PR-based merge workflow.
