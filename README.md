# smartthings
SmartThings apps, device handlers etc.

## [Light Police](https://github.com/batlinal/smartthings/tree/master/light-police.src)

Do your children call you the light police because you always tell them to switch off lights? Then this is for you! Install this app and then configure it to auto-switch-off lights!

* select the bulbs you want to switch off
* how frequent the patrol interval should be e.g. check and switch off every 5, 10 etc. minutes
* which illuminance lux sensor to use e.g. [Fibaro Motion Sensor](https://www.fibaro.com/en/products/motion-sensor/)  
* the lux level e.g. 50 plus is a pretty cloudy day.

## [Bulb Motion Sensor](https://github.com/batlinal/smartthings/tree/master/bulb-motion-sensor.src)

Thanks very much. I find ST not as responsive as the Hue bridge, so I did not want to connect Hue motion sensor to ST. Instead I wanted to create a virtual motion sensor, I used the excellent uDTH as you suggested, and trigger it whenever one of the Hue bulbs was switched on. Nice and simple. Appreciate that this will not work if Lux levels are set etc. but this is good enough for.

First create a [uDHT](https://community.smartthings.com/t/release-universal-virtual-device-type-and-translator/47836?source_topic_id=78358) device, enabled it as a switch input and motion sensor output. Install the app, select the bulbs you care about and the created uDHT device. Then on Smart Home Monitor create a custom rule to sound alarm etc. based on the uDHT motion sensor.



Based on on original ST community [thread](https://community.smartthings.com/t/hue-bulbs-as-motion-sensor-device-driver/78358).
