# weewx_fishwheel
weewx extension that POSTs live wx data to remote RESTful endpoint

Installation:
-------------

  1) Download the release from github repo https://github.com/zekim99/weewx-fishwheel to ~/Downloads/weewx-fishwheel-master.tar.gz

  2) Install with weewx's extension manager: in weewx directory run: ./setup.py --extension --install ~/Downloads/weewx-fishwheel-master.tar.gz

  3) modify weewx.conf:

    [StdRESTful]
      [[Fishwheel]]
          host = home.example.com
          port = 8080
          prefix = wxupdate

4) restart weewx

Usage
-----
When events are received from the weather monitoring device, a POST message will be sent to the host defined in 
weewx.conf, containing all weewx supported data fields:


   "monthET":0.0,
   "heatindex":38.3,
   "dayET":0.0,
   "maxSolarRad":null,
   "insideAlarm":0,
   "outsideAlarm1":0,
   "leafTemp3":null,
   "outsideAlarm2":0,
   "extraTemp2":null,
   "forecastRule":9,
   "soilLeafAlarm3":0,
   "outHumidity":45.0,
   "windSpeed10":3.0,
   "yearRain":21.51,
   "inDewpoint":38.33892530528093,
   "extraAlarm1":0,
   "extraAlarm2":0,
   "extraAlarm3":0,
   "extraAlarm4":0,
   "extraAlarm5":0,
   "extraAlarm6":0,
   "extraAlarm7":0,
   "extraAlarm8":0,
   "soilTemp1":null,
   "soilTemp2":null,
   "soilTemp3":null,
   "soilTemp4":null,
   "soilLeafAlarm2":0,
   "soilLeafAlarm4":0,
   "leafTemp4":null,
   "forecastIcon":6,
   "leafTemp2":null,
   "leafTemp1":null,
   "soilLeafAlarm1":0,
   "yearET":0.0,
   "txBatteryStatus":0,
   "appTemp":32.633349088602344,
   "dayRain":0.0,
   "outTemp":38.3,
   "windSpeed":1.0,
   "windGust":11.0,
   "pressure":29.913970479451482,
   "cloudbase":4982.008386772486,
   "rainAlarm":0,
   "rainRate":0.0,
   "humidex":38.3,
   "consBatteryVoltage":4.72,
   "monthRain":9.54,
   "dateTime":"2016-01-01 00:29:37",
   "stormRain":0.0,
   "sunrise":"2015-12-31 15:48:00",
   "windDir":63.0,
   "radiation":null,
   "stormStart":null,
   "inTemp":72.4,
   "inHumidity":29.0,
   "hourRain":0.0,
   "windGustDir":98.0,
   "barometer":30.556,
   "windchill":38.3,
   "dewpoint":18.843163098201057,
   "rain":0.0,
   "extraHumid6":null,
   "extraHumid7":null,
   "extraHumid4":null,
   "extraHumid5":null,
   "extraHumid2":null,
   "extraHumid3":null,
   "extraHumid1":null,
   "extraTemp6":null,
   "extraTemp7":null,
   "extraTemp4":null,
   "extraTemp5":null,
   "altimeter":30.515592220846926,
   "extraTemp3":null,
   "usUnits":1,
   "extraTemp1":null,
   "leafWet4":0.0,
   "leafWet1":null,
   "leafWet2":null,
   "leafWet3":null,
   "UV":null,
   "soilMoist3":null,
   "soilMoist2":null,
   "soilMoist1":null,
   "sunset":"2016-01-01 00:34:00",
   "rain24":0.0,
   "soilMoist4":null
}


Author
------
Mike Zimmerman <mike@fishwheel.com>


Copyright
---------
Copyright 2015 Fishwheel

License
-------
Apache License, Version 2.0. See LICENSE.


Source
------
https://github.com/ampledata/weewx_fishwheel
