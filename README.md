# ESP32 Snippets

The main reason that I forked this library is because the API design of the original repository does not allow the programmers to implement the app that BLE server and BLE client coexist and run simultaneously.

As one of the projects that I am participating in requires both BLE client and server on same board, thus, I decided to fork the esp32 library, and add new codes that allow me to do this.

To make the ESP32 to have BLE server mode and BLE client mode, we should be able to kill the BLE server if requried.
However, due to API design, it was impossible to kill the server, thus, I implemented a method called "removeServer" in the BLEDevice.cpp file to make it possible.

## Changes

### 1) BLEAdvertising.cpp update

Due to [this issue](https://github.com/nkolban/esp32-snippets/issues/797), removed [the 496th line](https://github.com/nkolban/esp32-snippets/blob/master/cpp_utils/BLEAdvertising.cpp#L496) from the original BLEAdvertising.cpp file.
