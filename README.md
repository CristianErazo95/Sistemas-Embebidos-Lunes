# Sistemas-Embebidos-Lunes

int led_1=13;
int led_2=12;
int led_3=11;
int led_4=10;
int led_5=9;
int led_6=8;
int led_7=7;
int led_8=6;
int led_9=5;
int led_10=4;
int sw_1=3;
int sw_2=2;
int sw_3=1;
int leds[5]={led_2,led_4,led_6,led_8,led_10};
int leds2[5]={led_1,led_3,led_5,led_7,led_9};
int leds3[10]={led_1,led_2,led_3,led_4,led_5,led_6,led_7,led_8,led_9,led_10};
int leds4[5]={led_1,led_2,led_3,led_4,led_5};
int leds5[5]={led_10,led_9,led_8,led_7,led_6};
int contad=0;
int cont=0;
int randnum;
void setup() {
    pinMode(led_1,OUTPUT);
  pinMode(led_2,OUTPUT);
  pinMode(led_3,OUTPUT);
  pinMode(led_4,OUTPUT);
  pinMode(led_5,OUTPUT);
  pinMode(led_6,OUTPUT);
  pinMode(led_7,OUTPUT);
  pinMode(led_8,OUTPUT);
  pinMode(led_9,OUTPUT);
  pinMode(led_10,OUTPUT);
  pinMode(sw_1,INPUT);  
  pinMode(sw_2,INPUT);
  pinMode(sw_3,INPUT);

}

void loop() {
  if(digitalRead(sw_1)==LOW&&digitalRead(sw_2)==LOW&&digitalRead(sw_3)==LOW)
  {
    digitalWrite(leds[5],LOW);
    
    }
 digitalWrite(leds[5],LOW);
   if(digitalRead(sw_1)==LOW&&digitalRead(sw_2)==HIGH&&digitalRead(sw_3)==LOW)
  {
    for(;contad<5;contad++){

     
      digitalWrite(leds[contad],HIGH);
      delay(200);
      digitalWrite(leds[contad],LOW);
      delay(75);
      }
      contad=0; 
  }


  if(digitalRead(sw_1)==LOW&&digitalRead(sw_2)==HIGH&&digitalRead(sw_3)==HIGH)

  {
    for(;contad<5;contad++){

      digitalWrite(leds2[contad],HIGH);
      delay(200);
      digitalWrite(leds2[contad],LOW);
      delay(75);
      }
      contad=0; 
  }


  if(digitalRead(sw_1)==HIGH&&digitalRead(sw_2)==LOW&&digitalRead(sw_3)==HIGH)
  {
    randnum=random(0,10);
          digitalWrite(leds3[randnum],HIGH);
          delay(200);
          digitalWrite(leds3[randnum],LOW);
          delay(75);
      
              }
              
  if(digitalRead(sw_1)==HIGH&&digitalRead(sw_2)==HIGH&&digitalRead(sw_3)==LOW)
  {

        for(;contad<5;contad++){
   
     
      digitalWrite(leds4[contad],HIGH);
      digitalWrite(leds5[contad],HIGH);
      delay(200);
      digitalWrite(leds4[contad],LOW);
      digitalWrite(leds5[contad],LOW);
      delay(75);

      
      }
      contad=0; 
     
      }
}
