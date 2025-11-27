# Smart Home Automation System (Arduino + Tinkercad)

This project is a simple **Home Automation System** built using Arduino and simulated entirely in **Tinkercad Circuits**.  
It demonstrates how appliances such as **lights, fans, or other home devices** can be controlled using an Arduino-based logic system.

The project can be used as a basic introduction to home automation, microcontroller programming, and circuit simulation.

---

## Tinkercad Project Link  
View and interact with the full simulation below:  
 **https://www.tinkercad.com/things/kcqqjfrVtT2-dd-home-automation-system**

---

## Features
- Control lights and other appliances using Arduino  
- Programmed logic for switching ON/OFF  
- Works entirely inside Tinkercad simulation environment  
- Beginner-friendly project suitable for learning microcontrollers  
- Shows the concept of automated home control systems  

---

## Components Used
- **Arduino UNO**
- **LEDs (represent home appliances)**
- **Resistors**
- **Push Buttons / Input Control**
- **Connecting Wires**
- **Breadboard**

---

## Circuit Description
This home automation setup uses:
- **Buttons** as control inputs  
- **LEDs** as output appliances  
- Arduino reads button states and turns devices ON or OFF accordingly  

Each LED represents an **appliance** such as a:
- Room Light  
- Fan  
- Decorative Light  
- Power Outlet Indicator  

---

## Arduino Code (Used in This Project)

```cpp
// Home automation code for Tinkercad Arduino

// Pin definitions
int ldr = A0;        // LDR pin
int lightout = 9;    // Light output pin

void setup()
{
  pinMode(ldr, INPUT);      // LDR input
  pinMode(lightout, OUTPUT);  // Output to LED or relay
  Serial.begin(9600);        // Serial monitor
}

void loop()
{
  int ldrvalue = analogRead(ldr);  // Read LDR
  Serial.println(ldrvalue);

  // Control output based on LDR value
  if (ldrvalue < 150)
  {
    digitalWrite(lightout, HIGH);   // Turn ON when dark
  }
  else
  {
    digitalWrite(lightout, LOW);    // Turn OFF when bright
  }

  delay(1000); // Delay for stability
}
