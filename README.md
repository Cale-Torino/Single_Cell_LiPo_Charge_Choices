# Single Cell LiPo Charge Choices


Looking at these suitable candidates for low power low current draw options the:

- TP4054 (no protection, 1 led, uA of current draw when disconnected from charger)
- TP4055 (protection, 1 led, uA of current draw when disconnected from charger)
- TP4057 (protection, 2 leds, uA of current draw when disconnected from charger)

add extra protection IC's (DW01A battery protection IC or similar) and (FS8205A dual Mosfets or similar)

are good choices

I received IC's with the markings LTH7 (probably a copy of the LTC4054) and 55b3 (maybe the TP4055?) 

So far only the 55b3 is working as expected [no current draw when off charge, flashing led when no battery, solid led when charging, led off when full, reverse battery protection works led off while in this state, 5k1 resistor programms 188mA of charging current]



# TP4054

```
 Pinout of the TP4054:
             __  __
       CHRG |1  \/5| PROG
        GND |2     | 
       BATT |3    4| VCC
            -------
```

- 1 led (see Traffic light control circuit for adding 2leds)
- no reverse battery protection
- no reverse input protection
- 0 ~ 0.6Ω dissipation resistor
- 5 pins
- When the input supply (wall adapter or USB supply) is removed, the TP4054 automatically enters a low current state, dropping the battery drain current to less than 2uA.

FEATURES
- Maximize Charge Rate Without Risk of Overheating
- For Single Cell titanic acid Lithium-Ion Batteries
- Trickle, constant-current and constant-voltage control
- Charges Single Cell Li-Ion Batteries Directly from USB Port
- Preset Charge Voltage with 1% Accuracy Automatic Recharge
- One Charge Status Output Pins
- C/10 Charge Termination
- 45uA Supply Current in Shutdown
- Available in 5-Lead SOT-23 Package

# TP4055

```
 Pinout of the TP4055:
             __  __
       CHRG |1  \/5| PROG
        GND |2     | 
       BATT |3    4| VCC
            -------
```

- 1 led 
- reverse battery protection
- reverse input protection
- 0 ~ 0.6Ω dissipation resistor
- 5 pins
- reverse battery protection and power supply reverse connect protection with a charging current of 500mA
- When the input supply (wall adapter or USB supply) is removed, the TP4055 automatically enters a low current state, dropping the battery drain current to less than 2uA.

FEATURES
- 500mA Programmable Charge Current
- Lithium-ion batteries Reverse battery protection
- Maximize Charge Rate Without Risk of Overheating
- For Single Cell titanic acid Lithium- Ion Batteries
- Trickle, constant-current and constant-voltage control
- Charges Single Cell Li-Ion Batteries Directly from USB Port
- Preset Charge Voltage with 1%Accuracy
- Highest input can be up to 9V
- Automatic Recharge
- One Charge Status Output Pins
- C/10 Charge Termination
- 40uA Supply Current in Shutdown
- Available in 5-Lead SOT-23 Package

# TP4057

```
 Pinout of the TP4057:
             __  __
       CHRG |1  \/6| PROG
        GND |2    5| STDBY
       BATT |3    4| VCC
            -------
```

- 2 leds
- reverse battery protection
- reverse input protection
- 0 ~ 0.6Ω dissipation resistor
- 6 pins
- When the input supply (wall adapter or USB supply) is removed, the TP4057 automatically enters a low current state, dropping the battery drain current to less than 2uA.

FEATURES
- 500mA Programmable Charge Current
- Lithium-ion batteries Reverse battery protection
- Maximize Charge Rate Without Risk of Overheating
- For Single Cell titanic acid Lithium-Ion Batteries
- Trickle, constant-current and constant-voltage control
- Charges Single Cell Li-Ion Batteries Directly from USB Port
- Preset Charge Voltage with 1% Accuracy
- Highest input can be up to 9V
- Automatic Recharge
- One Charge Status Output Pins
- C/10 Charge Termination
- 40uA Supply Current in Shutdown
- Available in 6-Lead SOT-23 Package

# TP4058

```
 Pinout of the TP4058:
             __  __
       CHRG |1  \/5| PROG
        GND |2     | 
       BATT |3    4| VCC
            -------
```

- 1 led
- reverse battery protection
- reverse input protection
- 0 ~ 0.6Ω dissipation resistor
- 5 pins
- When the input supply (wall adapter or USB supply) is removed, the TP4058 automatically enters a low current state, dropping the battery drain current to less than 2uA.

FEATURES
- 600mA Programmable Charge Current
- Lithium-ion batteries Reverse battery protection
- Maximize Charge Rate Without Risk of Overheating
- For Single Cell titanic acid Lithium-Ion Batteries
- Trickle, constant-current and constant-voltage control
- Charges Single Cell Li-Ion Batteries Directly from USB Port
- Preset Charge Voltage with 1% Accuracy
- Highest input can be up to 9V
- Automatic Recharge
- One Charge Status Output Pins
- C/10 Charge Termination
- 145uA Supply Current in Shutdown
- Available in 5-Lead SOT-23 Package

# TP4059

```
 Pinout of the TP4059:
             __  __
       CHRG |1  \/6| PROG
        GND |2    5| STDBY
       BATT |3    4| VCC
            -------
```

- using SOT23 package, high current application (above 400mA) heat dissipation effect is not good may cause the charging current is protected by temperature and reduce.
- In order to ensure reliable use in various situations and prevent chip damage caused by spike and burr voltage, it is recommended that the Vcc end and BAT end of TP4059 application are respectively connected with 1uF and 10uF capacitors, if possible, they can also be connected with a 0.1U ceramic capacitor.
- All capacitors should be located close to the chip pin, not too far away.
- Battery reverse leakage current 4.3mA
- 2 leds
- reverse battery protection
- reverse input protection
- 0 ~ 0.6Ω dissipation resistor
- 6 pins
- When the input voltage (AC adapter or USB power supply) is removed, the TP4059 automatically enters a low current state with the battery leakage current below 2uA.

FEATURES
- Lithium battery reverse connection protection
- Programmable Charge Current 600mA
- Trickle, constant-current and constant-voltage control
- Preset Charge Voltage with 1% Accuracy
- Highest input can be up to 9V
- Automatic Recharge
- Available in 6-Lead SOT-23 Package
- Two Charge Status Output Pins
- C/10 Charge Termination
- For Single Cell titanic acid Lithium-Ion Batteries

links
- https://electronics.stackexchange.com/questions/438262/ltc4054-odd-behaviour
- https://www.lcsc.com/product-detail/Battery-Management-ICs_TPOWER-TP4054_C382138.html
- https://www.analog.com/media/en/technical-documentation/data-sheets/405642f.pdf
- http://toppwr.com/eproduct/view.php?id=478
- https://www.lcsc.com/datasheet/lcsc_datasheet_1912111437_TPOWER-TP4054_C382138.pdf
- https://www.lcsc.com/datasheet/lcsc_datasheet_2401050929_JSMSEMI-TP4054_C5381776.pdf
- https://www.lcsc.com/datasheet/lcsc_datasheet_2504101957_UMW-Youtai-Semiconductor-Co---Ltd--TP4054_C668215.pdf
- https://www.lcsc.com/product-detail/Battery-Management-ICs_TPOWER-TP4054_C382138.html
- https://www.lcsc.com/product-detail/Battery-Management_TPOWER-TP4054_C382138.html
- https://www.lcsc.com/datasheet/lcsc_datasheet_2306011542_TPOWER-TP4582B_C5464794.pdf
- https://electronics.stackexchange.com/questions/710777/strange-resistor-in-battery-charger
- https://hmsemi.com/downfile/DW01A.PDF
- https://datasheet.lcsc.com/lcsc/2010271837_FUXINSEMI-FS8205A_C908265.pdf
- https://jlcpcb.com/partdetail/FortuneSemicon-FS8205A/C16052
- https://electronics.stackexchange.com/questions/656031/can-i-use-this-mosfet-instead-of-the-standard-fs8205



