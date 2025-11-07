## Project 2 — BirdNET-Pi (Raspberry Pi 5)

Source docs: https://github.com/Nachtzuster/BirdNET-Pi (start here) and https://blog.berrybase.de/bird-net-pi-vogelstimmenklassifizierung-diy-rpi/ (supporting info)

Screenshot (local):
![BirdNET-Pi overview](../assets/images/birdnet_overview.png)

**Steps**
1.  `pios_and_mic.md` (flash Raspberry Pi OS using Raspberry Pi Imager & attach and test microphone: UGREEN USB external sound card + Boya mic)
2. `placement_tips.md` (optimize microphone placement on the balcony)
3. `cornell_contribution.md` (prepare clips and upload to Macaulay Library / eBird)


**Required Hardware**
- UGREEN USB External Sound Card 2 in 1 (USB to 3.5mm) — used to connect the Boya BY-M1S lapel microphone
- Boya BY-M1S lapel microphone — recommended for clearer bird audio capture

### Hints 

- CPU and model size: BirdNET models are CPU-intensive. If performance is poor, reduce model size or consider using an external accelerator. Robby can help choose the right model and tune the system. 🔧
- Storage endurance: Continuous recording wears SD cards fast. Prefer an external SSD or set up periodic cleanup of old audio files.
- Microphone noise: Wind/stream noise increases false positives — use a windshield and proper placement.
- Time sync: Ensure NTP is configured so timestamps are accurate for uploads.
- Manual review: Automatically detect species but manually review clips before public uploads to Cornell or BirdWeather.

