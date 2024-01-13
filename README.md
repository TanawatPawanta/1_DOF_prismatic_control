> Written with [StackEdit](https://stackedit.io/).
> # 1 DOF prismatic robot arm
> This is complete of control part of 1 DOF prismatic robot arm, in this repostory will contain code  about the trajectory, controller, and state estimator. Each part will be split into a header file and source file.This code was implemented on STM32 f411re by C langue and and require DSP(Digital Signal Processing) for matrix calculation.
> ## Table of contents
 - [**Control System Architecture**](#Control-System-Architecture)
 - [**Trajectory**](#Trajectory)
 - [**Controller**](#Controller)
 - [**State Estimator**](#State-Estimator)
> ## Control System Architecture
> ## Trajectory
> In this project I had developed 2 types of trajectory 
> 
 1. Quintic Polynomial trajectory
   ![image](https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/b501ef99-1cc7-48c1-9f6e-91ac8eaa5505)

 2. Trapizoid velocity profile trajectory

> ## Controller
> ## State Estimator