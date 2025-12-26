BinNode-Tunnel

Secure, Fast, and Simple Intranet Penetration Tool

![alt text](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20RaspberryPi-blue)

![alt text](https://img.shields.io/badge/Status-Stable-green)

BinNode-Tunnel is a lightweight networking tool that allows you to securely access your home computers, office servers, NAS, or Raspberry Pi devices from anywhere in the world—without needing a public IP address or complex router settings.

Whether you need Remote Desktop (RDP) access, SSH management, or access to internal websites, BinNode-Tunnel makes it one-click easy.
✨ Key Features

    ⚡ Blazing Fast (P2P): Uses advanced Peer-to-Peer technology. If network conditions allow, your devices connect directly to each other for maximum speed and lowest latency, bypassing central servers.

    🔒 Secure & Private: Your network is isolated using a unique Network ID and Password. Only devices with the matching credentials can see or access each other.

    🖥️ Native Windows Experience: Runs quietly in the system tray. Features a visual configuration window—no command line required.

    🐧 Friendly Linux Interface: Even on Linux servers, it provides a BIOS-style graphical menu (TUI) for easy configuration. No need to hand-edit JSON files.

    🔌 Always On: Automatically reconnects if the internet drops and manages port mappings automatically.

📥 Download

Please download the version matching your device:
OS	Architecture	File Name	For Devices
Windows	64-bit	ZincNode.exe	Standard Windows 10/11 PCs
Linux	64-bit	node-bin	Standard Linux Servers / VPS
Linux	ARM64	ZincNode_linux_arm64	Raspberry Pi 4/5, Orange Pi
Linux	ARMv6	ZincNode_linux_armv6	Raspberry Pi Zero / 1 / 2
🚀 Quick Start Guide
🪟 Windows Users

    Run: Download ZincNode.exe and double-click it.

    First Setup:

        A Configuration Window will appear on the first run.

        Network ID: Create a group name (e.g., MyHomeNet).

        Net Password: Set a secure password.

        Hostname: Name this computer (e.g., Win10-LivingRoom).

        Services: (Optional) Add services you want to share (see "Service Configuration" below).

    Save & Go:

        Click "Save Configuration". The app will connect and minimize to the system tray (bottom right).

        Auto-Start: Right-click the tray icon -> Check "Start with Windows".

        Manage: Right-click the tray icon -> Configuration... to change settings anytime.

🐧 Linux / Raspberry Pi Users

    Permission:
    code Bash

    
chmod +x ./node-bin

  

Run:
code Bash

        
    ./node-bin

      

    Interactive Setup:

        If no config exists, a blue Graphical Interface will appear in your terminal.

        Use Tab or Arrow Keys to navigate.

        Enter your ID, Password, and Hostname.

        Select [ SAVE & START ] and press Enter.

    Edit Config Later:

        To change settings later, run: ./node-bin -setup

⚙️ Service Configuration

"Services" are the functions on this computer that you want to access from other devices.

In the configuration window (under "Local Services"), fill in:
Field	Description
Service Name	A nickname for the service (e.g., rdp, ssh, nas-web).
Local IP	Usually 127.0.0.1 (meaning this device itself).
Port	The actual port number the service is running on.
Common Examples
Scenario 1: Remote Desktop (RDP) to this Windows PC

    Service Name: rdp

    Local IP: 127.0.0.1

    Port: 3389 (Default Windows RDP port)

Scenario 2: SSH into this Linux Server

    Service Name: ssh

    Local IP: 127.0.0.1

    Port: 22 (Default SSH port)

Scenario 3: Access a Local Website / NAS Admin

    Service Name: nas-web

    Local IP: 127.0.0.1

    Port: 80 (or 8080)

🌐 How to Connect?

Once Computer A and Computer B are running BinNode-Tunnel with the same Network ID/Password:

    Open Dashboard:

        On Computer A, right-click the Tray Icon -> Open Management UI (or visit http://127.0.0.1:8888).

    Check Status:

        You will see Computer B in the list.

        BinNode-Tunnel automatically maps Computer B's service to a random port on Computer A (e.g., :10022).

    Connect:

        If Computer B's SSH is mapped to port 10022 on Computer A.

        You simply connect to: 127.0.0.1:10022.

❓ FAQ

Q: The Web UI says the connection is "Direct". What does that mean?
A: Great news! It means your devices are connected directly (P2P). Data travels straight between them, offering the best speed and security without passing through a relay server.

Q: What if P2P fails?
A: Don't worry. BinNode-Tunnel automatically switches to "Relay Mode," forwarding traffic securely through the server to ensure you can always connect.

Q: Can I change the Web Dashboard port?
A: Yes. Edit config.json and change the webserver_port value.
