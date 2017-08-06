## TVM802B Interconnections

Inside the TVM802B before the conversion to Smoothie / OpenPnP.

Inside of TVM802B:
[Inside of TVM802B](https://raw.githubusercontent.com/johngrabner/tvm802B_2_smoothie_and_OpenPnP/master/Images/Labels%20on%20Images/Slide1%20-%20Inside%20Before%20Changes.JPG)

Control Board:
[Control Board](Control Board)(https://raw.githubusercontent.com.com/johngrabner/tvm802B_2_smoothie_and_OpenPnP/master/Images/Labels%20on%20Images/Slide2%20-%20TVM802B%20Controller.JPG)


Dirver Board:
[Dirver Board](https://raw.githubusercontent.com.com/johngrabner/tvm802B_2_smoothie_and_OpenPnP/master/Images/Labels%20on%20Images/Slide3%20-%20TVM802B%20Driver.JPG)





## Stepper Mapping to Smoothie

| Steppers	          | Voltage	| Current	|Smoothie #-Pin  |  Example G-Code |
| ---                     | ---         | -------       | ----           | ---              |
| X Stepper	          |24V		|               | 1-M1		 | G0 X100	
| Left Stop	          |5V		|               | 1		 | M119	
| Right Stop	          |5V		|               | 1		 | M119	
| Y Stepper	          |24V		|               | 1-M2		 | G0 Y100	
| Back Stop	          |5V		|               | 1		 | M119	
| Front Stop	          |5V		|               | 1		 | M119	
| Z Stepper	          |24V		|               | 1-M3		 | G0 Z1	M17Z/M18Z to zero	
| Rotate 1	          |24V		|               | 2-M1		 | G0X2	
| Rotate 2	          |24V		|               | 2-M2		 | G0Y3	
| Strip 1 Back	          |24V		|               | 2-M4		 | G0Z3	
| Strip 2 Left	          |24V		|               | 2-M3		 | G0A3	

## Motor Mapping to Smoothie MOSFET

| Motor         | Voltage    | Current	|Smoothie #-Pin  |  Example G-Code |
| ---           | ---        | -------  | ----           | ---              |
| Pump 1        | 12V	     | 350mA     | 1-2.6	 | M48	M49
| Pump 2        | 12V	     | 350mA	 | 1-2.4	 | M42	M43

## Solenoid Mapping to Smoothie MOSFET 

| Solenoids	          | Voltage    | Current	|Smoothie #-Pin  |  Example G-Code |
| ---                     | ---        | -------        | ----           | ---              |
| Vacuum Solenoid #1	  | 24V	       | 82mA	        | 1-2.7	     | M44	M45
| Vacuum Solenoid #2	  | 24V	       | 82mA	        | 1-2.5	     | M46	M47
| Pin Solenoid	          | 24V	       | 312mA          | 2-2.6	     | M50	M51
| Blow Solenoid #1	  | 24V	       | 82mA	        | 2-2.7	     | M52	M53
| Blow Solenoid #2	  | 24V	       | 82mA	        | 2-2.5	     | M54	M55

## Miscellaneous Mapping to Smoothie MOSFET

| Lights	   | Voltage    | Current	|Smoothie #-Pin  |  Example G-Code |
| ---              | ---        | -------       | ----           | ---             |
| Up Cam Light	   | 12V	| 70mA	        | 2-2.4          | 	M56	M57


## Digital Sensor Mapping to Smothie IO

| Sensors	  | Voltage    | Current	|Smoothie #-Pin  |  Example G-Code |
| ---             | ---        | -------        | ----           | ---             |					
| Pin Sensor	  |3.3V	       |	        | 1-3.25         |	@switch pinread	
| Vac 1 Sensor	  |3.3V	       |	        | 1-3.26	 |	@switch vac1read
| Vac 2 Sensor	  |3.3V	       |	        | 1-2.11	 |     @switch vac2read

	
## Front Panel Buttons	

| Button                  | Voltage    | Current	|Smoothie #-Pin  |  Example G-Code |
| ---                     | ---        | -------        | ----           | ---             |					
| Start/Stop Button	  |   tbd      |   tbd          |   tbd          |   tbd           |				
| Pause Button	          |   tbd      |   tbd          |   tbd          |   tbd           |
| Step Button	          |   tbd      |   tbd          |   tbd          |   tbd           |					
| Y+ Button	          |   tbd      |   tbd          |   tbd          |   tbd           |
| Y- Button	          |   tbd      |   tbd          |   tbd          |   tbd           |
| X+ Button	          |   tbd      |   tbd          |   tbd          |   tbd           |
| X- Button	          |   tbd      |   tbd          |   tbd          |   tbd           |
