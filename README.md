//reciever uno
int button1=8;
int button2=9;
void setup() 
{
 
Serial.begin(9600);
pinMode(button1,input);
pinMode(button2,input);

}

void loop() 
{
   if(digitalread(button1)==0)
   Serial.write('1');
   else if(digitalread(button2)==0)
   serial.write('2');
}



// transmitter uno
int led1=8;
int led2=9;
void setup()
 {  
Serial.begin(9600);
pinMode(led1,output);
pinMode(led2,output);
}
void loop() 
{
if(serial.available())
{
  if(serial.read()=='1')
  digitalwrite(led1,high);
  else if(serial.read()=='2')
  digitalwrite(led2,low);
}
}
