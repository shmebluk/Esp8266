# Arduino 项目代码相关说明

#### Net_Weather_2.0.ino

更新了天气图标，可以显示12种天气图标，天气状况描述改为从Jason数据中直接获取。

尚未解决的问题：星期信息显示异常。

​							由于时区原因，需要 Hour + 8 得到实际时间，但是星期使用的是英文缩写，无法通过简单的加减转换，							希望有看到这个代码的大佬帮忙解决一下。

​							有一个想法是在 Hour + 8 后，判断是否大于24，若为真，通过switch()  case{} 来解决。

可能存在的问题：由于Jason中时间信息是需要改为上海时区的，所以直接在获取到的 int Time + 8 ；

​							导致一系列时间逻辑问题，可能存在日期显示与实际日期不相符的情况。



------

#### Net_Weather.ino

使用ESP8266开发板从网络（心知天气）获取最近三天的天气信息，并显示在OLED 屏幕上。

------

#### Blynk_DHT11_D1wifi_Web.ino

D1wifi模块读取DHT11温湿度传感器的数据，并上传到Blynk服务器，可以通过App端查看相关信息。

------

#### Blynk_DS18b20_W5100_web.ino

ArduinoUNO + W5100网络扩展模块 + DS18b2温度传感器， 读取传感器信息上传到Blynk服务器。