# Edge Impulse firmware for Arduino Nano 33 BLE Sense

Edge Impulse enables developers to create the next generation of intelligent device solutions with embedded Machine Learning. This repository contains the Edge Impulse firmware for the Arduino Nano 33 BLE Sense development board. This device supports all Edge Impulse device features, including ingestion, remote management and inferencing.

> **Note:** Do you just want to use this development board with Edge Impulse? No need to build this firmware. See the instructions [here](https://docs.edgeimpulse.com/docs/arduino-nano-33-ble-sense) for a prebuilt image and instructions.

## Requirements

### Hardware

* [Arduino Nano 33 BLE Sense](https://store.arduino.cc/usa/nano-33-ble-sense) or [Arduino Nano 33 BLE](https://store.arduino.cc/usa/nano-33-ble) development board.

### Tools

The arduino-cli tool is used to build and upload the Edge Impulse firmware to the Arduino Nano 33 BLE Sense board. Use following link for download and installation procedure:

* [Arduino CLI](https://arduino.github.io/arduino-cli/installation/).

The Edge Impulse firmware depends on libraries and the Mbed core for Arduino. Running the following script will install all the dependencies for you:

```
$ arduino-cli core update-index
$ arduino-cli core install arduino:mbed@1.1.4
$ arduino-cli lib update-index
$ arduino-cli lib install Arduino_LSM9DS1@1.0.0
```

## Building the application

1. Build the application:

    ```
    ./arduino-build.sh --build
    ```

1. Flash the application:

    ```
    ./arduino-build.sh --flash
    ```

## Caveats

* It's easy to brick the Nano 33 BLE board. You can double tap the button on the board to put it in bootloader mode and then flash a valid program through the Arduino IDE. Afterwards you can flash a new application again through the CLI.
