## Arduino Projects

## Various Configurations & Guides

### CH340 Driver Installation Guide
1. Connect the ESP8266-01 to the USB Port.
2. Install the Driver.
3. Upload the code from the Arduino IDE.

### Nano Configuration
1. Open IDE
2. Try to Upload
3. You get the error message
4. Open Device Manager and uninstall the driver
5. Install the CH341 Driver
6. Use the old bootloader

### ESP32 Cam Configuration
- **Board:** ESP Wrover Kit (all versions)
- **CPU Frequency:** 240MHz (WiFi/BT)
- **Flash Frequency:** 80MHz
- **Flash Mode:** QIO
- **Flash Size:** 4MB (32Mb)
- **Partition Scheme:** Huge App (3MB No OTA/1MB SPIFFS)
- **PSRAM:** Disabled

### ESP8266-01 Pins
- **GPIO0:** H - Start Up, L - Flash, should have 10K pull up resistor
- **GPIO1(TX):** L, H, Input by default, Controls the blue LED (on when low, off when high). At the start it is always an output for a short time, so use 330 Ohms resistor between this pin and the input
- **GPIO2:** H - Start Up - should have 10K pull up resistor when used as output. It is tough to use this pin as input
- **GPIO3(RX):** L, H, Output by default

**GPIO0** and **GPIO2** need to have pull-up resistors for normal startup if they are used as Inputs

**Example:**
`GPIO1 - input`
`GPIO3 - input`
`GPIO2 - output with pull up resistor`
