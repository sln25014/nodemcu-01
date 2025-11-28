# Komma igång med Arduino

Jag kommer gå igenom hur man kommer igång med Arduino genom att installera programvaran, inställningar och hur man skickar ett kodexempel till en faktisk mikroprocessor.

## Installera

Vi börjar att installera Arduinos IDE eller Integrated Development Environment som tillåter oss att skriva kod, kompilera denna och skicka till vår mikroprocessor.

[Länk för att installera](https://www.arduino.cc/en/software/#ide)

Installera versionen för ditt operativsystem och ändra ingenting i installationsprocessen och godkänn eventuella popups.

## Inställningar

Gå in på **Preferences** under fliken **File** (Se bild)

![bild](/bilder/Preferences.png)

För att sedan klistra in följande:

**http://arduino.esp8266.com/stable/package_esp8266com_index.json**

i rutan **Additional boards manager URLs** och tryck sedan på **OK**

Under fliken **BOARDS MANAGER** i den vänstra menyn sök sedan på **esp8266** och ladda ner följande 

![esp8266](/bilder/8266.png)

När det är klart gå till **Board** under fliken **Tools** (se bild)

![Boards](/bilder/boards.png)

och sedan under **esp8266** välj **Generic ESP8266 Module**

## Skicka kod till mikroprocessor

Börja med att koppla in din mikroprocessor till datorn och under fliken **Tools** se till att rätt **Port** är vald.

Under gå till **File>Examples>Basics** och välj **Blink** ett nytt fönster kommer öppnas med kod som ser ut såhär:

```C++
/*
  Blink

  Turns an LED on for one second, then off for one second, repeatedly.

  Most Arduinos have an on-board LED you can control. On the UNO, MEGA and ZERO
  it is attached to digital pin 13, on MKR1000 on pin 6. LED_BUILTIN is set to
  the correct LED pin independent of which board is used.
  If you want to know what pin the on-board LED is connected to on your Arduino
  model, check the Technical Specs of your board at:
  https://docs.arduino.cc/hardware/

  modified 8 May 2014
  by Scott Fitzgerald
  modified 2 Sep 2016
  by Arturo Guadalupi
  modified 8 Sep 2016
  by Colby Newman

  This example code is in the public domain.

  https://docs.arduino.cc/built-in-examples/basics/Blink/
*/

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}

```

Klicka sedan på knappen högst upp med en pil till höger som säger **Upload** och låt den tänka ett litet tag.

Och då var det klart, ett program som får en mikroprocessor att blinka skapat och skickat.
