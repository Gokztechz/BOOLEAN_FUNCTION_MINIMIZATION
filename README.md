# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:GOKUL SHARAN R
 RegisterNumber:212223040052
*/
module boolean_top(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule
```
**Output:**
![image](https://github.com/Gokztechz/BOOLEAN_FUNCTION_MINIMIZATION/assets/117667038/49e62d68-8a31-4c7a-ba2c-af6c4149c486)

**RTL realization**
![image](https://github.com/Gokztechz/BOOLEAN_FUNCTION_MINIMIZATION/assets/117667038/6cfe9cab-3ceb-4a73-9a09-d090c1234f4e)

**RTL**
![image](https://github.com/Gokztechz/BOOLEAN_FUNCTION_MINIMIZATION/assets/117667038/114975f9-e118-443b-92f8-3164edcf968b)

**Timing Diagram***
![image](https://github.com/Gokztechz/BOOLEAN_FUNCTION_MINIMIZATION/assets/117667038/3b7704ea-7407-422c-ba83-bb69d0a098df)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

