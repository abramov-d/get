```
import RPi.GPIO as GPIO
import time

GPIO.setmode(GPIO.BCM)

leds = 21, 20, 16, 12, 7, 8, 25, 24
aux = 22, 23, 27, 18, 15, 14, 3, 2
a = 777

GPIO.setup(leds, GPIO.OUT)
GPIO.setup(aux, GPIO.IN)

while a == 777:
    GPIO.output(leds, aux)
    #time.sleep(1)
``` 