# 00 — Connect to the Raspberry Pi remotely via VS Code (setup first)

Source docs: VS Code Remote - SSH extension: https://code.visualstudio.com/docs/remote/ssh

This is the recommended first step for the recipient: install VS Code and the Remote - SSH extension on their Windows laptop and connect to the Raspberry Pi over SSH so they can edit and view the guides and logs.

Why: VS Code provides a friendly UI and the ability to open the Pi's files directly. Robby can assist during the first remote session. 🔧

Prerequisites
- A PC with Visual Studio Code installed
- Internet access
- The Raspberry Pi's SSH enabled (Raspberry Pi Imager advanced options will enable SSH)
- Robby will help with public key setup if keys are used (🔧)

Steps — do this before step 1

1) Install VS Code on Windows
- Download from https://code.visualstudio.com/ and install.

2) Install Remote - SSH extension
- Open VS Code → Extensions (left menu) → search "Remote - SSH" by Microsoft and install.

3) Prepare the Pi for SSH (using Raspberry Pi Imager)
- In Raspberry Pi Imager, choose the OS (use Raspberry Pi Imager throughout), open the advanced options (gear), enable SSH, and set the username `ubuntu` if using Ubuntu, or `pi` if Raspberry Pi OS.

4) Add SSH key (recommended) or use password
- Option A — SSH key (recommended):
  - On Windows, open PowerShell and run `ssh-keygen` (accept defaults). Copy the public key content from `%USERPROFILE%\.ssh\id_rsa.pub`.
  - On the Pi (or before first boot via Imager's advanced options), add the public key to `~/.ssh/authorized_keys` for the user.
  - Robby can help transfer the key via a remote session if needed (🔧).
- Option B — password: you'll be prompted for the password when connecting.

5) Add known hosts and connect from VS Code
- In VS Code: Press F1 → "Remote-SSH: Add New SSH Host..." → Enter `ssh ubuntu@<pi-ip>` (or `ssh pi@<pi-ip>`).
- Choose the config file to update (user config).
- From the Remote Explorer, click the new host and "Connect to Host in New Window".
- On first connect you'll see a prompt about the host key — accept (this stores the host in your known_hosts file).

6) Troubleshooting
- If SSH times out, verify the Pi is on the network and SSH is enabled. If using Raspberry Pi Imager's advanced options, double-check username and key options.
- If the host key changes later, VS Code/ssh will warn — contact Robby if unsure (🔧).

Notes
- Use Ubuntu as default OS unless you want Home Assistant OS specifically for the Home Assistant project. Ubuntu is recommended when the repo docs didn't specify an OS because Robby is most familiar with it.
