# Operational-space Interview Questions
## Control

* how to deal with nonlinear terms?
* Calculate end-effector orientation error?
* what kind of force control?
  * direct vs indirect (impedance)
* what kind of motion control?
  * impedance vs admittance
* Calculate joint torque, to achieve an cartesian-space impedance?
* What happens near singularity?
* How can we deal with this?

## Operational-space

* J^T f is one solution. For redundant robot, what is the general solution?
* Equation for the Null-space matrix?
* Is this unique?
* Do all solutions guarantee that the null-space torque produces no force in the first task’s coordinates?
* Do all solutions guarantee that the null-space torque produces no acceleration in the first task’s coordinates?
* What is the solution that guarantees no acceleration?

## Optimization

* J^T f is an analytical solution
* Why would we want to solve it as an optimization problem instead?
* Write this as an optimization problem?
* Add in constraints?
* Add a null-space task?
* Strict vs soft prioritization?
