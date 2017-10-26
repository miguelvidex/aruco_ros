aruco_ros
=========

Software package and ROS wrappers of the [Aruco][1] Augmented Reality marker detector library.


### Features
<img align="right" src="https://raw.github.com/pal-robotics/aruco_ros/master/aruco_ros/etc/marker_in_hand.jpg" />
 * High-framerate tracking of AR markers
 * Generate AR markers with given size and optimized for minimal perceptive ambiguity (when there are more markers to track)
 * Enhanced precision tracking by using boards of markers
 * ROS wrappers


### Applications

 * Object pose estimation
 * Visual servoing: track object and hand at the same time

<img align="right" src="https://raw.github.com/pal-robotics/aruco_ros/master/aruco_ros/etc/reem_gazebo_floating_marker_world.png"/>

### ROS API

#### Messages

 * aruco_ros/Marker.msg

        Header header
        uint32 id
        geometry_msgs/PoseWithCovariance pose
        float64 confidence

 * aruco_ros/MarkerArray.msg

        Header header
        aruco_ros/Marker[] markers

### Test it with PIONEER p3dx

 * launch the aruco detector for pioneer p3dx robot simulator

    ```
    roslaunch aruco_ros mysingle.launch
    ```

 * Visualize the result
 
    ```    
    rosrun image_view image_view image:=/aruco_single/result
    ```

<img align="right" src="https://raw.github.com/pal-robotics/aruco_ros/master/aruco_ros/etc/reem_gazebo_floating_marker.png"/>


[1]: http://www.sciencedirect.com/science/article/pii/S0031320314000235 "Automatic generation and detection of highly reliable fiducial markers under occlusion by S. Garrido-Jurado and R. Muñoz-Salinas and F.J. Madrid-Cuevas and M.J. Marín-Jiménez 2014"
