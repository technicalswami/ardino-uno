void setup() {
  Serial.begin(115200);
  pinMode(13,OUTPUT);
  pinMode(12,OUTPUT);
  pinMode(11,OUTPUT);
 
}

void loop() {
  int t;
    if (Serial.available()) 
      {
      t=Serial.read();
      int x = t-48;
      if(x==1)
        { 
          Serial.println ("led 1 is ON");
       digitalWrite(13, HIGH);   
        delay(1000);
        Serial.println("led 1 is OFF");
        digitalWrite(13, LOW);   
        delay(1000);
        
        }
  else if(x==2)
    {
      Serial.println ("led 2 is ON");
      digitalWrite(12, HIGH);   
      delay(1000);
       Serial.println("led 2 is OFF");
      digitalWrite(12, LOW);   
      delay(1000);
        
      }
       else if(x==3)
    {
      Serial.println("led 3 is ON");
      digitalWrite(11, HIGH);   
      delay(1000);
      Serial.println("led 3 is OFF"); 
      digitalWrite(11, LOW);   
      delay(1000);
       
      }
  else
  {
    Serial.println ("not valid");
    Serial.print (x);
  }
 }

 }
