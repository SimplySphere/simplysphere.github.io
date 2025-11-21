---
title: Spherical Two-Axis Dual-Stepper Scanner Gimbal
layout: default
---

# Spherical Two-Axis Dual-Stepper Scanner Gimbal

## Motivating Questions + Objective
- How can I **rotate a scanner smoothly in two independent directions using stepper motors**?
- How do I design a structure that fits **two steppers inside a sphere** without collisions or instability?
- How can I demonstrate my CAD in a way that inspires others and promotes this idea?

**Objective:**  

---

## Materials
- Fusion 360 for CAD modeling  
- 2 stepper motors (25mm tall NEMA 17)  
- Stepper motor dimension reference sheets  
- 3D printer 
- Screws and mounting hardware
- UNO R3 Super Starter Kit
- Sharp GP2Y0A21YK0F IR Distance Sensor
- USB cable

# add image for materials
# add reference image

---

## Step-by-Step Process
1. **Initial Concept:**  
   I started by sketching the idea of a fully enclosed spherical mount where all mechanics are hidden inside the shell.

2. **Base + Yaw Motor Design:**  
   I designed the lower “flared” base to hold the first stepper motor. This motor is responsible for rotating the entire sphere left and right.

3. **Sphere Shell Modeling:**  
   I modeled the outer sphere to sit cleanly on the base, with enough clearance to rotate smoothly while still appearing seamless.

4. **Inner Ball + Tilt Motor:**  
   Inside the sphere, I created a central ball structure that holds the second stepper motor. This motor rotates the scanner up and down.

5. **Scanner Mount Plate:**  
   I added a front arm/plate directly connected to the tilt motor shaft so the scanner would maintain a rigid line of sight during rotation.

6. **Wire Routing + Geometry Adjustments:**  
   I added openings and internal tunnels to allow wiring to pass through the structure without interfering with motion.

7. **Motion Testing in CAD:**  
   Using Fusion 360 joints, I simulated the rotation of both axes to confirm the motors wouldn’t collide with the shell or with each other.

---

## Problems + Solutions
- **Finding dimensions**:
- **Finding leeway**

---

## Main Takeaways
- **Designing a mechanism inside a sphere requires precision**—even tiny geometry errors cause collisions.  
- **Steppers demand exact spacing and alignment**, which forced me to take measurement seriously instead of approximating.  
- **CAD simulations are essential**, especially for multi-axis systems where movement paths overlap.  
- **Mechanical design is iterative**, not linear. Almost every part needed multiple revisions as new constraints appeared.

---

## Reflection
At the beginning, this project felt intimidating. I had never designed something that combined geometry, motors, and motion constraints inside such a tight enclosure. As I started modeling, I kept running into unexpected issues—clearances that were too tight, walls that were too thin, steppers that didn't fit the way I imagined. Each problem forced me to slow down, remeasure, rethink, and revise.

Over time, the process shifted from confusing to genuinely satisfying. I began to understand the rhythm of mechanical design: test, adjust, test again. Every improvement made the model feel more real and more achievable. Seeing both axes rotate smoothly in Fusion 360 was a moment of real progress that made the earlier frustrations feel earned.

This project changed the way I think about engineering. Hardware design isn’t just creativity—it’s patience, geometry, accuracy, and the willingness to rebuild parts until they actually work. And even though this is only the design stage, I’m already developing a clearer sense of how mechanical systems, electronics, and software will connect in the final version. This journal is meant to help others follow that same journey, so they can replicate and build on what I’m doing.

