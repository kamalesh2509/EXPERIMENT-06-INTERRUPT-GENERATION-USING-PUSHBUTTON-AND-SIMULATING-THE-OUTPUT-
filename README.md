```
Name: E kamalesh
Register Number: 212222100019
```
# EXPERIMENT 07 INTERRUPT GENERATION USING PUSHBUTTON AND SIMULATING THE OUTPUT

### Aim:
To Interface a push button and generate an interrupt , simulate it using an led and simuate it on  proteus 

### Components required:
STM32 CUBE IDE, Proteus 8 simulator .

### Theory:

ARM v7 Core supports multiple great features for handling exceptions and interrupts. Which includes the Nested Vectored Interrupt Controller (NVIC).

Micro-Coded Architecture So that interrupt stacking, entry, and exit are done automatically in hardware. Which offloads this work overhead from the CPU
### Processor Mode

The processor mode can change when exceptions occur. And it can be in one of the following modes:
Thread Mode: Which is entered on reset.
Handler Mode: Which is entered on all other exceptions.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-INTERRUPT-GENERATION-USING-PUSHBUTTON-AND-SIMULATING-THE-OUTPUT-/assets/36288975/4f52f2d6-4cdb-4315-b2b2-b55dc1639c43)
The STM32 ARM microcontroller interrupts are generated in the following manner:

The system runs the ISR and then goes back to the main program. The NVIC and EXTI are configured. The Interrupt Service Routine (ISR) also known as the interrupt service routine handler is defined to enable the external interrupts.

Let us learn about the important features which are needed to configure external interrupts in STM32 microcontrollers

Interrupt Lines (EXTI0-EXTI15)
The STM32 ARM microcontroller features 23 event sources which are divided into two sections. The first section corresponds t external pins on each port which are P0-P15. The second section corresponds to RTC, ethernet, USB interrupts. Therefore, in the first section, we have 16 lines corresponding to line0 till line15. All of these map to a pin number.
The diagram below shows how the GPIO pins are connected to the 16 interrupt lines:

![image](https://github.com/vasanthkumarch/EXPERIMENT-06-INTERRUPT-GENERATION-USING-PUSHBUTTON-AND-SIMULATING-THE-OUTPUT-/assets/36288975/3e1ededb-144c-4103-a64e-9132b7e06e1b)

One important thing to note here is that same number pins are connected to line with the same number. All of these then join to form a single line. Additionally, we can not use two pins one one line at the same time. For example out of PA1, PB1, PC1, PD1, PE1, PF1 and PG1 you can only use a single pin out of all these. This is because they are all connected to the same line EXTI1. However you can use PA1 and PA2 at the same time as they are connected with different lines.

Now each of these lines EXTI0-EXTI15 can be used to trigger an interrupt on different modes of the signal : rising edge, falling edge or rising_falling edge.
## Procedure:
 1. Click on STM 32 CUBE IDE.

 2. Click on FILE, click on new stm 32 project. 

 3. Select the target to be programmed. 

 4. Select the program name. 

 5. Corresponding ioc file will be generated automatically.

 6. Select the appropriate pins as gipo, in or out, USART or required options and configure. 

 7. Click on cntrl+S , automatically C program will be generated.

 8. Edit the program and as per required. 

 9. Select EXIT pin configuration and clock configuration. 

10. Once the project is build, click on debug option.

11. Creating Proteus project and running the simulation.
We are now at the last part of step by step guide on how to simulate STM32 project in Proteus.

12. Create a new Proteus project and place STM32F40xx i.e. the same MCU for which the project was created in STM32Cube IDE. 

13. After creation of the circuit, double click on the the MCU part to open settings. Next to the Program File option, give full path to the Hex file generated using STM32Cube IDE. Then set the external crystal frequency to 8M (i.e. 8 MHz). Click OK to save the changes.

14. Click on debug and simulate using simulation. 
  

## STM 32 CUBE PROGRAM :



## Output screen shots of proteus  :
 
 
 ## CIRCUIT DIAGRAM (EXPORT THE GRAPHICS TO PDF AND ADD THE SCREEN SHOT HERE): 
 
 
## Result :
Interfacing a push button and interrupt genrateion is simulated using proteus 
