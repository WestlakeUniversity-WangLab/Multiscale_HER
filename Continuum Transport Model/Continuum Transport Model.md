# Contiunnm Transport Model
This repository contains a COMSOL tutorial to reproduce the models in the article "Toward Rational Understanding of the Hydrogen Evolution Polarization Curves Through Integrating Ab Initio Simulations and Mass Transport Effects"

## The function of the GMPNP model
modeling the mass transpport effect on HER in a rotation disk electrode (RDE, 1600rpm) in the pH=1 solution containing 0.1M NaClO₄

## Mathematical description of model

Geometry(1D) and Governing Equation
![boundarylayer](https://github.com/user-attachments/assets/310c5df8-3578-40c5-87ae-d4e4008ff815)


## COMSOL tutorial for building Contiunnm Transport Model
### 1.Bulid the framwork of Model
click "Model Wizard".

<img width="720" height="582" alt="图片1" src="https://github.com/user-attachments/assets/b9cefdd8-ae78-4e9d-b088-55be112fde9a" />

select "1D".

<img width="928" height="720" alt="图片2" src="https://github.com/user-attachments/assets/41307490-53a9-4703-8d62-b0f5f2fcd600" />

Add "Tertiary Current Distribution, Nernst-Planck (tcd)”, click "Study".

<img width="542" height="399" alt="图片3" src="https://github.com/user-attachments/assets/8e3a6bab-ad11-4bc2-b7ad-05b680b0c251" />

select "Stationary", then click "Done".

<img width="912" height="398" alt="图片4" src="https://github.com/user-attachments/assets/4187d2e2-6706-44e4-8218-dd63a32319c4" />

### 2.Import parameters
The parameter can be seen in file "para_pH_1.txt".

<img width="1280" height="720" alt="图片5" src="https://github.com/user-attachments/assets/a33de477-e877-4a7e-bf0a-b59b95e8d4e9" />

### 3.Import variables

<img width="2000" height="979" alt="图片6" src="https://github.com/user-attachments/assets/6602647d-5c12-42bf-a808-9bfc4b73febf" />

### 4.Build geometry

<img width="2003" height="1100" alt="图片7" src="https://github.com/user-attachments/assets/d9c6ee2b-3f10-4583-b851-7abee42246c4" />

### 5.Input charge number

<img width="1300" height="1097" alt="图片8" src="https://github.com/user-attachments/assets/dc6eb312-d3bc-4a2a-ba91-80ad437516b8" />

### 6.Build NP equation

Define the diffusion, ionization, convection, and water ionization equilibrium equations within the system.
<img width="1027" height="1134" alt="图片9" src="https://github.com/user-attachments/assets/4503f0c2-1f98-4362-90f0-4a974d4eedd5" />

### 7.Input initial value.

<img width="1265" height="628" alt="图片10" src="https://github.com/user-attachments/assets/3dc4f8d8-3826-4722-8aaa-86ec86d067e5" />

### 8.build "Elctrode Surface".

<img width="2000" height="701" alt="图片11" src="https://github.com/user-attachments/assets/a044f2df-6fc9-4de8-8fd3-283cb1c076a2" />

### 9.Define "Elctrode Reaction" in "Elctrode Surface".

The "Local current density" is calculated by MKM.

<img width="1185" height="1125" alt="图片12" src="https://github.com/user-attachments/assets/1a7d3a16-660d-4351-89ae-de9885eda661" />

### 10.Input the concentration of bulk solution.

<img width="2000" height="793" alt="图片13" src="https://github.com/user-attachments/assets/25fb9a2e-3368-42dc-a88f-48ecb625339f" />

### 11.Define "Elctrolyte Potential".

<img width="2000" height="843" alt="图片14" src="https://github.com/user-attachments/assets/0303b265-6640-48fd-a5e0-fd222c2ae133" />

### 12.set mesh

<img width="1306" height="755" alt="图片15" src="https://github.com/user-attachments/assets/f509f31a-0f2e-4495-ad67-2dfb6afc2f31" />

select "Distribution"

<img width="716" height="609" alt="图片16" src="https://github.com/user-attachments/assets/1043e5cb-4e6e-43cb-8bf1-3cb16dfb6a50" />

<img width="1482" height="918" alt="图片17" src="https://github.com/user-attachments/assets/af02e9eb-8617-489b-a510-e7a70855b685" />

### 13.Data output

<img width="1420" height="1125" alt="图片18" src="https://github.com/user-attachments/assets/fa1f0734-932d-4df3-9ea0-0904d42633a7" />

