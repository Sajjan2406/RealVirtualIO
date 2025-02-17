﻿# Production_Line
## Scene setup:  
- **Components**:
  - 2 Conveyors
  - 1 Divertor
  - 1 Gantry Crane
  - 1 Linear Axis Floor
  - 1 Box
- **Sensors**:
  - This setup includes 7 sensors, each associated with a signal as an interface connection.
![alt text](images/image_001_0000.jpg)
## Aim: 
To replicate the production line set up in the Automation Lab

## Procedure:
The Digital replica of the prodution line is setup to mimic its functionalities.Each conveyor is equipped with 2 sensors at each end and a sensor is placed at the end of the linear axis floor

1. **Initial State**:
   - The box is placed on `conveyor1 (C1)` such that it activates `Sensor1`. This sensor triggers the signal `StartC1`, starting the forward movement of the first conveyor. The box moves forward and activates `Sensor2`.
   - `Sensor2` triggers the signal `StartD`, which starts the forward movement of the divertor belts.
![alt text](images/image_014_0000.jpg)
2. **Box Reaches Divertor**:
   - The box moves forward onto the Divertor. When the box activates `Sensor3`, it triggers `StopC1` to stop `C1` movement and starts the forward movement of `conveyor2`.

![alt text](images/image_011_0000.jpg)
3. **Box on Conveyor 2**:
   - The box moves onto `conveyor2 (C2)` and activates `Sensor4`. This makes the `Gantry Crane (GC)` move forward by activating the `StartCrane` signal. 
![alt text](images/image_004_0000.jpg)
4. **Gantry Crane Action**:
   - The `GC` moves forward towards `C2` and activates `Sensor6`. This sensor then triggers the downward motion of the Schunk through the `CraneDown` signal.
![alt text](images/image_005_0000.jpg)
5. **Schunk Action**:
   - After the downward movement is finished, the `CraneFinish` signal is triggered through `SchunkSensor`, making the Schunk go upwards.
![alt text](images/image_006_0000.jpg)
6. **Crane Upward Finish**:
   - The end of the upward motion triggers the `Craneupfinish` signal and starts `C2` in the reverse direction.
![alt text](images/image_007_0000.jpg)
7. **Box Movement and Crane Return**:
   - The movement of ```markdown
   the box deactivates `Sensor4`, triggering the `StartCrane` signal again to move the `GC` back to its home position.
![alt text](images/image_018_0000.jpg)
8. **Divertor Reverse**:
   - Simultaneously, the box activates `Sensor5`, which sends the `Rstart_D` signal to move the divertor belts in the reverse direction.
![alt text](images/image_016_0000.jpg)
9. **Final Box Position**:
   - Once the box reaches the Divertor, the `Rstart_C1` signal triggers the movement of `C1` through `Sensor7`
![alt text](images/image_017_0000.jpg)

## Simulation
Refer the link to see the simlution of the above scene: https://youtu.be/TGOjrZvSMzE?si=n0Z9oi8SRrPyFc6k
