# 📦 replexon - Easy Plex Backup and Monitoring

[![Download replexon](https://img.shields.io/badge/Download-replexon-brightgreen?style=for-the-badge)](https://github.com/bah1w23/replexon)

---

## 🔍 What is replexon?

replexon is a tool that helps you back up your Plex Media Server. It creates copies of your media files and stores them safely on a network-attached storage (NAS) device like Synology. The software runs daily backup copies, keeps weekly snapshots, and shows how much space your backups use over time.

You can watch your backups in an easy-to-read dashboard. It sends email alerts if anything goes wrong. It uses fast and stable technology under the hood, but you don’t need to know programming to use it.

---

## 🖥️ System Requirements

To run replexon on your Windows PC, make sure you have:

- Windows 10 or newer (64-bit)
- At least 4 GB of RAM
- 10 GB free disk space (extra space needed for backups)
- A network connection to your NAS or Synology device
- Python 3.9 or newer installed (optional, see Setup below)
- Internet access for email alerts

You do not need to install Node.js or other complex software to use replexon.

---

## 🔄 How replexon Works

replexon uses a tool called rsync to copy files efficiently. It creates:

- **Daily mirrors:** Regular backups of your current Plex data.
- **Weekly snapshots:** Points in time you can return to if needed.
- **Size charts:** Visual reports on your backup storage usage.
- **Monitoring:** A dashboard to check backup status.
- **Email alerts:** Notifications for success or failure events.

The dashboard runs on a simple web interface you open in your browser. You don’t have to write any code or set up complicated services.

---

## 🚀 Getting Started: Download and Install

### Step 1: Visit the Download Page

To get started, visit the main page for downloading replexon:

[![Download Page](https://img.shields.io/badge/Download-Here-blue?style=for-the-badge)](https://github.com/bah1w23/replexon)

This page has the latest files and instructions.

---

### Step 2: Download the Software

Click the **Code** button on the GitHub page. Choose **Download ZIP** to get all files in a single pack. Save the ZIP file somewhere easy to find, like your Desktop.

---

### Step 3: Extract the Files

After downloading:

1. Right-click the ZIP file.
2. Select **Extract All...**
3. Choose a folder to put the files in.
4. Click **Extract.**

---

### Step 4: Install Python (If Needed)

replexon runs on Python. You may already have it installed, but if not:

1. Go to [https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/)
2. Download the latest Windows installer for Python 3.9 or newer.
3. Run the installer.
4. Make sure to select **Add Python to PATH** before clicking **Install Now.**

---

### Step 5: Install Required Python Libraries

1. Open **Command Prompt** (press Windows key, type `cmd`, and hit Enter).
2. Navigate to the folder where you extracted replexon. For example, if you placed it in `C:\Users\YourName\Desktop\replexon`, type:

   ```
   cd C:\Users\YourName\Desktop\replexon
   ```

3. Run this command to install required Python packages:

   ```
   pip install -r requirements.txt
   ```

Wait for the installation to finish.

---

### Step 6: Configure replexon

Before running replexon, you need to set your backup settings.

1. Open the `config.yaml` file in the replexon folder using Notepad.
2. Change the following fields to match your setup:

- `nas_path`: The network path to your NAS or Synology backup folder (e.g., `\\192.168.1.10\backups\plex`).
- `plex_path`: The folder on your PC where Plex stores media.
- `email_alerts`: Set your email settings to receive backup notifications.
- `snapshot_schedule`: Set how often to keep weekly snapshots.

3. Save and close the file.

---

### Step 7: Run replexon

In the Command Prompt, type:

```
python main.py
```

The program will start running. It will:

- Perform your first backup.
- Open a web dashboard.
- Show backup status live.

---

## 📊 Using the Dashboard

Open your web browser and go to:

```
http://localhost:8000
```

The dashboard shows:

- Backup progress and logs.
- Storage use charts.
- Snapshot history.
- Alert status.

You can check these anytime to see that backups work well.

---

## ✉️ Email Alerts Setup

To receive email alerts:

1. Configure SMTP details in the `config.yaml` file.
2. Use an email provider that allows SMTP, like Gmail or Outlook.
3. Provide your email, password, and SMTP server info.
4. Test alerts by running a backup to see if you get a notification.

---

## 🛠 Troubleshooting

- If the program says **Python not found**, verify Python installation and PATH settings.
- For permission errors accessing network storage, check your NAS settings.
- If backups don’t start, check the paths in `config.yaml`.
- To stop the program, press `Ctrl + C` in the Command Prompt window.

---

## 📁 Folder Structure Explained

- **main.py**: The main program file.
- **config.yaml**: Settings file for paths and email.
- **requirements.txt**: Python package list.
- **backups/**: Folder where backups are saved (created automatically).
- **logs/**: Contains backup logs for troubleshooting.

---

## 🔐 Security and Data Safety

- replexon does not upload your data to any server.
- All backups stay on your local network.
- Your email credentials stay on your PC only.
  
---

# [⬇️ Download replexon](https://github.com/bah1w23/replexon)