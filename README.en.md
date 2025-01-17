# Luobinsen 6th Generation Charger User Manual

 <div>
     <img src="image/wps1.jpg" alt="img" style="zoom:80%;" />
 </div>



- Generation6 chargers introduction

- Installation Operation Manual

- Service Manual

 

You can contact me via email: [overseas@luobinsen.net](mailto:overseas@luobinsen.net)

 

Generation6 chargers introduction

This is a supplemental file which contains:

1. How to use the charger for the first time

2. Procedures for checking for start failures, faults and abnormal charging stops

 

## How to use the charger for the first time

- The charger should be installed according to the Installation Operation Manual

- Open the cover on the back of the screen

- A rechargeable battery needs to be installed, Rechargeable battery should be used, Battery type ML2032 is recommended. If the battery is not fitted and the charger has an incorrect date and time, you will need to enter the correct date and time each time the power is supplied.

<div>
    <img src="image/wps2.jpg" alt="img" style="zoom: 150%;" />
</div>



- If you want to connect the charger to the Central System, a public network cable or a SIM card or WIFI needs to be provided. The public network cable or SIM card needs to be installed on the back of the screen.

- Close the cover on the back of the screen

- Check that each component on the outside and inside of the charger has not been damaged

- Check all screws for no looseness, AC circuit breaker, AC contactor, AC copper row, DC contactor, fuse, shunt, charge gun, AC copper row.

- Measure the AC supply voltage between L1/L2/L3/N to meet the requirements of the charger, you can refer to the nameplate of the charger. The type of AC supply cable should be in accordance with the installation documentation of the charger.

- Turn on the main circuit breaker and all miniature circuit breakers

- Setting the date and time after the screen is on

- Connect the connector to the vehicle and try to start charging with the card

## Steps for connecting charger to the Central  System

 

Go to Network Parameters and change the following parameters

- Example 1: 
  - for a charge point with identity “CP001” connecting to a Central System with OCPP-J endpoint URL "ws://centralsystem.example.com/ocpp" this would give the following connection URL: ws://centralsystem.example.com/ocpp/CP001

<div>
    <img src="image/wps3.png" alt="img" style="zoom:100%;" />
</div>



- Example 2: 
  - for a charge point with identity “RDAM 123” connecting to a Central System with OCPP-J endpoint URL "wss://centralsystem.example.com/ocppj" this would give the following URL:wss://centralsystem.example.com/ocppj/RDAM%20123

<div>
    <img src="image/wps4.png" alt="img" style="zoom:100%;" />
</div>


- Note: Both ends of the OCPPURL should contain “/”

- The reset button is in the manufacturer parameters

## Analysis and treatment of start-up failures

 

### there is voltage in battery

l Charger checks to vehicle battery voltage in standby condition, possible vehicle DC contactor damaged

l The CCM voltage is not accurate and the CCM AD voltage needs to be calibrated.

<div>
    <img src="image/wps46.jpg" alt="img" style="zoom:100%;" />
</div>


### 1.2 insulation detection fault

l Check the insulation of the DC output of the charger

l Check the charging module

l The CCM voltage is not accurate and the CCM AD voltage needs to be calibrated.

<div>
    <img src="image/wps47.jpg" alt="img" style="zoom:100%;" />
</div>


### 1.3 contactor not open

l Check the DC contactor

 

### 1.4 1802 telegram  time out

l Check and replace the SECC

l Check and replace the CCM

 

### 1.5 1806 telegram  time out

l Check and replace the SECC

l Check and replace the CCM

 

### 1.6 battery reverse connected

l GBT charger not detecting vehicle battery voltage

 

### 1.7 1811 telegram  time out

l Check and replace the SECC

l Check and replace the CCM

 

### 1.8 1009

l Check and replace the SECC

 

### 1.9 handshake time out

l Check and replace the SECC

 

### 1.10 BMS other message time out

l Check and replace the SECC

 

### BMS other message time out 1

l Check and replace the SECC

 

### connector disconnect and terminated

l Disable “JIS insulation fast test”,Enable “Insulation detection enable”

<div>
    <img src="image/wps48.jpg" alt="img" style="zoom:100%;" />
</div>





The AD board is a quick check board, select enable.

AD board is not a fast detection board, select disable.

Whether the AD is a quick check AD to see whether there is a white relay inside the AD board, without removing the shell, from the bottom to the inside, you can see it

 

### 1.13 contactor not closed or short circuit fault

l Check the DC contactor

l The CCM voltage is not accurate and the CCM AD voltage needs to be calibrated.

 

### 1.14 Abnormal detection voltage range

l The output voltage range of the charger（200-1000V） is not sufficient for the vehicle and the vehicle cannot be charged at this charger.

 

### 1.15 old standard(GB/T & Local area) disabled charger not support

l The charger's communication protocol does not meet the vehicle

 

1.16 SOC not reachable

l The charger's communication protocol does not meet the vehicle

 

1.17 battery voltage higher than charger Max.output voltage

l The output voltage range of the charger（200-1000V） is not sufficient for the vehicle and the vehicle cannot be charged at this charger.

 

1.18 Abnormal battery voltage - exceeding the current battery voltage range of BCP message

l The output voltage range of the charger（200-1000V） is not sufficient for the vehicle and the vehicle cannot be charged at this charger.

 

1.19 control command stop

l CMS has sent a stop command to the charger, check the CMS

 

1.20 Authentication failed

l User ID does not exist or is expired or frozen in CMS

 

1.21 BMS start on fault

l Charger and vehicle communication error, try replacing the SECC

 

1.22 over voltage fault

l Check charger output voltage

l The CCM voltage is not accurate and the CCM AD voltage needs to be calibrated.

 

1.23 insulation detection boost failed

l Check that the charging module is working properly

l The CCM voltage is not accurate and the CCM AD voltage needs to be calibrated.

 

1.24 The confirmation result of receiving the TCU message CMD12 from the State Grid is failed

l Replacement of TCU

 

1.25 TCU normal stop

l Replacement of TCU

 

1.26 TCU charge-control unit stop due to charging controler fault

l Replacement of TCU

 

1.27 Communication failure between TCU charging control unit and charging controller

l Check CCM power supply

l Check and replace the network cable between the TCU and the CCM

l Replacement of CCM

 

1.28 TCU card reader communication fault

l Check the card reader and its wiring harness

l Replacement of card reader

 

1.29 Communication failure between TCU and Meter device

l Check meter power supply

l Replacement Meter

 

1.30 TCUESAM fault

l Replacement of TCU

 

1.31 TCU metering data verification is abnormal

l Check and replace DC energy meters

 

1.32 TCU stop due to other faults

l For unknown reasons, please contact the supplier to check

 

1.33 TCU communication abnormal

l Check and replace TCU

 

1.34 Vehicle startup BRO message is abnormal

l Check and replace the SECC

 

1.35 channel no charging TUTEL

l TUTEL-specific protocols

 

1.36 connector charging stop

l Check the connection between the charging gun and the vehicle or replace the charging gun

 

1.37 Emergency stop fault

l The emergency stop button has been pressed and there is no abnormality, please restore it.

 

1.38 door open fault

l The door is open. Please close it.

l Check the door limit switches

 

1.39 DC Metering communication fault

l Checking the power supply to the DC energy meter

l Check the communication harness of the DC energy meter

l Check DC meter address

<div>
    <img src="image/wps49.jpg" alt="img" style="zoom:100%;" />
</div>





l Replacement of DC Meter

 

1.40 communicate with CCM time out

l Check CCM power supply

l Check and replace the network cable between the TCU and the CCM

l Checking the parameters of the CCM

<table>
    <tr>
    	<td>
        	<img src="image/wps50.jpg" alt="img" style="zoom:100%;" />
        </td>
        <td>
        	<img src="image/wps51.jpg" alt="img" style="zoom:100%;" />
        </td>
    </tr>
</table>



l Replacement of CCM

 

1.41 No charging fault

l Please contact the supplier to check

 

1.42 Fuse fault

l Check fuses

 

1.43 Lightning arrester fault

l Check or replace SPD

 

1.44 Termial board abnormal

l Check FZ power supply

l Check FZ communication harness

l Replacement of FZ

 

1.45 AC/DC controler fault

l Please contact the supplier to check

 

1.46 aircondition controler fault

l Check the power supply to the air conditioning control board

l Check the communication harness of the air conditioning control board

l Replacement of air conditioning control board

 

1.47 AD unit communicate module fault

l Check that the AD address is correct

l Check the power supply to the AD

l Check AD communication harness

l Replacement of AD

 

1.48 all airconditioner fault

l Check all air conditioning power

l Check all air conditioning communication harnesses

l Maybe all the air conditioners are broken.

 

1.49 Excessive wind speed

l The wind is too strong. Wait for the wind to die down.

l The anemometer's broken.

 

1.50 main breaker electrical operator fault

l The main breaker is broken, it needs to be replaced.

 

1.51 SDV fault

l The SDV is broken, it needs to be replaced.

 

1.52 Metering device fault

l Replacement of DC energy meters

 

1.53 main breaker electrical operator no power supply operation fault

l Check the power supply to the main circuit breaker

l The main breaker is broken, it needs to be replaced.

 

1.54 on maintenance

l The charger is in service mode, note the position of the service button

 

1.55 FLASH fault

l The flash board in the middle of the CCM is damaged and needs to be replaced.

 

1.56 RAM fault

l The flash board in the middle of the CCM is damaged and needs to be replaced.

 

1.57 SECC_PLC communication fault

l Check the power supply of the SECC

l Checking the communication cable between SECC and CCM

l Replacement SECC

 

1.58 Parallel contactor fault or module terminal voltage abnormality

l Check or replace the intermediate contactor

l The CCM voltage is not accurate and the CCM AD voltage needs to be calibrated.

 

1.59 smoke sensor fault

l Fire or smoke in the cabinet

l The smoke detector is broken.

 

1.60 eletrical locker fault

l GBT charging gun electronic lock abnormality

 

1.61 temperature of cabinet high fault

l High temperature inside the cabinet, need to stop and cool the charger

l The temperature sensor is broken

 

1.62 channel specific remote control time out

l Please contact the supplier to check

 

1.63 Real-time clock RTC fault

l The TCU's battery needs to be installed

l Time needs to be calibrated.

l TCU is damaged, please replace the TCU

 

1.64 CCM enters start charging

l Charger and vehicle communication is in progress, please wait

 

1.65 CCM enters charging time out

l Communication failure between charger and vehicle

l Check and replace the SECC

 

1.66 VIN Get failed

l Check AC power supply

l Check the AC contactor

l Check charging module

 

1.67 output short circuit

l Charger output short circuit, please check whether the charger or vehicle is short-circuited

 

1.68 input phase missing

l AC input phase sequence is wrong, please change the correct phase sequence

 

1.69 input over voltage

l Input AC voltage higher than charger AC voltage range2

l Checking the parameters of the CCM

<div>
    <img src="image/wps52.jpg" alt="img" style="zoom:100%;" />
</div>







1.70 input lower voltage

l Input AC voltage lower than charger AC voltage range

l Checking the parameters of the CCM

 

1.71 communication of insulation module fault

l Please contact the supplier to check

 

1.72 input insulation fault

l Please disconnect the power and check the input insulation

 

1.73 BMS communcation module fault

l Please contact the supplier to check

 

1.74 Fire alarm

l Please check the fire extinguisher.

 

1.75 other unkown reason

l Please contact the supplier to check

 

1.76 Electronic lock feedback abnormality

l Charging gun electronic lock abnormality, please replace the charging gun

 

1.77 DC contactor abnormality

l Damaged DC contactor, replace DC contactor

 

1.78 DC pre charging fault

l Please check the charging module

l Please check the AD voltage value of the CCM and calibrate it

 

1.79 Input insulation self-test abnormality

l The input insulation self-test board is abnormal, please replace it.

 

1.80 Abnormal output insulation self check

l The output insulation self-test board is abnormal, please replace it.

 

1.81 Manual shutdown during startup

l Stopped during startup

 

1.82 Card swiping shutdown during startup

l Stopped by a swipe during startup

 

1.83 Remote shutdown during startup

l Remote stop during startup

 

1.84 Power loss

l Input power suddenly cut off

 

1.85 Ground detection function communication failure

l Check the power supply to the ground detector

l Check the communication harness of the ground detector

 

1.86 Ground fault

l Earth wire error, please check if the earth wire is firmly connected

 

1.87 Phase loss alarm

l Check input for phase loss

 

##  Failure analysis and handling

 

2.1 Emergency stop fault

l The emergency stop button has been pressed and there is no abnormality, please restore it.

 

2.2 Parallel contactor fault or module terminal voltage abnormality

l Check or replace the intermediate contactor

l The CCM voltage is not accurate and the CCM AD voltage needs to be calibrated.

 

2.3 DC Metering communication fault

l Checking the power supply to the DC energy meter

l Check the communication harness of the DC energy meter

l Check DC meter address

 

2.4 communicate with CCM time out

l Check CCM power supply

l Check and replace the network cable between the TCU and the CCM

l Checking the parameters of the CCM

 

2.5 temperature of cabinet high fault

l High temperature inside the cabinet, need to stop and cool the charger

l The temperature sensor is broken

 

2.6 CCS2 communication module fault

l Check the power supply of the SECC

l Checking the communication cable between SECC and CCM

l Replacement SECC

 

2.7 door open fault

l The door is open. Please close it.

l Check the door limit switches

 

2.8 No charging fault

l Please contact the supplier to check

 

2.9 Fuse fault

l Check fuse

 

2.10 Lightning arrester fault

l Check or replace SPD

 

2.11 Termial board abnormal

l Check FZ power supply

l Check FZ communication harness

l Replacement of FZ

 

2.12 AC/DC controler fault

l Please contact the supplier to check

 

2.13 aircondition controler fault

l Check the power supply to the air conditioning control board

l Check the communication harness of the air conditioning control board

l Replacement of air conditioning control board

 

2.14 AD unit communicate module fault

l Check that the AD address is correct

l Check the power supply to the AD

l Check AD communication harness

l Replacement of AD

 

2.15 airconditioner fault

l Check the power supply to the air conditioner

l Check air conditioning communication harness

l Replacement of air conditioners

 

2.16 Excessive wind speed

l The wind is too strong. Wait for the wind to die down.

l The anemometer's broken.

 

2.17 main breaker electrical operator fault

l The main breaker is broken, it needs to be replaced

 

2.18 SDV fault

l The SDV is broken, it needs to be replaced

 

2.19 Metering device fault

l Replacement of DC energy meters

 

2.20 abnormal operation without power supply

l Check that the AC contactor is closed

 

2.21 maintenance status

l The charger is in service mode, note the position of the service button

 

2.22 smoke sensor fault

l Fire or smoke in the cabinet

l The smoke detector is broken.

 

2.23 eletrical locker fault

l GBT charging gun electronic lock abnormality,

l Replacement of charging gun

 

2.24 Real-time clock RTC fault

l The TCU's battery needs to be installed

l Time needs to be calibrated.

l TCU is damaged, please replace the TCU

 

2.25 CCM procedure fault

l Replacement of SECC

 

2.26 output short circuit

l Charger output short circuit, please check whether the charger or vehicle is short-circuited

 

2.27 input phase missing

l AC input phase sequence is wrong, please change the correct phase sequence

 

2.28 input over voltage

l Input AC voltage higher than charger AC voltage range2

l Checking the parameters of the CCM

 

2.29 input lower voltage

l Input AC voltage lower than charger AC voltage range

l Checking the parameters of the CCM

 

2.30 communication of insulation module fault

l Please contact the supplier to check

 

2.31 input insulation fault

l Please disconnect the power and check the input insulation

 

2.32 BMS communcation module fault

l Please contact the supplier to check

 

2.33 FLASH fault

l The flash board in the middle of the CCM is damaged and needs to be replaced.

 

2.34 RAM fault

l The flash board in the middle of the CCM is damaged and needs to be replaced.

 

2.35 Fire alarm

l Please check the fire extinguisher.

 

2.36 other unkown reason

l Please contact the supplier to check

 

2.37 Output contactor failure

l Check or replace the DC contactor

 

2.38 Input insulation self check fault

l The input insulation self-test board is abnormal, please replace it.

 

2.39 Output insulation self check fault

l The output insulation self-test board is abnormal, please replace it.

 

2.40 Power loss

l Input power suddenly cut off

 

2.41 Ground detection function communication failure

l Check the power supply to the ground detector

l Check the communication harness of the ground detector

 

2.42 Ground fault

l Earth wire error, please check if the earth wire is firmly connected

 

2.43 Phase loss alarm

l Check input for phase loss

 

 

 

## Analysis and handling of abnormal stop of transactions

3.1 BMS time out

l Check and replace the SECC

l Check and replace the CCM

 

3.2 Timeout or unknown reason process error

l Check and replace the SECC

l Check and replace the CCM

 

3.3 BMS insulation fault

l Check the insulation of the DC output of the charger

l Check the charging module

 

3.4 BMS output connector overtemperature

l Check charging gun temperature and replace charging gun

l Check if the vehicle's sockets are damaged, or that the sockets need to be replaced.

 

3.5 BMS element output connector overtemperature

l Check charging gun temperature and replace charging gun

l Check if the vehicle's sockets are damaged, or that the sockets need to be replaced.

 

3.6 BMS connector fault

l Check and replace charging gun

l Check if the vehicle's sockets are damaged, or that the sockets need to be replaced.

 

3.7 BMS battery group temperater high

l Vehicle battery performance issues

 

3.8 BMS other faults

l Please contact the supplier to check

 

3.9 BMS over current

l Check charger output current

 

3.10 BMS voltage abnormal

l Check charger output voltage

 

3.11 BMS high voltage relay fault

l Damaged vehicle DC contactor

 

3.12 BMS detection point fault

l Check that the charging gun is securely connected

 

3.13 BMS reach request SOC

l Normal stop or vehicle SOC issues

 

3.14 BMS reach total voltage setting value output over voltagve warning

l Check the AD voltage value of the CCM and calibrate it

 

3.15 BMS reach unit voltage setting value

l Normal stops or battery performance problems

 

3.16 BMS secondary alarm unit power battery voltage is too high

l Normal stops or battery performance problems

 

3.17 BMS secondary alarm unit power battery voltage is too low

l Normal stops or battery performance problems

 

3.18 BMS SOC too high

l Normal stops or battery performance problems

 

3.19 BMS SOC too low

l Battery performance problems

 

3.20 BMS charing over current

l Check charger output current

 

3.21 BMS battery temperature too high

l Battery performance problems

l 

3.22 BMS battery insulation abnormal

l Check charger or vehicle insulation

 

3.23 BMS connection status abnormal

l Check that the charging gun is securely connected to the vehicle

l Replace the charging gun or vehicle socket

 

3.24 BMS no charging or control point current too low for 10 minutes

l Low or no output current

l Check the DC contactor

l Check fuses

l Check AC power supply

l Check AC contactor

l Check charging module

l Check DC energy meter

 

3.25 manually stop

l The stop button on the screen is pressed

 

3.26 stop after reach request

l Full or battery performance issues

 

3.27 stop of insufficient account

l Insufficient user balance, need to top up from CMS

 

3.28 request voltage over Max.voltage

l The output voltage range of the charger（200-1000V） is not sufficient for the vehicle and the vehicle cannot be charged at this charger.

 

3.29 request voltage lower than Min.voltage

l The output voltage range of the charger（200-1000V） is not sufficient for the vehicle and the vehicle cannot be charged at this charger.

 

3.30 single battery unit over temperature

l Vehicle battery performance issues

 

3.31 battery temperature too high

l Vehicle battery performance issues

 

3.32 remote stop

l CMS controlled charging stop

 

3.33 no charging current exceeds the allowed time

l Low or no output current

l Check the DC contactor

l Check fuses

l Check AC power supply

l Check AC contactor

l Check charging module

l Check DC energy meter

 

3.34 swipe card to stop charging

l The card has been swiped to stop

 

3.35 connector pull out to stop charging

l Connector disconnection stops during charging

l Check or replace the charging gun

 

3.36 connector temperature too high

l Check or replace the charging gun

l Check the charging gun temperature from the parameter

 

3.37 disconnect  connector

l Connector disconnection stops during charging

l Check or replace the charging gun

 

3.38 stop of charger detect insulation failure

l Check the insulation of the DC output of the charger

l Check the charging module

 

3.39 the confirmation result of receiving the State Grid TCU message CMD12 is Failed.

l Replacement of TCU

 

3.40 TCU normal stop

l Replacement of TCU

 

3.41 TCU charge-control unit stop due to charging controler fault

l Replacement of TCU

 

3.42 Communication failure between TCU charging control unit and charging controller

l Check CCM power supply

l Check and replace the network cable between the TCU and the CCM

l Replacement of CCM

 

3.43 Communication failure between TCU and Meter device

l Check meter power supply

l Replacement Meter

 

3.44 TCUESAM fault

l Replacement of TCU

 

3.45 TCU metering data verification is abnormal

l Check and replace DC energy meters

 

3.46 stop of TCU other faults

l Please contact the supplier to check

 

3.47 stop of TCU communication faults

l Please contact the supplier to check

 

3.48 Max.current exceed fault

l Check and replace TCU

 

3.49 channel stop charging

l Please contact the supplier to check

 

3.50 stop charging due to charging current lower than 0.5A for 5 minutes

l Low or no output current

l Check the DC contactor

l Check fuses

l Check AC power supply

l Check AC contactor

l Check charging module

l Check DC energy meter

 

3.51 slave stop

l Failure of the second connector to start when charging a vehicle with two guns

 

3.52 Emergency stop fault

l The emergency stop button has been pressed and there is no abnormality, please restore it.

 

3.53 door open fault

l The door is open. Please close it.

l Check the door limit switches

 

3.54 DC Metering communication fault

l Checking the power supply to the DC energy meter

l Check the communication harness of the DC energy meter

l Check DC meter address

 

3.55 communicate with CCM time out

l Check CCM power supply

l Check and replace the network cable between the TCU and the CCM

l Checking the parameters of the CCM

 

3.56 No charging fault

l Please contact the supplier to check

 

3.57 Fuse fault

l Check fuses

 

3.58 Lightning arrester fault

l Check or replace SPD

 

3.59 Termial board abnormal

l Check FZ power supply

l Check FZ communication harness

l Replacement of FZ

 

3.60 AC/DC controler fault

l Please contact the supplier to check

 

3.61 aircondition controler fault

l Check the power supply to the air conditioning control board

l Check the communication harness of the air conditioning control board

l Replacement of air conditioning control board

 

3.62 AD unit communicate module fault

l Check that the AD address is correct

l Check the power supply to the AD

l Check AD communication harness

 

3.63 airconditioner fault

l Check the power supply to the air conditioning control board

l Check the communication harness of the air conditioning control board

l Replacement of air conditioning control board

 

3.64 Excessive wind speed

l The wind is too strong. Wait for the wind to die down.

l The anemometer's broken.

 

3.65 main breaker electrical operator fault

l The main breaker is broken, it needs to be replaced.

 

3.66 SDV fault

l The SDV is broken, it needs to be replaced.

 

3.67 Metering device fault

l Replacement of DC energy meters

 

3.68 main breaker electrical operator no power supply operation fault

l Check the power supply to the main circuit breaker

l The main breaker is broken, it needs to be replaced.

 

3.69 on maintenance

l The charger is in service mode, note the position of the service button

 

3.70 smoke sensor fault

l Fire or smoke in the cabinet

 

3.71 eletrical locker fault

l GBT charging gun electronic lock abnormality

 

3.72 SECC_PLC abnormal communication

l Check the power supply of the SECC

l Checking the communication cable between SECC and CCM

l Replacement SECC

 

3.73 temperature of cabinet high fault

l High temperature inside the cabinet, need to stop and cool the charger

l The temperature sensor is broken

 

3.74 channel specific remote control time out

l Please contact the supplier to check

 

3.75 Real-time clock RTC fault

l The TCU's battery needs to be installed

l Time needs to be calibrated.

l TCU is damaged, please replace the TCU

 

3.76 Active time reached

l Stop at set time

 

3.77 Authentication exception (application serial number USID exception)

l Please contact the supplier to check

 

3.78 Abnormal stop of metering The starting power is bigger than the ending power

l Please contact the supplier to check

 

3.79 Max.charging time reached 12 hours

l Charging duration over 12 hours stops

 

3.80 time record-start time fault

l Transaction start time error

 

3.81 hard reset finish

l CMS sends a hard reset

 

3.82 soft reset finish

l CMS sends a soft reset

 

3.83 stop charging due to internet fault

l Please contact the supplier to check

 

3.84 stop charging due to Metering fault

l Check and replace DC energy meters

 

3.85 output short circuit

l Charger output short circuit, please check whether the charger or vehicle is short-circuited

 

3.86 input AC phase missing

l AC input phase sequence is wrong, please change the correct phase sequence

 

3.87 input AC over voltage

l Input AC voltage higher than charger AC voltage range2

 

3.88 input AC low voltage

l Input AC voltage lower than charger AC voltage range

 

3.89 communication of insulation module fault

l Please contact the supplier to check

 

3.90 input insulation fault

l Please disconnect the power and check the input insulation

 

3.91 BMS communcation module fault

l Please contact the supplier to check

 

3.92 Power down

l Input power suddenly cut off

 

3.93 Fire alarm

l Please check the fire extinguisher.

 

3.94 BMS termination

l Normal stops or battery performance problems

 

3.95 stop for unknown reason

l Please contact the supplier to check

 

3.96 DC contactor abnormality

l Damaged DC contactor, replace DC contactor

 

3.97 Abnormal parallel contactor

l Check or replace the intermediate contactor

 

3.98 Abnormal output current exceeding control current

l Check output current

 

3.99 Input insulation self check fault shutdown

l The input insulation self-test board is abnormal, please replace it

 

3.100 Output insulation self check fault shutdown

l The output insulation self-test board is abnormal, please replace it.

 

3.101 Ground detection function communication failure

l Check the power supply to the ground detector

l Check the communication harness of the ground detector

 

3.102 Ground fault

l Earth wire error, please check if the earth wire is firmly connected

 

3.103 Phase loss alarm

l Check input for phase loss



## maintain





## appendix Ⅰ

 <div>
     <img src="image/image-20250116131712648.png" alt="image-20250116131712648" style="zoom:100%;" />
 </div>



 <div>
     <img src="image/image-20250116131808653.png" alt="image-20250116131808653" style="zoom:100%;" />
 </div>



 <div>
     <img src="image/image-20250116131849312.png" alt="image-20250116131849312" style="zoom:100%;" />
 </div>



