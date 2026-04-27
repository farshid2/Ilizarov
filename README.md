# 1 - Introduction
Data from modelling, simulation and analysis of Ilizarov external circular (ring) external fixators.
# 2 - Finite Element Simultion
Radial compressions of Ilizarov full rings (with different holes diameters, ring diameters and number of holes) under a 1000 [N] load were simulated using ABAQUS software with both solid (hexahedral) and shell (quadrilateral) elements. Ring diameters of 80, 100, 110, 120, 130, 140, 150, 160, 180, 200, 220, 240 [mm] were used, with number of holes for each ring diameter varying from 0 to the maximum whiich was permitted by the geometry.
## 2.1 Results
Results were oraganised into .json files:
### 2.1.1 Modelling with shell elements
The file [RingRadCompShellAbq.json](RingRadCompShellAbq.json) has the results for rings with different hole diameters (3, 5, 7, 9 [mm]), ring diameters (80, 100, 110, 120, 130, 140, 150, 160, 180, 200, 220, 240 [mm]) and number of holes (0, 2, 4, 6, 8, ....). For example, if the data is read into a Python dictionary or a JavaScript object named RESULTS, the values of RESULTS["3"]["150"]["36"]["U1"] is the maximum radial deformation (in [m]) of a ring with 3 mm holes, (inner) diameter of 150 mm and 36 holes, while RESULTS["3"]["150"]["36"]["U2"], gives the maximum lateral deformation (in [m]) and RESULTS["3"]["150"]["36"]["SP"] is the maximum (von Mises) stress in Pascals [Pa].
### 2.1.2 Modelling with solid elements
The file [RingRadCompSolidAbq.json](RingRadCompSolidAbq.json) has results from finite element simulation of radial compression of Ilizarov full rings with hole diameter of 7 [mm] and varying ring diameters and number of holes, with solid hexahedral elements.

