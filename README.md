# ArduinoGPS - released under GPLv3

Ingredients:
- Arduino MEGA 2560 (Should run on a uno with some modifications, to be tested)
- 0.96" SPI OLED display SSD1306 (spi)
- GPS Ublox (VK2828U7G5LF) (serial)
- 3 Axis Electronic Compass Magnetic Sensor (GY-273 HMC5883L) (i2c bus)
- Micro SD memorycard module (spi)
- PS2 joystick board (analog/digital)

Goals reached:
- Display custom bootlogo
- Display location in DDD MM.MMM format
- Display heading
- Display time
- Display altitude
- Display number of satellites found
- Notify when fix lost
- Pop-up menu when joystick is pressed

Goals to reach:
- Generate GPX track on SD card
- Set destination using joystick
- Import destinations from GPX files (SD card)
- Store settings on SD card
- Determine timezone based on location (now fixed +hours in code (buggy))
- Possible upgrade the screen to a bigger one, with better resolution
- Design 3d printable case
- ...

Pins in use:
- A0 - Joystick X-axis
- A1 - Joystick Y-axis
- 6  - Joystick button
- 7  - OLED chip select
- 8  - SD card chip select
- 18 - GPS RX
- 19 - GPS TX
- 20 - SDA compas
- 21 - SCL compas
- 50 - MISO to SD card
- 51 - MOSI to SD card and OLED display
- 52 - SCK to SD card and OLED display

The reason I use the Arduino MEGA 2560 (during development) is because this board has more ports, and also multiple serial connections. Since the GPS is serial (connected to Serial1) we can still use Serial for debugging. When switching to the Arduino UNO SoftSerial could be an option, but this has some limitations. If debugging is finished I will probably switch to an UNO.

All items are availabla at chinese online stores, but please consider supporting Arduino by buying an original board.
Since we use displaydrivers from adafruit, consider buying there displays too...
We also use the TinyGPS++ library from Mikel Hart, thanks for your great work.
