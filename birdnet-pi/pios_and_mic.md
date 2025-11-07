### Pi OS and microphone setup

Source docs: https://github.com/Nachtzuster/BirdNET-Pi (Installation section)

#### Steps

1) **Prepare OS (Raspberry Pi Imager)** - Use Raspberry Pi Imager to flash RaspiOS Bookworm. 

2) **Update system**

    ```bash
    sudo apt update ; sudo apt upgrade -y
    ```

3) **Attach and test the UGREEN USB-to-3.5mm dongle**  
    - Install ALSA utilities:

        ```bash
        sudo apt install -y alsa-utils
        ```

    - List devices:

        ```bash
        arecord -l
        aplay -l
        ```

4) **Test recording**
    ```bash
    arecord -D plughw:1,0 -f cd -t wav -d 5 test.wav
    aplay test.wav
    ```

    Replace `plughw:1,0` with the card/device numbers from `arecord -l`.

5) **Optional: Adjust levels** - Use `alsamixer` to set capture gain and unmute channels.

6) **Install BirdNET-Pi** - Follow the official installer (see README):

    ```bash
    curl -s https://raw.githubusercontent.com/Nachtzuster/BirdNET-Pi/main/newinstaller.sh | bash
    ```

Notes
- If the mic is quiet, consider a small USB-powered preamp. The gifted UGREEN dongle + Boya BY-M1S are a good starting point.
- For continuous recording, prefer external SSD or rotate storage to protect SD card endurance. 🔧
