### Onboard the Shelly BLU T&H

Source docs: Shelly product docs and Home Assistant Integrations (see `home-assistant/README.md` for main reference).

**Overview**

The Shelly BLU T&H is a BLE temperature & humidity sensor. Home Assistant can read BLE sensors via the Shelly integration or local Bluetooth. Home Assistant OS on Raspberry Pi 5 includes Bluetooth support.

**Steps**

1) **Powering the Shelly** - Install the batteries and place the sensor near the Pi (2–3 m) for initial onboarding.

2) **Install Shelly App (optional)** - You may use the Shelly smartphone app to put the BLU into onboarding mode.

3) **Add via Home Assistant** (Settings → Devices & Services → Add Integration)
    - Search for "Shelly" and follow prompts. If the BLU uses Shelly Cloud, sign in to your Shelly account; otherwise add via Bluetooth.
    - If adding over Bluetooth and the device isn't found, enable the Bluetooth integration in Home Assistant and restart the Pi.

4) **Confirm entities** - You should see entities for temperature, humidity, and battery. Rename (e.g., `sensor.balcony_temp`).

5) **Troubleshooting and Robby support**
    - If not discovered: move the Shelly closer, reboot Home Assistant, and check System → Hardware for Bluetooth.
    - If logs show pairing or permission errors, contact Robby for a remote troubleshooting session. 🔧


