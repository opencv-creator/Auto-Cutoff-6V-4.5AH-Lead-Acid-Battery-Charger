all the Schematics present in youtube or internet didnt work, either they never full charge the battery or they dont stop charging after full charge or 
they contain Relay which switches On and Off when full charge of Battery is about to Reach.

<img width="824" height="1000" alt="lead acid battery" src="https://github.com/user-attachments/assets/072354a9-f384-4698-a528-3bba5ce07cb2" />


Charging Current Limit: Do not exceed 10%–20% of the battery's Ah rating (for example, a 5Ah battery should use roughly a 0.5A to 1A charger)
Battery Charging Voltage for Cycle use where Battery is fully Discharged and Recharged again (the Lead Acid Battery is charged at 7.2 to 7.4V ) and for Standby Use or Backup Mode where Battery stays connected to charger continuously (charging voltage is 6.8 to 6.9v). I am using Cycle use, so Charging Voltage 7.2V

1) use 12v 1Amp Transformer with Full Wave Rectifier to create 12v Dc.(All diodes used in the below full wave rectifier are 1N4148)

<img width="671" height="329" alt="full wave rectifier" src="https://github.com/user-attachments/assets/700c677e-904c-4125-94d9-3aacc1ebe1c3" />

2) Use LM317T create 7.4V using 12V Dc which will be used for finally charging the 6V 4.5AH Lead Acid battery

<img width="748" height="380" alt="LM317-typical-adjustable-regulator-ckt" src="https://github.com/user-attachments/assets/c8a5e4ea-4b45-4db5-9dda-a48ffdc07d93" />


4) Use 7805 Voltage Regulator for creating 5V for powering the OpAmp LM358, CD4013 ( D-FLIP FLOP ) and TL431 programmable shunt voltage regulator

5) First Remove the 6v 4.5AH Lead acid battery , connect Variable Power Supply as shown in below figure

<img width="1674" height="1338" alt="variable power supply" src="https://github.com/user-attachments/assets/6a3ac4e7-23fc-4a4e-a379-6123e3f0cf19" />

<br>
<br>

6) In the Schematic mentioned in the below picture , Preset Resistors R1, R2 and R3, R4 (all are 200k ohms Presets) , connect the Variable power supply shown in above figure to COM pin of 5V Relay and keep 6v as the Variable power Supply output and adjust R1,R2 such that VL = 2.5v and in the same way keep 7.2v as the Variable power Supply output and R3, R4 should be adjusted ,such that they produce VH = 2.5v. after this Connect the 6v 4.5AH Lead acid battery and switch on the Power supply. when the battery voltage as read by R1, R2 is greater than 6v then Battery starts charging indicated by Green Led present at Relay's NC Pin and when Charging completes approximately after 17 Hrs then Red Led present Relays
NO pin will glow indicating Full Charge.

<img width="300" height="279" alt="RELAY" src="https://github.com/user-attachments/assets/a66d66fd-11a3-4539-b3e9-a7a7d74dc7e5" />


<br>

<img width="1536" height="1024" alt="final 6v auto cutoff with two opamps by chatgpt" src="https://github.com/user-attachments/assets/792827a1-06e8-4007-8cae-8889d6203b4a" />

