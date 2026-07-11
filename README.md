# task1-The-Boston-Dynamics-robot-dog
Initial mechanical design of a Boston Dynamics-inspired quadruped robot created in Tinker cad, focusing on body structure, leg mechanism, joints, and future actuator integration.

# shape:

 The robot features a compact rectangular chassis designed to house and protect its internal electronic components, such as the microcontroller, battery, sensors, and wiring, from dust and minor external impacts. The body is lightweight yet strong enough to support the robot's mechanical structure.

The robot is equipped with four symmetrical legs that provide excellent stability and balance during movement. Each leg is designed to support the robot's weight while allowing smooth and controlled motion over different types of terrain. The symmetrical leg arrangement also helps distribute the load evenly, improving the robot's overall stability and reducing stress on individual joints.

To increase the robot's functionality, a fifth robotic arm is mounted on the top of the chassis. This arm is intended for grasping, lifting, and carrying lightweight objects, making the robot suitable for simple manipulation tasks in addition to locomotion.

The robot is also designed with the ability to recover its upright position if it falls during operation. This self-recovery capability increases the robot's reliability and allows it to continue performing its tasks with minimal human intervention.

Overall, the design focuses on simplicity, structural stability, ease of manufacturing.


# the legs design:


The robot is equipped with four identical legs arranged symmetrically around the chassis to ensure stability and even weight distribution. Each leg is designed with multiple joints that mimic animal leg movement, allowing smooth motion and adaptability to different terrains. The lightweight yet strong structure supports the robot's weight while minimizing stress on the joints and actuators, improving both stability and efficiency.

 # Gear Reduction

The robot uses a gear reduction mechanism to increase the torque delivered to the leg joints. In this design, a small driving gear rotates a larger driven gear, reducing the output speed while increasing the available torque.

# Why Gear Reduction?

- Increases torque for lifting and supporting the robot's weight.
- Improves stability during walking.
- Reduces the load on the servo motors.
- Provides smoother and more controlled leg movement.

This approach is commonly used in quadruped robots because leg joints require high torque rather than high rotational speed.
this makes the legs more stable not moving so fast but also not too slow 


# number of joint and DOF:

4 Legs > 12 joints (3 × 4)
Robotic Arm > 3 joints

Total=15

# Hip Yaw

Left ↔ Right rotation
Changes the direction of the leg.

# Hip Roll
Side-to-side tilt
Helps the robot maintain balance.

# Hip Pitch

Forward ↔ Backward rotation
Moves the leg forward and backward while walking.

# Knee Pitch
Forward ↔ Backward bending
Bends and extends the leg.


# Type of MOtors:


The robot uses servo motors to actuate the leg joints and the robotic arm. Servo motors were selected because they provide precise position control, high accuracy, and are easy to interface with microcontrollers such as Arduino or ESP32. Their compact size and sufficient torque make them suitable for quadruped robot applications, where accurate and coordinated joint movement is essential. 
 but for the real Boston robot dog it uses custom electric actuators developed by Boston Dynamics.

These actuators typically consist of:

Brushless DC (BLDC) motor
Planetary gearbox (gear reduction)
Position encoder
Torque sensor
Motor controller





## Torque Calculation

To estimate the minimum torque required for one leg, the following assumptions were made:

- Robot mass = 3 kg
- Number of legs = 4
- Leg length = 0.10 m
- Gravitational acceleration = 9.81 m/s²

# Step 1: Calculate the total weight

Weight = Mass × Gravity

Weight = 3 × 9.81 = 29.43 N

# Step 2: Load on one leg

Force per leg = 29.43 ÷ 4 = 7.36 N

# Step 3: Calculate the required torque

Torque = Force × Distance

Torque = 7.36 × 0.10 = 0.736 N·m

 Result

 torque required for each leg =0.736 N·m




 # Stability and Center of Gravity:

The robot is designed with a low and centrally positioned center of gravity to improve balance and reduce the risk of tipping. Heavy components, such as the battery and controllers, should be placed near the center of the chassis and as low as possible.

The four legs create a wide support area around the robot. For stable movement, the center of gravity should remain inside the support polygon formed by the legs touching the ground. During walking, the robot shifts its body weight toward the supporting legs before lifting another leg.

The symmetrical leg arrangement and balanced weight distribution help the robot maintain stability on flat and slightly uneven surfaces. The feet should also provide sufficient ground contact and friction to reduce slipping.
 

 # type of wolking:
 
Since this robot is inspired by the Boston Dynamics Spot robot, it is designed to use a trot gait. In this gait, diagonal pairs of legs move together, allowing the robot to achieve faster and more stable movement across different terrains.

# excepted Mechanical issues:

1-Joint wear caused by continuous movement and repeated impacts
2-Limited servo motor torque, which may affect the robot's ability to carry weight or climb obstacles.
3-Limited battery capacity, reducing the robot's operating time.
4- Uneven weight distribution can cause the robot to lose balance.

