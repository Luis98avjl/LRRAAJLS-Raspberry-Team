# LRRAAJLS-Raspberry-Team

# Sistemas programables

## 37 Sensor KIT



## Joystick
  ### Codigo
  ~~~~
    from machine import Pin, ADC
import utime

xAxis = ADC(Pin(27))
yAxis = ADC(Pin(26))
button = Pin(17,Pin.IN, Pin.PULL_UP)

while True:
    xValue = xAxis.read_u16()
    yValue = yAxis.read_u16()
    buttonValue = button.value()
    buttonStatus = "not pressed"


    if buttonValue == 0:
        buttonStatus = "pressed"
        
        
    print("X: " + str(xValue) + ", Y: " + str(yValue) + " -- button value: " + str(buttonValue) + " button status: " + buttonStatus)
    utime.sleep(0.2)
  ~~~~
  ### Corrida
  
  ### Imagenes del circuito
  
 
 
## Flame
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
  
## RGB LED
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
  
## Heartbeat
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Light cup
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Hall Magnetic
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
 
## Realy
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Linear Hall
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## SMD RGB
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Color Flash

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Tilt switch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  

## 18B20 Temp

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Big Sound

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito


## Touch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Two-color

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Laser emit

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## Laser emit

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
  
## Ball switch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Analog temp

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Small sound
  
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Digital temperature

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Mini two-color

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Butom 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## Photo-esistor

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## IR emission

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Tracking

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Buzzer

  ### * Codigo
  ~~~~
    from machine import Pin, PWM
from time import sleep

buzzerPIN=16
BuzzerObj = PWM(Pin(buzzerPIN))

def buzzer(buzzerPinObject,frequency,sound_duration,silence_duration):

    # Set duty cycle to a positive value to emit sound from buzzer
    buzzerPinObject.duty_u16(int(65536*0.1))
    # Set frequency
    buzzerPinObject.freq(frequency)
    # wait for sound duration
    sleep(sound_duration)
    # Set duty cycle to zero to stop sound
    buzzerPinObject.duty_u16(int(65536*0))
    # Wait for sound interrumption, if needed 
    sleep(silence_duration)


#set translation table from note to frequency
do5=523
dod5=554
re5=587
red5=622
mi5=659
fa5=698
fad5=739
sol5=784
sold5=830
la5=880
lad5=932
si5=987


buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,la5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,sold5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,do5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,la5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.5,0.1)

buzzer(BuzzerObj,sol5,0.1,0.1)
buzzer(BuzzerObj,fa5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,re5,0.5,0.1)

buzzer(BuzzerObj,fa5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,la5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

#Deactivates the buzzer
BuzzerObj.deinit()
  ~~~~
  ### * Corrida
  
  ### * Imagenes del circuito
  
  
## Reed switch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Shock

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Shock

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Ky-015 Temp 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Ky-022 IR ???eiver 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Avoidance 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito



    
