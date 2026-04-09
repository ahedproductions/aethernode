NOTE: After some testing and rework it was discovered, that without RXEN high on receive, the E22-XXXM30/33S is very much deaf, because a diode switch inside draws the RX path to ground to protect the LNA input when transmitting. It the process all design files were changed, and the old ones have been removed and deemed erroneous. For all who have built the aethernode as was, there is option 1 with an addon of 3 parts [DIO2 Mod](https://github.com/ahedproductions/aethernode/blob/main/Schematic/DIO2%20Mod.jpg). Please check the schematic!

It includes provision for two types of transmission control of the LoRa module, and while I recommend using DIO2 based control, both are included:
1. DIO2 based control with an external transistor inverter to control also the RXEN pin. (REMOVE R3/R4 if selected!)

   Firmware: [rnode_firmware_aethernode_dio2.zip](https://github.com/ahedproductions/aethernode/blob/main/Firmware/rnode_firmware_aethernode_dio2.zip) - this is what will be flashed by the flashers by default! If you want to play with the TX/RX version, download the file directly and flash it.
2. TXEN/RXEN external control of the module via pins G17/G16. (REMOVE R2/Q1 if selected!)

   Firmware: [rnode_firmware_aethernode_rxtx.zip](https://github.com/ahedproductions/aethernode/blob/main/Firmware/rnode_firmware_aethernode_rxtx.zip)

<img width="823" height="576" alt="3drnode" src="https://github.com/user-attachments/assets/2e85072e-8f93-4287-a06a-2465e3da385d" />

A Reticulum Network stationary transport/discovery enabled node - RRNode. 
Designed around OrangePI Zero LTE, an AZDelivery NodeMCU ESP32 and a CDEBYTE E22-XXXM33S LoRa radio.
It has a built in power supply block, that takes from 18VDC to 53VDC, being designed for the nominal Power Over Ethernet(PoE) voltage of 48VDC,
and provides 5V@6A to power the RNode and the SBC, running RNS.
The node will provide up to 33dBm (2W) of output power.

A web flasher, that can flash the aethernode - https://rns.moscow/flasher

NOTE: While the power supply on the PCBA is capable of withstanding 75V input voltage, the protection diode D1 is set to conduct at around 55VDC.
This allows ample window for standard 48V PoE voltage. If one uses battery backup, for example Lead-Acid, the output voltage of a fully charged set
would be around 55-57VDC and this WILL cause D1 to conduct and short the PS. If one uses such backup, change D1 to SMCJ58A,
which will conduct at around 67VDC and will not interfere with normal operation under such backup.

Node with CDEBYTE TX433-JZLW-15 3dBi gain antenna for more compact build (https://www.cdebyte.com/products/TX433-JZLW-15)

![photo_2026-02-06_22-13-14](https://github.com/user-attachments/assets/54d9e64e-853c-4781-b15f-a51cd6763e93)

![DSCN4093](https://github.com/user-attachments/assets/248c2832-d29d-4ed9-8519-43ed4a5949d8) 

Node with CDEBYTE TX433-BLG-40 4.5dBi gain sleeve dipole antenna for best range (https://www.cdebyte.com/products/TX433-BLG-40)

![1000009271](https://github.com/user-attachments/assets/d668b151-c820-4559-8ed0-c183b8a2e09d)

Deployed in the sky!

![photo_2026-03-07_12-02-07 (4)](https://github.com/user-attachments/assets/c87236df-017e-4bb8-9c75-1c4c6a1c6729)
![photo_2026-03-07_12-02-07 (2)](https://github.com/user-attachments/assets/04e3f536-343c-439d-9a84-03e34cd89258)
![photo_2026-03-07_12-02-07 (3)](https://github.com/user-attachments/assets/939b221a-ae43-49a7-9221-91d2a7f85870)
![c30c4971-353e-48e3-90e8-260c9b61710a](https://github.com/user-attachments/assets/3470bb36-48e6-4974-8200-bfe25fdd7aa4)

In places with high winds, the box top wall might be too thin and allow for rocking movements to manifest in the antenna base at specific wind speeds, much like this happens with round-tubed parking barriers. In this case an additional metal detail will greatly reduce the chance of damage. Mine are cut from 2mm aluminium, but you can use whatever is stiff enough and not too thick. You might need to cut a bit from the baseplate mounting fins to make place for the new plate.

![photo_2026-03-22_11-58-17](https://github.com/user-attachments/assets/b8a311cf-1d03-460c-afaa-4a7c88c6d9fe)
![photo_2026-03-22_11-58-17 (2)](https://github.com/user-attachments/assets/d12e9b6f-6c12-4c48-be86-de530cec1c9b)
