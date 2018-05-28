# ManipulabilityTracking

The MATLAB codes show simple examples for a manipulability tracking task, where the robot is required to track a desired
manipulability ellipsoid either as its main task or as a secondary objective (where the nullspace of the robot is exploited).

This approach offers the possibility of transferring posture-dependent task requirements such as preferred directions
for motion and force exertion in operational space, which are encapsulated in manipulability ellipsoids.

The proposed formulation exploits tensor-based representations and takes into account that manipulability ellipsoids lie on
the manifold of symmetric positive definite matrices. The proposed mathematical development is compatible with statistical 
methods providing 4th-order covariances (see [1]), which are here exploited to reflect the tracking precision required by the task.


### Code description

	- demo_manipulabilityTracking_mainTask01
		This code shows how a robot can track a desired manipulability ellipsoid as the main task (no
		desired position) using the formulation based on the manipulability Jacobian (Mandel notation).
		The user can:

		1. Use different controller gains for the manipulability tracking
		2. Change the initial conditions and desired manipulability ellipsoid
		3. Modify the robot kinematics by using the Robotics Toolbox functionalities
		

	- demo_manipulabilityTracking_mainTask02
		This code shows how a robot matches a desired manipulability ellipsoid as the main task (no
		desired position) using the formulation based the manipulability Jacobien (Mandel notation).
		The matrix gain used for the manipulability tracking controller is now defined as the inverse 
		of a 2nd-order covariance matrix representing the variability information obtained from a 
		learning algorithm (see [1]). The user can:

		1. Change the number of iterations
		2. Choose different values for the covariance-based controller gain
		3. Modify the robot kinematics by using the Robotics Toolbox functionalities
		4. Change the initial conditions and desired manipulability ellipsoid
		
		
	- demo_manipulabilityTracking_secondaryTask01
		This code implements a manipulability tracking task as a secondary objective. Here, the robot 
		is required to hold a desired Cartesian position as main task, while matching a desired manipulability
		ellipsoid as secondary task using the manipulability Jacobian formulation(Mandel notation). 
		The user can:

		1. Use different controller gains for both the position controller and the manipulability tracking
		2. Change the initial conditions, desired Cartesian position and desired manipulability ellipsoid
		3. Modify the robot kinematics by using the Robotics Toolbox functionalities
		

### References  
	
	[1] Rozo, L., Jaquier, N. Calinon, S. and Caldwell, D. (2017). Learning Manipulability Ellipsoids for
	Task Compatibility in Robot Manipulation. IEEE Intl. Conf. on Intelligent Robots and Systems (IROS).	

### Authors

	Noemie Jaquier and Leonel Rozo
	http://njaquier.ch/
	http://leonelrozo.weebly.com/

		
	This source code is given for free! In exchange, we would be grateful if you cite the following
	reference in any academic publication that uses this code or part of it:

	@article{Jaquier18RSS,
	  author = "Jaquier, N and Rozo, L. and Caldwell, D. G. and Calinon, S.",
	  title  = "Geometry-aware Tracking of Manipulability Ellipsoids",
	  year   = "2018",
	  booktitle = "Robotics: Science and Systems ({R:SS})",
	  address = "Pittsburgh, USA"
	}

