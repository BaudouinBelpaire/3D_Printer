# DIY CoreXY 3D Printer

<p style="text-align: center;"> During this project, I designed and assembled a homemade 3D printer based on a CoreXY architecture. This one has been designed on AutoDesk Fusion 360, and is made from 3D printed and laser cutted parts. The machine has a maxiumum printing volume of 200x200x200mm which is sufficient for regular prints. </p>

## Specifications:
- The printing head is mounted on a CoreXY gantry enabling higher speeds and reducing the moving mass.
- The cubic frame makes the global architecture stiff which improves the print quality by absorbing the vibrations.
- The printer is running on an Arduino Mega2560 programmed with Marlin software.

## Mechanical design: 
<p style="text-align: center;"> The entire machine was designed on Fusion 360, and each part was either designed to be 3D printed/laser-cutted or bought online from suppliers. The CAD files from existing parts were found online on [GrabCAD](https://grabcad.com/library). The printer's assembly is shown in the next video:

https://github.com/BaudouinBelpaire/3D_Printer/assets/157626337/6a2e77a8-c60f-4968-856b-16abbe63af29 </p> 

## Bill Of Materials:
<p style="text-align: center;"> Once the machine designed and simulated on Fusion 360, a [BOM](https://github.com/BaudouinBelpaire/3D_Printer/blob/main/BOM.xlsx) was established to realise the entire assembly. The parts were bought from different suppliers, and the MDF was purchased at Leroy Merlin to manufacture the panels and few other parts.

![BOM](https://github.com/BaudouinBelpaire/3D_Printer/assets/157626337/4f2db5c5-96a2-4568-aff9-84f23fdeed17) </p>

## Electronics:
<p style="text-align: center;"> The electronics ensure the actuation of the stepper motors according to the sequence of coordinates required to make the part. This one is composed of the 3 stepper motors for the XYZ directions and an additional one for the filament extrusion. The motors are controlled by motor drivers converting the digital pulses into electrical signals rotating the shaft. The calibration of the printer is ensured by mechanical endstops to know the initial position location. Finally, the extrusion and bed temperature are satisfied by a closed-loop system composed of a thermal sensor and heater. Each subsystem is controlled by the Arduino microprocessor which controls the actuators and receives feedbacks from the sensors. The circuit wiring is shown below: 

![Wiring schematic](https://github.com/BaudouinBelpaire/3D_Printer/blob/main/Wiring_schematic.jpg) </p>

## Marlin software:
<p style="text-align: center;"> The Arduino board was programmed with the Marlin software which is a well-developed software for 3D printers. This one was adapted to the printer's parameters and flashed on the board. </p>
