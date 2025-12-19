---
title: Pan-Tilt LiDAR Scanner
layout: default
---

## Motivating Questions + Objective
- How can I **bridge hardware with software** or **join CAD and code** to create a **3D scanner** that uses this mechanism?
- How can I **connect with my peers** to implement an aspect I did not explore in depth?

**Objective:** 


## Materials
- VS Code
- Arduino IDE
- Fusion 360 for CAD modeling  
- 2 stepper motors (25mm tall NEMA 17)  
- Screws and mounting hardware
- UNO R3 Super Starter Kit
- Sharp GP2Y0A21YK0F IR Distance Sensor
- USB cable
- Completed & printed gimbal

<img src="images/stepper-final1.png">
<img src="images/code-platforms.png">


## Step-by-Step Process
1. **Starting high:** came out of thanksgiving break still on a high from being able to finish the design immediately asked patrick if he had looked into the code more which he said he had he was the only one of the two of us in our inital partnership that was working on the code while i was working on the cad because i had a design when we decided to split so naturally i thought he was gonna do some magic and get the code going 
2. **Hit of reality:** however that did not happen it took more than a week before he had any code running the mechanism in fact no one had any working code so i had to wait while i confirmed during that time i tried to understand the coding teams job better and appreciate what they were doing additionally i normally do coding and personally i think of myself much mroe as a coder than designer so i was personally interested in the code however when mr raus introduced laser cutting everyone started to follow that idea and suddenly my ball structure was ignored before it was ever given a chance
3. **A week of lows:** for a while i didnt know who to really work with patrick started to work with collin and i tried asking charlie but he didnt have much of a response and he had no code i needed someone who code and experience because the deadline was approaching and i had not gotten the necessary skills needed to operate arduino ide and with finals rapidly approaching i knew i needed to basically outsource and seek collaboration however this was not easy as it felt wrong to basically leave my partner for another because i technically was assigned to patrick but he seemed to have no intention to work with me and my ball mechanism
4. **Reaching out:** I started paying more attention to the people around me specifically someone who i have worked successfully before so i decided to talk to thomas during community dinner because we sit next to each other on a sunday night he had code but not much of a mechanism and i had no code and a mechanism we decided this was a good partnership and started work i taught him the design and how everything connected while he gave a rundown on the code progress so then i became part of thomas and kaydens group
5. **Finding time:** Finals were happening and everyone was stressed and tired i know especially for me not only did i have finals i also had a tennis tournament i had an sat to take and i had science fair which was something i knew i had to get ahead on because there was a lot less time than i thought so i had to be super efficient and not allow myself to take it so easy in the past few weeks unfortuantely that did cut away some of my self enjoyment time but i think the result was satisfactory in that i felt much mroe proud and satisifed with teh work i had done
6. **Until the last minute:** we discovered a small issue and i had to cad something that had to work first try and turns out it didnt which usually happens with 3d design so we went to robotics to drill out a whole quarter of it but then it worked and the problem of the mechanism being a bit too loose on the bottom was solved
7. **Demonstrate final form:** we presented on thursday after a morning of hard work starting at 5:30 getting everything prepped and checking in to the library as early as possible to start printing but overall the presentation went well and i finished tech sem semester one on a high note

<img src="images/broken-stepper.png">
<div style="display: flex; gap: 10px;">
  <video width="48%" controls>
    <source src="images/lidar-test1.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <video width="48%" controls>
    <source src="images/lidar-test2.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>
<p>&nbsp;</p>

<source src="images/lidar-test3.MP4" type="video/mp4">


## Problems + Solutions
- **Finding my group:**: patrick left without a proper notice just started to focus on laser cutting and stopped being responsive to the idea of the ball turret mechanism and collin initally was interested but then left with patrick soon i realized that i was on my own and i had to make adjustments so i tried my luck with charlie but he said he did not do any code nor was he really looking into partnerships so i was very lost and knew the project counted so i looked around and saw two other groups that i considered however i lacked a way to communicate with them after class when i was pondering so i thought of using community dinner to talk my collaboration with thomas's group over and in the end i was able to form a partnership and we went on from there
- **Last-minute fixes:** noticing a critical problem last minute is never fun and that was exactly what happened teh stepper motor at the bottom of the mechanism was shaky because of the movement of it kind of more so in general i never thought when desinging that it would have such a problem so the bottom was not a perfect fit like the one in the ball itself so i thought to make an insertion a kind of plug to be able to slot in so that the motor would be held in palce this i did the day of in the morning and printed the day of right before because we only noticed the night before but i just planned and made sure everything worked well

<img src="images/lidar-wip.png">

## Main Takeaways  
- **Fixing intuitively:** throghout this process i have messed up on multiple occasions and the only reason i was able to stay on track and continue was because i never overdid my solutions to the multitue of problems that arose in the process somehow many of these solutions involved a drill the first was when i designed the other half ot eh ball wrong so taht it turned the wrong way drilling the hole so it didnt catch the d shaft worked perfectly the second was when the plug did not have a slot for the wire outcropping area whcih a drill also sovled by dirlling out a quarter of the plug
- **Finding my people:** in teams you cant expect everything to follow your wavelength or even your goals some people simply have their own agendas and lives i knew of this and have experiecned this mayn times before but experiencing it is always a learning experience and not one that is fun i dont blame these people but if i was all powerful i know i would have changed some peoples minds in order to push for what i wanted to see in the end however since im no all powerful being i have to find my people that i can trust and i can work well with because forcing myself or forcing others to follow me is not fair to either party so from now on i will try to keep this idea more in mind and focus on compromising on all the steps rather than getting ahead of myself

<img src="images/lidar-present.png">
  

## Reflection
i think this project was more of a social project than an engineering one despite it being an engineering challenge in every way jsut because of the problems i was met with during these few weeks mostly involved connecting with people and being able to find a group i could apply myself to i know i had many ups and downs but i am happy that everything did work out in the end in terms of having an end result to be able to show off because such a thing is not guaranteed

i came into this project honestly a bit too confident to my liking i had managed to get ahead and create something that actually seemed functional i was ahead in terms of progress and very proud of myself so the hit was extra hard when people just didnt really care about it as it felt like all the effort and emotion i put into the other was wasted i felt like i was completely undeserving of such pride and didnt really know what to do with my design considering to just scrap the whole thing and follow along with my partner who seemed convinced in his path with collin however i started to really take observations and count my chances looking around to find people i know i have worked with thomas before but he wasnt even my first choice it was charlie who wasnt that open or ready and thomas was more readily available because he lives across me in alamo seperated by only the lawn so we can work easily at night so i managed to find the people i work best with and that was the main challenge of this project a lot less engineering based worries more so social and teamwork 

i think i can walk out of semester 1 knowing i have developed myself not only technically but as a student peer collaborator and friend because the tools and experiences i have had in tech sem have been instrumental in my devleopment as a developer of anything whether it be cad which i had only done a bit of before this cad or 3d printing hwich i never touched before this or coding which i have had new perspectives since the start of the new in terms of inutition and use i have never before this ever worked with sensors or motors besides robotics just a few months before so this was all new to me and i think i have taken the challenge head on and really tried to engage with each lesson i know in my journals i am refelct and always in every project find something to say something to experiecnce something to learn and something to be able to rample on and on about to be able to come out and say that i really lived my life at that time to the fullest personally i think i did myself justice
