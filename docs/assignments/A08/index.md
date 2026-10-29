# A8 – Gear Box Design

## Objective

- Design a gearbox that can be assembled and disassembled.
- Analyze and size input and output shafts for strength.
- Design journal bearings to support shafts.
- Create a gearbox housing with proper clearance and fastening.
- Use parametric CAD modeling to generate a final design.
- Document calculations, sketches, and lessons learned.

<img width="624" height="440" alt="image" src="images/image1.png" />

## Shaft Design

I started the design by listing all my knowns and unknowns for the input and output shafts.

<img width="624" height="578" alt="image" src="images/image2.png" />

Next, I drew a FBD for the input and output shafts.

<img width="431" height="447" alt="image" src="images/image3.png" />

Then I wrote out all the equations I would be needing so I can stay organized.

<img width="624" height="418" alt="image" src="images/image4.png" />

### Input Shaft Calculations

<img width="624" height="315" alt="image" src="images/image5.png" />

Since the calculated input stress was 1222 psi, which was below the maximum stress of 4000 psi obtained from Machinery’s Handbook, I know that my torque values are within my allowable limits. Additionally, the required diameter was below the diameter I had for my shaft. All my values were sufficient, so I moved onto the output shaft calculations.

### Output Shaft Calculations

<img width="624" height="210" alt="image" src="images/image6.png" />

I got the same results as my input shaft calculations which tells me my values are sufficient and I can move onto the journal bearing calculations.

## Journal Bearing Design

I started by listing out my knowns, unknowns, equations, and drawing a FBD.

<img width="624" height="693" alt="image" src="images/image7.png" />

<img width="607" height="400" alt="image" src="images/image8.png" />

<img width="266" height="221" alt="image" src="images/image9.png" />

### Bearing Input Calculations

<img width="519" height="177" alt="image" src="images/image10.png" />

<img width="555" height="179" alt="image" src="images/image11.png" />

### Bearing Output Calculations

<img width="506" height="173" alt="image" src="images/image12.png" />

<img width="582" height="174" alt="image" src="images/image13.png" />

### Results

<img width="624" height="289" alt="image" src="images/image14.png" />

I chose the model bearings I planned to use from McMaster-Carr using my shaft diameter. The bearings I am using are made of bronze (6291K111 and 6391K131), and comparing the results from the input and output calculations to this table, my results are well within the tolerable limit. Since the values are sufficient, I then calculated pressure, velocity, and PV for the input and output bearings.

### Bearing Thickness Calculations

I was not able to determine the minimum required thickness because I could not find an allowable hoop stress for my selected bearings. Because of this, I used the wall thickness of the selected McMaster-Carr bearings provided on the website. This made sense to me because I would be downloading the CAD files from the website, which means the thickness of the model should be the same as my CAD file so the tolerances line up. I believe that this material and thickness will provide adequate strength for this assembly, but I was technically unable to verify it. 

<img width="347" height="114" alt="image" src="images/image15.png" />

Since I could not use the minimum thickness equation, I did a simple calculation to find the thickness of the bearings listed on the website.

<img width="302" height="285" alt="image" src="images/image16.png" />

<img width="415" height="205" alt="image" src="images/image17.png" />

## Gearbox Design

For my gearbox design I decided to go with a simple rectangle put together with a snap fit. Using screws felt unnecessary for such a small housing component. Additionally, a snap fit will be easy to do since I made the gearbox out of ABS plastic. I believe ABS will be adequate for this design. However, the material can always be altered at a later date depending on what the needs for the gearbox are.

I attempted to illustrate my design idea for the gearbox before I began modeling.

<img width="624" height="735" alt="image" src="images/image18.png" />

## CAD

### Input shaft

I chose a generic steel for the material of my shafts. Steel will be compatible with the bronze bearings.

<img width="547" height="481" alt="image" src="images/image19.png" />

I began to parametrically model, but there was not much to input. I could have input all my equations into SolidWorks, but that felt unnecessary. The shafts are incredibly simple and only need the values provided to me at the beginning of the project.

<img width="624" height="86" alt="image" src="images/image20.png" />

<img width="624" height="361" alt="image" src="images/image21.png" />

<img width="624" height="478" alt="image" src="images/image22.png" />

<img width="624" height="499" alt="image" src="images/image23.png" />

I added a 0.01 in fillet because I want to avoid sharp edges.

### Output shaft

I followed the same exact process I did for the input shaft for the output shaft as well. 

<img width="624" height="88" alt="image" src="images/image24.png" />

<img width="624" height="418" alt="image" src="images/image25.png" />

<img width="624" height="445" alt="image" src="images/image26.png" />

### Gear box top

I did not record each and every little step as I normally would do because I feel like the CAD is incredibly simple and does not need too much explanation.

<img width="549" height="471" alt="image" src="images/image27.png" />

<img width="624" height="280" alt="image" src="images/image28.png" />

I chose these dimensions because I am going to make the box 0.25 in in thick and I want there to be a clearance of 0.25 from the gears. Additionally, I want the top half to be a little smaller than the bottom half so there is more material around the holes for the snap fit. Next, I cut my dimensions out and began building my prongs to snap it onto the other half of the gear box.

<img width="624" height="349" alt="image" src="images/image29.png" />

<img width="624" height="395" alt="image" src="images/image30.png" />

<img width="624" height="423" alt="image" src="images/image31.png" />

### Gear box bottom

<img width="549" height="471" alt="image" src="images/image27.png" />

<img width="624" height="306" alt="image" src="images/image32.png" />

<img width="624" height="424" alt="image" src="images/image33.png" />

I cut out all the dimensions I needed and added a 0.1 in fillet to the outside edges.

### Assembly

I put all the parts into an assembly, and it seems like it all fits properly. I struggled with forming mates to limit the movement of the pieces of the assembly. Additionally, I struggled with figuring out a way to verify my fits were correct.

<img width="624" height="462" alt="image" src="images/image34.png" />

<img width="624" height="612" alt="image" src="images/image35.png" />

<img width="624" height="559" alt="image" src="images/image36.png" />

## Lessons Learned

I learned a lot more about the differences between allowable power and transmitted power and the effect they have on required dimensions. Additionally, I realized how much purchased components can restrict your design. It was very frustrating trying to do calculations based on the preexisting models, especially since I have such little experience with this. I also learned how important it is to practice because I have not made an assembly in SolidWorks in roughly 5 years and I felt that as I was struggling to mate the pieces together.

## CAD Files:  
  
[CAD Files.zip](https://github.com/user-attachments/files/34131274/CAD.Files.zip)  
  
## Time Spent:  
  
I spend approximately 15 hours on this project.
