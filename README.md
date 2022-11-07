# Experiment--05-4X4-keypad-interface-with-LPC2148

Name :

Roll no :

Date of experiment :

 
### Interfacing a 4X4 keypad LPC2148 ARM 7 Microcontroller 

## Aim: To Interface 4x4 keypad interface  LPC2148 ARM 7 and write a code for displaying the inputs on a 16x2 lcd 
## Components required: Proteus ISIS professional suite, Kiel μ vision 5 Development environment 
## Theory 
The full form of an ARM is an advanced reduced instruction set computer (RISC) machine, and it is a 32-bit processor architecture expanded by ARM holdings. The applications of an ARM processor include several microcontrollers as well as processors. The architecture of an ARM processor was licensed by many corporations for designing ARM processor-based SoC products and CPUs. This allows the corporations to manufacture their products using ARM architecture. Likewise, all main semiconductor companies will make ARM-based SOCs such as Samsung, Atmel, TI etc.

What is an ARM7 Processor?
ARM7 processor is commonly used in embedded system applications. Also, it is a balance among classic as well as new-Cortex sequence. This processor is tremendous in finding the resources existing on the internet with excellence documentation offered by NXP Semiconductors. It suits completely for an apprentice to obtain in detail hardware & software design implementation.
LPC2148 Microcontroller
 The LPC2148 microcontroller is designed by Philips (NXP Semiconductor) with several in-built features & peripherals. Due to these reasons, it will make more reliable as well as the efficient option for an application developer. LPC2148 is a 16-bit or 32-bit microcontroller based on ARM7 family.
Features of LPC2148
The main features of LPC2148 include the following.
•	The LPC2148 is a 16 bit or 32 bit ARM7 family based microcontroller and available in a small LQFP64 package.
•	ISP (in system programming) or IAP (in application programming) using on-chip boot loader software.
•	On-chip static RAM is 8 kB-40 kB, on-chip flash memory is 32 kB-512 kB, the wide interface is 128 bit, or accelerator allows 60 MHz high-speed operation.
•	It takes 400 milliseconds time for erasing the data in full chip and 1 millisecond time for 256 bytes of programming.
•	Embedded Trace interfaces and Embedded ICE RT offers real-time debugging with high-speed tracing of instruction execution and on-chip Real Monitor software.
•	It has 2 kB of endpoint RAM and USB 2.0 full speed device controller. Furthermore, this microcontroller offers 8kB on-chip RAM nearby to USB with DMA.
•	One or two 10-bit ADCs offer 6 or 14 analogs i/ps with low conversion time as 2.44 μs/ channel.
•	Only 10 bit DAC offers changeable analog o/p.
•	External event counter/32 bit timers-2, PWM unit, & watchdog.
•	Low power RTC (real time clock) & 32 kHz clock input.
•	Several serial interfaces like two 16C550 UARTs, two I2C-buses with 400 kbit/s speed.
•	5 volts tolerant quick general purpose Input/output pins in a small LQFP64 package.
•	Outside interrupt pins-21.
•	60 MHz of utmost CPU CLK-clock obtainable from the programmable-on-chip phase locked loop by resolving time is 100 μs.
•	The incorporated oscillator on the chip will work by an exterior crystal that ranges from 1 MHz-25 MHz
•	The modes for power-conserving mainly comprise idle & power down.
•	For extra power optimization, there are individual enable or disable of peripheral functions and peripheral CLK scaling.
 

## 4x4 keypad 

 ![image](https://user-images.githubusercontent.com/36288975/198944736-c16e2134-193e-4810-a21e-1256c6eefc2d.png)

![image](https://user-images.githubusercontent.com/36288975/198944763-4db22ff4-63df-438a-a27e-9b90aed8eaf0.png)



 ![image](https://user-images.githubusercontent.com/36288975/198944803-b9298867-c5f1-4167-98f8-f17a6bab5ffe.png)


•	STEP1: First set all ROWS to OUTPUT and set them at +5V. Next set all COLUMNS as INPUT to sense the HIGH logic. Now consider a button is pressed on keypad. And that key is at 2ND COLUMN and 3rd ROW.
 
•	With the button being pressed the current flows as shown in figure. With that a voltage of +5V appears at terminal C2. Since the COLUMN pins are set as INPUTS, the controller can sense C2 going high. The controller can be programmed to remember that C2 going high and the button pressed is in C2 COLUMN.
 
•	STEP2: Next set all COLUMNS to OUTPUT and set them at +5V. Next set all ROWS as INPUT to sense the HIGH logic. Since the key pressed is at 2ND COLUMN and 3rd ROW. The current flows as shown below.

![image](https://user-images.githubusercontent.com/36288975/198944818-632726a7-c582-45b5-9ea0-97d2d0b07939.png)

With that current flow a positive voltage of +5V appears at R3 pin. Since all ROWS are set as INPUTS, the controller can sense +5V at R3 pin. The controller can be programmed to remember the key being pressed at third ROW of KEYPAD MATRIX.
![image](https://user-images.githubusercontent.com/36288975/198944848-bc93731c-dc7d-4e33-b32e-14d4c84c5a0b.png)

•	From previous step, we have known the COLUMN number of key pressed and now we know ROW number. With that we can match the key being pressed. We can take the key INPUT provided by this way for 4X4
•	

Procedure:
For creation of project on    Kiel μ vision 5 Development environment (LPC21 XX/48/38)
1.	Click on the menu Project — New µVision Project creates a new project. Select an empty folder and enter the project name, for example Project1. It is good practice to use a separate folder for each project.
2.	Next, the dialog Select Device for Target opens.

 ![image](https://user-images.githubusercontent.com/36288975/198944870-21526748-6345-436d-89c5-07b3902775b0.png)


Figure -01 Target selection
Select the device database. Default is Software Packs. You can have various local device databases, which show up in the drop-down box. For legacy devices (Arm7, Arm9), use the Legacy Device Database [no RTE]
3.	Select the device for your application. This selection defines essential tool settings such as compiler controls, the memory layout for the linker, and the Flash programming algorithms.
4.	Click OK.
5.	Click on the new file option and save the file using save option with .C extension 
6.	Build all for the hex code in the output of the target



For creating the simulation environment in Proteus suite 
Starting New Design
Step 1: Open ISIS software and select New design in  File menu
 ![image](https://user-images.githubusercontent.com/36288975/198944893-b936195d-2850-4543-b255-f4d2f8147e4d.png)

Figure -02 Proteus File Menu

 Step 2: A dialogue box appears to save the current design. However, we are creating a new design file so you can click Yes or No depending on the content of the present file. Then a Pop-Up appears asking to select the template. It is similar to selecting the paper size while printing. For now select default or according to the layout size of the circuit..
 ![image](https://user-images.githubusercontent.com/36288975/198944918-be6a0e5d-e52b-4cff-beb2-0b9f7cabe175.png)
  
  Figure -03 Proteus Default Template Select
 
Step 3:An untitled design sheet will be opened, save it according to your wish,it is better to create a new folder for every layout as it generates other files supporting your design. However,it is not mandatory.
  Figure -04 Proteus Design Sheet
 ![image](https://user-images.githubusercontent.com/36288975/198944933-084a499d-efc3-43ef-ac86-08c7ba3fbf99.png)

Step 4:To Select components, Click on the component mode button.
 ![image](https://user-images.githubusercontent.com/36288975/198944943-d240ac7b-287a-4a64-9be2-2c2344e9f5cd.png)
  
Figure -05 Component Mode
Step 5:Click On Pick from Libraries. It shows the categories of components available and a search option to enter the part name.
 ![image](https://user-images.githubusercontent.com/36288975/198944962-b752aa86-f4e7-47fe-8cca-434d65eb6462.png)

  Figure -06 Pick from Libraries

Step 6: Select the components from categories or type the part name in Keywords text box.
 Place all the required components and route the wires i.e, make connections.
Either selection mode above the component mode or component mode allows to connect through wires. Left click from one terminal to other to make connection. Double right-click on the connected wire or the component to remove connection or the component respectively.
 ![image](https://user-images.githubusercontent.com/36288975/198944983-d2b555d8-6094-431a-ab95-12f693137b9f.png)

 Figure -07 Component Properties Selection
Double click on the component to edit the properties of the components and click on Ok.
Step 8: Select ARM microcontroller form the library – pick part 
 ![image](https://user-images.githubusercontent.com/36288975/198944993-d9480186-2d50-405f-9d81-c425944445c3.png)

Figure -08 LPC2138/48 selection
Step 7:

After making necessary connections click on debug from 
 Figure -09 Keywords Textbox
Example shows selection of push button. Select the components accordingly.
 ![image](https://user-images.githubusercontent.com/36288975/198945018-ddc37b08-f4b0-4a99-99cc-378202d3735e.png)

 Figure -09 Push Button Selection
Step 8: The selected components will appear in the devices list. Select the component and place it in the design sheet by left-click., post which select all the associated components as shown in the circuit diagram below.
 
![image](https://user-images.githubusercontent.com/36288975/198945047-9ef54f44-c4df-46f1-970a-f168330a7048.png)


Figure -10 Circuit diagram of4X4 keypad and  16x2 LCD interface with LPC2148/38
![image](https://user-images.githubusercontent.com/36288975/198945057-7c3a4172-e4d6-4797-9c75-f4f5d0de2797.png)


 
Figure -11 Hex file for simulation 

Step 9: Select the hex file from the Kiel program folder and import the program in to the microcontroller as shown in figure 11 ,  debug and if no errors in connections are found, run the VSM simulation to view the output.


## Kiel - Program:
~~~
#include &lt;lpc21xx.h&gt;
#define LCD (0xff&lt;&lt;8)
#define RS (1&lt;&lt;16)
#define RW (1&lt;&lt;17)
#define EN (1&lt;&lt;18)
#define r1 (1&lt;&lt;16)
#define r2 (1&lt;&lt;17)
#define r3 (1&lt;&lt;18)
#define r4 (1&lt;&lt;19)
#define c1 (1&lt;&lt;20)
#define c2 (1&lt;&lt;21)
#define c3 (1&lt;&lt;22)
#define c4 (1&lt;&lt;23)

void delay(unsigned int time);
void lcd_ini(void);
void lcd_print(char*str);
void lcd_cmd(unsigned char command);
void lcd_dat(unsigned int data);

unsigned char keypad(void);
void keypad_delay(void);

int main(void)
{
	PINSEL0 = 0x00000000;
	IODIR0 = 0Xffffffff;
	PINSEL1 = 0x00000000;
	IODIR1 = 0x00f00000;
	
	lcd_ini();
	lcd_print("Press any key");
	lcd_cmd(0xc0);
	
	while(1)
	{
		lcd_dat(keypad());
	}
	return 0;
}
void keypad_delay(void)
{
	unsigned int t1,t2;
	for(t1=0;t1&lt;300;t1++)
			for(t2=0;t2&lt;1275;t2++);
}


unsigned char keypad (void)
{
	unsigned char key;
	IOCLR1|=(c1|c2|c3|c4|r1|r2|r3|r4);
	while(1)
	{
		IOCLR1|=c1;
		IOSET1|=(c2|c3|c4);
		if((IOPIN1&amp;r1)==0)
		{
			key='7';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r2)==0)
		{
			key='8';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r3)==0)
		{
			key='9';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r4)==0)
		{
			key='/';
			keypad_delay();
			return key();
		}
		
		
		IOCLR1|=c2;
		IOSET1|=(c1|c3|c4);
		
		if((IOPIN1&amp;r1)==0)
		{
			key='4';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r2)==0)
		{
			key='5';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r3)==0)
		{
			key='6';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r4)==0)
		{
			key='*';
			keypad_delay();
			return key();
		}
		
		
		IOCLR1|=c3;
		IOSET1|=(c1|c2|c4);
		
		if((IOPIN1&amp;r1)==0)
		{
			key='1';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r2)==0)
		{
			key='2';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r3)==0)
		{
			key='3';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r4)==0)
		{
			key='-';
			keypad_delay();
			return key();
		}
		
		IOCLR1|=c4;
		IOSET1|=(c1|c2|c3);
		
		if((IOPIN1&amp;r1)==0)
		{
			lcd_cmd(0x01);
			keypad_delay();
		}
		else if((IOPIN1&amp;r2)==0)
		{
			key='0';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r3)==0)
		{
			key='=';
			keypad_delay();
			return key;
		}
		else if((IOPIN1&amp;r4)==0)
		{
			key='+';
			keypad_delay();
			return key();
		}
	}
}
void lcd_cmd(unsigned char command)
{
	IO0CLR|=(RS|RW|EN|LCD);
	IO0SET|=(command&lt;&lt:8);
	IO0CLR|=RS;
	IO0CLR|=RW;
	IO0SET|=EN;
	delay(2);
	IO0CLR|=EN;
	delay(3);
}

void lcd_dat(unsigned int data)
{
	IO0CLR|=(RS|RW|EN|LCD);
	IO0SET|=(data&lt;&lt;8);
	IO0SET|=RS;
	IO0CLR|=RW;
	IO0SET|=EN;
	delay(2);
	IO0CLR|=EN;
	delay(3);
}
void lcd_print(char*str)
{
	while(*str!="\0")
	{
		lcd_dat(*str);
		str++;
	}
}
void lcd_ini(void)
{
	delay(5);
	lcd_cmd(0X38);
	lcd_cmd(0X0f);
	lcd_cmd(0X06);
	lcd_cmd(0X01);
	delay(5);
	lcd_cmd(0X80);
}

void keypad_delay(void)
{
	unsigned int t1,t2;
	for(t1=0;t1&lt;time;t1++)
			for(t2=0;t2&lt;1275;t2++);
}
}
~~~




## Output screen shots :
## BEFORE SIMULATION:
![exp 5 1](https://user-images.githubusercontent.com/94187572/200333041-427d38b9-a882-4431-b827-03c4e4da9a07.png)


## AFTER SIMULATION:
![exp 5 2](https://user-images.githubusercontent.com/94187572/200333284-463b5257-52c7-4861-9c81-25ae54eb2f06.png)


## LAYOUT:
![exp 5 3](https://user-images.githubusercontent.com/94187572/200333451-126d5026-609d-4d70-bcb6-41350922f010.png)


## Result :
Interfacing a keypad 4x4 is interfaced  with LPC2148







