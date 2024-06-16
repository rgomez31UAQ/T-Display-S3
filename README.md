<h1 align = "center"> 🌟T-Display-S3🌟</h1>

[![PlatformIO CI](https://github.com/Xinyuan-LilyGO/T-Display-S3/actions/workflows/platformio.yml/badge.svg)](https://github.com/Xinyuan-LilyGO/T-Display-S3/actions/workflows/platformio.yml)
[![Arduino_CI](https://github.com/Xinyuan-LilyGO/T-Display-S3/actions/workflows/arduino_ci.yml/badge.svg)](https://github.com/Xinyuan-LilyGO/T-Display-S3/actions/workflows/arduino_ci.yml)

## 1️⃣Support Product

| Product (PinMap)        | SOC        | Flash | PSRAM    | Resolution | Size     |
| ----------------------- | ---------- | ----- | -------- | ---------- | -------- |
| [T-Display-S3][1]       | ESP32-S3R8 | 16MB  | 8MB(OPI) | 170x320    | 1.9 Inch |
| [T-Display-S3-Touch][2] | ESP32-S3R8 | 16MB  | 8MB(OPI) | 170x320    | 1.9 Inch |
| [T-Display-S3-MIDI][3]  |            |       |          |            |          |

[1]: https://www.lilygo.cc/products/t-display-s3?variant=42589373268149
[2]: https://www.lilygo.cc/products/t-display-s3?variant=42351558590645
[3]: https://www.lilygo.cc/products/t-display-s3?variant=43164741632181

## 2️⃣Examples

```
./examples/
├── Arduino_GFXDemo              #  Arduino_GFX example
├── Arduino_GFX_PDQgraphicstest  #  Arduino_GFX example
├── GetBatteryVoltage            #  Get battery voltage example
├── I2CScan                      #  Scan for external devices using I2C
├── ImageScroll                  #  Image scrolling example by @Rudi Ackermann
├── MPR121TouchSensor            #  Example of using MPR121 capacitive touch
├── PCBClock                     #  TFT_eSPI PCBClock example by @VolosR
├── PokerS3                      #  TFT_eSPI PokerS3  example by @VolosR
├── SerialExample                #  Example of using serial communication
├── T-Display-S3-MIDI            #  T-Display-S3-MIDI Shield example
├── TFT_Rainbow                  #  TFT_eSPI example
├── factory                      #  factory example
├── lv_demos                     #  lvgl demo                        
├── nes                          #  NES game emulator
├── ota                          #  Over-the-air upgrade example
├── sd                           #  T-Display-TF Shield example
├── tft                          #  TFT_eSPI example
├── touch_test                   #  Capacitive touch test example
├── usb_hid_pad                  #  Capacitive Touch Screen Simulation USB HID Example
├── ULP_ADC                      #  Example of ADC detection for ULP-FSM(arduino_esp32 version: 3.0.0-rc3)
└── ULP_Count                    #  Example of register counting for ULP-FSM(arduino_esp32 version: 3.0.0-rc3)
```

## 3️⃣ PlatformIO Inicio rápido (recomendado)

1. Install [Visual Studio Code](https://code.visualstudio.com/) y [Python](https://www.python.org/)
2. Busca el plugin `PlatformIO` en la extensión `VisualStudioCode` e instálalo.
3. Una vez finalizada la instalación, deberá reiniciar `VisualStudioCode`.
4. Después de reiniciar `VisualStudioCode`, seleccione `File` en la esquina superior izquierda de `VisualStudioCode` -> `Open Folder` -> seleccione el directorio `T-Display-S3`.
5. Espere a que finalice la instalación de las bibliotecas dependientes de terceros
6. Haga clic en el archivo `platformio.ini` y en la columna `platformio
7. Descomenta una de las líneas `default_envs = xxxx` para asegurarte de que sólo funciona una línea
8. Haga clic en el símbolo (✔) en la esquina inferior izquierda para compilar
9. Conectar la placa al ordenador USB
10. Haga clic en (→) para cargar el firmware
11. Haga clic en (símbolo de clavija) para supervisar la salida serie
12. Si no se puede escribir, o el dispositivo USB sigue parpadeando, por favor, compruebe el **FAQ** a continuación


## 4️⃣  Arduino IDE Manual installation

1. Instalar [Arduino IDE](https://www.arduino.cc/en/software)
2. Instalar [Arduino ESP32 V 2.0.5 o superior y por debajo de V3.0](https://docs.espressif.com/projects/arduino-esp32/en/latest/)
3. Descargar `T-Display-S3` , mover a la carpeta de la biblioteca Arduino (e.g. C:\Users\YourName\Documents\Arduino\libraries)
4. Copie todas las carpetas de la [carpeta lib](./lib/) en la carpeta de bibliotecas de Arduino (por ejemplo, C:\Users\SuNombre\Documents\Arduino\libraries).
5. Entre en el directorio descargado `T-Display-S3/examples`.
6. Seleccione cualquier ejemplo y haga doble clic en `any_example.ino` para abrirlo
7. Abra ArduinoIDE ,`Tools` ，Haga su selección de acuerdo con la siguiente tabla.
    | Arduino IDE Setting                  | Value                             |
    | ------------------------------------ | --------------------------------- |
    | Board                                | **ESP32S3 Dev Module**            |
    | Port                                 | Your port                         |
    | USB CDC On Boot                      | Enable                            |
    | CPU Frequency                        | 240MHZ(WiFi)                      |
    | Core Debug Level                     | None                              |
    | USB DFU On Boot                      | Disable                           |
    | Erase All Flash Before Sketch Upload | Disable                           |
    | Events Run On                        | Core1                             |
    | Flash Mode                           | QIO 80MHZ                         |
    | Flash Size                           | **16MB(128Mb)**                   |
    | Arduino Runs On                      | Core1                             |
    | USB Firmware MSC On Boot             | Disable                           |
    | Partition Scheme                     | **16M Flash(3M APP/9.9MB FATFS)** |
    | PSRAM                                | **OPI PSRAM**                     |
    | Upload Mode                          | **UART0/Hardware CDC**            |
    | Upload Speed                         | 921600                            |
    | USB Mode                             | **CDC and JTAG**                  |
    * Las opciones en negrita son obligatorias, las demás se seleccionan en función de las condiciones reales.

8. Espere a que se complete la compilación y la escritura.
9. Si no se puede escribir, o el dispositivo USB sigue parpadeando, por favor revise el **FAQ** a continuación

* También puede elegir `LilyGo T-Display-S3` como placa, pero la tabla de particiones se fija en **16M Flash (3M APP/9.9MB FATFS)**.
* [T-Display-S3 Arduino IDE Record](https://www.youtube.com/watch?v=PgtxisFvMcc)

## 5️⃣ ESP-IDF

* `T-Display-S3` esp-idf version example, please jump to this [LilyGo-Display-IDF](https://github.com/Xinyuan-LilyGO/LilyGo-Display-IDF)

## 6️⃣ Micropython

* [russhughes/st7789s3_mpy](https://github.com/russhughes/st7789s3_mpy)
* [Micropython](https://github.com/Xinyuan-LilyGO/lilygo-micropython)


# 7️⃣ ESP32 basic examples

* [BLE Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/BLE)
* [WiFi Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/WiFi)
* [SPIFFS Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/SPIFFS)
* [FFat Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/FFat)
* For more examples of esp32 chip functions, please refer to [arduino-esp32-libraries](https://github.com/espressif/arduino-esp32/tree/master/libraries)


# 8️⃣ Resource

| Product(PinMap)         | schematic                                               | Dimensions                  | PCB 3D                                    | PinMap                                   |
| ----------------------- | ------------------------------------------------------- | --------------------------- | ----------------------------------------- | ---------------------------------------- |
| [T-Display-S3][1]       | [schematic](./schematic/T_Display_S3.pdf)               | [DWG](./dimensions/PCB.dwg) | [STP](./dimensions/t-display-s3-full.stp) | [PinMap](./image/T-DISPLAY-S3.jpg)       |
| [T-Display-S3 Touch][1] | [schematic](./schematic/T_Display_S3.pdf)               | [DWG](./dimensions/PCB.dwg) | [STP](./dimensions/t-display-s3-full.stp) | [PinMap](./image/T-DISPLAY-S3-TOUCH.png) |
| [T-Display-S3-MIDI][1]  | [schematic](./schematic/SCH_T-Display-S3-MIDI_V1.1.pdf) | DWG                         | STP                                       |                                          |


## 9️⃣ FAQ

1. **The screen does not light up when using battery?**
   * When T-Display-S3 is powered by battery, GPIO15 must be set to HIGH to turn on the backlight.
   * Please add the following two lines at the beginning of the setup
   ```C++
   void setup(){
      //Turn on display power
      pinMode(15, OUTPUT);
      digitalWrite(15, HIGH);
   }
   
   ```
2.  **The program can be written normally, but there is still no display after writing**
   * If you are using **TFT_eSPI**, then you can try running `Arduino_GFXDemo` first. If nothing is displayed after writing, you can determine that there is a problem with the hardware.
   * If `Arduino_GFXDemo` is written normally, but **TFT_eSPI** is not displayed, then it can be judged that `User_Setup_Select` has been overwritten, then please read the third article of **FAQ** to reconfigure **TFT_eSPI**
3. **How to update **TFT_eSPI**, or confirm whether the **TFT_eSPI** pin configuration is correct?**
   * Search for **TFT_eSPI** in the ArduinoIDE library manager and click Update.
   * Enter the default library manager installation location and open the **TFT_eSPI** folder. The default installation location is:(e.g. C:\Users\YourName\Documents\Arduino\libraries)
   * Open User_Setup_Select.h, comment out #include <User_Setup.h> which is enabled by default, or delete it
   * Search **Setup206_LilyGo_T_Display_S3**, find it, cancel the previous comment, then save it, and finally close it, so that TFT_eSPI uses the pin definition of T-Display-S3 by default
   ```c++
   #include <User_Setups/Setup206_LilyGo_T_Display_S3.h>     // For the LilyGo T-Display S3 based ESP32S3 with ST7789 170 x 320 TFT
   ```
4. **Can't upload any sketch，Please enter the upload mode manually.**
   * Connect the board via the USB cable
   * Press and hold the **BOOT** button , While still pressing the **BOOT** button
   * Press **RST** button
   * Release the **RST** button
   * Release the **BOOT** button (If there is no **BOOT** button, disconnect IO0 from GND.)
   * Upload sketch
   * Press the **RST** button to exit download mode

5. **If you use external power supply instead of USB-C, please turn off the CDC option. This is because the board will wait for USB access when it starts.**

   * For Arduino IDE users, it can be turned off in the options , Please note that turning off USB CDC will turn off Serial redirection to USBC. At this time, you will not see any Serial message output when opening the port from USB-C, but output from GPIO43 and GPIO44.

   ```c
   Tools -> USB CDC On Boot -> Disable
   ```

   * For platformio users, you can add the following compilation flags in the ini file

   ```c
   build_flags =
       ; Enable -DARDUINO_USB_CDC_ON_BOOT will start printing and wait for terminal access during startup
       ; -DARDUINO_USB_CDC_ON_BOOT=1

       ; Enable -UARDUINO_USB_CDC_ON_BOOT will turn off printing and will not block when using the battery
       -UARDUINO_USB_CDC_ON_BOOT
   ```

6. **If all the above are invalid, please flash the factory firmware for quick verification, please check [here](./firmware/README.MD)**
7. **Can I use an external 5V pin for power? Please see here [issues/205](https://github.com/Xinyuan-LilyGO/T-Display-S3/issues/205)**
9. The default charging current is set at 500mA per hour. If you need to adjust the charging current, please see this [issue](https://github.com/Xinyuan-LilyGO/T-Display-S3/issues/230)

