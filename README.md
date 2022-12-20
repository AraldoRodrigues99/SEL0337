from requests import get
import json
from pprint import pprint
from picamera import PiCamera, Color
import time

weather = 'https://apex.oracle.com/pls/apex/raspberrypi/weatherstation/getlatestmeasurements/'

station_id = 966583 # ufsc

weather = weather + str(station_id)

weather_now = get(weather).json()['items']

camera = PiCamera() 
camera.rotation = 180 # rotate 
camera.framerate = 15 #adjust framerate

camera.start_preview(alpha = 250) # alpha test

camera.brightness = 50
camera.image_effect = 'colorswap' #change color

camera.annotate_text = "10788742"
camera.annotate_text_size = 50

time.sleep(5)

camera.stop_preview()

camera.capture("/home/sel/pratica_camera.jpg") # nome da foto

camera.start_recording("/home/sel/video_pratica_camera.h264") # gravar 

time.sleep(10)

camera.stop_recording()

time.sleep(5)

print(weather_now)

