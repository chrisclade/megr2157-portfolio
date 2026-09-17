# A4 – Motor Mount

## Objective  
  
For this project, I was tasked with designing a motor mount for a 24-volt DC gear motor. The mount had to attach the motor to a rigid wall while supporting a 300-newton load applied perpendicular to the end of the motor shaft. The main design requirements were to prevent yielding using a factor of safety of 3 and to limit the maximum deflection to 0.30 mm. The mount was divided into two features. Feature 1, which supports the motor, and Feature 2, which attaches the bracket to the wall. Both features were modeled as cantilever beams for the hand calculations.  
  
<img width="296" height="368" alt="image" src="https://github.com/user-attachments/assets/d05f592d-c8df-4e43-a7b3-e3925d9c6b69" />  
  
We were also given the dimensions of the motor itself.  
  
<img width="867" height="327" alt="image" src="https://github.com/user-attachments/assets/91801041-6304-44bc-aa39-9b276d095ab1" />  
  
For the material, I chose ABS. Since the provided material properties were given as ranges, I used the lowest values in those ranges as a conservative design choice. I used a yield strength of 29.6 MPa and a Young’s modulus of 1.79 GPa.  
  
## Feature 1  
  
I started designing feature 1 by deciding on dimensions for it. I decided to give it a length of 38 mm and a base of 38 mm while I had to solve for the thickness based on the maximum allowable deflection I was provided.  
  
Next, I wrote down all my known values, unknowns, and assumptions.  
  
<img width="975" height="1070" alt="image" src="https://github.com/user-attachments/assets/e8e63ec6-2ced-4054-ae8d-42c09dcec24c" />  
  
Then I drew a FBD of feature 1, analyzing it as a cantilever beam with an applied moment and force.  
  
<img width="883" height="373" alt="image" src="https://github.com/user-attachments/assets/64cd38ac-412e-4b17-bbe0-80fbe41f78da" />  
  
First, I solved for the moment. Then using the bending stress equation and the equation for maximum deflection of a cantilever beam, I solved for the minimum thickness feature 1 would have to be.  
  
<img width="944" height="745" alt="image" src="https://github.com/user-attachments/assets/616208da-fca7-48ca-9319-03b2c018efd4" />  
  
Solving these equations for thickness gave me values of 9.30 mm and 13.2 mm. Since the deflection requirement required the larger thickness, deflection controlled the design of Feature 1. Therefore, I selected a thickness of 13.2 mm.  
  
## Feature 2  
  
Feature 2 is the vertical portion that attaches the mount to the rigid wall. I made the exposed portion 38 mm tall so the inside dimensions of the bracket form a 38 by 38 mm area. Since Feature 1 is 13.2 millimeters thick, the total height of Feature 2 is 51.2 millimeters.  
  
Additionally, I had to decide on the location of four wall mounting holes. I arranged the holes symmetrically on the exposed 38 by 38 mm area. The holes are 3.4 millimeters in diameter for M3 fastener clearance. Based on the location of the lower bolt holes, the portion of Feature 2 that was considered free to bend was 21 millimeters long.  
  
I began by writing all my known values, unknowns, and assumptions.  
  
<img width="975" height="1023" alt="image" src="https://github.com/user-attachments/assets/8a2b990b-3411-4c38-8f33-9cbb09a6683a" />  

Next, I drew a FBD of feature 2.  
  
<img width="427" height="337" alt="image" src="https://github.com/user-attachments/assets/ba6a9480-a47a-4d18-9691-d4696bff6f6e" />  
  
Feature 2 experiences the same moment as feature 1. Using the same bending stress equation, I calculated a minimum thickness of approximately 9.30 mm based on yielding. The deflection calculation gave approximately 8.88 mm. In this case, the yield requirement controlled, so Feature 2 was designed with a thickness of approximately 9.3 mm.  
  
<img width="703" height="477" alt="image" src="https://github.com/user-attachments/assets/e861d894-b7dc-4fa7-8cd3-37111a6acb71" />  
  
## Isometric Drawing  
  
I sketched the design of the bracket with dimensions, making it easier to model in CAD.  
  
<img width="711" height="597" alt="image" src="https://github.com/user-attachments/assets/71505cb7-973f-4c0b-8650-7f58ba8d5918" />  
  
## CAD  
  
After completing the analytical design, I created the mount in CAD using the calculated dimensions. I added clearance holes for the motor and wall fasteners and added reinforcement features such as ribs near the 90 degree joint. These features increase the stiffness of the bracket and reduce deflection around the connection between Feature 1 and Feature 2.  
  
I started by creating global variables to assign to me dimensions of the model.  
  
<img width="975" height="393" alt="image" src="https://github.com/user-attachments/assets/381dfba5-132f-4c0f-be54-a77da21a261f" />  
  
Then, I created the main portion of the bracket, and extruded it 38 mm.  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/80239f70-c71e-48d3-8338-499a0623bda5" />  
  
The ribs were added for reinforcement. I sketched and extruded one, then used the linear pattern function to place the second rib on the other corner of the model.  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/671ea907-c772-4d4a-8afa-8a08e6254656" />  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/8f593fce-635c-4915-a546-716b9de7ad05" />  
  
Next, the holes for the wall fasteners were symmetrically placed on feature 2 and cut out of the model.  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/49f36932-48a5-4a63-a229-fc03d9e5ecc7" />  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/c364b3a7-09d7-4a0c-92a2-592c0991641e" />  
  
Using the provided dimensions of the motor I modeled and cut out the mounting holes for the motor and a pocket for the motor to rest in.  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/08cd45e7-7620-4d04-9efc-a6886767f589" />  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/2f509e9b-8a0c-4475-a029-17c3bc47fdb0" />  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/02471b28-6e14-4207-9631-94bb3e0704c3" />  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/b28f8193-10c7-42c1-8fc3-574f1e07dfa4" />  
  
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/44db49b0-9f79-4819-8f44-8142d872c53f" />  
  
The indentation in the mount does not feel very correct since I am removing a lot of material. However, If I do not add this pocket for the motor to rest, then the motor shaft will not even stick out of the bottom of the bracket. This design should be altered depending on the specific needs and uses for the motor.  
  
## Lessons Learned  
  
This project taught me how material properties, geometry, and loading conditions all affect the design of a structural component. I learned that meeting the yield-strength requirement does not always mean a design is acceptable, because deflection can control the required dimensions instead. I also learned how simplifying a real bracket into cantilever beam models can make the design easier to analyze before creating the final CAD model.  
  
**I spent approximately 7 hours on this assignment.**  
  
## CAD Files  
  
Motor Mount:  
[Motor_Mount.zip](https://github.com/user-attachments/files/32336335/Motor_Mount.zip)













