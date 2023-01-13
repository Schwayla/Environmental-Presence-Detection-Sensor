# Introduction
  - This is a sensor that uses the DFRobot mmWave Sensor, Panasonic PIR Sensor, and BME280 for motion detection and environmental data for use on **ESPHome**. As you may have guessed this was a project inspired by Everything Smart Home's video and subsequent sensor as well as his inspiration igiannakas who made a similar sensor.
  - I am new to coding so this is probably not the best way to code this but it works.
  - I also used PowerPoint to make the diagrams.

![IMG_7314](https://user-images.githubusercontent.com/59221079/212090045-82cee1fa-611c-445f-a656-584071f84cd9.jpg)
  
# Bill of Materials
  - D1 Mini 8266, Type-C (Aliexpress)
  - USB-C to USB-C Cable (Aliexpress)
  - USB-C Charger (I use an ANKER PowerPort III buts that's overkill)
  - DFRobot mmWave Sensor (SEN0395) (I get from DFRobot Store)
  - Panasonic EKMC1603111 (Digi-Key: 255-3086-ND)
  - BME280 (Aliexpress / Amazon)
  - Solid-Core 22AWG wire - 63.5cm / 25in (Aliexpress)
  - 10K Ohm Resistor (Aliexpress / Amazon)
  - ElecrtoCookie Prototyping PCB Board (Amazon)
  
  [BOM Reference](https://github.com/Schwayla/Environmental-Sensor/blob/280037779f692ed72e2192dc8d59334414fc8657/Documents/Materials-Tools/Bill%20of%20Materials)
  
# Tools Needed
  - Safety Glasses
  - Soldering Iron (I like the TS100)
    - Solder
    - Iron Cleaner
    - Brush-on or Liquid Flux
    - Smoke/Fume Filter
  - Hot Glue Gun (I use a Gorilla Glue Hi/Low)
  - Wire strippers
  - Flush-Cut Wire Cutters (Aliexpress or Knipex)
  - Permanent Marker (I use silver)
  - (OPT) Soldering mat or holder
  - (OPT) Breadboard (To test everything first)
  
  [Tools Reference](https://github.com/Schwayla/Environmental-Sensor/blob/9cfe84de354dd05abc04a752588c11a8314ef70a/Documents/Materials-Tools/Mentioned%20Tools)
  
# Software/Programs
  - [Home Assistant](https://www.home-assistant.io/)
  - [ESPHome](https://esphome.io/)
  
# Not Included in this project...
  - The Skills to do the things in this project. YouTube is my best friend when it comes to learning how to do something and it can do a much better job of teaching you the skills needed to make this than I can.
  - I had to look up how to make a README on here so...
  
**Skills Needed**
  - [Soldering](https://youtu.be/6rmErwU5E-k)
  - [Wire Stripping](https://youtu.be/JVJsJ4scCBk)
  - Basic Understanding of Code (I barely know it) 
  - Computer Skills 
    
# How-To Guide
## Setup/Prep
  1. [Setup ESPHome Instance on Home Assistant](https://esphome.io/guides/getting_started_hassio.html) (Just grab it from Add-Ons)
  2. [Load initial software on to the ESP8266 from ESPHome](https://youtu.be/Viqvx7hMMJs)
    - MUST BE DONE BEFORE INSTALLING THE 8266 BOARD ONTO THE PCB/BREADBOARD!
  3. Cut and strip wires - [Wire List](https://github.com/Schwayla/Environmental-Sensor/blob/1f8e7593d6e171ae759ecf0c736d8ca7518d715f/Documents/Diagrams/ElectroCookie_MD_WireList.png) | [Pre-Cut Wires](https://github.com/Schwayla/Environmental-Sensor/blob/2cb97e723ad9acc277df67176590945e9eb55532/Documents/Diagrams/WireList_pre-cut_wires.PNG)

  <img width="308" alt="ElectroCookie_MD_WireList" src="https://user-images.githubusercontent.com/59221079/212226799-7544f6d9-7b95-49da-a0d4-6a07d3952d85.png">
  
## Fabrication
  1. Solder pins to components.
  
  ![IMG_7322](https://user-images.githubusercontent.com/59221079/212224511-2bbd6608-4331-41dc-ba26-4d4862dabbb2.jpg)

   - I like to stick the pins into a breadboard to hold them in place while soldering.

  ![IMG_7323](https://user-images.githubusercontent.com/59221079/212224208-e66168a7-9599-49a2-93e1-31439c454720.jpg)
  
   - After soldering the pins to the components, slide the pin retainer strips 3mm down away from the component boards. This will help in the installation of the components in the future and allow for clearance over the wires on the board.
  
  ![IMG_7325](https://user-images.githubusercontent.com/59221079/212227666-52b8147e-9b34-4130-9e0e-ba3a8efbf130.jpg)
  
  2. solder wires in-place on ElectroCookie Board. [Reference Diagram](https://github.com/Schwayla/Environmental-Sensor/blob/6eeecd7a87b013b7dbf060ae7f8748a2fa184cad/Documents/Diagrams/esp8266_env_sensor_pcb_va.pdf) **(Path: Documents/Diagrams/esp8266_env_sensor_pcb_va.pdf)**
    - Verify all wires are correctly soldered to the specified spot.
    - Visually inspect all solder points and repair as needed.
      
  ![IMG_7319](https://user-images.githubusercontent.com/59221079/212224895-159c1262-37bc-4098-9e41-74957c07bb0c.jpg)
  
  3. Solder components to board. [Reference Diagram](https://github.com/Schwayla/Environmental-Sensor/blob/6eeecd7a87b013b7dbf060ae7f8748a2fa184cad/Documents/Diagrams/esp8266_env_sensor_pcb_va.pdf) **(Path: Documents/Diagrams/esp8266_env_sensor_pcb_va.pdf)**
    - Visually inspect all solder points and repair as needed.
  4. Connect board to power (Connect the ESP8266 to the power brick via USB-C cable).
    - Allow around 2 minutes for the board to boot and connect to wifi.
  5. Edit the device in ESPHome and [add the code from this project](https://github.com/Schwayla/Environmental-Sensor/blob/90b6b86ba92d5fca961ce72326073a1cad06f3d1/env-sensor-code.txt) to your device UNDER the existing code that was loaded to the ESP8266 in step 2 of setup / prep.
  6. Install the code **Wirelessly** and wait for the board to connect (You can watch the progress of the load and the connection via the Logs)
  
  ![esphome-wireless-install](https://user-images.githubusercontent.com/59221079/212228829-1e62ddeb-5c42-444f-ae28-270e3a187d85.png)
  
   - This will take a few minutes...
  
  7. Home Assistant will automatically recognize the device. You can njow configure it and add it to automations and what not.

### Adding Sensor to Automations (I'm only including this because I was confused)
  - When searching for a Device Trigger, search the name of the device ie. Environmental-Sensor (or whatever you named yours) THEN select the sensor as an entity from that device.

<img width="750" alt="HA_Sensor_Add_Trigger" src="https://user-images.githubusercontent.com/59221079/212088207-bb94546a-d7cc-4de2-b20b-c7d3afb68a19.png">

# References, Guides, & Resources
 - igiannakas's guide: https://github.com/igiannakas/mmwave-d1mini
 - hjmcnew's documentation on mmWave sensors in ESPHome: https://github.com/hjmcnew/esphome-hs2xx3a-custom-component/tree/release
 - Everything Smart Home's Video: https://youtu.be/Viqvx7hMMJs
 - crlogic Home Assistant Forum Post: https://community.home-assistant.io/t/mmwave-presence-detection-esphome-style/382778
 - ESPHome's Main Site: https://esphome.io/
   - ESP8266: https://esphome.io/components/esp8266.html
   - UART: https://esphome.io/components/uart.html
   - BME280: https://esphome.io/components/sensor/bme280.html
   - PIR Sensor: https://esphome.io/cookbook/pir.html
   - mmWave Sensor: It is programmed via UART, but on this current build it is treated as a Binary Sensor. No ESPHome Docs yet
   
   



