"# Object Sorting" 

Object sorting:
scene setup:
1 plunger and 2 conveyor
3 signals: BackwardFininsh(BF), CanDetected(CD) and ForwardFinish(FF)

Aim: To push the boxes from one conveyor onto another

PRocedure: 
The signals are placed 3 positions. One at the back of the plunger. Second, at the plunger face and on top of conveyor one. Third on the conveyor 2. The signals turn red when actvated and remain yellow when not activated

At the start state. the box is placed on the 1st conveyor and also the BW signal is activated. This trigegrs 1st conveyor to move
![alt text](image-1.png)
The box on the conveyor also moves alongwith the conveyor. When the box reaches the point infront of the Plungerface, signal CD is triggerd. This sends the signal to the plunger to move forward and stops the conveyor movement. The forward movement of the plunger pushes the box onto the 2nd conveyor.
![alt text](image-2.png)
The signal FF detects the Box on the 2nd conveyor and sends the singal to the plunger to move backward and activated the 2nd conveyor movement.
![alt text](image-3.png)
The plunger moves backward and triggers the BF signal activate the movement of the conveyor 1
![alt text](image-4.png)

Refer the link to see the simlution of the above scene: https://www.youtube.com/watch?v=JlNDoXkk2YA

