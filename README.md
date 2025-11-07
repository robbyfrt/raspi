# Raspberry Pi 5 Starter Pack

This starter pack contains step-by-step guides and resources to help a non-coder set up four projects on a new Raspberry Pi 5. It's intended to be a gift you (Robby) will guide remotely.

## Included projects:

1. Home Assistant (with Shelly BLU T&H)
2. BirdNET-PI (bird sound classification)
3. Pi-hole (adblock DNS, installed without Docker)
4. Extras: media server suggestions and further reading

## Folder structure:

- `home-assistant/` — Home Assistant guide, Shelly onboarding, mobile automation, citizen-science contribution
- `birdnet-pi/` — BirdNET-Pi setup, microphone test, placement tips, Cornell contribution
- `pihole/` — Pi-hole installation and post-install steps (no Docker)
- `extras/` — Media server (Jellyfin) and other optional projects
- `assets/` — Images, screenshots, and additional resources

## Included Hardware:
- Raspberry Pi 5 4GB Starter Kit | 64GB Edition | Official 27W Power Supply | Official Case with Fan | 4K Micro HDMI Cable
- Shelly Blu H&T (temperature and humidity BLE sensor)
- UGREEN USB External Sound Card 2 in 1 to 3.5mm (for BirdNET microphone)
- Boya BY-M1S lavalier microphone
- AZDelivery BMP180 barometric pressure sensor (optional metadata for bird/weather projects)

## Remote Support
The raspberry can be operated remotely with VSCode. Checkout `extras/remote_vscode.md`. This can be done at any point so Robby can help remotely. 🔧

## Notes:

- Use Raspberry Pi Imager throughout for flashing and pre-configuring SSH/username. If an OS was not specified in a project doc, use Ubuntu (username `ubuntu`) — Robby is most familiar with Ubuntu.
- Each project is intended to run as the primary application on the Pi. Running multiple services on a single Pi is possible but adds complexity; the final step can be to containerize everything with Docker, but that's advanced and Robby will guide if you choose to proceed. 🔧

Start with `home-assistant` and then follow the numbered steps in each project's README.

Happy gifting!
