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


## Materials
- Fusion 360 for CAD modeling  
- 2 stepper motors (25mm tall NEMA 17)  
- Stepper motor dimension reference sheets  
- 3D printer 
- Screws and mounting hardware
- UNO R3 Super Starter Kit
- Sharp GP2Y0A21YK0F IR Distance Sensor
- USB cable

<img src="images/stepper-box.png">
<img src="images/stepper-nema17.jpg">
<img src="images/stepper-reference.jpg">


## Step-by-Step Process
1. **Initial concept and inspiration:** thought of star wars ball turret and thought of how 2 axis would work; know the two servos would need an orientation in which they were pointed up and to the side in order for movement to work; based on fundamentals placed into this idea of ball turret to create basic idea of design components
2. **Test low-fidelity prototypes:** tested for friction with simple designs that took around 20 minutes each, interacting with the 3D printer and servos actively
3. **Researching dimensions:** found a reference sheet in chinese, used ruler to find other unknowns, and contacted others for their numbers to create understanding of the measurements that would go into this design
4. **Create medium-fidelity look-alike:** used measurements and created a crude, dysfunctional look-alike that served its role in showing me the dimensions in context, allowing me to tweak the design within the CAD software without having to move to higher fidelity and the real world yet
5. **Finalize design:** design idea is finalized and components are selected to be a certain waay; cading takes the most time here and is the majority of this step as each part of the idea has to be recognized
- the design has 5 parts: 
6. **Iterative design with revision:** printed on wendesday 5:30, 8:30, 9:00 and thursday 8:30, 9:00 and final print started 11:30 to test different parts such as offset, the fitting of the motors, the fitting of all the components, etc; each time brough a list of 3-5 things to revise and edit, some taking 5 minutes to change some requiring a full run through of the cad to edit everything taking up to an hour; overall cading time amounted to close to 4 hours in one day
7. **Present and demonstrate final design:** be able to present this design in a way that is educative and informative, keeping the design open source: this is link to the download for anyone who wishes to explore or pursue this idea

<img src="images/stepper-starwars.png">
<img src="images/stepper-low.png">
<img src="images/stepper-cad.png"> 
Download .fbx or .f3d here
<img src="images/stepper-makeshift.jpg">
<img src="images/stepper-final.jpg">

## Problems + Solutions
- **Finding dimensions**: finding reference sheet - nemo 17 had to research myself to find -- found a chinese reference using diagrams i got the numbers, still missing height of motor base and jut-out for cable -- had to measure myself; still needed those for the scanner so i reached out ot patrick to ask for it because i did not know them and he had just measured them before me
- **Finding leeway** finding the extra space to give the shaft so that it maximizes friction while also allowing the shaft into itself without a big struggle; leveraged the d shaped shaft to be a better fit (now fit is directional); initally was too tight at 0.10mm, was still too much at 0.15mm finally last designw as 2.5mm of offset, which worked

<img src="images/stepper-analysis1.png">
<img src="images/stepper-canalysis2.png">

## Main Takeaways  
- **Mechanical design is iterative**, almost every part needed multiple revisions as new constraints appeared: i had to change the offset of the shaft holders 3 times, the length of the vertical holder was too short, the base was too short, the container for the bottom servo was too tight, the length was miscalcualted for the horizontal servo holder, the jut-out was miscalculated so did not fit, the space for wires inside the base and ball was too little, the first print of everything melded together, the printer ran out of filament for a complete print that happened overnight, the axis ball and stick failed to print 2 times due to weaker support from the bottom and a heavy head, the ball itself was underestimated two times during cading process, the servo height was underestimated until finally measured, the printer spagetti-ified on the final print (shoutout henry for saving this project as a heroic passerby who restarted the print), the model was without smooth edges for two iterations, etc. these are problems that would have never been solved if not for revisions, each of them enough to break the project
- **Importance of lower fidelity for testing:** this process would have been much, much worse if i had not taken the time to print smaller sections and allow imperfection. my photo in context was an amalgamation to the point of being an abomination with parts from 4 different print jobs of the 5 components possible. allowing imperfection to occur to push for progress was what allowed this project to take shape in this short time span

<img src="images/stepper-cad-list.jpg">
  

## Reflection
when i first head of this project on tuesday, I was instantly overwhelmed and did not know what to do. however, i think my approach this time to the time cunch alonh eith all the other challenges helped. I tried to focus on the iteration i was on currently, never trying to overpush or expected too much of any single try i made. i kept myself organized and focused on whatever it was i was doing and working for at that stage without any care for appearances.
this project felt the best out of all the projects ive dont this year including pnp. i felt like in the short time span which was literally around a day, i spent my time efficiently and brought a product no one else was able to create. i know i spent many hours cading with a passion and checked the 3d printers more than 10 times a day to check my cad as well as to print, using all the times available to me to their fullest despite dorm meetings, study halls, summatives, and an already tight schedule. i felt like i took this one the smartest, playing with the fidelity and incompleteness without worry for appearances or a complete finished iteration every time. i felt like i wanted to show my process not my final result. in doing that i was able to put more progress into creating a final result i was able to revisit and revise multiple times that i can say i am very proud of. all in all i feel proud of the work ive done and i think i should be able to recognize the growth ive had over the year, especially with the original rocky first impression of this project. 

