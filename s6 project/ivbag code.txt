#include <Arduino.h>
#include "HX711.h"

#define BLYNK_TEMPLATE_ID "TMPL3G-LFnS8S"
#define BLYNK_TEMPLATE_NAME "iv bag"
#define BLYNK_AUTH_TOKEN "g4AZgvzK3531kTc3_FQtoB_LOZRHuVVa"

#define BLYNK_PRINT Serial
#include <ESP8266WiFi.h>
#include <BlynkSimpleEsp8266.h>

// HX711 circuit wiring
const int LOADCELL_DOUT_PIN = D6;
const int LOADCELL_SCK_PIN = D5;
#include <Wire.h> 
#include <LiquidCrystal_I2C.h>
int sc1;
int led=D7;
int a=0,b=0;

LiquidCrystal_I2C lcd(0x27,16,2);
HX711 scale;

char ssid[] = "realme C15";    
char pass[] = "Arya1234"; 

void setup() {
  Serial.begin(9600);
   lcd.init();
  lcd.backlight();
  pinMode(led,OUTPUT);
  digitalWrite(led,LOW);
  Blynk.begin(BLYNK_AUTH_TOKEN, ssid, pass);
  Serial.println("HX711 Demo");
  Serial.println("Initializing the scale");

  scale.begin(LOADCELL_DOUT_PIN, LOADCELL_SCK_PIN);

  Serial.println("Before setting up the scale:");
  Serial.print("read: \t\t");
  Serial.println(scale.read());      // print a raw reading from the ADC

  Serial.print("read average: \t\t");
  Serial.println(scale.read_average(20));   // print the average of 20 readings from the ADC

  Serial.print("get value: \t\t");
  Serial.println(scale.get_value(5));   // print the average of 5 readings from the ADC minus the tare weight (not set yet)

  Serial.print("get units: \t\t");
  Serial.println(scale.get_units(5), 1);  // print the average of 5 readings from the ADC minus tare weight (not set) divided
            // by the SCALE parameter (not set yet)
            
  scale.set_scale(233.588);
  //scale.set_scale(-471.497);                      // this value is obtained by calibrating the scale with known weights; see the README for details
  scale.tare();               // reset the scale to 0

}

void loop() {

  sc1 = scale.get_units(10);
  delay(1000);
  if(sc1<10)
  {
    Blynk.logEvent("iv_bag_notification");
   digitalWrite(led,HIGH); 
  lcd.setCursor(0,0);
  lcd.print("weight =");
  lcd.setCursor(10,0);
  lcd.print(sc1);
  lcd.setCursor(11,0);
  lcd.print("     ");  
  }
  else
  {
    a=0;
    digitalWrite(led,LOW);
  lcd.setCursor(0,0);
  lcd.print("weight =");
  lcd.setCursor(10,0);
  lcd.print(sc1);
  lcd.print("     "); 
  }
}