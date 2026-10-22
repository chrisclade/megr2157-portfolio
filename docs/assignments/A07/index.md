# A7 – FEA on Bracket

## Objective  
  
The objective of this Project is to take the bracket I have been designing in previous projects and improve its strength and stiffness while minimizing its mass using finite element analysis. Each design iteration of the bracket will be evaluated for maximum stress, displacement, and safety factor while using mesh refinement to check if the results converge within 7%. The results will guide geometrical changes to the bracket through at least three design iterations.  
  
I have been provided with these images during the entire bracket design process and I have been using them to guide my design process as well as my naming convention.  
  
<img width="666" height="419" alt="image" src="https://github.com/user-attachments/assets/8e8c392d-660c-47b1-886c-7c97e7c1dbc5" />  
  
<img width="667" height="575" alt="image" src="https://github.com/user-attachments/assets/e49a2607-fc9a-407f-bc3f-7e70f023d288" />  
  
Additionally, the material previously chosen for the bracket will remain the same throughout this process.  
  
<img width="659" height="792" alt="image" src="https://github.com/user-attachments/assets/10c359be-5b51-4a09-88e8-f66889a65325" />  
  
## Design 1  
  
The first design I tested was the initial bracket I created in previous projects. The results of this will give me an idea of where the brackets weaknesses are and what needs to be changed.  
  
<img width="384" height="322" alt="image" src="https://github.com/user-attachments/assets/7f36cca9-446e-49d5-ad52-6dc8dbd3d798" />  
  
I began by treating the part of the bracket that rests on the T-beam (feature E) as a fixed point because it will maintain constant contact with the beam while the force is being applied.  
  
<img width="975" height="853" alt="image" src="https://github.com/user-attachments/assets/c09a975b-d11a-44cd-ac47-566a8b4c9cab" />  
  
<img width="975" height="929" alt="image" src="https://github.com/user-attachments/assets/819cc26a-9021-43a1-90a1-e1ee1c519b1c" />  
  
As I was applying the force to my bracket. I realized that by default, the force wants to distribute itself across the entire cylindrical surface, even the part that the hypothetical strap would not be touching. To fix this, I made some additional sketches onto the bracket to use as reference geometry to create a split line. This will allow me to apply the force to the only part of the bracket the hypothetical strap should being applying a force to.  
  
<img width="975" height="600" alt="image" src="https://github.com/user-attachments/assets/02e50774-e44d-4879-9259-237de45351cc" />  
  
<img width="975" height="576" alt="image" src="https://github.com/user-attachments/assets/41a9c6f3-48de-4bde-8e09-af78bc34e8c0" />  
  
<img width="975" height="582" alt="image" src="https://github.com/user-attachments/assets/007ea162-4996-4034-b88e-88b7105dee02" />  
  
### Coarse mesh  
  
To begin testing on design 1, I created a coarse mesh and started the computational simulation. I made sure to record the details of each mesh I created in case I needed it later.  
  
<img width="975" height="662" alt="image" src="https://github.com/user-attachments/assets/5e3c02ae-d19c-4d7f-b987-6cdedb12cbe5" />  
  
<img width="744" height="670" alt="image" src="https://github.com/user-attachments/assets/f10be502-5ed8-4969-9251-844f5e36cdaf" />  
  
<img width="975" height="765" alt="image" src="https://github.com/user-attachments/assets/a0700e3d-dc9d-4562-8d54-d7bf00f5b38b" />  
  
<img width="975" height="801" alt="image" src="https://github.com/user-attachments/assets/0169be76-839d-4a5e-82b0-630b62ddcf93" />  
  
<img width="475" height="422" alt="image" src="https://github.com/user-attachments/assets/832355e5-acec-4e5a-890a-f001bd4679fd" />  
  
### Medium mesh  
  
Next, I collected the data and ran the simulation again but with a mesh in between the coarse and fine extremes.  
  
<img width="745" height="672" alt="image" src="https://github.com/user-attachments/assets/78d53c35-9721-4ec4-ae02-d7ccd93f8e7d" />  
  
<img width="975" height="878" alt="image" src="https://github.com/user-attachments/assets/b3f73b0b-9f5b-4c8e-a839-d21b726676fe" />  
  
<img width="975" height="872" alt="image" src="https://github.com/user-attachments/assets/dc3f6e2c-2c33-41f8-9256-16012c8365bb" />  
  
<img width="527" height="413" alt="image" src="https://github.com/user-attachments/assets/63a2366b-ad4f-481d-a69a-11812d7c5017" />  
  
#### Analysis and Interpretation  
  
The maximum stress is around double the yield strength in both the coarse and medium mesh simulations, which immediately tells me this bracket will fail where feature A connects to feature B.  
  
Despite this, I compared the data from the coarse and medium mesh simulations to check if they are converging within 7%. This will let me know if the results depend too much on mesh size and will inform me in the reliability of my geometry.  
  
<img width="822" height="384" alt="image" src="https://github.com/user-attachments/assets/daa09b9a-bbb5-4d0f-b275-0cd976fad2d8" />  
  
Only the deflection was under 7% which means I cannot be completely confident in the data quite yet.  
  
### Fine mesh  
  
Because the data did not converge, I ran the simulation one more time but with a fine mesh.Because the data did not converge, I ran the simulation one more time but with a fine mesh.  
  
<img width="975" height="661" alt="image" src="https://github.com/user-attachments/assets/3d85ea7f-3a57-47b7-bc91-8810035c38fc" />  
  
<img width="745" height="666" alt="image" src="https://github.com/user-attachments/assets/954eb477-138c-4959-bc31-734b1cf8bfa2" />  
  
<img width="975" height="629" alt="image" src="https://github.com/user-attachments/assets/e88b1ced-34b6-45fc-9ad2-1f987ee94399" />  
  
<img width="975" height="611" alt="image" src="https://github.com/user-attachments/assets/b350c577-2b08-44db-91fb-9a3c46759131" />  
  
<img width="563" height="431" alt="image" src="https://github.com/user-attachments/assets/ab8e6544-cf60-4ab0-bf87-910b0e2e4036" />  
  
#### Analysis and Interpretation  
  
The maximum stress got even higher while the deflection did not change much. I would not be confident in using this bracket based on large differences between each kind of mesh.  
  
<img width="491" height="339" alt="image" src="https://github.com/user-attachments/assets/35f09d57-82b6-4c25-b3c4-3b4359da5593" />  
  
Except for the deflection, the differences between the medium mesh and fine mesh was even greater than that of the coarse and medium mesh.  
  
## Design 2  
  
The biggest weakness I gleaned from design 1 was right where feature A and B connect. In order to try and mitigate this weakness I decided to add a fillet at their intersection in an attempt to more evenly distribute the stress into feature B.  
  
<img width="975" height="765" alt="image" src="https://github.com/user-attachments/assets/8dfc826e-eff7-42bd-b909-d2c821f14951" />  
  
<img width="975" height="942" alt="image" src="https://github.com/user-attachments/assets/7b29863e-30f1-485c-a2cc-c9edc27d6f59" />  
  
However, I realized that it will still not be strong enough. A fillet will help reduce stress concentrations but with such a large maximum stress on the previous design, I decided I should do more than add only a fillet. In another attempt to distribute stress concentration and make the bracket more rigid, I also changed feature B to be much larger.  
  
<img width="975" height="974" alt="image" src="https://github.com/user-attachments/assets/1a4b7e53-b359-4e43-9f9d-16a4f7b500b4" />  
  
<img width="975" height="843" alt="image" src="https://github.com/user-attachments/assets/b603c5c2-31b2-450a-96ee-e86c38a4866e" />  
  
<img width="427" height="317" alt="image" src="https://github.com/user-attachments/assets/8112dfe8-f5b5-40c7-85d0-31cd6f7d97d2" />  
  
These geometry changes increased the weight from 1.10 lbs to 1.14 lbs.  
  
### Coarse mesh  
  
<img width="975" height="925" alt="image" src="https://github.com/user-attachments/assets/d52300ba-4869-4688-8e05-8e0888309600" />  
  
<img width="747" height="666" alt="image" src="https://github.com/user-attachments/assets/d93a91b9-1f8b-494e-a87d-ce01b15896e8" />  
  
<img width="975" height="754" alt="image" src="https://github.com/user-attachments/assets/53eec385-4a28-4546-9912-1b998a7ca66c" />  
  
<img width="975" height="834" alt="image" src="https://github.com/user-attachments/assets/ab1fe72e-0a15-4d7e-abfe-6c065b29dc0c" />  
  
<img width="545" height="413" alt="image" src="https://github.com/user-attachments/assets/63c429bd-0b5b-4615-9715-c8eb90fedadd" />  
  
### Medium mesh  
  
<img width="975" height="916" alt="image" src="https://github.com/user-attachments/assets/49ddd370-eba8-4b1b-920b-e2c427ea261c" />  
  
<img width="749" height="670" alt="image" src="https://github.com/user-attachments/assets/63bb046d-2f57-470e-a848-6680e6e31bfc" />  
  
<img width="975" height="836" alt="image" src="https://github.com/user-attachments/assets/5fe11ad7-5d6f-4201-b5ce-b21df240be5b" />  
  
<img width="975" height="903" alt="image" src="https://github.com/user-attachments/assets/6b7b959d-a33c-4307-bc29-b5abfee9b2f8" />  
  
<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/d891be5d-6278-4c11-ba05-06fe87eda8d7" />  
  
#### Analysis and Interpretation  
  
The changes to the geometry, compared to the first design, decreased both the maximum stress and deflection. However, the maximum stress still greatly exceeds the yield strength which tells me this bracket will most likely fail.  
  
However, the data for the coarse and mediums meshes converge within 7%. This tells me that the changes to the geometry were effective and I can have more confidence in the results of the simulation. Because of this, I did not run another simulation with a fine mesh and I moved onto the next design iteration.  
  
<img width="558" height="386" alt="image" src="https://github.com/user-attachments/assets/93866b9f-390d-4cde-b12d-8c4ca5ca7ce3" />  
  
## Design 3  
  
The largest stress concentration for Design 2 was still at the point where features A and B connect at the fillet. To fix this, I increased the radius of the fillet from 0.1in to 0.2in to try and distribute the stress even further. Additionally, I noticed there was little to no stress around features C and E. Because of this, I decided to place large fillets of radius 0.4in at a few points on the bracket in order to cut down on material mass and offset the added weight from the increased size of feature B.  
  
<img width="975" height="975" alt="image" src="https://github.com/user-attachments/assets/46d235d4-560a-4b74-8c73-a35ffcc4fd74" />  
  
<img width="975" height="931" alt="image" src="https://github.com/user-attachments/assets/b989c9bb-e0c4-48ee-8f78-0e5b5bf7ac81" />  
  
I believe I could take off more material to further decrease the weight but I have to know when to stop optimizing and for the purpose of this project, I believe this is enough.  
  
<img width="428" height="327" alt="image" src="https://github.com/user-attachments/assets/b23493ae-64ea-4697-bcb2-b9f9ce156f5a" />  
  
The removal of material was effective because the weight dropped from 1.14 lbs to 1.07 lbs, which is a little bit lighter than design 1 as well.  
  
### Coarse mesh  
  
<img width="975" height="751" alt="image" src="https://github.com/user-attachments/assets/9eff2fa8-9cd4-4bc7-82b5-2c20f0d157e2" />  
  
<img width="747" height="669" alt="image" src="https://github.com/user-attachments/assets/53ed4de2-1bea-40aa-9be7-5e278ebf131b" />  
  
<img width="975" height="807" alt="image" src="https://github.com/user-attachments/assets/5959ebac-1314-4401-b0bd-aa1552a159b7" />  
  
<img width="975" height="812" alt="image" src="https://github.com/user-attachments/assets/1f8c1acb-978b-457f-8261-4eebc8a263a0" />  
  
<img width="475" height="416" alt="image" src="https://github.com/user-attachments/assets/f9915610-92fb-44d6-be67-16267a3d5a25" />  
  
### Medium mesh  
  
<img width="975" height="900" alt="image" src="https://github.com/user-attachments/assets/5bae1861-40bf-4e83-bca4-88b3d6e2b471" />  
  
<img width="749" height="670" alt="image" src="https://github.com/user-attachments/assets/861a1e25-6968-4589-bfd2-574fc0a42699" />  
  
<img width="975" height="781" alt="image" src="https://github.com/user-attachments/assets/f346ca53-9c19-4b01-824c-a39b05b07665" />  
  
<img width="975" height="878" alt="image" src="https://github.com/user-attachments/assets/9c09f066-b823-4780-9d2a-3bc1247d077a" />  
  
<img width="511" height="420" alt="image" src="https://github.com/user-attachments/assets/c6a33ba8-7202-418d-af76-2a5e94048dbe" />  
  
#### Analysis and Interpretation  
  
<img width="492" height="341" alt="image" src="https://github.com/user-attachments/assets/1d666582-f9c1-4537-94a4-f032c95a2849" />  
  
The maximum stress is now below the yield strength, and the deflection has gotten even smaller. Additionally, this is the first time the safety factor has been greater than 1. The design changes made a large difference, but the convergence is still just outside of 7%. In order to be fully comfortable with this design, I decided to run the simulation with a fine mesh to see if the convergence would go below 7%.  
  
### Fine mesh  
  
<img width="975" height="945" alt="image" src="https://github.com/user-attachments/assets/266cb2f5-bf03-402a-946b-07cfe7954f81" />  
  
<img width="747" height="670" alt="image" src="https://github.com/user-attachments/assets/eb825a6e-1191-41e0-a267-9bbb7c7dcc9d" />  
  
<img width="975" height="764" alt="image" src="https://github.com/user-attachments/assets/f3ad78af-ce99-4e27-8bce-84251eaf3b12" />  
  
<img width="975" height="830" alt="image" src="https://github.com/user-attachments/assets/d7489707-a142-48c3-95b1-8b7cf14ee5c4" />  
  
<img width="594" height="419" alt="image" src="https://github.com/user-attachments/assets/d7a3712f-f530-4f6d-b6e7-3742b8f481b4" />  
  
#### Analysis and Interpretation  
  
<img width="548" height="361" alt="image" src="https://github.com/user-attachments/assets/83615b66-7f5b-429a-9482-65a4ff8576e6" />  
  
The convergence did drop below 7% which means the geometry changes were successful and my design meets the project’s tolerance. With even more design iterations, the bracket could become lighter and stronger but I have reached a point where I am comfortable with this bracket design.  
  
## Reflection  
  
I learned that material placement and smooth transitions between features can play a much larger role than it seems. For example, from design 2 to design 3, the only strength related changes I made was increasing the fillet by 0.1 inches. However, this small change was enough to bring the max stress down by roughly a factor of 5.  
  
I also learned that checking mesh convergence helps ensure that my design decisions are based on stable simulation results. This will give me a lot more confidence going forward whenever I am creating more simulations.  
  
<img width="975" height="568" alt="image" src="https://github.com/user-attachments/assets/9ce630d5-738e-4399-847f-601d05a64e81" />  
  
# 2157 Students Only - Finite Element Method  
  
## Design 1  
  
I followed the same exact process for designing this link as I did for the bracket.  
  
I decided to treat the hole that attaches to the bracket as a fixed point since it will be in tension from the applied force. Then I applied the 600 lbf to the opposite hole. I only used half of the cylindrical surface in each hole, similar to what I did with the bracket. I believe this will provide me with the most realistic distribution of forces.  
  
<img width="975" height="1028" alt="image" src="https://github.com/user-attachments/assets/6db05ad0-1d5b-41ac-bc32-0c1d8cf851ca" />  
  
<img width="975" height="998" alt="image" src="https://github.com/user-attachments/assets/458b3a36-dd7b-40b1-b3ac-e654439727dd" />  
  
<img width="975" height="1269" alt="image" src="https://github.com/user-attachments/assets/d6549634-bc1b-453c-a673-36744577416b" />  
  
<img width="894" height="1088" alt="image" src="https://github.com/user-attachments/assets/62abb4b2-69d0-4de8-8919-540f42755604" />  
  
<img width="392" height="322" alt="image" src="https://github.com/user-attachments/assets/f3b44eae-7ac2-4821-ac7c-c47b35eb382e" />  
  
### Coarse mesh  
  
<img width="975" height="1157" alt="image" src="https://github.com/user-attachments/assets/3c5eb86a-e3ad-47b6-9672-fa53c0cdb3cb" />  
  
<img width="747" height="667" alt="image" src="https://github.com/user-attachments/assets/a8a33913-2ee4-4765-8798-07f7ced4ace7" />  
  
<img width="975" height="936" alt="image" src="https://github.com/user-attachments/assets/8b6d7993-d878-4640-afb5-f9da947a1686" />  
  
<img width="975" height="1001" alt="image" src="https://github.com/user-attachments/assets/a8e4cdbf-e7b4-4bb5-9803-94e6a2191d13" />  
  
### Medium mesh  
  
<img width="975" height="1293" alt="image" src="https://github.com/user-attachments/assets/3d26e571-701e-44fe-b54f-1578e3102e0a" />  
  
<img width="752" height="673" alt="image" src="https://github.com/user-attachments/assets/246830df-58c0-4a2e-8826-6d1007cc8a54" />  
  
<img width="975" height="994" alt="image" src="https://github.com/user-attachments/assets/68d98d12-72fe-40b4-9447-406b5bdd0454" />  
  
<img width="975" height="946" alt="image" src="https://github.com/user-attachments/assets/4411f766-be24-4d52-955a-d34999743f17" />  
  
#### Analysis and Interpretation  
  
<img width="975" height="678" alt="image" src="https://github.com/user-attachments/assets/eaa2b4bd-9201-41ad-b15a-0ca087b21bff" />  
  
The initial simulation did not give much feedback. The max stress is already less than half of the yield strength. The safety factor is greater than 1, the deflection is very minimal, and they converge well under 7%. There is not much room to improve on this design but I am going to attempt it.  
  
## Design 2  
  
The largest deflection was at the load bearing hole. I decided to put more material around it and add a 4in fillet in order to try and minimize deflection.  
  
<img width="975" height="1056" alt="image" src="https://github.com/user-attachments/assets/4b9a6431-e47e-48a9-95fe-e3480bc3be63" />  
  
<img width="975" height="1133" alt="image" src="https://github.com/user-attachments/assets/43c314e9-5b3f-4fb9-a363-de2dc4e8fa61" />  
  
<img width="975" height="1039" alt="image" src="https://github.com/user-attachments/assets/e3a9d449-ebb3-4b6a-856c-d3bc145ab365" />  
  
<img width="384" height="320" alt="image" src="https://github.com/user-attachments/assets/f2b1b9b2-5c42-4876-b166-2b59a44edf84" />  
  
This change added 0.05 pounds to the link.  
  
### Coarse mesh  
  
<img width="975" height="1160" alt="image" src="https://github.com/user-attachments/assets/a1cbf2b9-430b-43fb-bd40-04e7725f23ee" />  
  
<img width="749" height="666" alt="image" src="https://github.com/user-attachments/assets/3200c107-475c-4f4d-a9ac-bb939931ee4e" />  
  
<img width="975" height="962" alt="image" src="https://github.com/user-attachments/assets/47c2d1c5-175e-4f55-b46e-ba9b18d8a41f" />  
  
<img width="975" height="1056" alt="image" src="https://github.com/user-attachments/assets/3fb7a1f6-869b-4da1-8c1e-1c9214331948" />  
  
### Medium mesh  
  
<img width="975" height="1045" alt="image" src="https://github.com/user-attachments/assets/568296a0-9726-41cf-b902-1f3c3d2e71e4" />  
  
<img width="750" height="670" alt="image" src="https://github.com/user-attachments/assets/a82fa7cc-65b1-4166-a60e-f6948a9807d9" />  
  
<img width="975" height="1006" alt="image" src="https://github.com/user-attachments/assets/40def1f0-32d3-404c-8327-464497eea131" />  
  
<img width="975" height="1084" alt="image" src="https://github.com/user-attachments/assets/742a0488-0105-40f7-8480-547ec46ecad4" />  
  
#### Analysis and Interpretation  
  
<img width="975" height="570" alt="image" src="https://github.com/user-attachments/assets/3d977444-08c2-4968-8e2c-749ed440a12f" />  
  
The simulation results for the coarse mesh make it seem like the changes in geometry were effective. However, there was a very large convergence for the max stress and safety factor but I did manage to minimize the deflection more. The large changes between the coarse and medium meshes are signs that the data is not stable and should not be trusted yet. I decided to run the simulation again with fine mesh.  
  
### Fine mesh  
  
<img width="975" height="1180" alt="image" src="https://github.com/user-attachments/assets/e5ba3761-ee49-4c5f-8393-bc27e6b97919" />  
  
<img width="749" height="663" alt="image" src="https://github.com/user-attachments/assets/b0372021-650b-4048-b492-a16cd8af1121" />  
  
<img width="975" height="1057" alt="image" src="https://github.com/user-attachments/assets/7e7af3bd-1b5f-4e5e-9f02-820f569b69ef" />  
  
<img width="975" height="1051" alt="image" src="https://github.com/user-attachments/assets/003e1433-eb4f-4ef8-9334-2f7d9445c2c8" />  
  
#### Analysis and Interpretation  
  
<img width="625" height="711" alt="image" src="https://github.com/user-attachments/assets/238e5f47-6bcc-4058-89e1-79ec8232d69b" />  
  
Despite the convergence percentage getting smaller, the data is still too unstable to trust.  
  
## Design 3  
  
The highest stress concentration is in the hole attached to the bracket. I believe the best way to modify this would be to remove unnecessary material to cut down on weight. So, I cut out part of the link closer to the bracket side since the stress concentration and deflection are low in that area. Then I applied a 2in fillet to each of the new edges.  
  
<img width="975" height="1206" alt="image" src="https://github.com/user-attachments/assets/0c636348-cdfb-43a8-a0e0-16e622a621a2" />  
  
<img width="975" height="1096" alt="image" src="https://github.com/user-attachments/assets/f8a75ced-668d-42d6-bdd6-5121ff55f208" />  
  
<img width="394" height="327" alt="image" src="https://github.com/user-attachments/assets/006c920a-04e4-47e1-b4e8-3756820fa949" />  
  
The mass decreased by 0.04 lbs making it only 0.01 lbs heavier than design 1.  
  
### Coarse mesh  
  
<img width="975" height="1153" alt="image" src="https://github.com/user-attachments/assets/168f9f8a-0a74-484d-ad48-3d96e625bba8" />  
  
<img width="749" height="669" alt="image" src="images/link-design-3-102.png" />  
  
<img width="975" height="1033" alt="image" src="images/link-design-3-103.png" />  
  
### Medium mesh  
  
<img width="975" height="1302" alt="image" src="images/link-design-3-104.png" />  
  
<img width="753" height="666" alt="image" src="images/link-design-3-105.png" />  
  
<img width="975" height="1103" alt="image" src="images/link-design-3-106.png" />  
  
#### Analysis and Interpretation  
  
<img width="975" height="587" alt="image" src="images/link-design-3-107.png" />  
  
The convergence percentage is still not as good as it was in the first design, but there are improvements from the second design. Since it is not under 7% I decided to run the simulation again with a fine mesh.  
  
### Fine mesh  
  
<img width="975" height="1265" alt="image" src="images/link-design-3-108.png" />  
  
<img width="750" height="667" alt="image" src="images/link-design-3-109.png" />  
  
<img width="975" height="1137" alt="image" src="images/link-design-3-110.png" />  
  
<img width="975" height="1079" alt="image" src="images/link-design-3-111.png" />  
  
#### Analysis and Interpretation  
  
<img width="612" height="717" alt="image" src="images/link-design-3-112.png" />  
  
The fine mesh simulation made the results more unstable. I am not entirely sure where I went wrong in this design or why the results are so inconsistent. However, the first design meets the projects tolerances and gives stable results with convergence percentages under 7%. Because of this, I am going to scrap the new design and stay with my original because it seems to be the most effective.  
  
## Reflection  
  
My bracket design got better with each design change while my linkage got worse. This taught me that the design process is not easy and it takes time. Just because one part of the design process goes smoothly does not mean the rest will.  
  
<img width="975" height="577" alt="image" src="images/link-design-3-113.png" />  
  
## CAD FILES  
  
## HOW LONG THIS TAKE?  
  

## Analyze


## Decide


## Communicate
