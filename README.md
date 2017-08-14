# M5Stack

## Installation Instructions

### 1. Install the SiLabs CP2104 Driver
- [Download the SiLabs CP2104 Driver](http://community.silabs.com/t5/Interface-Knowledge-Base/Legacy-OS-Software-and-Driver-Packages/ta-p/182585)

### 2. Using through Arduino IDE

#### [Instructions for Windows](doc/windows.md)

#### Instructions for Mac
- Install latest Arduino IDE from [arduino.cc](https://www.arduino.cc/en/Main/Software)
- Open Terminal and execute the following command (copy->paste and hit enter):

  ```bash
  mkdir -p ~/Documents/Arduino/hardware/espressif && \
  cd ~/Documents/Arduino/hardware/espressif && \
  git clone https://github.com/espressif/arduino-esp32.git esp32 && \
  cd esp32/tools/ && \
  python get.py && \
  cd ~/Documents/Arduino/libraries && \
  git clone https://github.com/m5stack/M5Stack.git
  ```
- Restart Arduino IDE

#### Instructions for Debian/Ubuntu Linux
- Install latest Arduino IDE from [arduino.cc](https://www.arduino.cc/en/Main/Software)
- Open Terminal and execute the following command (copy->paste and hit enter):

  ```bash
  sudo usermod -a -G dialout $USER && \
  sudo apt-get install git && \
  wget https://bootstrap.pypa.io/get-pip.py && \
  sudo python get-pip.py && \
  sudo pip install pyserial && \
  mkdir -p ~/Arduino/hardware/espressif && \
  cd ~/Arduino/hardware/espressif && \
  git clone https://github.com/espressif/arduino-esp32.git esp32 && \
  cd esp32/tools/ && \
  python get.py && \
  cd ~/Arduino/libraries && \
  git clone https://github.com/m5stack/M5Stack.git
  ```
- Restart Arduino IDE

#### Installing with Boards Manager(beta)

Starting with 1.6.4, Arduino allows installation of third-party platform packages using Boards Manager. We have packages available for Windows, Mac OS, and Linux (32 and 64 bit).

- Install Arduino 1.8.2 from the [Arduino website](http://www.arduino.cc/en/main/software).
- Start Arduino and open Preferences window.
- Enter ```http://www.m5stack.com/download/package_m5stack_index.json``` into *Additional Board Manager URLs* field. You can add multiple URLs, separating them with commas.
- Open Boards Manager from Tools > Board menu and install *ESP32* platform (and don't forget to select your ESP32 board from Tools > Board menu after installation).
