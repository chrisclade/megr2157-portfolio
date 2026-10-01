# A6 – Bracket Drawing

## Objective  
  
For this project, I was tasked with continuing my bracket design by creating a parametric model and a detailed engineering drawing. I will be deciding on what dimensions are appropriate to use while creating a comprehensive model of the bracket and the drawing must accurately represent the bracket.  
  
## Parametric Design  
  
The first step I took was to decide whether it was appropriate to use the dimensions calculated for each feature from the stress analysis or the stiffness analysis. I put the values from each in a table so it was easy to read and decide. For feature A, the calculated minimum radius was 0.154 in from the stiffness analysis and 0.398 in from the stress analysis. Since the minimum required radius from the stress analysis was greater, I chose that as my dimension. I followed the same process for choosing which dimension to use for the rest of the features. Feature B will have a thickness of 0.166 in. Feature C will have a thickness of 0.813 in. Feature D will have a thickness of 0.0883 in. Feature E will have a thickness of 0.727 in.  
  
<img width="975" height="539" alt="image" src="https://github.com/user-attachments/assets/52fbb7ac-849b-4d6b-996a-a63393b6e8df" />  
  
Next, I made sure to change my material to the chosen material and then I inputted all the parametric equations into SolidWorks so I could begin modeling the bracket.  
  
<img width="867" height="1028" alt="image" src="https://github.com/user-attachments/assets/97827195-1704-4b4b-ae3a-18512b223226" />  
  
<img width="975" height="301" alt="image" src="https://github.com/user-attachments/assets/eaa9b1e6-315b-4a83-b371-d712b7b14842" />  
  
# Feature A  
  
I started with feature A and then modeled off of that since that was how I previously solved for the dimensions.  
  
<img width="975" height="621" alt="image" src="https://github.com/user-attachments/assets/01a509c5-760d-400f-97d7-cf03538c104c" />  
  
# Feature B  
  
After feature A was modeled, I started on feature B but I realized I did not have a specified length for it. I decided to go with 1.195 because it is approximately 3 times the radius of feature A, which makes it easy to parametrically model with because I can input the length as 3 times “r”.  
  
<img width="975" height="965" alt="image" src="https://github.com/user-attachments/assets/9f0e055a-d7b4-4119-8e99-e86cc8f90a8c" />  
  
<img width="975" height="906" alt="image" src="https://github.com/user-attachments/assets/dd1b8687-15b9-4ec4-9443-568783253274" />  
  
Additionally, I made the bottom of feature B shape around feature A instead of just leaving it as a rectangle.  
  
<img width="975" height="547" alt="image" src="https://github.com/user-attachments/assets/c1c7478a-52df-46ec-b002-a8d37caa1068" />  
  
<img width="975" height="850" alt="image" src="https://github.com/user-attachments/assets/1e572320-a45b-47e0-9c99-89e8714c10af" />  
  
# Feature C  
  
I began working on feature C next but when extruding the feature I realized I had made a mistake with my sketch planes. I had been sketching on the front plane but I extruded features A and B in different directions. Because of this, feature C was not where it was intended to be and it was not the correct depth either.  
  
<img width="975" height="647" alt="image" src="https://github.com/user-attachments/assets/72e69f6f-b790-40ea-8f6f-b389f9558a87" />  
  
<img width="975" height="744" alt="image" src="https://github.com/user-attachments/assets/368e00c4-d36d-4295-b8ce-968a0a2f44a0" />  
  
<img width="975" height="677" alt="image" src="https://github.com/user-attachments/assets/c0a3f08a-a1c4-41a9-ad17-a0f937837b92" />  
  
I had intended for feature C to have a depth equal to the length of features A and B. I thought about changing the depth to the length of feature A plus the thickness of feature B, but I realized feature C relies on the depth to calculate its thickness. However, because I parametrically modeled the part with dimensions in SolidWorks, I decided to add a new global variable for depth, b, that equals the length of feature A plus the thickness of feature B. Then where I previously used the length of feature A, 0.75 in, for the depth, I changed the value to that of my new depth. Then SolidWorks gave me a new value for the thickness of feature C, which automatically affected the part because it was parametrically modeled.  
  
<img width="975" height="258" alt="image" src="https://github.com/user-attachments/assets/41e5931c-1fd6-4490-8df1-0aacdedaca15" />  
  
The new depth had an effect on the thickness of the remaining features as well. This alteration did not change the minimum required thickness to values lower than the ones calculated by stiffness analysis. This means I can continue with modeling.  
  
<img width="975" height="736" alt="image" src="https://github.com/user-attachments/assets/bbf756a3-1878-4280-8828-d172f669ad4b" />  
  
Additionally, instead of starting the sketch on the front plane, I started it on the back of feature B. This way the depth would line up properly when extruded.  
  
# Feature D  
  
While modeling feature D, I found two more issues. First, when I chose a length for feature C, I did it based on the dimensions of the rigid beam the bracket would be attaching to. However, I made the length of feature C equal to the length of the rigid T beam, which is 2.496 in.  
  
<img width="945" height="269" alt="image" src="https://github.com/user-attachments/assets/674b1e87-0f7a-4920-b188-88f069fac0f8" />  
  
This caused feature D to hang off the end of the bracket without attaching to feature C.  
  
<img width="975" height="706" alt="image" src="https://github.com/user-attachments/assets/9ee30c9f-3c68-4a7e-a6a1-428ce6c97cdb" />  
  
To fix this, I changed the global variable for the length of feature C to be equal to 2.496 plus the thickness of feature D. Additionally, I foresaw the same exact problem happening between feature E and feature D so I preemptively changed the length of feature E to its original length, 0.9992 in, plus the thickness of feature D.  
  
<img width="975" height="232" alt="image" src="https://github.com/user-attachments/assets/9097feee-35b2-4c31-bfed-06ec4a1d9346" />  
  
These changes had a small effect on the other dimensions but they are still within the expected range.  
  
The second issue was I had never assigned a global variable to the height for feature D. Before I continued modeling, I assigned the variable “c” as the height and set it equal to the dimensions of the rigid T beam.  
  
<img width="975" height="255" alt="image" src="https://github.com/user-attachments/assets/9c8bfc86-7f74-41d6-a27f-f5c7c0c64a00" />  
  
<img width="975" height="754" alt="image" src="https://github.com/user-attachments/assets/95c678a0-c31c-4862-98ca-fb851598e255" />  
  
<img width="975" height="826" alt="image" src="https://github.com/user-attachments/assets/0d9fabfb-449e-49ab-a01a-b9a22b76eb1e" />  
  
# Feature E  
  
While modeling feature E, I caught another mistake. When I added the thickness of feature D to the length of feature C, I forgot to double the thickness in the equation. I fixed it in my global variables and continued with the model.  
  
<img width="975" height="252" alt="image" src="https://github.com/user-attachments/assets/bdbdeb3f-f0af-41c2-b14c-e9baee4dd98d" />  
  
<img width="975" height="945" alt="image" src="https://github.com/user-attachments/assets/00121e09-55fb-40c0-aa08-42a6d10017d5" />  
  
<img width="975" height="1142" alt="image" src="https://github.com/user-attachments/assets/3fd78b37-0295-4138-a40f-58737501aafc" />  
  
## Drawing  
  
Once the I was done modeling the bracket, I started on the drawing. Dimensioning the drawing did not take much time but I am not sure I understand where I am supposed to specify more precise tolerances to make sure the bracket is a sliding fit.  
  
<img width="975" height="758" alt="image" src="https://github.com/user-attachments/assets/2cbe1568-cab5-4f88-a0d3-6ba45dc0857e" />  
  
## Reflection  
  
Designing this bracket using stress and stiffness analysis taught me a few valuable lessons. One of the most important lessons I learned was to be very cognizant of the physical dimensions of a part or design while I am doing my calculations. I solved for my dimensions without paying much attention to how the individual features were supposed to attach together, this caused me to run into a lot of errors while I was modeling the part. For example, I used stress analysis to derive the radius for feature A, which I then used to drive the width and, in turn, the thickness for feature B. I input my derived equation for the radius at the variable “r” and used that same variable in my equation to find the thickness of feature B.  
  
<img width="975" height="29" alt="image" src="https://github.com/user-attachments/assets/8465efa7-4f9d-4c1e-8408-8db7af790119" />  
  
However, because I was not thinking about the model when I calculated these values, I failed to realize that these two features build on each other and directly impact the next feature. I designed each feature as if it were its own individual part, and not a piece of a whole design. Fixing my error was not difficult because my bracket was parametrically designed allowing me to change one small dimension and the rest of the part automatically worked itself out.  
  
Another lesson I learned was that good drawings are incredibly important. Throughout my time in other classes I have taken for granted the drawings I have been given to work with. Now that I am creating more drawings myself, I can understand how easy it is to make an error in a drawing. Tolerances are my biggest concern when it comes to errors because I am unfamiliar with assigning them myself. On my drawing for this bracket, I applied a tighter tolerance ± 0.005 on the 0.072 in width of feature D. This feature will have a direct impact on the sliding fit interface of the bracket and since it is so thin I believe it is important to keep that dimension as tight as possible. I applied a loose tolerance of ±.02 to the 0.80 diameter of feature A because if those dimensions are not precise, it should not make a large difference. Feature A does not have a mating surface with the rigid T beam which I believe makes it a non-critical feature. I am currently unconfident in the total tolerances of my drawings, but I hope I can continue to learn from my experiences and improve in my drawing abilities.  
  
**Time spent:**  
I spent approximately 10 hours on this project.  
  
## 2157 Students Only  
  
# Parametric Design  
  
I started modeling the link by inputting my previously calculated dimensions and creating the simple geometry in SolidWorks.  
  
<img width="975" height="902" alt="image" src="https://github.com/user-attachments/assets/9bfff939-0346-41ac-8b22-7236e7d3acab" />  
  
Then I drew the circles to be cut through the link. The hole meant for the bracket was directly linked to the parametric radius of the bracket. I imported the parametric equations used from the bracket to the CAD file so I could easily relate the diameters.  
  
<img width="975" height="1016" alt="image" src="https://github.com/user-attachments/assets/e50d07ad-a21e-4a9b-9afd-cf007845d812" />  
  
<img width="975" height="1165" alt="image" src="https://github.com/user-attachments/assets/69919d41-bb58-4fac-a391-9515f7123a0c" />  
  
# Drawing  
  
The drawing was very straight forward assuming I did it correctly. The two critical features in the link are both of the holes. I changed the tolerances to be +.005 and -.000 inches for both of them because it is supposed to be snug to slide fit. It is better for the holes to be slightly too big than too small otherwise the link will not fit at all.  
  
<img width="975" height="755" alt="image" src="https://github.com/user-attachments/assets/6cf80290-b0d2-4b4c-bfd8-e31217e6bb8f" />  
  
# Reflection  
  
I learned that there is a lot of different ways tolerancing can work. The tolerance callouts I made, for example, specify that it is better for the holes to be too big than too small. I have learned this is a way to specify design intent through tolerancing.  
  
## CAD Files  
  
**Parts:**  
[A6 Bracket.zip](https://github.com/user-attachments/files/32890515/A6.Bracket.zip)  
[A6 Link.zip](https://github.com/user-attachments/files/32890524/A6.Link.zip)  
  
**Drawings:**  
[A6 Link Drawing.zip](https://github.com/user-attachments/files/32890570/A6.Link.Drawing.zip)  
[A6 Bracket Drawing.zip](https://github.com/user-attachments/files/32890567/A6.Bracket.Drawing.zip)  
  
**Parts and Drawings in one .zip:**  
[A6 Parts and Drawings.zip](https://github.com/user-attachments/files/32890659/A6.Parts.and.Drawings.zip)































