### Create a simple automation from Android

This explains how to create a simple automation using the Home Assistant Android app (no coding required). Robby can join remotely to show the exact steps on your device. 🔧

**Example: Send a notification when balcony temperature exceeds 28°C**

1) Install Home Assistant Android app and log in.
2) Open the app → Menu → Automations (or Settings → Automations & Scenes on the web UI).
3) Add a new automation → Start with an empty automation.
4) Name it: "Hot balcony alert".
5) Trigger: choose "State" or "Numeric state" and select the balcony temperature sensor (e.g., `sensor.balcony_temp`), set threshold > 28°C.
6) Condition: optional (only if someone is home).
7) Action: Send a mobile notification (mobile_app_<your_device> notify). Message example: "Balcony temp is {{ states('sensor.balcony_temp') }}°C — open the app to check."
8) Save and test by temporarily adjusting the threshold or warming the sensor.

Tip: The editor uses dropdowns, so no YAML editing is required. If you see YAML and are unsure, stop and call Robby. 🔧
