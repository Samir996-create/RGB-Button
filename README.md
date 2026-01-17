int buttonPin=6;
int ledPin1=13;
int ledPin2=12;
int ledPin3=11;
int ledPin4=10;
int ledPin5=9;
int ledPin6=8;
int buttonState=0;
void setup(){
  pinMode(6,INPUT);
  pinMode(13,OUTPUT);
  pinMode(12,OUTPUT);
  pinMode(11,OUTPUT);
  pinMode(10,OUTPUT);
  pinMode(9,OUTPUT);
  pinMode(8,OUTPUT);
  Serial.begin(9600);
}
void loop(){
  buttonState=digitalRead(6);
  if(buttonState==HIGH){
    digitalWrite(13,HIGH);
    digitalWrite(12,LOW);
    digitalWrite(11,LOW);
    digitalWrite(10,HIGH);
    digitalWrite(9,LOW);
    digitalWrite(8,LOW);
    Serial.println("Button Pressed");
  }else{
    digitalWrite(13,LOW);
    digitalWrite(12,HIGH);
    digitalWrite(11,LOW);
    digitalWrite(10,LOW);
    digitalWrite(9,HIGH);
    digitalWrite(8,LOW); 
    Serial.println("Button Released");
  }
}  
