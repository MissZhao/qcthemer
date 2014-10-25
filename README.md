#Quick Circle Themer

Quick Circle Themer is a Xposed Module which allows you to easily change the watchfaces of the LG G3 Quick Circle Case


##Theme creation
See Getting the original resources to get an Idea about the files to modify.
Once you've got your modified files, you need to package them for the app.

1. You need a clock.xml, here's an example:

  ```xml
  <?xml version="1.0" encoding="utf-8"?>
  <clock>
      <title>Awesome clock</title>
      <id>com.coolguy.awesome</id>
      <author>CoolGuy42</author>
      <description>Some description</description>
      <activate>2</activate><!--Automatically switch to second clock-->
      <replaces>
          <file>b2_quickcircle_analog_style03_hour.png</file>
          <file>b2_quickcircle_analog_style03_minute.png</file>
          <file>b2_quickcircle_analog_style03_second.png</file>
          <file>b2_quickcircle_analog_style03_bg.png</file>
      </replaces>
  </clock>
  ```
2. You should optionally provide a preview.png which will be shown in the watchface chooser
3. Now zip up all your files, in the example you would zip the following files:
```
clock.xml
preview.png   
b2_quickcircle_analog_style03_hour.png
b2_quickcircle_analog_style03_minute.png
b2_quickcircle_analog_style03_second.png
b2_quickcircle_analog_style03_bg.png
```

###Getting the original resources
1. Make sure your phone is rooted and your adb is working
2. Get your LGAlarmClock.apk from your phone:
  ```sh
  adb pull /system/priv-app/LGAlarmClock.apk LGAlarmClock.apk
  ```
3. Extract LGAlarmClock.apk
4. The original resource are in ```LGAlarmClock/res/raw-xxxhdpi/```

## Version
0.1

## Acknowledgements 
* Excilys team for [Android annotations](https://github.com/excilys/androidannotations/wiki)
* Jake Wharton for [viewpagerindicator](http://viewpagerindicator.com/).
* rovo89, Tungstwenty for [Xposed Framework](http://repo.xposed.info/)
* Yaovst for [rolexquickcircle](https://github.com/yoavst/rolexquickcircle)
* Kevin Slaton for the example watchface
