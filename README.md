# RADAR_MOT
## summary
We can get position$$(P_{x}, P_{y},P_{z})$$ of objects using __Radar clustering code__.  
   
   And If we input this Position to MOT package, we can plot objects' __position__ and calculate objects' __velocity__.
  
## contents
1. RADAR_TRACKING CODE
2. MOT PACKAGE
## 1. RADAR_TRACKING CODE
_RadarTrackingVer3.py_   
In this code, we subscribe & get plenty of data of points. after clustering those points, We publish rostopic as     
```

(Point_id,Px,Py,Pz,time)
```
__Type of published rostopic__   
Segment_centers
```
Header header
int16[] id
int16[] pixel_x
int16[] pixel_y
float64[] x
float64[] y
float64[] z
float64[] secs
```
We only use id, x,y,z,secs
## 2. MOT PACKAGE CODE
_object_track_ROS.py_     
In this code, we subscribe __(Point_id,Px,Py,Pz,time)__ and publish __(Point_id,Px,Py,Pz,Vx,Vy,Vz)__.    Alse we can see bird-eye-view plot of objects.   

__Type of published rostopic__
obj_tracking   
```
Header header
int16 object_id
float64 x
float64 y
float64 z 
float64 vx
float64 vy
float64 vz
```
