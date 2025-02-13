# SwitchBot RGB+CT E26 W1401400

5 Channel RGB+CT E26 800 lumen bulb with an ESP32-C3.  This smart bulb can currently be upgraded via the SwitchBot OTA process - [GitHub](https://github.com/kendallgoto/switchbota) or [digiblurDIY Video](https://youtu.be/iTexFQ0Th0I), no soldering or manual flashing invovled.  

Purchase via [Amazon](https://amzn.to/38Vhuv3)  
Purchase via [SwitchBot Store](https://switchbot.vip/3mkXt45)

Supported in Tasmota 12.0.2.2 or later, use this [Tasmota bin file](/firmware/tasmota32c3_2022_06_26.bin) until the next standard Tasmota release. Thanks to Cossid for his [efforts](https://github.com/arendst/Tasmota/pull/15839)!  
Please note the required SetOption below for correct color order.  A user configurable brightness limit of default of 9 is set via the template SM2335 Dat option.  This was found to be close to stock as possible.  Setting this higher could create power supply issues, excessive **heat/fire**, LED flame out errors, etc.

Until the next Tasmota standard release, it is necessary to upgrade to 12.0.2.2 or later dev version.  Paste the following command on the Tasmota Console, do NOT interrupt it during the upgrade.  

<iframe allowfullscreen height="353" src="https://www.youtube.com/embed/iTexFQ0Th0I" width="625" youtube-src-=""></iframe>  

#### Quick Setup via Tasmota Console Command
```
backlog template {"NAME":"Switchbot E26 Bulb","GPIO":[0,0,0,0,9128,9088,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],"FLAG":0,"BASE":1}; module 0; so37 25; so59 1
```

#### Tasmota Template
```json
{"NAME":"Switchbot E26 Bulb","GPIO":[0,0,0,0,9128,9088,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],"FLAG":0,"BASE":1}
```

<details><summary>GPIO Layout</summary>     
<p>

| GPIO |    Component | Description |
|------ |-------------|-------------|         
|GPIO04	| SM2335 Dat | Data - Brightness limit - Default 9
|GPIO05	| SM2335 Clk | Clock
</p></details>


<details><summary>Settings</summary>     
<p>

| Setting | Description
|---------------|-------------
| setoption37 25 | Set the correct RGB+CT order
| setoption59 1  | Report light state changes via MQTT
</p></details>

<details><summary>Rules</summary>     
<p>
None necessary.
</p></details>

<details><summary>ESPHome YAML</summary>     
<p>

```yaml
Currently not supported.
```
</p></details>

![alt text](/img/devices/switchbot_bulb1.jpg "SwitchBot RGB+CT E26 W1401400 #1")

![alt text](/img/devices/switchbot_bulb2.jpg "SwitchBot RGB+CT E26 W1401400 #2")

![alt text](/img/devices/switchbot_bulb3.jpg "SwitchBot RGB+CT E26 W1401400 #3")

![alt text](/img/devices/switchbot_bulb4.jpg "SwitchBot RGB+CT E26 W1401400 #4")