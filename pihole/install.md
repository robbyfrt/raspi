## Pi-hole Setup (no Docker) 

Source docs: https://github.com/pi-hole/pi-hole (see "One-Step Automated Install")

**Steps**

1) **Flash Raspberry Pi OS** - using Raspberry Pi Imager.
    - Update the system:

    ```bash
    sudo apt update ; sudo apt upgrade -y
    ```
2) **Install Pi-hole** - via official one-line installer:
   
    ```bash
    curl -sSL https://install.pi-hole.net | bash
    ```
    - Follow the interactive prompts to pick an upstream DNS provider and set the web admin password.


3) **Post-install steps** 
    - Set a DHCP reservation in your router or configure a static IP on the Pi.
    - Point your router's DHCP DNS option to the Pi's IP, or set devices manually to use the Pi's DNS.
    - Access the admin UI at `http://<pi-ip>/admin`.

4) **Troubleshooting**
    - If using Wi‑Fi, DHCP lease changes can break Pi-hole; use DHCP reservation.
    - If the router won't accept custom DNS, use Pi-hole's built-in DHCP server (disable router DHCP first).
    - For blocked sites, check Query Log → whitelist as necessary. 🔧

### Tips and Hints

- DHCP vs static IP: It's usually better to set a DHCP reservation in the router than force a static IP on the Pi. Ensure the Pi's IP persists.
- Router compatibility: Some routers don't allow custom DNS addresses in DHCP settings; check router docs.
- Local network services: If you use local hostnames, enable/configure Pi-hole's DHCP or DNS records accordingly.
- Overblocking: If sites are blocked, check the query log and whitelist as needed.
- Admin password: Save the web UI password or bind Pi-hole to single-sign-on if desired.