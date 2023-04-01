# Kinematics/Dynamics related questions

## Robotics System
for the case when candidate only operates the commercial robot

* Controling rate
* Control loop that user can access
  * If the torque loop is available but not directly used, why not use it?
  * Or, what will they expect (pros and cons) if the motion-based controller is replaced with a torque-based controller?
* Any glitches they found when operating the robot?
  * What is the possible cause?
  * Is there any method that they can improve it without modifying the hardware/software archetecture? 
* Any observer is used for enhacing sensor feedback?
* What kind of calibration is done before running the experiment?
* What kind of benchmark methods has been used to understand system’s peroformance?


## Kinematics
###  Transformations

* Transformations 
* assuming there is a vector p point from frame a to frame b, what will be the homogenuous transformation matrix Tab?

###  Jacobian

* What is the Jacobian matrix?

* if the Jacobian matrix is a fat, thin, or squared matrix, what does that implies for a robotic system?

* Derive one term in the Jacobian?

* or , describe how can we derive the Jacobian matrix? 

* How to find the joint torque, to achieve end-effector force?

* Derive tau = J^T f

* Is tau the only solution? What is the meaning of this solution?

* From tau, how can i estimate f?

* How to find the joint velocity, to achieve end-effector velocity?

* Is this the only solution? what is the meaning of this solution?

###  Singularity

* Physically, what is a singularity?

* Mathematically, what is a singularity?

* What is manipulability?

* What are the issues when trying to achieve an end-effector acceleration near singularity? 

###  Kinematics

* Describe what forward kinematics and inverse kinematics do,

* Inverse kinematics
  * the inverse kinematics solution from  puesdo inverse is also an optimal solution from an optimization problem, what is the optimization objective?
  * how to avoid singularity when solving inverse kinematics?

##  Dynamics
* impact equation,
* EOM with contact,
* grasping matrix stuff
* external torque estimation (for force control or HRI
* external wrench estimation (for force control or HRI
* For simpler dynamics (e.g. 2nd order model
  * Derive EOM for mass/spring/damper equation
  * Damping ratio and Natural frequency
  * Ways to increase natural frequency/BW (eitehr through control input or hardware adjustment

###  Frictions
* how does friction affects manipulator control?
* motion control
* motion control with contact
* motion force control
* what strategy is considered if any?
  * what is its pros and cons
* how to identify the friction model if it is used?

##  Kinematics Calibration
* what is the used device? pros and cons?

* what is the assumption made for the calibration based on the kinematic relation?
  * (e.g. assuming the input and output side is co-axis, also if mdh is used, assuming the DH parameters are described along perfectly vertical axis)
* what is the acheived kinematic accuracy?
* how the redundency will affect the kinematics calibration result?

## Dynamic Calibration
* what is the method that you use
* what is its limitations
  * will the identified dynamics has positive-definite inertia matrix?
  * what would be the constraints that can help to ensure the inertia matrix will be PD?
  * any attemp or resolution for the limitations
* how do you verify the results?
