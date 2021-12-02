# .rP
#define pin2 2 
#define pin3 3
#define pin4 4 
#define pin5 5 
#define pin6 6 
#define pin7 7 
#define pin8 8  


#define spdl 44 // analog wr skorost 
#define dirl 45     // digital napravlenie 
#define spdr 46 
#define dirr 47 
#define analogPin A0  
#define analogPin1 A1 
#define analogPin2 A2  
#define analogPin3 A3 
#define analogPin4 A4 
#define analogPin5 A5 
int sum = 0, sum1 = 0, sum2 = 0;  int a = 0, b = 0, c = 0, d = 0, e = 0, f = 0;
void setup() { 
Serial.begin(9600); 
pinMode(analogPin,INPUT); 
pinMode(analogPin1,INPUT);
pinMode(analogPin2,INPUT);
pinMode(analogPin3,INPUT);
pinMode(analogPin4,INPUT);
pinMode(analogPin5,INPUT); 
pinMode(spdl ,OUTPUT);
pinMode(dirl ,OUTPUT);
pinMode(spdr ,OUTPUT); 
pinMode(dirr ,OUTPUT); 
}  void loop() {  
//dvigatel
analogWrite(spdl, 100);
digitalWrite(dirl, 1);   
analogWrite(spdr, 100); 
digitalWrite(dirr, 1); 

Serial.print(analogRead(analogPin)); 
Serial.print("A ");   
Serial.print(analogRead(analogPin1)); 
Serial.print("A ");   
Serial.print(analogRead(analogPin2)); 
Serial.print("A "); 
Serial.print(analogRead(analogPin3)); 
Serial.print("A ");   
Serial.print(analogRead(analogPin4)); 
Serial.print("A ");  
Serial.print(analogRead(analogPin5));   
Serial.print("A "); 
Serial.println();       
/////1        if (analogRead(analogPin) &amp;&amp; analogRead(analogPin1) > 600){   
analogWrite(spdl, 100);
digitalWrite(dirl, 1); 
analogWrite(spdr,0); 
digitalWrite(dirr, 1);    
} else{   
analogWrite(spdl, 0);
digitalWrite(dirl, 1);   
analogWrite(spdr, 0);
digitalWrite(dirr, 1);
}
////2 if (analogRead(analogPin4) &amp;&amp; analogRead(analogPin5) > 600){         
analogWrite(spdl, 100 );
digitalWrite(dirl, 1);   
analogWrite(spdr,10);
digitalWrite(dirr, 1);   
} else{   
analogWrite(spdl, 0);
digitalWrite(dirl, 1);    
analogWrite(spdr, 0);
digitalWrite(dirr, 1); 
}          
}
