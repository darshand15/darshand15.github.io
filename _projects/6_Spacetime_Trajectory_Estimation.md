---
title: "Spacetime Trajectory Estimation"
collection: projects
---

<style>
  video:target
  {
    outline:none;
    border:none;
  }

  a 
  {
    color: blue;
    text-decoration: none;
  }
</style>

## Summary

A project aimed at simulating the events occuring after the end of a given video, in Unreal Engine by accurately estimating the three-dimensional kinematic parameters of the objects in the video. Let's consider a case where the video is that of moving traffic on a busy urban road. The objective of the project was to accurately simulate the events occuring after the end of the video. In this case, that would mean simulating the speed, acceleration, direction of the vehicles and their interaction with the environment, for example simulating the accident that might occur when multiple vehicles are heading in the same direction. This ability to accurately simulate events can have various applications and use cases. For example, a self-driving vehicle encounters such a situation at every instant of its journey and needs to make accurate decisions on its future movement by thoroughly considering the various parameters of the current environment around it. Thereby, such a system to simulate and predict events can be extremely useful in developing the decision making abilities of autonomous driving vehicles. Another interesting use case is related to the generation of data for training learning models. In this era where both the quality and quantity of data is a significant factor in the success of different models, there can often be a dearth of quality data that includes all possible scenarios in a comprehensive manner. Such a system where events can be simulated and tweaked to generate new data from a minimal subset of data can prove to be very critical and can help do away with the tedious nature of generating data for learning models. Therefore, this project can be used for a wide variety of use cases to simulate events comprehensively and extensively. This project was developed and implemented as part of my Summer Internship at the Centre for Data Science and Applied Machine Learning (CDSAML) at PES University.

## Video Demo
  
<video id="CDSAML_video_demo" width="320" height="240" controls>
   <source src="/videos/CDSAML_Project_Demo.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

## Implementation Details

The project involved the implementation of the following different stages in sequence to achieve the objective of accurately simulating events:
 * Detecting and perceiving the relative depth of objects from a single camera using relative monocular depth perception. As the project involved the use of videos shot from a single camera (which happens to be the more prevalent scenario as compared to multiple cameras being used to capture the same video), relative monocular depth perception was used to estimate the relative depth of all the objects in the video.
 * Identifying and recognizing the different objects in the video using the YOLO Object Detection model.
 * Tracking the selected objects using a Multi-Object Tracker and OpenCV.
 * Using the above assimilated information to generate the three-dimensional kinematic parameters of the objects including positional coordinates, speed, acceleration and directions of the objects under consideration.
 * Simulating the events occuring after the end of the video in Unreal Engine by spawning the selected objects with the estimated three-dimensional parameters.

The project involved the implementation of an interactive GUI that let the user select the objects of interest for the simulation. These selected objects are tracked for the duration of the video to estimate the required three-dimensional kinematic parameters and are spawned in Unreal Engine initialized with these parameters to accurately simulate the events after the video.

