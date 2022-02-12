# English Translation from original github link below
https://github.com/robo8080/M5Paper_Keyboard <br>

# M5Paper_Keyboard
M5Paper_Keyboard is a serial Interface keyboard that runs on M5Paper.<br>
It also supports BLE keyboard Mode.<br><br>
This is a modified version of the M5Paper_FactoryTest keyboard process.。<br>
Click here for the original base.<br>
M5Paper_FactoryTest <https://github.com/m5stack/M5Paper_FactoryTest><br>

![画像1](images/image1.png)<br><br>

### What you need ###
* [M5Paper](http://www.m5stack.com/ "Title")<br>
* Arduino IDE (I checked the operation with 1.8.13.)<br>
* [Arduino core for the ESP32](https://github.com/espressif/arduino-esp32 "Title")
* [M5Paper Library](https://github.com/m5stack/M5EPD "Title")
* [NimBLE-Arduino Library](https://github.com/h2zero/NimBLE-Arduino "Title") 
* [ESP32 NimBLE Keyboard library](https://github.com/wakwak-koba/ESP32-NimBLE-Keyboard "Title") 
<br>

The library is easy to install from the Arduino IDE's Sketch | Include Libraries | Manage Libraries ....

### Serial port specifications ###
* Use M5 Paper's PORT C. The settings are as follows.<br>
    // Serial2.begin(unsigned long baud, uint32_t config, int8_t rxPin, int8_t txPin, bool invert)<br>
    Serial2.begin(115200, SERIAL_8N1, 19, 18);

### supplement ###
* To turn off the power, use the "BATTERY OFF" button on the back of the M5 Paper.<br>
* The "Fn" key is unused, so please use it for function expansion.<br><br>

---

The M5Stack program (M5Stack_Serial2_test) for checking the operation of M5Paper_Keyboard is prepared.<br>

![画像2](images/image2.png)<br><br>

### What you need ###
* [M5Stack](http://www.m5stack.com/ "Title")<br>
* Arduino IDE (I checked the operation with 1.8.13.)<br>
* [Arduino core for the ESP32](https://github.com/espressif/arduino-esp32 "Title")<br>
* [M5Stack Library](https://github.com/m5stack/M5Stack "Title")
* [LovyanGFX](https://github.com/lovyan03/LovyanGFX "Title")

The library is easy to install from the Arduino IDE's Sketch | Include Libraries | Manage Libraries ....

### Serial port specifications ###
* M5StackのPORT Cを使用します。設定は以下の通り。<br>
    // Serial2.begin(unsigned long baud, uint32_t config, int8_t rxPin, int8_t txPin, bool invert)<br>
    Serial2.begin(115200, SERIAL_8N1, 16, 17);<br><br>
Note: PSRAM must be disabled when using M5Stack Fire there is.<br><br>
![画像3](images/image3.png)<br><br>

---

### How to make a cross cable ###
* A crossover cable is required to connect M5Stack and M5Paper_Keyboard with M5StackSerial2_test.<br>
Unplug the red cable (power supply) and cross the white and yellow cables.<br><br>
![画像4](images/image4.png)<br><br>
The cable can be easily pulled out by lifting the claw part of the connector with a sharp object. <br><br>
![画像5](images/image5.png)<br><br>
<br>

---

### When using as a BLE keyboard ###

Uncomment "#define USE_BLE_KEYBOARD" in "keyboard_config.h" and build.。<br><br>
![画像6](images/image6.png)<br><br>
Pair with "M5 Paper-Keyboard".
How to switch between half-width and full-width (confirmed)<br>
iPhone11(iOS14) ： [Ctrl] + [Space]<br>
Android(FIRE HD 8) ： [Shift] + [Space]<br>
Windows 10 ： [Alt] + [`]<br>
<br><br>

