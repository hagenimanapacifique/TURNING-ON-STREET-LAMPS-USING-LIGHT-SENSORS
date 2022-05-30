# TURNING-ON-STREET-LAMPS-USING-LIGHT-SENSORS
# Abstract

Our project is about automatic switching of street light. In the present scenario, we
will continuously illuminate of street lights using LDR as a light sensor. Therefore, 
this project proposes sensor based automatic switching off and on of street light. 
LDR is used to detect the presence of light and turn on and off the street light 
accordingly and is used to control the switching action of lamps or street lights 
depending on sun light condition. A relay is to provide isolation between the 
controller and the device, as we know devices that may work on both AC and DC
currents always need to get a signal from the microcontroller. Therefore, a relay will
be used in such case to switch from low DC current of 5V to AC current to be 
consumed by our street bulb lamps[1]

# Problem statement

It is a well-known fact that in today’s modern world the development in 
transportation system plays a big role. It consists of roads, streets, highways etc., 
these pathways must be illuminated brightly with the help of several types of 
glowing light bulbs or LEDs. It has been seen that during the night a lot of things 
happen on these pathways like theft, accidents due to the absence of light. The main 
purpose of providing the light to these highways, roads or street is to provide safety 
to the vehicle and number of persons crossing these paths and prevent them from 
any happen and track of the road or accident. Another purpose of providing lighting 
to these places is that during the night times when a smaller number of vehicles 
passes the road, the pedestrian cannot have hard time crossing due darkness on the 
road. Since electricity is costly due to continuous glowing for 12hrs or even more we 
will solve this problem by illuminating the streets with sufficient light.

# DESCRIPTION

In this system mainly two devise are used a relay and a light dependent resistor 
(LDR). Firstly, I the Light Dependent Resistor (LDR) is used for switching ON or 
switching OFF the bulb lamps during day and night times by detecting the light 
intensity. Secondly, a relay is to switch from low DC voltage of 5V to usable AC 
voltage of 220V and to provide isolation between the microcontrollers as to bridge
that gap. The micro controller Arduino UNO was used to automatically control the 
system[2].
# BLOCK DIAGRAM
![image](https://user-images.githubusercontent.com/106548784/171034350-4dacc683-66cb-4606-a5de-bf3ec2cc4d8e.png)

# SOURCE CODES
int ldr=A0;

int led=8;

int value=0;

void setup() 

{

 Serial.begin(9600);
 
 pinMode(8,OUTPUT);
 
}

void loop()

{

 Serial.println("Welcome to Tec ponder LDR tutorial");
 
 value=analogRead(ldr);
 
 Serial.println(value);
 
 if(value>100)
 
 {
 Serial.println("LED light on");
 
 digitalWrite(led,HIGH);
 
 
 }else
 
 {
 
 digitalWrite(led,LOW);
 
 delay(value);
 
 
}}

# CIRCUIT DIAGRAM(drawn using fritzing)
![image](https://user-images.githubusercontent.com/106548784/171034921-31fc2305-d8f5-45bc-aae5-6b3ca249af31.png)

Reference
[1] H. Katara, “Automatic Switching of Street Light,” Int. J. Innov. Technol. Explor. Eng., 
vol. 8, no. 12S, pp. 135–137, 2019, doi: 10.35940/ijitee.l1041.10812s19.
[2] “bulbulart203.
# Implemented by: -HAGENIMANA Pacifique
# -IRADUKUNDA Albert
