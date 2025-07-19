### [Projekt - Struktur] ###


Beispiel Struktur:


```md

pico_freertos_webserver/
├── CMakeLists.txt
├── cmake/
│   └── pico_sdk_import.cmake      # falls nötig
├── include/                       # Public headers
│   └── config.h
├── src/                           # App-spezifische Tasks
│   ├── main.c
│   ├── led_task.c
│   ├── ssd1306_task.c
│   ├── lcd1602_task.c
│   ├── usb_rndis_task.c
│   └── webserver_task.c
├── lib/                           # Eigene statische Libraries
│   ├── lcd1602/
│   │   ├── CMakeLists.txt
│   │   ├── lcd1602.c
│   │   └── lcd1602.h
│   └── ssd1306/
│       ├── CMakeLists.txt
│       ├── ssd1306.c
│       └── ssd1306.h
├── external/                      # Third-party
│   ├── FreeRTOS/                  # Port für RP2040
│   ├── lwip/
│   └── tinyusb/
└── README.md

```


UPDATE:


```md
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