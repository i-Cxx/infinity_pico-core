# [Checklist] - !!!#


```md


✅ Danke für die gute Zusammenfassung — ich formuliere dir eine **vollständige, übersichtliche Checkliste**, die du für den Aufbau & Build eures Projekts abarbeiten kannst.
Dabei sind alle Komponenten enthalten: **FreeRTOS, TinyUSB+LWIP (RNDIS Webserver), Pico SDK, SSD1306, LCD1602, Blink.**

---

# 📋 **Infinity RTS Build-Checklist (RP2040 / Pico)**

## 📁 **1️⃣ Projektstruktur prüfen**

```
infinity_rts_core/
├── CMakeLists.txt
├── pico_sdk_import.cmake
├── pico_extras_import.cmake
├── src/
│   ├── CMakeLists.txt
│   ├── main.c
│   ├── usb_rndis_task.c
│   ├── webserver_task.c
│   └── FreeRTOSConfig.h
├── lib/
│   ├── CMakeLists.txt
│   ├── blink/
│   │   ├── CMakeLists.txt
│   │   ├── Blink.cpp
│   │   └── blink_task_wrapper.cpp
│   ├── lcd_1602_i2c/
│   │   ├── CMakeLists.txt
│   │   └── lcd_1602_i2c.c
│   └── ssd1306_i2c/
│       ├── CMakeLists.txt
│       └── ssd1306_i2c.c
└── external/
    ├── FreeRTOS/
    │   ├── CMakeLists.txt
    │   ├── include/
    │   │   ├── CMakeLists.txt
    │   │   └── ...
    │   ├── portable/
    │   │   └── GCC/
    │   │       └── ARM_CM0/
    │   │           ├── CMakeLists.txt
    │   │           └── *.c/h
    ├── lwip/
    │   └── ...
    └── tinyusb/
        └── ...
```

✅ **Ordner vorhanden & alle Dateien wie oben strukturiert?**

---

## ⚙️ **2️⃣ CMake / Build-System prüfen**

✅ Installiere:

* `cmake >= 3.13`
* arm-none-eabi-gcc toolchain
* `ninja` oder `make`

✅ Root `CMakeLists.txt`:

* Importiert Pico SDK & Extras korrekt
* Fügt `external/FreeRTOS`, `external/lwip`, `external/tinyusb` hinzu
* Fügt `lib/` und `src/` hinzu

✅ `src/CMakeLists.txt`:

* Definiert `infinity_rts` Executable
* Verlinkt:

  ```
  pico_stdlib hardware_i2c hardware_gpio
  freertos_kernel freertos_config
  lwip tinyusb_device
  blink_lib lcd1602_lib ssd1306_lib
  ```
* Aktiviert UART für printf:

  ```cmake
  pico_enable_stdio_uart(infinity_rts 1)
  pico_enable_stdio_usb(infinity_rts 0)
  ```

✅ FreeRTOS:

* `freertos_kernel` & `freertos_config` Targets definiert
* `FreeRTOSConfig.h` liegt im `src/` und wird von `freertos_config` bekannt gemacht:

  ```cmake
  add_library(freertos_config INTERFACE)
  target_include_directories(freertos_config INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
  ```

  (entweder in `src/CMakeLists.txt` oder `lib/CMakeLists.txt`)

✅ LwIP & TinyUSB:

* in `external/lwip` und `external/tinyusb` vorhanden
* Standard-Targets (z. B. `tinyusb_device`) verfügbar

---

## 🔗 **3️⃣ Pico SDK & Toolchain**

✅ `PICO_SDK_PATH` gesetzt:

```bash
export PICO_SDK_PATH=/path/to/pico-sdk
```

✅ Optionale Extras (`pico_extras_import.cmake`) vorhanden & kompatibel mit SDK-Version.

✅ `arm-none-eabi-gcc` verfügbar:

```bash
arm-none-eabi-gcc --version
```

---

## 👨‍💻 **4️⃣ Quellcode prüfen**

✅ **main.c**

* Initialisiert FreeRTOS, USB, LWIP
* Startet Tasks (`blink_task`, `webserver_task`, …)

✅ **usb\_rndis\_task.c / webserver\_task.c**

* Enthalten & korrekt eingebunden
* RNDIS-Setup über TinyUSB
* LWIP-HTTPD/Webserver läuft

✅ `blink_task_wrapper.cpp` / `Blink.cpp`

* Implementieren `Blink`-Klasse und Wrapper für FreeRTOS-Task

✅ `lcd_1602_i2c.c` & `ssd1306_i2c.c`

* I2C-Treiber korrekt initialisiert & getestet

✅ `FreeRTOSConfig.h`

* Auf aktuellem Stand (siehe meine verbesserte Version)
* Im Build inkludiert

---

## 🖥️ **5️⃣ Build**

```bash
cd build
cmake ..
make -j4
```

✅ Output:

* `infinity_rts.elf`
* `infinity_rts.uf2`
* Flashbar auf RP2040

---

## 🔌 **6️⃣ Flash & Test**

✅ Pico in BOOTSEL + USB stecken
✅ `.uf2` flashen
✅ Seriell/UART Log prüfen
✅ Webserver per USB-RNDIS erreichbar
✅ LCD & SSD1306 zeigen Daten
✅ LED blinkt

---

# 📝 **Zusammenfassung:**

✅ FreeRTOS (mit konfiguriertem Scheduler, Tasks & Heap)
✅ TinyUSB (RNDIS) & LWIP (HTTP Server)
✅ SSD1306 & LCD1602 I2C-Treiber
✅ Blink-Library (GPIO + FreeRTOS-Task)
✅ Pico SDK inkl. UART für Logs

---

💡 **Wenn du möchtest, kann ich dir auch noch:**

* ein `build.sh`-Script zum Vereinfachen
* einen einfachen `vApplicationMallocFailedHook()` & `vApplicationStackOverflowHook()`
* eine Beispiel-`main.c`-Skeleton-Datei für den Start

Sag einfach Bescheid! 👌

```