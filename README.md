# PhysicsSim

Simulating Physics\
Most video games are designed to balance the tradeoff between physical realism and gameplay. A completely realistic simulation of all the physical interactions between moving objects can be very mathematically complex and can potentially make it difficult to play the game on a 2D screen, especially with the limited amount of control possible using a keyboard/mouse or controller input. Although we generally want objects interact to in a "physically plausible" way, using physics models that approximate or even change the laws of physics (e.g., gravity) can often result in gameplay that is more fun and engaging.\
\
Donut County is a great example of a game that makes effective use of "magical" physics. As Ben Esposito discovered, making a hole in computer graphics is actually much trickier than it sounds, and this Rock Paper Shotgun articleLinks to an external site. has a very interesting discussion of the physical approximations and fakery that he used when developing the game. For the purposes of this programming assignment, we will further simplify the simulation by assuming that all moving objects are spheres, which will make our physics calculations more mathematically straightforward and computationally efficient.\
\
Rigid Body Dynamics\
The movement and interaction of solid, inflexible objects is known as rigid body dynamics, which is the most commonly used physical simulations in computer graphics and video games. This introduction to video game physicsLinks to an external site. provides a nice supplemental reading if you are interested in learning more about the concepts and math involved in simulating rigid body dynamics.\
\
To make this assignment practical to implement, we will make a few simplifying assumptions about the physics. Specifically, you should follow these guidelines in your code.\
\
Motion: When implementing rigid body physics, the change in the object's position p is computed using its velocity v. This occurs each frame in the update() method of the RigidBody class, using the formula described in class: p' = p + v dt*.\
\
Friction: To simulate friction, you can simply reduce the velocity of the rigid body when it hits something. For example, you might multiply the current speed by 0.9 after a bounce, which would slow it down by 10% due to friction. The starter code already includes the friction slow down parameter used in the instructor's example.\
\
Gravity: The rigid body should accelerate downward due to gravity, but this should be a plausible approximation of gravity. This is, after all, a game where objects are falling into a magical hole in the ground. The starter code already includes the gravity constant.\
