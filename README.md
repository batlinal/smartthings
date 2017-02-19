# smartthings
SmartThings apps, device handlers etc.

## [Light Police](https://github.com/batlinal/smartthings/tree/master/light-police.src)

Do your children call you the light police because you always tell them to switch off lights? Then this is for you! Install this app and then configure it to swith off lights every 5, 10 etc. minutes if it is not dark outside!

* set which bulbs you want to switch off e.g. [Hue Bulbs](http://www2.meethue.com/en-us/productdetail/philips-hue-white-and-color-ambiance---extension-bulbs)
* set which illuminance lux sensor to use e.g. [Fibaro Motion Sensor](https://www.fibaro.com/en/products/motion-sensor/)
* set how frequent the patrol interval should be e.g. check and switch off every 5, 10 etc. minutes
* set the minimum lux level before switching off lights e.g. 50 plus is a pretty cloudy day

## [Bulb Motion Sensor](https://github.com/batlinal/smartthings/tree/master/bulb-motion-sensor.src)

[Hue Motion Sensor](http://www2.meethue.com/en-us/productdetail/philips-hue-motion-sensor) is light and motion sensor used to turn on [Hue Bulbs](http://www2.meethue.com/en-us/productdetail/philips-hue-white-and-color-ambiance---extension-bulbs), but it does not have an official ST driver, and if paired directly to ST through a community driver is not as responsive as when paired to a [Hue Bridge](http://www2.meethue.com/en-hk/support/faq-categories/product/hue-bridge/).

So, this is a workaround app. Essentially it subscibes to selected bulb switch on events, and when detected sends an on command to a [uDHT](https://community.smartthings.com/t/release-universal-virtual-device-type-and-translator/47836?source_topic_id=78358) device that must be configured as a switch on input and as a motion sensor on output. Assuming that the uDHT device is selected as a motion sensor for a Smart Home Monitor automation, an alarm can sound when a Hue Bulb is switched on by a Hue Motion Sensor. 

* create a uDHT device configured as a switch on input and as a motion sensor on output
* create a Smart Home Monitor automation with the uDHT device as a motion sensor trigger
* add this app and select the bulbs you care about and the created uDHT device

Appreciate that this will not work if Lux levels are set to not respond in daylight. but this is good enough for some circustances. Based on an original ST community [thread](https://community.smartthings.com/t/hue-bulbs-as-motion-sensor-device-driver/78358).
