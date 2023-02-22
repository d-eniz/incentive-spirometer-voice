int trigPin = 11;    // Trigger
int echoPin = 12;    // Echo
long duration, cm, inches;
const int buzzer = 9;

void setup() {
  //Serial Port begin
  Serial.begin (9600);
  //Define inputs and outputs
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  pinMode(buzzer, OUTPUT);
}

void loop() {
  // Wait until the object is further than 4cm away
  while (true) {
    digitalWrite(trigPin, LOW);
    delayMicroseconds(5);
    digitalWrite(trigPin, HIGH);
    delayMicroseconds(10);
    digitalWrite(trigPin, LOW);
    duration = pulseIn(echoPin, HIGH);
    cm = (duration/2) / 29.1;
    if (cm > 4) {
      break;
    }
  }

  // Record for 4 seconds
  long startTime = millis();
  long endTime = startTime + 4000;
  int numReadings = 0;
  long totalDistance = 0;
  while (millis() < endTime) {
    digitalWrite(trigPin, LOW);
    delayMicroseconds(5);
    digitalWrite(trigPin, HIGH);
    delayMicroseconds(10);
    digitalWrite(trigPin, LOW);
    duration = pulseIn(echoPin, HIGH);
    cm = (duration/2) / 29.1;
    totalDistance += cm;
    numReadings++;
    delay(50); // Wait for 50ms before taking the next reading
  }

  // Calculate and display the final value
  cm = totalDistance / numReadings;
  Serial.print("Final distance: ");
  Serial.print(cm);
  Serial.print("cm");
  Serial.println();
  tone(buzzer,cm*100);

  delay(1000); // Wait for 1 second before taking another measurement
}
