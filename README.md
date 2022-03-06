# Automatic-Water-Dispenser Prototype-Rhino camp refugee settlement Uganda.
This is a motor driven system that allows user to access water in a tank by touching a sensor once.

**Materials**

*Arduino Uno*

*Touch pad sensor*

*Wires*

*LED Light*

*PC with the IDE*

*5v motor*

*Water Container*

*Bread board*


**PICTURES**

1. ![Screenshot_20220301-060922](https://user-images.githubusercontent.com/56769901/156922846-3868ad65-864b-4f4c-add9-fa2f3565a49c.png)
2. ![Screenshot_20220301-061054](https://user-images.githubusercontent.com/56769901/156922871-bc84303b-ed31-43ce-bb83-e54744595fc9.png)
3. ![Screenshot_20220301-061035](https://user-images.githubusercontent.com/56769901/156922883-e4434e0f-2c96-4658-9598-a3c9ce953edc.png)


**RAW CODES**

// Maliamungu touch water dispenser prototype.


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


}
