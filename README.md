# BEOK-BOT313-Wifi-Thermostat
After searching for a wifi thermostat on Aliexpress, I found this really nice BEOK BOT-313 wifi controlled thermostat.
In this repository all knowledge up till now will be contained.

#Media:
* Manual of the thermostat, scanned.
* Manual of the wifi chip.
* Pictures of the boards inside.

#Found out up till now:
* The Android or IOS app is used to communicate the wifi acces point name and password to the device.
* The app and thermostat only work on a local lan, not via the cloud. No idea if the app or thermostat itself communication unknowingly with Beok without letting us know about it.
* The wifi chip is a WT1SBS from Broadlink (more infos in the pdf folder).
* The main microprocessor is a PIC16F1947 with build in LCD driver/peripheral.
* There are two relais on the powerboard, one is a NO contact and is isolated. The other relais is directly connected to mains with one and and has a NC and NO contact, so it can be used to switch lights or heaters. Not knowing that that relais is connected to mains is quite dangerous and the feedback on the product shows some funny pictures from users connectin there HVAC to the wrong relais pins, putting 230V on their mains. Both relais are switched with the same GPIO pin, so no way to switch them individually.
* The main pcb has space for a buzzer.


* WARNING, the isolation between mains and the rest of the PCB is really bad, less than 1mm as far as I could find out, so not really safe.
* WARNING, it is stated that about 3A of current can be switched, but even for that the PCB traces seem kind of thin.
