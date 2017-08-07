The TVM802B has 2 vacuum pumps, 2 vacuum solenoids, and 2 vacuum sensors.
This makes 2*2*2*2=16 configurations to test, but times 2 since nozzle may be blocked or not.

# Is Pump 1 labeled correctly

Turn on both solenoid (Smoothie #1 - M44 M46)

turn on Pump 1 (Smoothie #1 - M48)

See if vacuum is present on heads 1

turn off Smoothie #1 - M45 M47 M49


Pass

# Is pump 2 labeled correctly

Turn on both solenoid (Smoothie #1 - M44 M46)

turn on Pump 1 (Smoothie #1 - M42)

See if vacuum is present on heads 1

turn off Smoothie #1 - M45 M47 M43

pass

# Is solenoid 1 label correctly

Turn on pump 1 (Smoothie #1 - M48)

Turn on Solenoid 1 (Smoothie #1 - M44)

Verify vacuum on nozzle 1

Turn off Smoothie #1 - M49 M45

Pass

# Is solenoid 2 labeled correctly

Turn on Pump 2 (Smoothie #1 - M42)

Turn on Solenoid 2 (Smoothie #1 - M46)

Verify vacuum on nozzle 2

Turn everything off Smoothie #1 - M43 M47

pass

# Is vacuum sensor 1 labeled correctly

Turn on Pump 1 Smoothie #1 - M48

Turn on Solenoid 1 Smoothie #1 - M44

red sensor 1 @switch vac1read and validate 1 = off

Block nozzle validate @switch vac1read is 0=vacuum present

Turn everything off Smoothie #1 - M49 M45

pass

#Is Vacuum Sensor 2 Labeled correctly

Turn on Pump 2 Smoothie #1 - M42

Turn on Solenoid 2 Smoothie #1 - M46

Read vacuum sensor 2, 1 = no vacuum 

block nozzle

Read vacuum sensor 2, 0= vacuum present

Turn everything off Smoothie #1 - M43 M47

pass


# Nozzle blocked tests

| test | Pump 1    | Pump 2    | Solenoid 1 | Solenoid 2 | Sensor 1                 | Sensor 2                 | Result |
| ---  | ---       | ---       | ---        | ---        | ---                      | ---                      | ---    |
|      | input     | input     | Input      | input      | Expected Result          | Expected Result          |        |
|   1  | off - M49 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |   pass     |
|   2  | on  - M48 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |   pass     |
|   3  | off - M49 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |   pass     |
|   4  | on  - M48 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |   pass     |
|   5  | off - M49 | off - M43 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |   pass     |
|   6  | on  - M48 | off - M43 |  on -  M44 | off - M47  | on  = 0 @switch vac1read | off = 1 @switch vac2read |   pass     |
|   7  | off - M49 | on  - M42 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |   pass     |
|   8  | on  - M48 | on  - M42 |  on -  M44 | off - M47  | on  = 0 @switch vac1read | off = 1 @switch vac2read |   pass    |
|   9  | off - M49 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  10  | on  - M48 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  11  | off - M49 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | on = 0  @switch vac2read |        |
|  12  | on  - M48 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | on = 0  @switch vac2read |        |
|  13  | off - M49 | off - M43 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  14  | on  - M48 | off - M43 |  on -  M44 | on  - M46  | on  = 0 @switch vac1read | off = 1 @switch vac2read |        |
|  15  | off - M49 | on  - M42 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | on = 0  @switch vac2read |        |
|  16  | on  - M48 | on  - M42 |  on -  M44 | on  - M46  | on  = 0 @switch vac1read | on = 0  @switch vac2read |  pass
     |

# Nozzle NOT blocked tests

| test | Pump 1    | Pump 2    | Solenoid 1 | Solenoid 2 | Sensor 1                 | Sensor 2                 | Result |
| ---  | ---       | ---       | ---        | ---        | ---                      | ---                      | ---    |
|      | input     | input     | Input      | input      | Expected Result          | Expected Result          |        |
|   1  | off - M49 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   2  | on  - M48 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   3  | off - M49 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   4  | on  - M48 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   5  | off - M49 | off - M43 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   6  | on  - M48 | off - M43 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   7  | off - M49 | on  - M42 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   8  | on  - M48 | on  - M42 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   9  | off - M49 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  10  | on  - M48 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  11  | off - M49 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  12  | on  - M48 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  13  | off - M49 | off - M43 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  14  | on  - M48 | off - M43 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  15  | off - M49 | on  - M42 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  16  | on  - M48 | on  - M42 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |   pass     |
