# Tugas-Besar---Pemodelan-Simulasi

**1. Problem Description**
   
   The government has a plan to build a highway congestion detection system that can provide information about the location of congestion points based on the density of vehicles in unit locations. For this purpose, our research team is tasked with creating a simulation system that can describe the flow of vehicles on the highway. This simulation is based on the Nagel-Schreckenberg Model, with predetermined assumptions. The main objective of this simulation is to determine the density of vehicles per unit time at certain intervals, see the results after the system runs for a certain period of time, and analyze the average time of the vehicle returning to the initial position.

**2. Description of Simulation Program Methods and Algorithms
   
  ** A. Road Section Location Selection****

   -  Use the osmnx library to select unique road section locations.
   -  Apply periodic boundary condition to keep the number of cars constant.
   -  Discretize/partition the vehicle path map into M subintervals.

  **B.  System Simplification with Discrete Models**
    -  Using a discrete model of position x and time t.
    -  Simplify the behavior of the rider according to predefined rules.
      a.  Simplification Rule-1: Adding 1 unit of speed for each car per time unit           with a maximum speed limit (vmax).
      b.  Simplification Rule-2: Ensure that the speed of each car does not exceed
          the safe distance (d - 1) between two cars together.
      c.  Simplified Rule-3: Provides p opportunities for the driver to
          to brake, which results in the car slowing down by 1
          speed unit.
      -  Update the speed and position of the vehicle according to the equation
        that has been determined.

    **C.  Simulation System**
    
    -  Using fixed parameters: M = 100, p = 0.3, v0 = 0, d = 2, N = 20, tmax =             1000, vmax = 5.
    -  Running the simulation with iteration time t until it reaches tmax.
    -  Monitoring and collecting necessary data during the simulation run.

      **D.  Result and Discussion**

        **A.  Simulation Results**
            -  After the system has been running for tmax, we can see how the flow                 of vehicles move on the highway and how the vehicle density                        changes over time.
            -  Calculate the density per unit time of vehicles in the interval                     [x80, x90], where x80 and x90 are the specified interval                           boundaries.
            -  Calculate the maximum density per unit time of vehicles in each
               interval with a length of 5 position units.
            -  Calculate the average time for cars to return to the starting                      position.

          **B. Discussion**
          
            -  Based on the simulation results, it is possible to observe changes                 in vehicle flow and density on the highway during the simulation                   period. This can assist in the understanding of traffic congestion                 and how factors such as speed, distance, and driver behavior affect                traffic flow.
            -  The density per unit time of vehicles in the interval [x80, x90]                   provides information about the density of vehicles on a particular                 section of the observed highway. This can help in identifying                      possible congestion points.
            -  The maximum density per unit time of vehicles in each interval with                a length of 5 position units helps in determining which intervals                  has the highest vehicle density. This can provide insight into how                 vehicle density is distributed on the highway.
            -  The average time for cars to return to the starting position gives                 an idea of the effectiveness of the traffic system in moving                       vehicles through the roadway. The faster the car returns to the                    starting position, the better the traffic flow.

     
