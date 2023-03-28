# Example2

## Intro:
In this 1 hour, we go through the theory and implementation for controlling a robot arm. We will start with dynamics, then control, and then software. 

For equations, just type them in chat. You can write the derivative of x as dx. For example: f = m ddx

* Dynamics:
  * Write the rigid body dynamics.
  * M ddq + c + g = tau
  * What is the size of the generalized coordinates?
  * Which terms are nonlinear? Which terms can be approximated as linear? Why is this approximation ok? 
    * M, C, g are all nonlinear. M can be approximated as linear.
  * We have series elastic actuators (SEA). What are the new dynamics?
    * M ddq + c + g = k (q - theta)
    * diag(B) ddtheta = k (theta - q) + u
    * What is the size of the generalized coordinates?
  * What is the advantage of a series elastic actuator?
    * main advantage: torque sensing, which is needed for closed-loop torque control, which is needed for friction rejection. 
  * How would you choose a motor mass and spring stiffness?
    * big motor, high stiffness, low gear ratio for high bandwidth
  * What are the rigid body dynamics as the stiffness approaches infinity?
    * (M + diag(B)) ddq + c + g = u
  * For industrial robots with no torque sensor, what is the stiffness?
    * 10,000 Nm/rad for harmonic drive
  * Stiffness → infinity allowed us to approximate the elastic equations using the rigid body equations. What other condition(s) would allow us to approximate elastic equations using rigid body equations?
    * B << M, will result in original rigid body equation. 
    * B >> M, will result in B ddq + c + g = k (q-theta), when doing position control.
  * For cobots, can we assume that stiffness is infinite, or B << M, or B >> M ?
    * No. natural frequency = sqrt(K/B) ~= sqrt(K/M) ~= 20 Hz is within our controller bandwidth.  B and M are similar magnitude. 
  * Mechanically, how would we reduce B while maintaining the torque capacity?
    * bigger motor, lower gear ratio
  * Can we reduce B through control? How?
    * closed-loop torque control

* Controls
  * What are the end-effector dynamics for the rigid body dynamics (stiffness → infinity)?
    * operational space
  * Design an impedance controller for position
  * Design an impedance controller for orientation
  * How to determine if a robot is singular?
    * condition number calculated from eigen or SVD decomposition

* Software
  * What math library would you use?

  * Write a class implementation

  * Real-time analysis

  * Write a ROS message for this

  * What are the advantage and disadvantage of using ROS interface?
