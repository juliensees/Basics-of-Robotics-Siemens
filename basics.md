- Classification of handling facilities
  * Controlled manually
      - person controlled manipulators for moving very heavy or very small objects (micromanipulators), or dangerous environments (teleoperators)
  * Program controlled
      - Inserting devices
        - fixed programmed: mechanically adjustable and travel limit
            - used for point-to-point movements, and feeding components
            - movement limitation via stops, sensors or limit switches
      - Freely programmable
          - high mobility with at least three axes
          - used for welding, gluing, grinding, painting, etc.
          - partly sensor-guided
        - computer-controlled: by CNC or PLC

### PLC - A Programmable Logic Controller (PLC) is an electronic module that is used in automation technology for control and regulation tasks. In principle, it is a control device with specialized input and output interfaces for sensors and actuators. A PLC can thus control, monitor and influence production processes.

### PLM - Product Lifecycle management - a process of product management from design to discontinuation to maximize the business benefits fror the company and its business partners. Everything from idea generation, design, engineering, manufacturing process management, product portfolio management, and supply chain functions for product realization

### TIA Portal - Totally Integrated Automation Portal - provides complete access to the tnire digitzed automation from digital planning and integrated engineering to transparent operation. It serves as a common engineering tool for robots and machines. 

ROS - Robot Operating System is an open source system that then companies build software on top of that is often closed source

### The robot is made up of the socket (base), the joints, the end effector, and the arm 

  * End effector - the last piece on the robot arm that corresponds to its selected task
  * Robot Arm
      - drives: energy converters located in the base or axis, that are motors that set the arm in motion and can be electric or hydraulic
      - joints and gears: ensure the accuracy and reliability (very precise)
      - measuring systems: measure and record all positions and speeds at each drive or joint
      - sensors: touch or optical sensors that allow the robot to interact with objects and provide safety (someone or something comes too close)
      - mechanical holding brakes that prevent movement dur to safety of a power failure
   
### the workspace - the possible movement range of a robot

Repeatability - a robot never actually repeats the same task in the actual exact position. it is usually off by microns, and so the repeatable accuracy is always a specific number that is determined with each robot to see how accurate it can be

Articulated arm robot - typically 6 axes, and have very little restrictions in movement and thus are very flexible
Delta/linear arm robot - 3, 4, or 6 axes, and is mainly used for 3D printing
SCARA (Selective Compliance Assembly Robot Arm) - 2 or 3 rotation and 1 translation axis, and are used often for screwing or sorting on assembly lines

Vertical articulated arm robot 
 - main axis: the larger arm that provices the positioning and pre-orientation fo the tool (including the base, covers 80-90% of working area
 - minor axis: the smaller arm that brings the Tool Center Point into the exact position and orientation
   - main work area: the area close to the arm for optimal accuracy
   - secondary work area: usually farther away from the center, where the robot must work slowly (less accuracy), and is not as accurate (changing tools)

### TCP (Tool Center Point) - a specific point on the robot's end-effector that the controller treats as THE point whose position and orienation it controls. Robot kinematics don't really care about the whole geometry, but specifically where the TCP lands (and if it's in the exact right spot).

Cell control - the "Brain" that makes all the pars work together (the robot, end effector, sensors, conveyors, PLC's & HMI's, and safety systems)
 - handles sequencing and logic (workflow)[usually runs on a PLC], communication (manages sigals between controller, PLC, etc), error handling, etc.

### HMI (Human Machine Interace) - USED TO OPERATE AND MONITOR THE PROCESS, AND CONNECTED TO THE CELL CONTROLLER (USED TO CONTROL THE ROBOT ARM)

- The robot controller (PLC) is like the factory foreman, telling the robot what to do... while the robot controller figures out how to do that smoothly and safely

Maximum payload - operates at a reduced speed, but with a maximum supply of "stuff'
