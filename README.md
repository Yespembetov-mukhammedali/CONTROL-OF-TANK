# CONTROL OF TANK FILLING, MIXING AND PUMPING WITH FBD LANGUAGE

This project is about controlling a process tank automatically, using FBD (Function Block Diagram) in TIA Portal. The tank can fill with liquid, mix it, and then pump it out — all controlled by a PLC program instead of manual switches.

This kind of system is used in real factories: food production, chemical plants, pharmaceutical plants — anywhere liquids need to be stored, mixed, and moved safely.

## Blocks I used

* AND / OR / NOT – to combine sensor signals and decide what should happen next.
* TON / TOF / TP timers – to add delays or short pulses (for example, wait a few seconds before starting the mixer).
* RS / SR triggers – to "remember" a state, like keeping the pump ON until a stop condition happens.
Scaling and comparison blocks – to turn analog sensor values into real numbers (like percentage of tank level) and compare them to set points.

## Safety and Protection
Because tanks and pumps are physical equipment, protecting them is a big part of this project:
* Hysteresis is added between the ON and OFF levels, so valves and pumps don't switch on and off too fast and wear out.
* If something dangerous happens — like the tank running dry or overflowing — the system stops the equipment right away and sends an alarm.
* Alarms stay active (latched) until the operator confirms them on the HMI screen, even if the problem is already gone. This way, nothing gets ignored.

## Video Demonstration (Just click to the picture)

Develop a program for automatic filling of the tank. When the set level thresholds are reached, the indicators LOW, MED, HIGH should be triggered, and the degree of filling should be displayed on a graphical scale. Implement visualization on the HMI: pump start/stop buttons, level indicators and filling scale.

[![Watch the video](./images/HMI9_screen.jpg)](https://youtu.be/3jc2v3dQB6U)

## Task 2

Develop a tank level control program with two modes: automatic and manual, as well as with two operation directions: filling and draining. The values "lower threshold" and "upper threshold" are set from the operator panel. In automatic mode "Filling", when the level is lower or equal to the lower threshold, switch on the pump and conduct the process until the upper threshold is reached, after which the pump is switched off. In automatic mode "Drain", when the level is above or equal to the upper threshold, open the drain valve and conduct the process until the level drops below the lower threshold, then switch off the pump. Level below the lower threshold, then close the valve. In manual mode the operator can switch on only one actuator - pump or drain valve; simultaneous switching on is prohibited. On the operator panel to provide buttons "Start" and "Stop", mode switches, input fields of thresholds, graphical scale of level and three indicators "low", "medium", "high". Provide emergency stop and correct operation of indication when the level passes  the set thresholds.

[![Watch the video](./images/Video_preview.png)](https://youtube.com/shorts/PptSstsuSxg)


