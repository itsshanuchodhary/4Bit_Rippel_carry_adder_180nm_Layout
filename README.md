# 4Bit_Rippel_carry_adder_180nm_Layout
Layout of 4bit Ripple Carry Adder formed using CMOS logic in gpdk180nm technology node done in Cadence Virtuoso with no DRC and LVS errors.

# 4bit Ripple Carry Adder (RCA)
A 4-bit Ripple Carry Adder (RCA) is formed using four 1-bit Full Adders cascaded in a series connection with the Carry out of one stage acting as Carry in to another stage. A 4-bit Ripple Carry Adder (RCA) is used to calculate the binary addition of two 4bit binary numbers. Since it is made using four 1-bit Full Adders, a 4-bit RCA has 8 inputs namely (A0 B0,………A3B3) and 4 Sum outputs namely (S0,…..S3) and a single Carry in as (Cin) to the adder at first stage and a single Carry out as (Cout) from the final stage in the adder chain
<img width="357" height="200" alt="image" src="https://github.com/user-attachments/assets/4bb744ee-c7f6-4677-beb4-76331149932a" />

Fig 1: Adding two 4bit numbers.

# Ripple Carry Adder formed using CMOS logic
Since we know that, to form a 4bit RCA we require four 1bit Full Adders. To make Full Adders we require Half Adders. Furthermore Half Adders can be made with simple Logic Gates. In this section, I will be showing how to make these components leading upto a 4bit RCA in gpdk 180nm technology node using CMOS logic.

# Half Adder
A half adder is a simple digital circuit used to add two binary numbers. It contains two outputs, namely Carry (C) and Sum (S), and two inputs, as A and B, denoting the two bits to be added. XOR and AND gates are two common logic gates that can be used to create the half adder.

<img width="412" height="92" alt="image" src="https://github.com/user-attachments/assets/933b475c-3294-4848-ab6a-0939ef059f74" />

Fig 2: Boolean Expression for Sum and Carry output of a Half Adder.

<img width="447" height="221" alt="image" src="https://github.com/user-attachments/assets/55fdc110-d2f3-4062-84f6-07c58348935f" />

Fig 3: Truth Table of a Half Adder.

<img width="992" height="639" alt="image" src="https://github.com/user-attachments/assets/88452ae2-70ef-4ffd-880b-424a2452205c" />

Fig 4: Schematic of a Half Adder.

**1bit Full Adder**
A 1-bit Full Adder is formed using two Half Adders cascaded in series with each other and an OR gate. It takes in three 1-bit inputs namely A, B, Cin and performs the binary addition to give Sum and Carry output (Cout) from these three bits.

<img width="255" height="61" alt="image" src="https://github.com/user-attachments/assets/bdce523d-2905-4628-b794-5539cbce4eff" />

Fig 5: Boolean Expression for Sum output of a 1bit Full Adder.

<img width="457" height="83" alt="image" src="https://github.com/user-attachments/assets/4b8b084d-2573-411d-8e6f-67db8e4e0442" />

Fig 6: Boolean Expression for Carry output of a 1bit Full Adder.

<img width="716" height="466" alt="image" src="https://github.com/user-attachments/assets/48923dd5-9573-4a62-b0a9-7afa3f0550ba" />

Fig 7: Truth Table of a 1bit Full Adder.

<img width="1569" height="536" alt="image" src="https://github.com/user-attachments/assets/9e19390e-17fd-42dd-b3f6-72a26e3e1cd8" />

Fig 8: Schematic of a 1bit Full Adder.


**4bit RCA
<img width="1580" height="432" alt="image" src="https://github.com/user-attachments/assets/0ba50b3c-f6fd-4b75-8fc9-08e604bcfad5" />

Fig 9: Schematic of a 4bit Ripple Carry Adder.

<img width="973" height="558" alt="image" src="https://github.com/user-attachments/assets/4214b7cd-d129-4d74-b682-5e50d73b1f83" />

Fig 10: Waveform of a 4bit Ripple Carry Adder.

# Layout
In this section, I will demonstrate how to construct the layout for a 4-bit Ripple Carry Adder (RCA). The process begins with creating the layouts for the individual components that make up the 4-bit RCA, specifically the Half Adders and Full Adders. Additionally, designing the layouts for the Half Adders and Full Adders necessitates constructing the layouts for the various logic gates involved in making of these adders. A maximum of two metal layers (metal 1 and metal 2) are used to form the connections (routes) for our design.

**Layout - Inverter (CMOS logic)

<img width="288" height="719" alt="image" src="https://github.com/user-attachments/assets/831ba550-0b7a-48ab-85ae-4222fb92c7fa" />

Fig 11: Layout of an Inverter.


**Layout - AND Gate (CMOS logic)
<img width="584" height="716" alt="image" src="https://github.com/user-attachments/assets/69469b9c-32bb-4b69-b3eb-2345ab15815f" />

Fig 12: Layout of an AND Gate.

**Layout - XOR Gate (CMOS logic)

<img width="861" height="724" alt="image" src="https://github.com/user-attachments/assets/140478f5-74aa-4bee-9739-6bcdcd43ac9b" />

Fig 13: Layout of a XOR Gate.


**Layout - OR Gate (CMOS logic)
<img width="580" height="708" alt="image" src="https://github.com/user-attachments/assets/0054deee-fd94-4f7e-8309-1fa68e8520e3" />

Fig 14: Layout of a OR Gate.


**Layout - Half Adder (CMOS logic)**
Since we know, to form a half adder requires a XOR and an AND gate. Similarly, we can can instantiate the layouts of these individual components to form the layout for a half adder.

<img width="1359" height="717" alt="image" src="https://github.com/user-attachments/assets/a0e15c19-fa1c-4a14-8380-0fec6e2f832f" />

Fig 15: Layout of a Half Adder.


**Layout - 1bit Full Adder (CMOS logic)
A 1bit full adder requires 2 half adders and an OR gate. We'll instantiate these already formed components to form a 1bit full Adder. Remember additional routing is to be done to connect these components of the FA

<img width="1585" height="348" alt="image" src="https://github.com/user-attachments/assets/f8a95222-7c41-4e28-bf41-a75a3f730073" />

Fig 15: Layout of a 1bit Full Adder.


**Layout - 4bit RCA (CMOS logic)
A 4bit RCA requires four 1bit Full adders connected in series (cascade fashion). We will instantiate them and connect the carry outs to carry in of the successive 1bit FA to form a 4bit RCA.

<img width="893" height="721" alt="image" src="https://github.com/user-attachments/assets/fcaea13c-fd02-4d05-b030-b4158586470a" />

Fig 15: Layout of a 4bit RCA.


# DRC and LVS checks
Our 4bit RCA layout is meets all the design rules specified for gpdk 180nm technology node and also meets the LVS requirements.

<img width="501" height="520" alt="image" src="https://github.com/user-attachments/assets/f0cde8b8-dc8d-4c43-b06d-53f3b6c717aa" />

Fig 16: DRC for 4bit RCA.

<img width="1316" height="721" alt="image" src="https://github.com/user-attachments/assets/dfd55f56-1600-4080-bcad-44353403ce49" />

Fig 17: LVS check (1/2) for 4bit RCA.

<img width="1337" height="764" alt="image" src="https://github.com/user-attachments/assets/31fd112a-d70e-4202-92fd-d707d883ffae" />

Fig 17: LVS check (2/2) for 4bit RCA.


Note: All of these design or layout are performed in Cadence Virtuoso design tool. Cadence Assura tool is used for DRC and LVS checks for layout in gpdk 180nm library. Widths of PMOS's are kept 2x the width of NMOS's.
