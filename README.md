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

1. Instalar [Visual Studio Code](https://code.visualstudio.com/) y [Python](https://www.python.org/)
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

* `T-Display-S3` esp-idf ejemplo de versión, vaya a [LilyGo-Display-IDF](https://github.com/Xinyuan-LilyGO/LilyGo-Display-IDF)

## 6️⃣ Micropython

* [russhughes/st7789s3_mpy](https://github.com/russhughes/st7789s3_mpy)
* [Micropython](https://github.com/Xinyuan-LilyGO/lilygo-micropython)


# 7️⃣ ESP32 ejemplos básicos

* [BLE Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/BLE)
* [WiFi Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/WiFi)
* [SPIFFS Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/SPIFFS)
* [FFat Examples](https://github.com/espressif/arduino-esp32/tree/master/libraries/FFat)
* Para más ejemplos de funciones del chip esp32, por favor consulte [arduino-esp32-libraries](https://github.com/espressif/arduino-esp32/tree/master/libraries)


# 8️⃣ Resource

| Product(PinMap)         | schematic                                               | Dimensions                  | PCB 3D                                    | PinMap                                   |
| ----------------------- | ------------------------------------------------------- | --------------------------- | ----------------------------------------- | ---------------------------------------- |
| [T-Display-S3][1]       | [schematic](./schematic/T_Display_S3.pdf)               | [DWG](./dimensions/PCB.dwg) | [STP](./dimensions/t-display-s3-full.stp) | [PinMap](./image/T-DISPLAY-S3.jpg)       |
| [T-Display-S3 Touch][1] | [schematic](./schematic/T_Display_S3.pdf)               | [DWG](./dimensions/PCB.dwg) | [STP](./dimensions/t-display-s3-full.stp) | [PinMap](./image/T-DISPLAY-S3-TOUCH.png) |
| [T-Display-S3-MIDI][1]  | [schematic](./schematic/SCH_T-Display-S3-MIDI_V1.1.pdf) | DWG                         | STP                                       |                                          |


## 9️⃣ FAQ

1. **La pantalla no se enciende cuando se utiliza la batería?**
   * Cuando el T-Display-S3 funciona con batería, GPIO15 debe estar en HIGH para encender la retroiluminación.
   * Por favor, añada las dos líneas siguientes al principio de la configuración
   ```C++
   void setup(){
      //Turn on display power
      pinMode(15, OUTPUT);
      digitalWrite(15, HIGH);
   }
   
   ```
2.  **El programa puede escribirse con normalidad, pero no se muestra nada después de escribir**.
   * Si está utilizando **TFT_eSPI**, entonces puede intentar ejecutar `Arduino_GFXDemo` primero. Si no se muestra nada después de escribir, puede determinar que hay un problema con el hardware.
   * Si `Arduino_GFXDemo` se escribe normalmente, pero **TFT_eSPI** no se muestra, entonces se puede juzgar que `User_Setup_Select` ha sido sobreescrito, entonces por favor lea el tercer artículo de **FAQ** para reconfigurar **TFT_eSPI**.
3. **¿Cómo actualizar **TFT_eSPI**, o confirmar si la configuración de pines **TFT_eSPI** es correcta?**.
   * Busca **TFT_eSPI** en el gestor de librerías de ArduinoIDE y haz clic en Actualizar.
   * Entre en la ubicación de instalación por defecto del gestor de librerías y abra la carpeta **TFT_eSPI**. La ubicación de instalación por defecto es:(p.ej. 
     C:\NUsuNombreDocumentos\NArduino\libraries).
   * Abra User_Setup_Select.h, comente #include <User_Setup.h> que está activado por defecto, o bórrelo.
   * Busca **Setup206_LilyGo_T_Display_S3**, encuéntralo, cancela el comentario anterior, luego guárdalo, y finalmente ciérralo, para que TFT_eSPI use la definición de pin de T-Display-S3 por defecto.
   ```c++
   #include <User_Setups/Setup206_LilyGo_T_Display_S3.h>     // Para el LilyGo T-Display S3 basado en ESP32S3 con ST7789 170 x 320 TFT
   ```
4. **No se puede cargar ningún boceto, por favor entre en el modo de carga manualmente.
   * Conectar la placa mediante el cable USB
   * Mantén pulsado el botón **BOOT** , Mientras sigues pulsando el botón **BOOT**
   * Pulse el botón **RST**.
   * Release the **RST** button
   * Suelte el botón **BOOT** (Si no hay botón **BOOT**, desconecte IO0 de GND).
   * Cargar sketch
   * Pulse el botón **RST** para salir del modo de descarga.

5. **Si utiliza una fuente de alimentación externa en lugar de USB-C, desactive la opción CDC. Esto se debe a que la placa esperará el acceso USB cuando se inicie.**

   * Para los usuarios de Arduino IDE, se puede desactivar en las opciones , Tenga en cuenta que al desactivar USB CDC se desactivará la redirección Serial a USBC. En este momento, usted no verá ningún mensaje Serial de salida al abrir el puerto desde USB-C, pero la salida de GPIO43 y GPIO44.

   ```c
   Tools -> USB CDC On Boot -> Disable
   ```

   * Para los usuarios de platformio, puede añadir las siguientes opciones de compilación en el archivo ini

   ```c
   build_flags =
       ; Enable -DARDUINO_USB_CDC_ON_BOOT will start printing and wait for terminal access during startup
       ; -DARDUINO_USB_CDC_ON_BOOT=1

       ; Enable -UARDUINO_USB_CDC_ON_BOOT will turn off printing and will not block when using the battery
       -UARDUINO_USB_CDC_ON_BOOT
   ```

6. **Si todo lo anterior no es válido, por favor flashear el firmware de fábrica para una verificación rápida, por favor revise [aquí](./firmware/README.MD)**.
7. **¿Puedo utilizar un pin externo de 5V para la alimentación? Por favor, consulte aquí [issues/205](https://github.com/Xinyuan-LilyGO/T-Display-S3/issues/205)**
9. La corriente de carga por defecto es de 500mA por hora. Si necesita ajustar la corriente de carga, consulte esta [edición](https://github.com/Xinyuan-LilyGO/T-Display-S3/issues/230)

