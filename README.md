# City_of_Madison
start date: Sep 10, 2019
end date: Dec 10, 2019

Focus: Pedestrian, Traffic, and Light Patterns in State Street Intersections

Basic Assumptions:
1. No directions for pedestrian are specified. Assumed 4/5 pedestrian wait for Main Street Red Light, 3/5 pedestrian will wait for Cross Street Red Light.
2. Every car will pass the intersection in 2 seconds.(observation)
3. Pedestrian and Cars come in a constant speed. Uniformly distributed according to time.
4. Define anger index = 1/3000*(waiting time)^2 for pedestrian, anger index = 1/100*(waiting time)^2 for traffic, so the weight is 1:30. 
5. Both common red light time and yellow light time is 1.5s. Only optimize green light time (the total cycle time will change accordingly).
6. A cycle for Main/State Street is between 20s to 50s (both ends included). 
7. No correlation between the waiting time among intersections nearby. 

Methodology:
Construct cost function based on anger index for both pedestrian and traffic. Use scipy.optimize to minimize the cost. The result will be ideal time cycle. 

Notes:
Some data are not allowed to public. They are not uploaded to this directory. Please reach out to administrators from City of Madison to get these sensitive data. 

p7_mid goes hand in hand with slide presentation1.pptx. No new plots are created in this notebook. This is a presentation in the middle of the term to allow administrators from City of Madison learn about my progress. 


