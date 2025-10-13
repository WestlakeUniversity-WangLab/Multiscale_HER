# Contiunnm Transport Model
This repository contains a COMSOL tutorial to reproduce the models in the article "Toward Rational Understanding of the Hydrogen Evolution Polarization Curves Through Integrating Ab Initio Simulations and Mass Transport Effects"

## The function of the GMPNP model
modeling the mass transpport effect on HER in a rotation disk electrode (RDE, 1600rpm) in the pH=1 solution containing 0.1M NaClO₄

## Mathematical description of model

Geometry(1D) and Governing Equation
![boundarylayer](https://github.com/user-attachments/assets/f98ad924-1e34-48f3-a7a9-6fb587e068f2)

## COMSOL tutorial for building Contiunnm Transport Model
### 1.Bulid the framwork of Model
click "Model Wizard".

<img width="720" height="582" alt="图片1" src="https://github.com/user-attachments/assets/2aae75d3-4798-4b5a-841c-15be91268d91" />

select "1D".

<img width="928" height="720" alt="图片2" src="https://github.com/user-attachments/assets/fd431681-ccb6-4d64-80d3-2db5ca2bcb3f" />

Add "Tertiary Current Distribution, Nernst-Planck (tcd)”, click "Study".

<img width="542" height="399" alt="图片3" src="https://github.com/user-attachments/assets/3c624133-ec4f-415c-a5de-3647d5ab2dfd" />

select "Stationary", then click "Done".

<img width="912" height="398" alt="图片4" src="https://github.com/user-attachments/assets/bc61ae15-17f9-43ef-b8b3-801906a5a37d" />

### 2.Import parameters
The parameter can be seen in file "para_pH_1.txt".

<img width="1280" height="720" alt="图片5" src="https://github.com/user-attachments/assets/769d2d13-1587-40dd-9565-7810477ae48f" />

### 3.Import variables

<img width="2000" height="979" alt="图片6" src="https://github.com/user-attachments/assets/20c8e482-a255-4e88-b35d-63324b8ceee6" />

### 4.Build geometry

<img width="2003" height="1100" alt="图片7" src="https://github.com/user-attachments/assets/30ee1654-e868-4319-9858-c2e52b75e785" />

### 5.Input charge number

<img width="1300" height="1097" alt="图片8" src="https://github.com/user-attachments/assets/282aacfa-e6d0-403c-81a9-52cc383ed7ca" />

### 6.Build NP equation

Define the diffusion, ionization, convection, and water ionization equilibrium equations within the system.
<img width="1027" height="1134" alt="图片9" src="https://github.com/user-attachments/assets/f7e4bbde-3dd1-4927-8f94-08fd9c2ed6c9" />

### 7.Input initial value.

<img width="1265" height="628" alt="图片10" src="https://github.com/user-attachments/assets/de5e6cd3-cb90-4405-ba84-990386fd54d3" />

### 8.build "Elctrode Surface".

<img width="2000" height="701" alt="图片11" src="https://github.com/user-attachments/assets/5acf0e04-e1b8-4c32-b7e5-b12b32ea726a" />

### 9.Define "Elctrode Reaction" in "Elctrode Surface".

The "Local current density" is calculated by MKM.

<img width="1185" height="1125" alt="图片12" src="https://github.com/user-attachments/assets/8b3ea34c-22ca-403b-b3a0-d58cff71f5be" />

### 10.Input the concentration of bulk solution.

<img width="2000" height="793" alt="图片13" src="https://github.com/user-attachments/assets/92a2b9fc-ecd0-4961-82af-01bfc279a3a3" />

### 11.Define "Elctrolyte Potential".

<img width="2000" height="843" alt="图片14" src="https://github.com/user-attachments/assets/0f3938ff-777a-4277-aa42-e97f1ae8d64c" />

### 12.set mesh

<img width="1306" height="755" alt="图片15" src="https://github.com/user-attachments/assets/664da195-0c4d-4b40-8629-79b7305db33c" />

select "Distribution"

<img width="716" height="609" alt="图片16" src="https://github.com/user-attachments/assets/56d9e43a-e01a-43b1-b674-bd7c631014b4" />


<img width="716" height="609" alt="图片16" src="https://github.com/user-attachments/assets/bdc6ce2a-bbb4-485c-af64-fd87673b6ef9" />

### 13.Data output

<img width="1420" height="1125" alt="图片18" src="https://github.com/user-attachments/assets/8a63b8a8-fe1a-44c2-9c33-4385d93647ab" />

