---
title: Dual-Stepper Scanner Gimbal
layout: default
---

# Spherical Two-Axis Dual-Stepper Scanner Gimbal

## Motivating Questions + Objective
- How can I **rotate a scanner smoothly in two independent directions using stepper motors**?
- How do I design a structure that fits **two steppers inside a sphere** without collisions or instability?
- How can I design and present my CAD work in a way that inspires others to replicate or improve this idea?

**Objective:** Create a mechanism that lets a **scanner** rotate smoothly on **two independent axes** using **two stepper motors** inside a sphere and base. This type of setup is called a **gimbal**, a structure that enables controlled rotation. Inspired by **ball turrets from Star Wars**, I am adapting the idea into a fully spherical form that others can study, understand, and rebuild.

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


This project changed the way I think about engineering. Hardware design isn’t just creativity—it’s patience, geometry, accuracy, and the willingness to rebuild parts until they actually work. And even though this is only the design stage, I’m already developing a clearer sense of how mechanical systems, electronics, and software will connect in the final version. This journal is meant to help others follow that same journey, so they can replicate and build on what I’m doing.

