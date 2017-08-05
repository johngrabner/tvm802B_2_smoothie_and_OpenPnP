# Smoothie version

Version of SW that came on smoothie 
```
Build version: edge-8e4a64c, Build date: Apr 24 2017 11:46:31, MCU: LPC1769, System Clock: 120MHz 5 axis
```
did not give correct response to switch commad line
```
>>>@switch vac1read
SENDING:switch vac1read
switch vac1read set to:
```

The version that works is 
```
>>>@version
SENDING:version
Build version: upstreamedge-b6153da, Build date: Jun 21 2017 21:02:36, MCU: LPC1769, System Clock: 120MHz
5 axis
```
 produces the output
```
>>>@switch vac2read
SENDING:switch vac2read
switch vac2read is 0
```

##Validate smoothie 1 - Done
##Validate smoothie 2 - Done
