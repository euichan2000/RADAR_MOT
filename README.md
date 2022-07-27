# RADAR_MOT
## summary
We can get position$$(P_{x}, P_{y},P_{z})$$ of objects using __Radar clustering code__.  
   
   And If we input this Position to MOT package, we can plot objects' __position__ and calculate objects' __velocity__.
  
## contents
1. RADAR_TRACKING CODE
2. MOT PACKAGE
## 1. RADAR_TRACKING CODE
_RadarTrackingVer3.py_   
In this code, we get plenty of data of points. after clustering those points, We publish rostopic as     
```
(Point_id,Px,Py,Pz,time)
```
Type of rostopic
