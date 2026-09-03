# A2 – Truss Stress Analysis

## Objective  
For this project, I have been tasked with designing light weight planar truss using A500 structural steel or another equivalent. I will be creating free body diagrams, calculating the forces, and determining cross-sectional areas to satisfy load requirements. Additionally, I will be using CAD to model the truss I design and very the calculated weight for the truss and supporting pins.  

The following image was provided as a template to creating my truss:  
  
<img width="716" height="433" alt="image" src="https://github.com/user-attachments/assets/6d47a641-2c66-4eaa-8aa5-0cf8a8963c4f" />  

The unknowns on the initial diagram were given to me. P equals 20 kN, a equals 0.4 meters, b equals 0.3 meters, point A is a pin, and point B is a roller.  

## Analyze
### Truss Structure  
I chose to design my truss in a way I have seen many times in my previous classes. It has the same structure as a Warren Truss. I sketched the shape of the truss, including a new point, E, to fit my design. It contains 3 triangles to give it the best load distribution. Additionally, I labeled the members as x, y, and z to make it easy to identify and calculate each length.  

<img width="975" height="583" alt="image" src="https://github.com/user-attachments/assets/ea09b26d-3385-4701-a504-27a1423256b2" />  

To calculate the values of x, y, and z, I sketched a portion of the truss and applied the Pythagorean theorem and symmetry.  

<img width="975" height="1307" alt="image" src="https://github.com/user-attachments/assets/10ab092f-75fc-44b2-88f2-432d573d21d0" />  

With the truss fully dimensioned, I could begin on a free body diagram.  

### Free Body Diagram  

I sketched the free body diagram with as many dimensions as possible to make the sum of forces and moments calculations easier. I decided to orient my reaction forces at A and B based on the directions of the applied forces. I intuitively assumed By would be down because the force, P, on the left side was pointing up. I followed the same logic for orienting Ay.  

<img width="975" height="654" alt="image" src="https://github.com/user-attachments/assets/518a240e-e2c5-42a3-9d8d-de3caa5c7cb4" />  

Even though I could tell by looking at the free body diagram that the sum of forces would equal 0 in the X direction, I solved for it anyway to keep good habits. Next, I took the sum of forces in the Y direction, which told me the Ay and By values equal each other. Then I calculated the moment about point A. This gave me the value of By in terms of P, which also means I have the value of Ay since the two are equal.  

<img width="975" height="397" alt="image" src="https://github.com/user-attachments/assets/731a1ab6-1a4e-46a3-97fb-a29e68449c02" />  

### Solving Internal Forces  

Once I solved the external forces, it was time to analyze the forces acting in each member. Since the truss was symmetrical, I only had to solve one half and then I would know the other half as well.  

To find the internal forces, I used the method of joints starting at point B. Instead of finding the angles by using arc tangent, I simply used ratios. For example, in joint B, instead of multiplying the force BC by sine or cosine, I went straight to either (opposite/hypotenuse) or (adjacent/hypotenuse). This way I can bypass the angle and just use exactly what the sine or cosine of some angle would have equaled. This was easy to do because I had already calculated the length of every member in the truss.  

<img width="975" height="669" alt="image" src="https://github.com/user-attachments/assets/8d1fc852-bccd-4806-a34b-431371b90615" />  

After calculating the forces BC, BE, CE, and CD, I decided I would solve for the other side of the truss anyway to check my work.  

<img width="975" height="651" alt="image" src="https://github.com/user-attachments/assets/05f67253-a64a-4e63-a1d5-111ce520bb95" />  

Since I always assume each member is in tension when using the method of joints, sometimes the answers come out negative. This is not a problem; it just means the member is in compression and not tension. Once each member was solved symbolically, I plugged in the value of 20 kN for P to get the final values for each member.  

<img width="975" height="333" alt="image" src="https://github.com/user-attachments/assets/f75e3a79-5450-4134-8130-c5d4d519a8cc" />  

### Cross-Sectional Area of the Truss  

Next, I had to calculate the minimum cross-sectional area required for each of the truss elements by using the largest internal force. I was planning on using A500 steel as my material but the CAD I use, SolidWorks, does not have it. Instead, I picked an equivalent steel that was listed in SolidWorks called AISI 4130 steel. I was given a safety factor value of 3.5 and the yield strength and density for AISI 4130 steel was listed in the SolidWorks material properties section.  

<img width="861" height="439" alt="image" src="https://github.com/user-attachments/assets/a9e55535-8359-4a8e-9e6c-7661a89d103d" />  

My largest internal force was 16.04 kN found in the members CE and ED.  

To solve for the only unknown, Area, I used the equations for maximum allowable stress, which is equal to the yield stress divided by the factors of safety, and our general stress equation, force divided by cross-sectional area. I don’t want the stress caused by the largest internal force to be greater than the highest allowable stress because the truss could be damaged and safety would be at risk. This means the stress caused by the largest internal force must be less than the maximum allowable stress. If they are set equal to each other, then I can solve for cross-sectional area and find the minimum value required to keep the truss from failing.  

<img width="975" height="438" alt="image" src="https://github.com/user-attachments/assets/388a9be8-19b2-4e82-9972-9987231ccb0e" />  

This means the minimum cross-sectional area that should support this truss is equal to the factor of safety times the largest internal force divided by the yield strength. Once I plug in my known values, the area comes out to be 122 millimeters squared.  

<img width="975" height="225" alt="image" src="https://github.com/user-attachments/assets/537f79db-1cfb-41e7-94fb-ccb9a29c4929" />  

### Weight of the Truss  

Since I know the density of AISI 4130 steel, I can calculate the approximate weight of the truss. First, I found the mass because I was given SI units. The mass is equal to density times volume and volume is equal to area times length. Before I solve for the mass, I convert my Area and length from millimeters to meters to cancel units out. After I calculate the mass, I use the equation weight equals mass times gravity to find the approximate weight.  

<img width="975" height="471" alt="image" src="https://github.com/user-attachments/assets/f7c0a057-43a6-48c6-99a5-d9dc6c248251" />  

### Cross-Sectional Area of the Pins  

Next, I calculated the cross-sectional area of the connecting pins in the same way I did with the truss to find the required cross-sectional area to withstand the expected shear forces. However, I am given different information about the material for the pins. The pins are made of a hardened tool steel, have a yield shear strength of 170 ksi, and have a density of 0.278 pounds per inch cubed. Additionally, I can assume any elements in compression won’t fail in buckling and I have a safety factor of 4.  

I started by listing all my relevant, known and unknown values and drawing a free body diagram of the joint with the largest reaction load on it.  

<img width="975" height="665" alt="image" src="https://github.com/user-attachments/assets/e4845c3d-5af0-45b7-a3cc-2b739137c2e1" />  

To solve for the minimum required cross-sectional area, I used the same process I used with the truss. However, this time the equations are very slightly different, but they are still functionally the same. The equations are shear force equals the largest reaction load divided by the cross-sectional area and the maximum allowable shear stress equals the yield shear strength divided by factor of safety.  

<img width="975" height="719" alt="image" src="https://github.com/user-attachments/assets/505adda8-09ee-4576-b119-3ff509730dbd" />  

### Weight of the Pins  

To calculate the weight of the pins, I first converted the given density from English units to SI units, and I used the previously calculated cross-sectional area of the pins to calculate the radius of each pin.  

<img width="975" height="305" alt="image" src="https://github.com/user-attachments/assets/bafdff58-f9d2-4f32-8224-f473c752f745" />  

Next, I had to decide on how long I wanted each pin to be. Because my model of the truss is only 2D, I only had to make the pin a little bit longer than the depth of one member. However, I did not know the exact depth of the members, I only knew the area. To find the length of one of the square sides of the truss, I used the equation for the area of a square. I found one side of the truss is approximately 11 millimeters. I then decided to make the pin 13 millimeters long, just slightly longer than the depth of the truss, because I did not want it to be smaller than the hole in the truss. However, I did not want it to stick out too far either because that would make each pin heavier and it would be a waste of materials.  

<img width="975" height="286" alt="image" src="https://github.com/user-attachments/assets/c5fe71eb-f4be-4e21-a04f-e478851116b8" />  

Once I had the radius and the length of the pin, I could into the equation for mass.  

<img width="975" height="464" alt="image" src="https://github.com/user-attachments/assets/d1b66f81-4e1f-4ab9-8d92-824fefa7f07a" />  

Using the calculated mass, I found the weight in Newtons per pin. Then I multiplied the weight per pin by 5 to account for the 5 pins in the truss.  

<img width="975" height="292" alt="image" src="https://github.com/user-attachments/assets/4bf1bd19-0bb3-45c2-b4c9-8a71ebe51c67" />  






















## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._
I chose a warren truss structure because its strong and distributes loads well

## Communicate

