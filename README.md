# Repetier0.92.9-DMY3DP
Repetier 0.92.9 for DMY3DP-001 (anet a8 clone)

https://raw.githubusercontent.com/crazytiti/Repetier0.92.9-DMY3DP/master/SJCM0003.jpg

This is preconfigurated repetier firmware 0.92.9 with auto level for DMY3DP-001 3d printer (anet a8 clone with modified melzi electronics)
It use the bed sensor to auto level and correct distortion.

Be aware on first use !
You must check if the head will scratch the bed.
To adjust the first layer height you must adjust Z_Probe_height in eeprom settings accordingly to your printer.

The starting G-code must contain :
G28 ; home X and Y (Z homing disabled in firmware)
G1 X10 Y10 Z10; going out of parking pos
G32 ; auto bed level Repetier

To compile it you need to add the sanguino board to arduino :
Add this board manager to your arduino : 
https://raw.githubusercontent.com/Lauszus/Sanguino/master/package_lauszus_sanguino_index.json 
See full explanation on  https://github.com/Lauszus/Sanguino

To upload it you may need and ISP to put the arduino bootloader on your board, then use classic arduino USB upload.
