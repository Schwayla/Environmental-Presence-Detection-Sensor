# Introduction
  - This is a sensor that uses the DFRobot mmWave Sensor, Panasonic PIR Sensor, and BMP280 for motion detection and environmental data for use on **ESPHome**. As you may have guessed this was a project inspired by Everything Smart Home's video and subsequent sensor as well as his inspiration igiannakas who made a similar sensor.
  - I am new to coding so this is probably not the best way to code this but it works.
  - I also used PowerPoint to make the diagrams.
  
# Bill of Materials
  - D1 Mini 8266, Type-C (Aliexpress)
  - USB-C to USB-C Cable (Aliexpress)
  - USB-C Charger (I use an ANKER PowerPort III buts that's overkill)
  - DFRobot mmWave Sensor (SEN0395) (I get from DFRobot Store)
  - Panasonic EKMC1603111 (Digi-Key: 255-3086-ND)
  - BMP280 (Aliexpress / Amazon)
  - Solid-Core 22AWG wire (Aliexpress)
  - 10K Ohm Resistor (Aliexpress / Amazon)
  - ElecrtoCookie Prototyping PCB Board (Amazon)
  
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
  
# Software/Programs
  - Home Assistant: https://www.home-assistant.io/
  - ESPHome: https://esphome.io/
  
# Not Included in this project...
  - The Skills to do the things in this project. YouTube is my best friend when it comes to learning how to do something and it can do a much better job of teaching you the skills needed to make this than I can.
  - I had to look up how to make a README on here so...
  
**Skills Needed**
  - Soldering https://youtu.be/6rmErwU5E-k 
  - Wire Stripping https://youtu.be/JVJsJ4scCBk
  - Basic Understanding of Code (I barely know it) 
  - Computer Skills 
    
# How-To Guide
**Setup**
  1. Setup ESPHome Instance on Home Assistant: https://esphome.io/guides/getting_started_hassio.html (Just grab it from Add-Ons)
  2. Load initial software into ESP8266 from ESPHome.
    - https://youtu.be/Viqvx7hMMJs
    - MUST BE DONE BEFORE INSTALLING BOARD ONTO PROJECT!
  3. Cut and strip wires (Documents/Diagrams/ElectroCookie_Med_Pinout.png)
  
  
# References, Guides, & Resources
 - igiannakas's guide: https://github.com/igiannakas/mmwave-d1mini
 - hjmcnew's documentation on mmWave sensors in ESPHome: https://github.com/hjmcnew/esphome-hs2xx3a-custom-component/tree/release
 - Everything Smart Home's Video: https://youtu.be/Viqvx7hMMJs
