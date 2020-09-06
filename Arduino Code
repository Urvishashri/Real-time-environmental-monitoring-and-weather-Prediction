float temperatureC;
float temperatureF;
float vout;
float vout1;
int LEDR=12;
int LEDG=13;
int gas_sensor;
int piezo=4;

void setup(){
  pinMode(A0,INPUT);
  pinMode(A1,INPUT);
  pinMode(LEDR,OUTPUT);
  pinMode(LEDG,OUTPUT);
  pinMode(piezo,OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  vout=analogRead(A0);
  vout1=vout*(500/1024);
  temperatureC=(vout1-500)/10;
  temperatureF=(temperatureC*1.8)+32;
  gas_sensor=analogRead(A1);
  
  if(temperatureC>=100)
  {
    digitalWrite(piezo,HIGH);
  }
  else
  {
    digitalWrite(piezo,LOW);
  }
  if(gas_sensor>=800)
  {
    digitalWrite(LEDG,HIGH);
  }
  else
  {
    digitalWrite(LEDG,LOW);
  }
  if(gas_sensor<800)
  {
    digitalWrite(LEDR,HIGH);
  }
  else
  {
    digitalWrite(LEDR,LOW);
  }
  
  Serial.print("in DegreeC=");
  Serial.print(" ");
  Serial.print(temperatureC);
  Serial.print("/t");
  Serial.print("in DegreeF=");
  Serial.print(" ");
  Serial.print(temperatureF);
  Serial.print("/t");
  Serial.print("garsensor=");
  Serial.print(" ");
  Serial.print(gas_sensor);
  Serial.println();
  delay(1000);
}

  
    
