# swing-windows-opener
This repository contain all you need to create from scratch a swing dual external shutter windows opener Apple Homekit opener: from mechanical to electronical parts.

SCOPE:

This project would help everyone to create itself an automated swing shutter window opener using modern vocie assistant at lowest price (in Italy commercial product have a price of 500€ for each window, and there isn't a commercial product able to communicate with Alexa, Google Home and Apple HomeKit); the objective is to obtain a working product more cheaper than commercial products.


REQUIREMENTS FOR FIRST VERSION:
- opener for 2 doors max 40KG of weights for each door
- max/min dimensions of shutter windows ????
- manage power on n.2 DC Motor 24VDC?;
- delay in opening and closing: when opening, first open right window and then left window; when closing first close left window and then right window;
- opening/closing slowdown;
- 2 motor with worm screw to open swing windows at 180 degree;
- opening/closing mode:
  - full closing;
  - full opening 180 degree;
  - partial opening (10-20-30-40-50-60-70-80-90 %);
- End of stroke of the motors should be controlled measuring the current or power
- 230 VAC
- control using Apple HomeKit via WiFi using ESP82xx at 2.4 GHz
- not use 433 MHz (less secure)
- manual motor release from internal of house for emergency
- irreversible engine
- metal box to install DC motor, electronic mainboard
- little space to install between external and internal window
- installatin in top of existing window
- protection IP24 or IP44???

OPTIONAL FOR NEXT/ADVANCED VERSION:
- close sensor (I can mov this to inital version because it's very simple attach reed sensor: 1 side without wire to the window and the other one nead ESP; use this sensor is raccomanded for secuirty matters)
- simplest version for 1 door
- open sensor
- solar panels similar to it https://ducatihome.it/collections/persy/products/persy-sol
- battery similar to it https://ducatihome.it/collections/persy/products/bat-0212
- wall button
- control using Alexa, Google Home
- detection obstacle, wind, ice (using PM, contact, motion detection, resistive safety rib of 8,2KOhm or 16KOhm...)
- adapt to other type of windows (padovana, trevigiana, vicentina, vicentina rovesciata, libro)
- anti-crushing system
- lock mechanism similar to it https://ducatihome.it/collections/persy/products/persy-lock https://ducatihome.it/collections/persy/products/persy-block


BOM:
- n.2 metal crank mechanism to connect DC motor to windows similar to it https://ducatihome.it/collections/persy/products/arko-2 I think it's easier buy it!
- n.2 DC motor 24VDC
- n.1 power supply 220V->24VDC
- n.2 metal engine support?
- n.4 end of stroke (micro-switch?)
- n.1 metal box
- ESP8266 with WIFI (it require a WIFI infrastructure): 1 o 2 relay with 1 NC sensor using HAA firmware (no PM feature available now)
- electronic for control delay and PM?????
- DUAL CONTROL DRIVER L298N (Max 2A) oppure POLOLU (Max 5A) control driver H-BRIDGE????

TODO LIST:
1) buy list of materials
2) assembler all-in-one solution
3) we have 2 ways to automate a self made swing window opener: 1) use a commercial garage swing gate opener + ESP82xx with 1 relay dry contact without PM , with HAA firmware; 2) use an unique PCB with ESP82xx, 4 relay 24VDC, PM features, ... with HAA firmware

PHASE OF THIS PROJECT:
1) documentation (actual)
2) prototype and test (next 3 months)
3) production/final release (next 6 months)

EXAMPLE of italian commercial products for dual swing shutter windows:
- CAME VOILA' https://www.came.com/it/installatori/soluzioni/automazioni-tende-tapparelle-e-scuri/blinds/voila
- FAAC N1D KIT https://faac.it/prodotti/soluzioni-in-kit-1/catalogo/faac-night-one-day-kit-shutters/
- DUCATI HOME PERSY https://it.ducatihome.it/pages/persy
- SOMFY SYNAPSIA https://shop.somfy.it/kit-motore-per-persiane-synapsia.html
- SOMFY YSLO FLEX RT https://www.somfy.it/soluzioni/1240035/yslo-flex-rts
- ANTAMATIC (AMER GROUP) CLASSIC KIT https://antamatic.com/automazioni-scuri for about 500€
- CHIAROSCURO ST40 http://www.chiaroscuro.eu/Product/Battente.html
* it seems there aren't other similar products in the rest of the world (at lowest price)

AAA looking for CAD designer 2D/3D, mechanical expert, eletronical expert
