ReefCube BLE Logger v46 — Chrome Web Bluetooth
================================================
Compatible firmware (as inspected 2026-10-17):
  nRF52840_Logger_v46_BMA400_AS7343_AutoExposure_VBAT_NA.ino

Hardware: XIAO nRF52840 / Sense, XIAO Logger HAT, external BMA400 and AS7343.
The on-board Sense IMU is not used by this firmware. Vbat is NA.

Firmware GATT settings:
  ENABLE_LEGACY_A000_SERVICE = true
  ENABLE_NUS_SERVICE = false
  Service: 7E400000-B5A3-F393-E0A9-E50E24DCCA9E
  Command: 7E400001-B5A3-F393-E0A9-E50E24DCCA9E (write)
  Output:  7E400002-B5A3-F393-E0A9-E50E24DCCA9E (notify)

SETUP
1. Put ReefCube_BLE_Logger_v46_Chrome.html on an HTTPS website.
   Example: create a v46/ directory in your existing GitHub Pages repository
   and upload the file as v46/index.html. Do not overwrite the v41 page unless
   you intend to replace it. The URL then is https://<username>.github.io/v46
   here: https://matthiasbirkich.github.io/v46
2. Use Chrome on an Android phone or supported desktop Chromium browser with BLE.
   Standard Chrome on an iPad/iPhone does not support Web Bluetooth.
3. Wake the logger using the reed magnet / reset as appropriate.
4. Click Connect; select UW52840-RC46; grant Bluetooth access.
5. Verify STATUS, RTC_CHECK, BMA_CHECK and AS_CHECK.
6. To log once per minute, click 'Set 1 minute'; confirm GET_INTERVAL reports 1.
7. Click START. After testing, reconnect and click COUNT and CSV export.
8. To download data, click Last 10 / Last 100 / All CSV and wait for CSV_END;
   then click 'Save received CSV'.

NOTICE
- This version was matched by source inspection to the uploaded firmware.
  Actual BLE integration, sensor behaviour and runtime must be tested on hardware.
- The v46 firmware command SETINT takes SECONDS, not minutes.
  This app uses SET_INTERVAL_MIN=1 (minutes) to avoid ambiguity.
- In firmware v46, battery-voltage logging is intentionally disabled (NA).
- Formatting the flash is not an app command; do not erase the logger's logs
  without backing them up.
- To test the latest firmware with a v41-only NUS app, first switch the app
  to this v46 BLE service or change the firmware's GATT configuration.
- Web Bluetooth requires a secure origin: HTTPS or localhost. Opening the HTML
  as a local file is not the recommended distribution method.
