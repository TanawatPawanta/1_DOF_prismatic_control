
> # 1 DOF prismatic robot arm
> This is complete of control part of 1 DOF prismatic robot arm, in this repostory will contain code  about the trajectory, controller, and state estimator. Each part will be split into a header file and source file.This code was implemented on STM32 f411re by C language and and require DSP(Digital Signal Processing) for matrix calculation.
> ## Table of contents
 - [**System Architecture**](#System-Architecture)
 - [**Trajectory**](#Trajectory)
 - [**Trajectory Tracker**](#Trajectory-Tracker)
 - [**State Estimator**](#State-Estimator)
 - [**Hardware**](#Hardware)
> ## System Architecture
>
> <img width="978" alt="image" src="https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/56750dac-22e1-4bfb-b804-850b0ac4647f">
> 
> ## Trajectory
> In this project I had developed 2 types of trajectory 
> 
 1. Quintic Polynomial trajectory(current use in project)
    ![image](https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/b501ef99-1cc7-48c1-9f6e-91ac8eaa5505)

 2. Trapizoid velocity profile trajectory
    ![image](https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/7ab99fa7-cd0c-4cc5-8204-e1d720ba64b8)

> ## Trajectory Tracker
  In this project I use cascade control for control velocity and position
  ![image](https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/fbb96503-c6bc-42bc-8ed9-13df1e0a099d)

> ## State Estimator
  Use Kalman Filter for estimate a velocity
>
  ![image](https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/7641d945-e50f-4440-a596-71ba243ed197)
>
  reference:https://www.kalmanfilter.net/multiSummary.html
 - Process model
>
> <img width="561" alt="image" src="https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/bd3e285f-d64b-450d-89dc-8b8b2ae52fa5">
>
 - Measurement model(measure from encoder)
>
> <img width="254" alt="image" src="https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/e6d47762-5d16-4b2b-8e59-41d197582a42">
>
>
 - resault from Kalman Filter
>
  ![image](https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/ef971293-67da-498f-becb-999ebc60311b)
>
> velocity from trajectory : orange graph
>
> velocity calculate from encoder : blue graph
>
> Estimate velocity : green graph
>
> ## Hardware
>
><img width="508" alt="image" src="https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/6bd922af-48d5-4c56-a118-e82fbd673290">
>
><img width="455" alt="image" src="https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/0d953b60-ccb4-47a3-a9f5-327f7c540013">
>
><img width="237" alt="image" src="https://github.com/TanawatPawanta/1_DOF_prismatic_control/assets/83177015/4987802e-ac71-4c0e-ac6e-6fba5470c79c">





