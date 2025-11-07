### Contribute weather data to citizen science

**Options**

- Holfuy (https://holfuy.com/en/weather/605) — check format/support for Shelly sensors
- Windguru, Meteobridge, Weather Underground — check platform upload requirements

**Approach**

1) Choose a target service and read their station registration and data format requirements.
2) Create an account and register a station if required.
3) Use Home Assistant to forward sensor data via MQTT or REST:
   - Create an automation that posts JSON payloads to the service endpoint.

**Example automation (conceptual)**
- Trigger: time pattern (every 10 minutes)
- Action: Call REST service with payload:

- ```json
  {"temp": {{ states('sensor.balcony_temp') }}, "hum": {{ states('sensor.balcony_humidity') }}}
  ```

  Note: Payload and authentication depend on target service. Robby can help configure endpoint and credentials. 🔧

**Privacy and safety**
- Sharing location-tagged data reveals location. Consider reducing coordinate precision and discuss risks with Robby before publishing.

