The TVM802B has 2 vacuum pumps, 2 vacuum solenoid, and 2 vacuum sensor.
This makes 2*2*2*2=16 configurations to test times 2 since nozzle may be blocked or not.

# Nozzle blocked tests

| test | Pump 1    | Pump 2    | Solenoid 1 | Solenoid 2 | Sensor 1                 | Sensor 2                 | Result |
| ---  | ---       | ---       | ---        | ---        | ---                      | ---                      | ---    |
|   1  | input     | input     | Input      | input      | Expected Result          | Expected Result          |        |
|   2  | off - M49 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   3  | on  - M48 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   4  | off - M49 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   5  | on  - M48 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   6  | off - M49 | off - M43 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   7  | on  - M48 | off - M43 |  on -  M44 | off - M47  | on  = 0 @switch vac1read | off = 1 @switch vac2read |        |
|   8  | off - M49 | on  - M42 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   9  | on  - M48 | on  - M42 |  on -  M44 | off - M47  | on  = 0 @switch vac1read | off = 1 @switch vac2read |        |
|  10  | off - M49 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  11  | on  - M48 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  12  | off - M49 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | on = 0  @switch vac2read |        |
|  13  | on  - M48 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | on = 0  @switch vac2read |        |
|  14  | off - M49 | off - M43 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  15  | on  - M48 | off - M43 |  on -  M44 | on  - M46  | on  = 0 @switch vac1read | off = 1 @switch vac2read |        |
|  16  | off - M49 | on  - M42 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | on = 0  @switch vac2read |        |
|  17  | on  - M48 | on  - M42 |  on -  M44 | on  - M46  | on  = 0 @switch vac1read | on = 0  @switch vac2read |        |

# Nozzle NOT blocked tests

| test | Pump 1    | Pump 2    | Solenoid 1 | Solenoid 2 | Sensor 1                 | Sensor 2                 | Result |
| ---  | ---       | ---       | ---        | ---        | ---                      | ---                      | ---    |
|   1  | input     | input     | Input      | input      | Expected Result          | Expected Result          |        |
|   2  | off - M49 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   3  | on  - M48 | off - M43 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   4  | off - M49 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   5  | on  - M48 | on  - M42 |  off - M45 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   6  | off - M49 | off - M43 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   7  | on  - M48 | off - M43 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   8  | off - M49 | on  - M42 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|   9  | on  - M48 | on  - M42 |  on -  M44 | off - M47  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  10  | off - M49 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  11  | on  - M48 | off - M43 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  12  | off - M49 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  13  | on  - M48 | on  - M42 |  off - M45 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  14  | off - M49 | off - M43 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  15  | on  - M48 | off - M43 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  16  | off - M49 | on  - M42 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |
|  17  | on  - M48 | on  - M42 |  on -  M44 | on  - M46  | off = 1 @switch vac1read | off = 1 @switch vac2read |        |