``home-assistant-custom-components`` include some custom components I wrote for my implementation of home-assistant - the open-source home automation platform.

Learn more about the [Home-assistant platform](https://home-assistant.io/)


# Included Components

## Sensibo

For my smart thermostat [Sensibo](https://www.sensibo.com/) I created 3 different components you can choose from:

* **Switch** - (``sensiboswitch``) a simple on/off switch that turns Sensibo on or off using the existing settings (this will be very easy to use as action for automation rules)
* **Sensor** - (``sensibosensor``) this will query the temperature / humidity from Sensibo at specific intervals and you can check this data on the dashboard / use it for automation rules as trigger / condition etc.
* **Climate** - this is a standard climate control component for Home-assistant that includes updated information similar to sensors, allows you to change the settings of the AC (hot / cold... fan speed etc.) but also allows you to set a temperature range (min - max) and automate on/off accordingly.
  * ``sensibosettingsandswitch`` includes on/off switch in operation selection
  * ``sensibosettingsonly`` only allows you to change the AC settings (for on/off use the switch mentioned above)
  
    These are just two implementations for climate components I was playing with - chose the one you prefer (no need to setup both!)

## Pushover - Glances
While Home-Assistant already had a [notification platform implementation for pushover](https://home-assistant.io/components/notify.pushover/), at present it's only for sending push notifications...

My implementation of the ["Glances" API](https://pushover.net/api/glances) allows you to send information directly to Apple Watch face (not as push). 

* **Notify** - (``pushoverglances``) will let you connect the service and set it up so you can send *count numeric messages* to the little info placeholder and  *short text messages* to the the larger placeholder

**You will want to get [The Pushover App](https://itunes.apple.com/us/app/pushover-notifications/id506088175?mt=8&at=1010l3fx) from the Apple app store if you haven't already...**

![Apple-Watch-Example](/images/apple-watch-with-pushover-glances.PNG?raw=true "Apple Watch with Home-Assistant Data via Pushover Glances")