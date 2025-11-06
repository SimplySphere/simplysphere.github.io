---
title: VR Show & Tell
layout: default
---

# VR Show & Tell

To show off the capabilities of VR inside our school, I built a scene on **Unity** and connected it to the **Meta Quest Pros**, creating an experience that allows the user to **move around and view models**. This project made me master a new software I had never used before, fight the limits of Macbook and Windows, and troubleshoot the fickle VR headsets. I expanded on my patience and willingness to explore deeper into topics more foreign to me. 


## History

## Overview


## Creative Process
1. Brainstorming: Started with only the certainty that the project would use VR in some way. I was inspired by Dr. Dzula to make something that would immerse you, showing a model or object. 
2. Choosing a platform: I knew that to make something like that, you needed a design platform. I began with SimLab, which I managed to run on the headset. However, the limit of 5 uploads, movement issues, and a corrupted final file led me to discard the idea.
<div style="display: flex; gap: 10px;">
    <img src="images/simlab.png" alt="SimLab Logo" width="28%">
    <img src="images/simlabdemo.jpg" alt="SimLab demo" width="68%">
</div>
3. Starting over: After that setback, I decided to start from scratch. After surveying my options, I moved to Unity, a search started thanks to a suggestion from Thomas.
4. Learning Unity basics: At first, I had to figure out Unity’s 2D vs 3D views along with every other feature. I also got stuck for an hour because I did not realize that scrolling out resized the scene view to fullscreen, and I did not know that scrolling in would reset it. After many hours, I started to settle into the software
<img src="images/unitybasics.png" alt="Unity">
5. Building the environment: I used PNP as a reference for modeling and lighting. I added movement and turning systems after several trial-and-error attempts, finally achieving freedom of viewing and navigation after many hours.
<img src="images/unitypnp.png" alt="Unity + PNP">
6. Adding detail: I added a skybox to bring life to the scene. I then imported a collection of random models that would work inside of Unity to give a bit of diversity to the scene. For each model, I had to add its textures. This sounds easy, but the learning curve was steep, and some models had a lot of textures, each of which I had to sort through and find its corresponding box. For one, I had to assign 91 textures to its correct part. 
<div style="display: flex; gap: 10px;">
    <img src="images/unitymodels1.png" alt="Unity Models 1" width="48%">
    <img src="images/unitymodels2.jpg" alt="Unity Models 2" width="48%">
</div>
<div style="display: flex; gap: 10px;">
    <img src="images/unitymodels3.png" alt="Unity Models 3" width="48%">
    <img src="images/unitymodels4.jpg" alt="Unity Models 4" width="48%">
</div>
7. Transitioning to VR controls: I swithced all the standard controls to VR-based inputs, sorting through countless messy prefabs and folders until I got the controller reacting properly.
<img src="images/unityprefabs.png" alt="Unity + Mess">
8. Testing with the XR Simulator: I used the XR Interaction Simulator to test motion and interaction inside the editor before headset deployment.
<img src="images/unityvrsimulator.png" alt="Unity VR Simulator">
9. Platform challenges: I faced compatibility issues as I tried to connect the two. The Meta Questo Pros support Android and Windows, but I was building on a Macbook, which required me to make many adjustments and find methods to export properly.
<img src="images/unityplatforms.png" alt="Unity Platforms">
10. Final build: After resolving input handling, platforms, and model conflicts, I successfully compiled the project into an .apk file, a small representation of the larger whole of my VR world and experience.
<img src="images/unityapk.png" alt="Unity APK">

## Results 


## Reflection
