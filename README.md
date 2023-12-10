# swing-windows-opener
This repository contain all you need to create from scratch a swing dual external shutter windows opener Apple Homekit opener: from mechanical to electronical parts.

## SCOPE:

This project would help everyone to create itself an automated swing shutter window opener using modern vocie assistant at lowest price (in Italy commercial product have a price of 500€ for each window, and there isn't a commercial product able to communicate with Alexa, Google Home and Apple HomeKit); the objective is to obtain a working product more cheaper than commercial products.


## REQUIREMENTS FOR FIRST VERSION:
- operator on sight (no need to include it in the wall);
- installation in top of existing window
- from internal of home: open first right windows and then left windows (reverse action for closing)
- window size minimum width 80 cm ???
- available depth minimum 11 cm ???
- motor section:
  - opener for 2 doors max 40KG??? of weights for each door
  - max/min dimensions of shutter windows ????
  - manage power on n.2 DC Motor 24VDC?; the absorbed power is equal to 24 VA, the no-load absorption is 0.2 A, the load one is 1 A, the output torque is 40 Nm, the reduction is equal to 1/4380, the rotation speed corresponds to 1.5 revolutions per minute, the opening time is 18 sec; they are soundproofed, exactly 33 dB with 230 Volt synchronized movement, the mechanical clutch is windproof; 6 RPM?
  - delay in opening and closing: when opening, first open right window and then left window; when closing first close left window and then right window;
  - opening/closing slowdown;
  - 2 motor with worm screw to open swing windows at 180 degree;
  - irreversible engine
  - opening/closing mode:
    - full closing;
    - full opening 180 degree;
    - partial opening (10-20-30-40-50-60-70-80-90 %);
- electronic section:
  - End of stroke of the motors should be controlled measuring the current or power
  - manage power to send to motors: 0,6 0,9 1,2 2 Ampere
  - delay to stop motor after too high current consumption 100 or 300 ms
  - space useful for electronic board (PCB):  6,5 x 11 cm ???
- principal power supply 230 VAC 50-60Hz
- control using Apple HomeKit via WiFi using ESP82xx at 2.4 GHz
- not use 433 MHz (less secure)
- manual motor release from internal of house for emergency
- metal box to install DC motor, electronic mainboard
- little space to install between external and internal window
- protection IP24 or IP44???
- low costs
- emergency opening/closing in case of power outage
- respect EU laws

## OPTIONAL FOR NEXT/ADVANCED VERSION:
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
- calibration procedure
- include DC motors and electronics in the wall

## BOM:
- n.2 metal crank mechanism to connect DC motor to windows similar to it https://ducatihome.it/collections/persy/products/arko-2 I think it's easier buy it!
- n.2 DC motor 24VDC; example: https://it.aliexpress.com/item/32888516359.html?spm=a2g0s.9042311.0.0.4e664c4dSgpuqS&aff_platform=portals-tool&sk=_AqnxON&aff_trace_key=810f27c442794444b2219e4e737806c2-1610551102388-04855-_AqnxON&terminal_id=b7ba9f6d8cbb47889715383f86120e5e&tmLog=new_Detail
- n.2 metal engine support plate; example: https://it.aliexpress.com/item/32873411717.html?spm=a2g0o.detail.1000013.1.707e1f47Agh9zM&pvid=e8e14976-86d7-431f-9209-a1cb5174aa7f&aff_platform=portals-tool&sk=_9wATLX&aff_trace_key=f90564cf31fc4e9eb008cc5a6facd4a3-1610551108928-07616-_9wATLX&gps-id=pcDetailBottomMoreThisSeller&scm=1007.13339.146401.0&scm-url=1007.13339.146401.0&scm_id=1007.13339.146401.0&terminal_id=b7ba9f6d8cbb47889715383f86120e5e&tmLog=new_Detail
- n.4 end of stroke (micro-switch?) example: https://it.aliexpress.com/item/32968198983.html?spm=a2g0s.9042311.0.0.4e664c4dSgpuqS&aff_platform=portals-tool&sk=_A0nO05&aff_trace_key=8f8cebd09f184fb19475cbc3ed159733-1610551110576-03638-_A0nO05&terminal_id=b7ba9f6d8cbb47889715383f86120e5e&tmLog=new_Detail
- n.1 metal box 77 mm x 50 mm x 800 mm (for enclousure case)
- rigid flange joint; example: https://it.aliexpress.com/item/32967906911.html?spm=a2g0s.9042311.0.0.4e664c4dSgpuqS&aff_platform=portals-tool&sk=_ACLkVP&aff_trace_key=863311a21d194eadb2d6385eb3706ea6-1610551104055-06114-_ACLkVP&terminal_id=b7ba9f6d8cbb47889715383f86120e5e&tmLog=new_Detail
- ESP8266 with WIFI (it require a WIFI infrastructure): 1 o 2 relay with 1 NC sensor using HAA firmware (no PM feature available now)
- n.1 power supply 220V->24VDC (or use electronic board to pwoer also DC Motors????)
- electronic for control delay and PM (maximum dimension 77 mm x 50 mm x ???)????? example: https://it.aliexpress.com/item/32833407097.html
- DUAL CONTROL DRIVER L298N (Max 2A) oppure POLOLU (Max 5A) control driver H-BRIDGE????
- wiring between each DC motor and mainboard (n.6 x 0.5-1.5 mm);
- wiring between mainboard and power supply 220 VAC (n.2 x 1-1.5 mm);

## TODO LIST:
1) buy list of materials
2) assembler all-in-one solution
3) we have 3 ways to automate a self made swing window opener:
   A) use a commercial garage swing gate opener + ESP82xx with 1 relay dry contact without PM , with HAA firmware; 
   B) use an unique PCB with ESP82xx, 4 relay 24VDC, PM features, with TASMOTA firmware and then integrate via HOME ASSISTANT to HOMEKIT
   C) use an unique PCB with ESP82xx, 4 relay 24VDC, PM features, ... with HAA firmware, when HAA will support PM??!?!?!

## PHASE OF THIS PROJECT:
1) documentation (actual)
2) prototype and test (next 3 months)
3) production/final release (next 6 months)


## REFERENCES:
homekit firmware: https://github.com/RavenSystem/esp-homekit-devices
TASMOTA firmware: https://github.com/arendst/Tasmota
HOME ASSISTANT: https://github.com/home-assistant/core


## EXAMPLE of italian commercial products for dual swing shutter windows:
- CAME VOILA' https://www.came.com/it/installatori/soluzioni/automazioni-tende-tapparelle-e-scuri/blinds/voila
- FAAC N1D KIT or Night ONE Day https://faac.it/prodotti/soluzioni-in-kit-1/catalogo/faac-night-one-day-kit-shutters/
- DUCATI HOME PERSY https://it.ducatihome.it/pages/persy from about 480€
- SOMFY SYNAPSIA https://shop.somfy.it/kit-motore-per-persiane-synapsia.html
- SOMFY YSLO FLEX RT https://www.somfy.it/soluzioni/1240035/yslo-flex-rts
- ANTAMATIC CLASSIC, SLIM, SERIE3, ... KIT (AMER GROUP) https://antamatic.com/automazioni-scuri from about 500€
- CHIAROSCURO ST40 http://www.chiaroscuro.eu/Product/Battente.html
- APRIMATIC BUONGIORNO https://www.aprimatic.it/?dima-portfolio=automazione-serramenti-buongiorno
- EHRET VOLETRONIC 230 V https://www.ehret.com/it-it/prodotti/persiane-battenti/motorizzazione
- ANCELLOTTI ELETTROMECCANICA mod. S/A http://www.ancellotti.it/home.htm from about 850€
- OPEN SMALL ANTE BATTENTI http://www.openautomazioni.it/index.php/it/prodotti/ante-a-battenti/soluzione-a-vista
- WIMOVE https://www.wimove-store.fr/32-c-wibat-linteau-commande-filaire from about 360 - 550€
- FGMICRODESIGN http://www.fgmicrodesign.com/index.php?page=products&language=1&ec_product=kitclickr&ec_category=1
- THOMSON (ADVISEN / THOMSONBOX) 350€
* it seems there aren't other similar products in the rest of the world (at lowest price)

## OUT OF SCOPE:

This project don't be useful to other type of windows dirrerent from swing shutter window (padovana/trevigiana, vicentina, vicentina rovescia, vicentina 3 ante, ante legate, scorrrevole, ...)
AAA looking for CAD designer 2D/3D, mechanical expert, eletronical expert

THANKS to @marcok625
https://github.com/marcok625/Persiane_Smart
https://www.youtube.com/watch?v=GMPM3Aij41A

