# kali-Windows-Subsystem-Linux-setup
Automatisiertes Setup-Skript und Anleitung für Kali Linux unter Windows Subsystem for Linux (WSL2). Enthält ein Bash-Skript zur Installation wichtiger Tools (kali-tools-top10, win-kex, optional Wireshark &amp; zsh/oh-my-zsh) sowie Schritt-für-Schritt-Erklärungen zur Installation von WSL und Kali.

🚀 Install Kali Linux on Windows Subsystem for Linux (WSL2)
📖 Step-by-Step Guide
Step 1 – Check Windows version

Make sure you’re running Windows 10 version 2004 (Build 19041) or later or Windows 11.

Press Win + R, type:

winver

If needed, update Windows before continuing.

Step 2 – Open PowerShell as Administrator

Press Win + S → type PowerShell → Right-click → Run as Administrator.

Step 3 – Enable WSL

Run the following command:

wsl --install

This will:

Enable the required features (VirtualMachinePlatform and Windows Subsystem for Linux)

Install the latest WSL2 engine

Set WSL2 as default

Step 4 – Restart Windows

After installation, restart your PC to apply changes.

Step 5 – Verify WSL installation

Check if WSL is installed:

wsl --status

Step 6 – Check available distributions

To see which Linux distributions are available:

wsl --list --online

Step 7 – Install Kali Linux

Install Kali from the command line:

wsl --install -d kali-linux


(Alternatively, you can install it from the Microsoft Store by searching for Kali Linux).

Step 8 – Launch Kali Linux

Start Kali for the first time (from Start Menu or PowerShell):

wsl -d kali-linux

Step 9 – Create user

On the first launch, you’ll be asked to:

Choose a username

Set a password

Step 10 – Update Kali system

Inside Kali terminal, update all packages:

sudo apt update && sudo apt upgrade -y

Step 11 – Install Kali Top 10 Tools

Recommended toolset for penetration testing:

sudo apt install kali-tools-top10 -y

Step 12 – (Optional) Install GUI support (Win-Kex)

If you want a desktop-like GUI:

sudo apt install -y kali-win-kex


Then start it with:

kex --win -s

Step 13 – (Optional) Install extra tools

Wireshark:

sudo apt install wireshark -y


Oh-My-Zsh (improved shell):

sudo apt install zsh -y
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
