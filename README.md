# esp8266 test with max30105

ESP8266 tests with max30105 over WeMOS D1-r2 like board 

## Connection

From SparkFun library of max30105:

Hardware Connections (Breakoutboard to Arduino):
  -5V = 5V (3.3V is allowed)
  -GND = GND
  -SDA = D2 (or SDA in Wemos D1-r2)
  -SCL = D1 (or SCL)
  -INT = Not connected

The MAX30105 Breakout can handle 5V or 3.3V I2C logic. We recommend powering the board with 5V
but it will also run at 3.3V.

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


