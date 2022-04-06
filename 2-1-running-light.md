import RPi.GPIO as GPIO
import time

GPIO.setmode(GPIO.BCM)
#leds1 = 26, 19, 13, 6, 5, 11, 9, 10
leds = 21, 20, 16, 12, 7, 8, 25, 24
GPIO.setup(leds, GPIO.OUT)

#GPIO.setup(leds1, GPIO.OUT)
#GPIO.output(leds1, 0)

for i in range(0, 3) :
    for leds in 21, 20, 16, 12, 7, 8, 25, 24 :
        GPIO.output(leds, 1)
        time.sleep(0.2)
        GPIO.output(leds, 0)
        i = i + 1

GPIO.cleanup()