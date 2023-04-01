# Classical Control Theory Interview Questions

## System
System related questions on robots used in Candidate’s past projects
* Control loop, controling rate,
* How do they benchmark system
  * system ID?
  * calibration?
    * sensor
    * actuator
  * control bandwidth
  * analysis tool
    * time domain?
    * frequency domain?
  * disturbance?
    * friction?
    * sensor noise
    * experience on observer design
  * mechanical resonance, ripple…etc,
  * signal processing
    * LPF
    * notch filter…etc,
    * cutoff freq,
    * filter order,
  * Development experience
    * level of participation

## Control
### linear control
* PID
  * purpose of P/I/D controller
  * e.g. in terms of step response
  * tuning order
  * physical consideration on control gain limitation
* linear system
  * e.g. in terms of 2nd oder system
  * stability
    * BIBO
    * pole
    * Bode plot
      * gain 
      * phase plot
    * damping ratio and its effect on system characteristics
      * over damped
      * under damped
      * critical damped
    * other controller design
      * LQR
        * system requirement
        * controllability
      * Kalman filter
      * Adaptive control
        * convergence guarantee
      * Robust control
        * H2…
      * MPC
      * how do appplicant relate linear control methods to their system
        * (since most of the systems are nonlinear
        * 
### nonlinear control 
* stability
  * Lyapunov
* feedback linearization
  * computed torque control
  * inverse dynamics + PD control
* other controller design
  * QP-based controller
  * nonlinear MPC..
