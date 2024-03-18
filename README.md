# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module boolean_function(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
//type code for f2 as like f1
endmodule
```

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: GANESH.D

RegisterNumber: 212223240035


**RTL realization**
<img width="865" alt="boolean_funct circuit dia" src="https://github.com/Ganesh23013987/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473768/a94715a9-85db-4545-9df9-c842953377ff">

**TRUTH TABLE:**
![image](https://github.com/Ganesh23013987/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473768/4c324af5-5752-441e-985c-e0d313854e06)

**Timing Diagram**
![boolean_function](https://github.com/Ganesh23013987/BOOLEAN_FUNCTION_MINIMIZATION/assets/147473768/6e544e34-68ab-4a25-8161-279bb56bed5a)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

