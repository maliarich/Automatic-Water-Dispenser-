# Automatic-Water-Dispenser Prototype-Rhino camp refugee settlement Uganda.
This is a motor driven system that allows user to access water in a tank by touching a sensor once. working on this simple DIY project to help students use it in the school compound.
In most schools in the refugee settlement, a water tap is used at the wash rooms. Therefore students tend to turn on the tap to wash their hands 

**Materials**

*Arduino Uno*

*Laptop with a IDE software

*Batteries 

*Touch pad sensor*

*Wires*

*LED Light*

*PC with the IDE*

*5v motor*

*Water Container*

*Bread board*


**PICTURES**

1. ![Water Dispenser](https://user-images.githubusercontent.com/56769901/156925389-1d5acf67-4d15-470c-8a10-a6b49437012c.png)
2. ![Water Dispenser 2](https://user-images.githubusercontent.com/56769901/156925403-fb6b7506-7704-4993-9e84-f46169fcd98c.png)
3. ![water Dispenser 3](https://user-images.githubusercontent.com/56769901/156925440-6364a682-045f-4671-a247-3107813820d9.png)



**RAW CODES**

``` // Maliamungu touch water dispenser prototype.


// When Sig Output is high, touch sensor is being pressed

#define ctsPin 2

// Pin for capactitive touch sensor

int motor = 13;

// pin for the LED

void setup() {
  Serial.begin(9600);

pinMode(motor, OUTPUT);

pinMode(ctsPin, INPUT);

}

void loop() {
  int ctsValue = digitalRead(ctsPin);

if (ctsValue == HIGH)
{

digitalWrite(motor, HIGH);

Serial.println("TOUCHED");

}

else{

digitalWrite(motor,LOW);

Serial.println("not touched");

}

delay(500);


} ```
