# weewx_wxPublish
weewx extension that POSTs live wx data to remote RESTful endpoint

Preconditions:

  1) Script is written for python3
  2) Assumes weewx installation from setup.py, in /home/weewx
  3) Requires use of the python-requests library: https://docs.python-requests.org/en/latest/

Installation:
-------------

  1) copy the file wxPublish.py to your local weewx installation's bin/user directory

  2) modify weewx.conf, adding:

    [StdRESTful]
      [[wxPublish]]
          host = home.example.com
          port = 8080
          prefix = wxupdate

3) restart weewx

Usage
-----
When events are received from the weather monitoring device, a POST message will be sent to the host defined in
weewx.conf, containing all weewx supported data fields:

```
{
    "humidex": 55.90412378085054,
    "heatindex": 52.292,
    "barometer": 29.977,
    "insideAlarm": 0,
    "outsideAlarm2": 0,
    "soilLeafAlarm4": 0,
    "dewpoint": 51.69067254449513,
    "sunrise": "2021-11-13 15:07:00",
    "rain24": 0.3200000000000001,
    "soilLeafAlarm2": 0,
    "windSpeed": 1.0,
    "inHumidity": 46.0,
    "extraAlarm4": 0,
    "rain": 0.0,
    "extraAlarm5": 0,
    "pressure": 29.369390359278192,
    "rainRate": 0.07,
    "extraAlarm8": 0,
    "windGust": 3.0,
    "dayRain": 0.32,
    "soilLeafAlarm1": 0,
    "rainAlarm": 0,
    "dateTime": "2021-11-14 05:17:30",
    "windchill": 52.8,
    "windDir": 283.0,
    "inDewpoint": 47.711815602745205,
    "hourRain": 0.060000000000000005,
    "sunset": "2021-11-14 00:39:00",
    "yearRain": 10.83,
    "extraAlarm7": 0,
    "maxSolarRad": 0.0,
    "altimeter": 29.973457843211353,
    "extraAlarm3": 0,
    "extraAlarm1": 0,
    "appTemp": 52.78951546692744,
    "forecastIcon": 7,
    "cloudbase": 812.1198762511063,
    "stormRain": 0.32,
    "outHumidity": 96.0,
    "extraAlarm2": 0,
    "windGustDir": 255.0,
    "monthET": 0.0,
    "extraAlarm6": 0,
    "usUnits": 1,
    "leafWet4": 0.0,
    "monthRain": 5.03,
    "outTemp": 52.8,
    "stormStart": 1636790400,
    "consBatteryVoltage": 4.73,
    "dayET": 0.0,
    "forecastRule": 93,
    "outsideAlarm1": 0,
    "txBatteryStatus": 0,
    "soilLeafAlarm3": 0,
    "inTemp": 69.4,
    "windSpeed10": 2.0,
    "yearET": 0.0
}
```

Author
------
Mike Zimmerman <mike@fishwheel.com>


Copyright
---------
Copyright 2021 Fishwheel

License
-------
Apache License, Version 2.0. See LICENSE.


Source
------
https://github.com/ampledata/weewx_wxPublish
