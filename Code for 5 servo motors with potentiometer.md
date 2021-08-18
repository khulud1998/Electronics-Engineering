### 1.add servo library
```
$ #include <Servo.h> 
```

### 2.create servo object to control a servo
```
$ Servo S1, S2, S3, S4, S5;
```

### 3.analog pin used to connect the potentiometer


```
$ int Q = 0;  
$ int W = 1;
$ int E = 2;
$ int R = 3;
$ int T = 4;
```


### 4.variable to read the value from the analog pin

```
$ int valA0;    
$ int valA1;
$ int valA2;
$ int valA3;
$ int valA4;
```

### 5.attaches the servo on pin 9 to the servo object
```
void setup() {
  S1.attach(10);  
  S2.attach(9);
  S3.attach(6);
  S4.attach(5);
  S5.attach(3);
}
```
### 6.reads the value of the potentiometer (value between 0 and 1023)
### 7.scale it to use it with the servo (value between 0 and 180)
### 8.sets the servo position according to the scaled value
### 9.waits for the servo to get there

```
void loop() {
  valA0 = analogRead(Q);             
  valA0 = map(valA0, 0, 1023, 0, 180);      
  S1.write(valA0);                  
  delay(15);                           
  
  
  valA1 = analogRead(W);
  valA1 = map(valA1, 0, 1023, 0, 180);
  S2.write(valA1);
  delay(15);
  
  valA2 = analogRead(E);
  valA2 = map(valA2, 0, 1023, 0, 180);
  S3.write(valA2);
  delay(15);
  
  valA3 = analogRead(R);
  valA3 = map(valA3, 0, 1023, 0, 180);
  S4.write(valA3);
  delay(15);
  
  valA4 = analogRead(T);
  valA4 = map(valA4, 0, 1023, 0, 180);
  S5.write(valA4);
  delay(15);
  
}
```
