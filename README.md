# satellite-firmware
OTA Update for satellites using bin files
OTA Update Flow (ESP32):
Device runs check_update (boot/interval) → fetches manifest.json → compares version with current → if different, downloads .bin → verifies MD5 → flashes firmware → reboots → marks firmware valid.
GitHub hosts manifest.json + firmware. Device checks for updates every 1 hour and on boot. Update is triggered only when the version changes.
