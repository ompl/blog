---
title: V-REP Now Supports OMPL
author: mmoll
---
I am very pleased to announce that [V-REP](http://coppeliarobotics.com) has recently added support for OMPL. OMPL is now the [recommended way](http://www.coppeliarobotics.com/helpFiles/en/pathAndMotionPlanningModules.htm) to perform motion planning in V-REP.

{% youtube JAs2yciPjvM %}

[The V-REP platform](http://coppeliarobotics.com) is a modular, generic and general purpose robot simulation framework that offers various tools related to robotics (4 physics engines, collision detection, minimum distance calculation, proximity sensor simulation, vision sensor simulation, full FK/IK kinematic solver, etc.), with various kinds of interfaces (ROS, remote API, plug-ins, add-ons) and language support: C/C++, Python, Java, Matlab, Octave, Lua. It is built on a distributed control architecture, allowing virtually any number of scripts running in parallel and controlling various aspects of a simulation. The OMPL interface for V-REP was implemented via a plug-in wrapping the OMPL functionality, and offering that functionality via scripting functions. This allows to quickly test various scenarios, without the need to recompile/load test code over and over again. In combination with V-REP's kinematic functionality, complex movement sequences can easily be computed: e.g. V-REP can also quickly compute several valid robot configurations for a desired end-effector pose.

This is the latest robotics software package to add support for OMPL. Other packages include ROS/MoveIt!, OpenRAVE, MORSE, Kautham, VEROSIM, and others. A more detailed description of the integration between these packages and OMPL is described [here](http://ompl.kavrakilab.org/integration.html).
