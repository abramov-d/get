import RPi.GPIO as GPIO
import time
import random

GPIO.setmode(GPIO.BCM)

dac = 26, 19, 13, 6, 5, 11, 9, 10

GPIO.setup(dac, GPIO.OUT)

number = []
for i in range(len(dac)):
    i = random.randint(0, 1)
    number.append(i)
    i = i + 1

GPIO.output(dac, number)

print(number)

time.sleep(10)

GPIO.output(dac, 0)

GPIO.cleanup()