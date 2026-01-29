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

### Actuator - a device that converts energy into motion (like the muscle of a robot)
 - receives a signal (electrical, hydraulic, pneumatic) and produces motion (linear, rotary, or oscillating)

Maximum payload - operates at a reduced speed, but with a maximum supply of "stuff'

kinematics - describes the motion mechanics of a robot

working area - the base, shoulder, and elbow axis (the three main axes)
the minor axis - encompasses the wrist axes and controls the "the orientation of the end effector"

transitory axes (linear axes) - move up and down, and laterally side to side 

back and forth (x-axis)
left and right (y-axis)
up and down (z-axis)

rotation around the x-axis - rolling movement 
rotation around the y axis - pitching motion
rotation around the z axis - yaw movement

DOF (Degree of freedom) - connotates the degree of movement 
  - a door hinge has 1 degree of freedom
  - a human elbow has 2 degrees of freedom (bending, and also a slight twist)

  - serial kinematics - if at least 3 arm lengths are connected together by axes, it is called a kinematic chain  
  - parallel kinematics - a mechanical system where the end effector is supported and moved by multiple independent kinematic chains working together, instead of a single chain of joints in a serial robot arm

  - world coordinate system - a cartesian coordinate system with an xyz axis
     - unchangeable in space
     - origin: usually it's at the rotation center at the 1st robot axis (at the base)
     - reference for tool coordinate system
  - tool coordinate system - cartesian coordinate system with an xyz axis
     - changeable in space, as it moves together with the tool
     - source: tool center point (TCP)

Linear and gantry robots use:
  TTT kinematics - Tilt-Tilt-Translate kinematics
   - a robot where the end effector is controlled by two tilting (rotational) joints followed by a translational (linear) joint)
   - good for simple orientation and positioning for tasks like pick-and-place (loading pallets, assembly of workpiece)
   - work in cuboid or cubic areas

Swivel arm robot
   - RTT kinematics - Rotation-tilt-tilt
   - the base rotates
   - working area is cylindrical

Scara robot
   - RRT Kinematics - revolute-revolute-translational
   - two rotation joints and one linear joint
   - kidney-shaped workspace
   - good for assembly, drilling, milling, testing

Vertical articulated arm robot
   - RRR kinematics
   - working area - hollow sphere
   - advantage: minimum acceleration forces and space-saving
   - downside: greater intertial forces
   - used in welding/painting/assembly/deburring

   - Delta robots
     - use parallel kinematics
     - advantages: can move very fast, mechanical stiffness --repeatability, low moving mass (small inertia)
     - disadvantage: low load capacity, small workspace, coordinating transformation is complex (complex control)
      - used for packaging, food handling, electronics assembly
      - fast pick and play tasks
