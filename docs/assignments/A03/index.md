# A3 – Parametric and FEA  

The purpose of this project was to use parametric design and FEA to model a bar which has a circular cross section with given values of the criteria for the material, maximum deflection, load, and diameter. The material had to be Aluminum with a Young’s Modulus range from (8.5 – 11.5) x 106 and an applied direct load had to be chosen between 300 lbf and 500 lbf. Additionally, the max axial deflection of the bar was given to be 0.009 inches, and I had to pick my own diameter.  

<img width="845" height="619" alt="image" src="https://github.com/user-attachments/assets/90d5ce5a-cd6e-44f4-9fb3-13b66263ba01" />  

For the applied load, I chose 400 lbf. For the diameter, I chose 5 inches. And using the SolidWorks material list, I chose 1060 Aluminum Alloy, which has a Young’s Modulus of 10.0 x 106.  

<img width="975" height="800" alt="image" src="https://github.com/user-attachments/assets/500de83c-9cd8-49d7-807c-eaf4db94ea84" />  

I started by writing down my given values, chosen values, and equations I would be using.  
  
<img width="975" height="572" alt="image" src="https://github.com/user-attachments/assets/d9751c33-7f09-4493-8a43-5d276bbe5172" />  
  
Using the direct tension elongation equation, I was able to solve for L and plug in the known values for each of the other variables to find the length of the bar. Solving for the length will help me verify I input my values into SolidWorks correctly next.  
  
<img width="975" height="248" alt="image" src="https://github.com/user-attachments/assets/8fcfa742-5aea-4907-a5b6-09593157e39a" />  
  
### CAD  

Since I had all my variables, I could begin modeling the bar in SolidWorks. I started by creating parameters with all my variables and equations by inputting them as Global Variables. Since the length calculated in SolidWorks matched the length calculated by hand, I knew the Global Variables were correctly set up.  

<img width="975" height="226" alt="image" src="https://github.com/user-attachments/assets/576b42c0-daa5-4800-a78d-48e4ef945c3f" />  

Next, I sketched a circle at the origin in SolidWorks and assigned its diameter to the Global Variable “d”.  

<img width="975" height="1006" alt="image" src="https://github.com/user-attachments/assets/7c5ef0d5-4c86-412d-9d9d-3faf923a8440" />  

Then I went to extrude the circle, I set the extrusion length as the Global Variable “L”.  

<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/4b557d3f-ff66-4573-a73d-f28fb7810d8f" />  

<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/6d2bf90b-9702-4bef-9d2f-87a2038c5410" />  

The bar became very long and required SolidWorks to be zoomed out to see the whole bar in the viewing window. This was annoying to work with because it made it hard to see the surfaces unless the screen was zoomed in a substantial amount. Because I wanted to view the whole bar on the screen with some level of clarity, I decided to change my diameter from 10 inches to 0.5 inches. I picked such a small value because I thought if I made the diameter smaller, the length would also shorten. Because I solved the variables parametrically through SolidWorks, changing the diameter caused all the other dimensions to also change accordingly, including the extrusion.  

<img width="975" height="224" alt="image" src="https://github.com/user-attachments/assets/c7a2b67c-8bab-46dc-b4a2-b74e0e0de664" />  

<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/c44acb34-1d40-4348-9829-1d7b89ad064a" />  

### FEA  

Now that I was satisfied with the clarity of the bar, I began to conduct a FEA on it. First, I assigned a fixed surface on one end of the bar to simulate a welded support. Then at the opposite end of the bar, I applied the direct load of 400 lbf.  

<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/b3760ec2-3ea3-4f39-9316-c458f787e345" />  

<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/b54900f2-75d4-4141-99b7-8bfd69454eed" />  

#### Deflection map  

After applying the fixed surface and direct load, I ran the simulation, which resulted in a deflection value of 0.009. I was not expecting the simulation value to match the given value.  

<img width="975" height="283" alt="image" src="https://github.com/user-attachments/assets/3fd38515-38d5-4953-8da3-c85cb8a32d34" />  

#### von Mises Stress map  

According to the von Mises Stress map, the maximum stress is approximately 2.238 ksi. This is much smaller than the given yield strength of 40 ksi for Aluminum. I calculated an applied safety factor of 17.87.  

<img width="975" height="295" alt="image" src="https://github.com/user-attachments/assets/7adc3f2b-2f27-4c1e-beb4-54744db2ba5c" />  

<img width="975" height="313" alt="image" src="https://github.com/user-attachments/assets/8cd97f00-4d55-4cb3-b98a-8274a2564bd4" />  

### Design Reflection  

The FEA gave me a deflection value of 0.009 inches, which is identical to the given max deflection. I should have expected the two deflections to be essentially the same value because the bar has a simple, uniform geometry with a constant cross-sectional area.  

If I had to choose which deflection result to trust more, I would pick the hand calculations because the bar is very simple and straightforward. The equations I used are functional for a reason. The FEA simulation is an incredibly useful tool, but it is just that.  

Additionally, I had to imagine there was a fairly substantial pin hole on the left side of the bar. Using the stress concentration factor, Kt, for a hole in a flat bar in tension from Peterson’s charts or Machinery’s Handbook, I had to estimate the peak stress at the hole and state whether it would still pass my safety factor. I could not find a value for the stress concentration factor for a whole in a flat bar in tension because I do not have access to Machinery’s Handbook and I could not find Peterson’s charts. Since I could not find the value for Kt, I solved it symbolically.  

From my assumption, as long as the new factor of safety exceeds a value of 1, the bar does not reach aluminum’s yield strength, and it would still pass. I found Kt to be equal to the local max stress (the peak stress at the hole) divided by the nominal stress. I solved the equation for the peak stress at the hole and then plugged it into my equation for the factor of safety. Since the factor of safety must be greater than one, I found that as long as the value of Kt is less than the previous safety factor of 17.87, the peak stress at the hole would still pass my safety factor.  

<img width="975" height="421" alt="image" src="https://github.com/user-attachments/assets/204920c9-6d4b-441f-8fde-1dcde57a1724" />  


### Modifying Design Parameters  

I changed the diameter of the bar to 50 inches and the direct applied force to the maximum in the given range, 500 lbf. Increasing the size of the diameter in the direct tension elongation equation will always increase the length. If I decreased the diameter, then the length would go down. The change in the force will also affect the length. If I increase the force, the length will shorten, and If I decrease the force, the length will grow. In this case, the diameter was increased to 50 inches, and the force was increased to 500 lbf. Both changes counteract each other, but I believe the change in diameter will have a greater effect on the length than the change in force.  

<img width="975" height="225" alt="image" src="https://github.com/user-attachments/assets/20de78e9-ce56-4329-9946-4d929cb6625d" />  

### Time Spent  
I spent approximately 5 hours on this project.  
  
### CAD Files  
  
[MEGR2157_A3_ChrisClade.zip](https://github.com/user-attachments/files/32034178/MEGR2157_A3_ChrisClade.zip)
