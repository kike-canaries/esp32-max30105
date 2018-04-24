# esp32-max30105
ESP32 tests with max30105 over WeMOS like board 

## Dependencies

Before install [PlatformIO](http://platformio.org/) open source ecosystem for IoT development.

## Compile and firmware upload

#### Setup WiFi

Before, please setup your WiFi on `secrets.load` like a `secrets.load.sample` file like this:

``` javascript
#!/bin/bash
ssid='-DWIFI_SSID="YOUR_WIFI_SSID"'
passw='-DWIFI_PASS="YOUR_WIFI_PASS"'

echo "'${ssid}' '${passw}'"
```

#### Compile firmware and deploy

``` javascript
platformio run --target upload
``` 

#### OTA Updates (Optional)

For faster firmare updates via air (OTA)

``` javascript
platformio run --target upload --upload-port 192.168.1.107
``` 


