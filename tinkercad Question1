#include <Servo.h>

int tempPin = A0;
int tempVal;
Servo myservo;

void setup() {
  myservo.attach(9);
  Serial.begin(9600);
}

void loop() {
  tempVal = analogRead(tempPin);
  float mv = (tempVal / 1024.0) * 5000;
  float cel = mv / 10;
  Serial.print("Temperature: ");
  Serial.print(cel);
  Serial.println("C");

  if (cel > 30) {
    myservo.write(90);
    delay(1000);
  }
}
