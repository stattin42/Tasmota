# FORK from [arendst/Tasmota](https://github.com/arendst/Tasmota)
![Tasmota logo](/tools/logo/TASMOTA_FullLogo_Vector.svg#gh-light-mode-only)![Tasmota logo](/tools/logo/TASMOTA_FullLogo_Vector_White.svg#gh-dark-mode-only)

Alternative firmware for [ESP8266](https://en.wikipedia.org/wiki/ESP8266) and [ESP32](https://en.wikipedia.org/wiki/ESP32) based devices with **easy configuration using webUI, OTA updates, automation using timers or rules, expandability and entirely local control over MQTT, HTTP, Serial or KNX**.
_Written for PlatformIO._

Original [README.md](/README.md)

<hr></hr>

## Purpose of fork
The purpose of this fork is local customization

## Additions

1. New targets

   + tasmota-neopool

   + tasmota-sr04_rx

## Changes/modifications

1. Update SR04 sensor code to support rx only AA02YYUW

     + don't configure tx pin when using hw serial for rx only AA02YYUW

    NOTE: This exception may no longer be needed after commit 67d725d
          which should, supposedly, have fixed this issue.

<hr></hr>

## Short build instructions for CLI with Debian

- Setup environment and tools

  + Install python3, python3-venv and python3-pip
    > apt install python3 python3-ven python3-pip

  + Create python virtual environment (venv) to not interfere with global python environment  
    > python3 -m venv venv

  + Activate the virtual environment  
    > . bin/activate

  + Upgrade pip (in venv)
    > pip install --upgrade pip

  + Install platformio
    > pip3 install -U platformio


- Get sources

  + Clone repo
    > git clone https://github.com/stattin42/Tasmota.git


- Configure source

  +  ...
  +  TO DO
  +  ...


- Build the firmware

  + Build target
    > pio run -e \<target\>  
    >
    where \<target\> is a valid target (see [platformio_tasmota_cenv_sample.ini](/platformio_tasmota_cenv_sample.ini));  
    e.g., tasmota-neopool, tasmota-sr04_rx or tasmota-minimal
    
  + Firmware is available in build_output/firmware


- Install or upgrade the firmware

  + ...
  + TO DO
  + ...

## Credits, License and more

See [README.md](/README.md)

