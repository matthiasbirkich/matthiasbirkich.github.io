ReefCube BLE Logger v41 — Chrome Web Bluetooth

when you put it to an repository, rename it to index.html

SETUP
1. Put ReefCube_BLE_Logger_v46_Chrome.html on an HTTPS website.
   Example: create a v46/ directory in your existing GitHub Pages repository
   and upload the file as v46/index.html. Do not overwrite the v46 page unless
   you intend to replace it. The URL then is https://<username>.github.io
   here: https://matthiasbirkich.github.io
2. Use Chrome on an Android phone or supported desktop Chromium browser with BLE.
   Standard Chrome on an iPad/iPhone does not support Web Bluetooth.
3. Wake the logger using the reed magnet / reset as appropriate.
4. Click Connect; select UW52840-CLEAN41; grant Bluetooth access.
5. Verify STATUS, RTC_CHECK, BMA_CHECK and AS_CHECK.
6. SET_INT_30
7. START...