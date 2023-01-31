---
title: "2022.7 - A stunning performance"
date: 2022-07-06 00:00:00 +0000
dateadded: 2023-01-31 09:17:01 +0100
description: "
 Home Assistant Core 2022.7! ������ 
 This was one exciting and busy month! In case you���ve missed it, there was
a Matter in Home Assistant workshop
and a Let���s get loud! event
about bringing audio to the Open Home.
If you have missed those, it is worthwhile to check those recordings out. 
 Meanwhile, preparations are happening for the upcoming Matter and of course,
the soon-to-be-released Home Assistant Yellow! ���� More about that soon���. 
 This release is definitely representing the ���streamlining experiences���
motto we have been using. The performance improvements in this release are
once more: stunning! Furthermore, there are some wonderful new features to
explore too. 
 This release has the perfect mix! I���m sure there is something in here you
like. So without further due: Enjoy the release! 
 ../Frenck 

 
 Improved stability and performance, and Python 3.10 
 Update Z-Wave devices directly from Home Assistant 
 The about page is now beautiful too! 
 Change any weather unit to your preference 
 Labels instead of values for gauge cards segments 
 Code editors now auto-complete MDI icons 
 Filter the history panel 
 Easily convert values to booleans in templates 
 Other noteworthy changes 
 New Integrations 
 Integrations now available to set up from the UI 
 Release 2022.7.1 - July 7 
 Release 2022.7.2 - July 8 
 Release 2022.7.3 - July 10 
 Release 2022.7.4 - July 13 
 Release 2022.7.5 - July 14 
 Release 2022.7.6 - July 20 
 Release 2022.7.7 - July 26 
 Need help? Join the community! 
 Breaking Changes 
 Farewell to the following 
 All changes 
 
 Don���t forget to join our release party live stream on YouTube today at 12:00 PDT / 21:00 CET! 
  
 Improved stability and performance, and Python 3.10 
 The quest to improve the performance of Home Assistant continues. For many
releases, @bdraco has been analyzing every single aspect of
Home Assistant and manages to make it faster every single release. 
 Usually, we have a section at the end of our release notes informing you
about the performance improvements made. The improvements in this release,
however, are a big deal. 
 Our YAML &amp; JSON tooling improved, using faster libraries and methods.
JSON is used internally and for communication with the frontend, which is
A LOT snappier now. If you use lots of YAML, you will undoubtedly notice this
when starting Home Assistant or reloading things like your automations ����. 
 Devices with an integration error during startup that can self-recover
will now do that instantly as soon as the device is discovered. 
 We now use a better and faster encryption method for the HomeKit Accessory
Protocol (HAP). It improves the performance of the HomeKit, HomeKit Controller,
and Apple TV integrations and prepares Home Assistant for iOS 16. 
 Lastly, @pvizeli has been working hard to ship Home Assistant on Python 3.10!
Which also brings quite a performance improvement. If you run the Home Assistant
Operating System or use our container installation method, you will
automatically get this; there is no need to do anything. ���� 
 Update Z-Wave devices directly from Home Assistant 
 All software has bugs, including the software on your Z-Wave devices. But how
to update those? Have no fear! As of today, we have a solution for this! 
 Thanks to the hard work and collaboration between @AlCalzone from Z-Wave JS
and @raman325 from Home Assistant, you can now install updates on your
Z-Wave devices directly from the Home Assistant interface! 

 On the device page of your Z-Wave device, there is now a menu item allowing
you to install Z-Wave firmware updates onto your device manually. 
 Get a software update for your Z-Wave device from the manufacturer,
and start an update in Home Assistant, which allows you to upload the
update file you got from the manufacturer. The rest is pure magic! 

 During update installation, you���ll be presented with the update���s progress. 
 It is that easy ���� 
 The about page is now beautiful too! 
 Have you ever looked at the about page in the Home Assistant settings menu? 
 It was probably one of the least visually appealing pages still in our menus,
and @zsarnett seemed to agree. He made it a lot more cleaner and functional. 
 It now clearly shows the versions of the different components your instance is
made up of, and provides a clean menu to all kinds of Home Assistant related
links. 

  
 Change any weather unit to your preference 
 Home Assistant has many weather services that can be integrated; it is
great to have a choice! The differences between those are often their
accuracy for your region and the  units of measurement used for the
different weather data points. 
 But what if you���d like the barometric pressure unit to be in mbar instead of
hPa? Or maybe use m/s or knots instead of km/h for wind speed? No problem! 
 You can now change the units each weather entity uses! Not just temperature,
but for all of the values a weather entity provides. When changing a unit,
Home Assistant will take care of converting the values for you. 

 On a similar note, number entities that represent a temperature are now converted to
the temperature unit used by the configured unit system. 
 Thanks @emontnemery and @gjohansson-ST for adding this and updating
all existing weather integrations to support this ����. 
 Labels instead of values for gauge cards segments 
 When displaying an entity gauge card on your dashboard, it would show the
gauge with the sensor value. For example, if you���d use a humidity sensor,
it shows the humidity percentage in the middle of the gauge. 
 In the 2022.5 release, we added segment support to our gauge card.
In this release, @kristjanbjarni added label support to those segments! 
 This means that if your segment has a label, the gauge card will show
that label instead of the sensor value when it is in that range. 

 For more information, check out our gauge card documentation. 
 Code editors now auto-complete MDI icons 
 All of our code editors in the frontend now have auto-completions for
MDI icons. Just start typing mdi: and it will help you find the exact icon
you need. 

 Like the normal icon picker, it supports searching on parts of the icon
name, its aliases and categories. Additionally, it will show a little preview
of the icon you are about to select, so you know you got the right one. 
 Thank you @bramkragten, this is a really nice addition! 
 Filter the history panel 
 If you have lots of devices and entities then the
history panel can be long! Actually,
it would become so large, that it becomes unpractical. You could always
filter it down to a single entity, but that is fairly limited as well.
For this release, @D3v01dZA improved these filters. 
 The history can now be filtered by one or more entities, by all entities of
one or more areas, or by all entities of one or more devices. 

 This is super helpful, as you can now view the history of all entities in,
for example, your living room area quick and easy. 
  
 Easily convert values to booleans in templates 
 If you are into templates, @pyos has a surprise for you: We now have a bool
function that can be used as a filter too! 
 If you are a bit into coding, this is not the standard bool(), but one that
is very specific for Home Assistant, making it very useful. 
 This bool method converts a value into a boolean and considers
Home Assistant���s specific rules for truthy values. Some examples: "on" will
be considered true, and "disabled" will be considered false. 

 Using bool as a filter and combined with and iif
filter, you can quickly change, for example, binary sensors values into any
text you���d like. 
 For more information, check out our Templating documentation. 
 Other noteworthy changes 
 There is much more juice in this release; here are some of the other
noteworthy changes this release: 
 
 The Material Design Icons have been updated to v6.9.96, giving you
100 and another
100 brand new icons
to use ���� . 
 You can now control the loudness and various additional surround-related
settings of your Sonos speakers, thanks @jjlawren! ���� 
 You can now trigger Alexa routines from switches, toggles, and buttons
without the need to wrap them into a binary template sensor first.
Fantastic addition, @mdegat01! 
 The logbook live feeds will now automatically pause when you start
scrolling and resume when you are back at the top again. Thanks, @bdraco! 
 @matrixd2 extended YoLink; It now supports thermostats, valve controllers,
locks, and vibration, CO, and Smoke Sensors! 
 Jellyfin now supports movie collections in the media browser, thanks @j-stienstra! 
 Thanks to @dmulcahey, the widely discussed Aqara FP1 sensor is now
supported by ZHA! 
 @ghedo has been busy improving the Area Card. It can now show
moisture/flood alerts, humidity, and shows an icon for temperature. Nice! 
 @kingy444 added support for Top/Down, Bottom/Up to Hunter Douglas PowerView.
Additionally, buttons to calibrate and jog (identify) have been added. @bdraco
added support for polling in case the device is mains powered. 
 Thanks to @thrawnarn, you can now send polls via Telegram bot! 
 The Home Connect integration now has whole collection of new services
that can be used to control and configure options of device programs.
Really nice, @BraveChicken1! 
 If you have WiZ power plugs with power monitoring, these are now supported,
thanks to @bdraco ������. 
 @gjohansson-ST added lots of love to Sensibo this release. Support for
(split) timers, Pure Boost, improvements to setting temperature, bug fixes,
and many more. Nice work! 
 @iAutom8 made his first-time-ever open source contribution ������; And added
support for additional temperature sensors in ViCare. 
 
 New Integrations 
 This release does not include new integrations. 
 Integrations now available to set up from the UI 
 The following integrations are now available via the Home Assistant UI: 
 
 Eight Sleep, done by @raman325 
 Radio Thermostat, done by @bdraco 
 Simplepush, done by @engrbm87 
 SkyBell, done by @tkdrob 
 
 Release 2022.7.1 - July 7 
 
 Bump deCONZ dependency to v96 (@Kane610 - #74460) (deconz docs) 
 Bump satel_integra to 0.3.7 to fix compat with python 3.10 (@c-soft - #74543) (satel_integra docs) 
 fjaraskupan: Make sure we stop bleak on home assistant stop (@elupus - #74545) (fjaraskupan docs) 
 Minimize Sonos media_player.unjoin timeout (@jjlawren - #74549) (sonos docs) 
 Bump aioskybell to 22.7.0 (@tkdrob - #74559) (skybell docs) 
 Bump pyenvisalink version to 4.6 (@ufodone - #74561) (envisalink docs) 
 ElkM1 bump lib to support Python 3.10 SSL (@gwww - #74569) (elkm1 docs) 
 Fix openweathermap hourly forecast (@emontnemery - #74578) (openweathermap docs) 
 Fix mix of aiohttp and requests in Bloomsky (@frenck - #74598) (bloomsky docs) 
 Update aiokafka to 0.7.2 (@frenck - #74601) (apache_kafka docs) 
 Poll cast groups when media player is added or reconnected (@emontnemery - #74610) (cast docs) 
 Ikea Starkvind support all models (@arnemauer - #74615) (zha docs) 
 Update frontend to 20220707.0 (@bramkragten - #74625) (frontend docs) 
 Fix mix of aiohttp and requests in ZAMG (@frenck - #74628) (zamg docs) 
 Fix smart energy polling for Tuya plugs (@TheJulianJES - #74640) (zha docs) 
 Fix exception in doorbird logbook during startup (@bdraco - #74649) (doorbird docs) 
 Update kaiterra-async-client to 1.0.0 (@Michsior14 - #74677) (kaiterra docs) 
 
 Release 2022.7.2 - July 8 
 
 Add missing strings for here_travel_time (@eifinger - #74641) (here_travel_time docs) 
 Add ssh-rsa as acceptable an host key algorithm (@siyuan-nz - #74684) (unifi_direct docs) 
 Fix ZHA group not setting the correct color mode (@TheJulianJES - #74687) (zha docs) 
 Bump deconz dependency to fix #74523 (@Kane610 - #74710) (deconz docs) 
 Bump atomicwrites (@balloob - #74758) 
 Bump regenmaschine to 2022.07.0 (@bachya - #74680) (rainmachine docs) 
 Fix error with HDD temperature report in Freebox integration (@BenoitAnastay - #74718) (freebox docs) 
 
 Release 2022.7.3 - July 10 
 
 Fix Vicare One Time Charge (@oischinger - #74872) (vicare docs) 
 Fix KeyError from zwave_js diagnostics (@kpine - #74579) (zwave_js docs) 
 Update systembridgeconnector to 3.3.2 (@timmo001 - #74701) (system_bridge docs) 
 air_quality and filter_life fixes for Pur131S (@jetpacktuxedo - #74740) (vesync docs) 
 Update pyCEC to version 0.5.2 (@inytar - #74742) (hdmi_cec docs) 
 Bump pyezviz to 0.2.0.9 (@regevbr - #74755) (ezviz docs) 
 Update aioqsw to v0.1.1 (@Noltari - #74784) (qnap_qsw docs) 
 Bump python-gammu to 3.2.4 with Python 3.10 support (@PaulAnnekov - #74797) (sms docs) 
 Bump deCONZ dependency to fix #74791 (@Kane610 - #74804) (deconz docs) 
 Bump regenmaschine to 2022.07.1 (@bachya - #74815) (rainmachine docs) 
 Fixed unit of measurement. #70121 (@StephanU - #74838) (edl21 docs) 
 Bump rokuecp to 0.17.0 (@ctalkington - #74862) (roku docs) 
 Bump pymazda to 0.3.6 (@bdr99 - #74863) (mazda docs) 
 Fix Vicare One Time Charge (@oischinger - #74872) (vicare docs) 
 Bump pysml to 0.0.8 (fixes #74382) (@DavidMStraub - #74875) (edl21 docs) 
 Bump afsapi to 0.2.5 (@wlcrs - #74907) (frontier_silicon docs) 
 
 Release 2022.7.4 - July 13 
 
 Migrate ecobee to native_* (@emontnemery - #74043) (ecobee docs) 
 Migrate homematicip_cloud to native_* (@emontnemery - #74385) (homematicip_cloud docs) 
 Update pyialarm to 2.2.0 (@RyuzakiKK - #74874) (ialarm docs) 
 Correctly handle device triggers for missing ZHA devices (@Adminiuga - #74894) (zha docs) 
 Remove pip ���prefix workaround (@henryptung - #74922) 
 Fix Pyload request content type headers (@iMarkus - #74957) (pyload docs) 
 JSON serialize NamedTuple subclasses with aiohttp (@bdraco - #74971) 
 Fix mix of aiohttp and requests in ClickSend TTS (@frenck - #74985) (clicksend_tts docs) 
 Do not spam log when Life360 member location is missing (@pnbruckner - #75029) (life360 docs) 
 Upgrade huawei-lte-api to 1.6.1 (@scop - #75030) (huawei_lte docs) 
 Fix Ruckus Unleashed SSH connection failures (@gabe565 - #75032) (ruckus_unleashed docs) 
 Bump afsapi to 0.2.6 (@wlcrs - #75041) (frontier_silicon docs) 
 Bump homematicip to 1.0.4 (@hahn-th - #75053) (homematicip_cloud docs) 
 Bump AIOAladdinConnect to 0.1.23 (@mkmer - #75065) (aladdin_connect docs) 
 Fix Insteon thermostat issues (@teharris1 - #75079) (insteon docs) 
 Fix missing ordered states in universal media player (@Drafteed - #75099) (universal docs) 
 Make sure device tuple is a list on save (@elupus - #75103) (rfxtrx docs) 
 Fix Powerview top shade open position (@kingy444 - #75110) (hunterdouglas_powerview docs) 
 Bump ZHA dependencies (@puddly - #75133) (zha docs) 
 Ensure SimpliSafe diagnostics redact the code option (@bachya - #75137) (simplisafe docs) 
 Block bad pubnub version (@balloob - #75138) 
 
 Release 2022.7.5 - July 14 
 
 Address Blebox uniapi review sidenotes (@riokuu - #74298) (blebox docs) 
 Fix Alexa: Only trigger doorbell event on actual state change to ���ON��� (@Tho85 - #74924) (alexa docs) 
 Fix Blebox light scenes (@riokuu - #75106) (blebox docs) 
 Fix playback of hls cameras in stream (@uvjustin - #75166) (stream docs) 
 Bump version of pyunifiprotect to 4.0.10 (@AngellusMortis - #75180) (unifiprotect docs) 
 Bumped AIOAladdin Connect to 0.1.24 (@mkmer - #75182) (aladdin_connect docs) 
 Bump zigpy from 0.47.2 to 0.47.3 (@puddly - #75194) (zha docs) 
 Skip iso4217 version 1.10, which includes a broken __init__.pyi file (@puddly - #75200) 
 Fix Hive power unit of measurement (@KJonline - #75210) (hive docs) 
 Bump frontend to 20220707.1 (@zsarnett - #75232) (frontend docs) 
 Bump AIOAladdinConnect to 0.1.25 (@mkmer - #75235) (aladdin_connect docs) 
 Bump pylitterbot to 2022.7.0 (@natekspencer - #75241) (litterrobot docs) 
 Remove nest mac prefix that matches cast devices (@allenporter - #75108) (nest docs) 
 
 Release 2022.7.6 - July 20 
 
 Fix ZHA light turn on issues (@dmulcahey - #75220) (zha docs) 
 Fix aruba ssh host key algorithm (@apaperclip - #75224) (aruba docs) 
 Force _attr_native_value to metric in bmw_connected_drive (@rikroe - #75225) (bmw_connected_drive docs) 
 Bump venstarcolortouch to 0.18 (@craftyguy - #75237) (venstar docs) (dependency) 
 Improve UniFi Protect unauth handling (@AngellusMortis - #75269) (unifiprotect docs) 
 Update pyotgw to 2.0.0 (@mvn23 - #75285) (opentherm_gw docs) (dependency) 
 Add fixes for hive light (@KJonline - #75286) (hive docs) 
 Bump bimmer_connected to 0.10.1 (@rikroe - #75287) (bmw_connected_drive docs) (dependency) 
 Bump simplisafe-python to 2022.07.0 (@bachya - #75294) (simplisafe docs) (dependency) 
 Upgrade ness_alarm dependencies (@nickw444 - #75298) (ness_alarm docs) 
 Use the orjson equivalent default encoder when save_json is passed the default encoder (@bdraco - #74377) 
 Use default encoder when saving storage (@bdraco - #75319) 
 Apply filter to libav.hls logging namespace (@uvjustin - #75330) (stream docs) 
 Handle (and better log) more AirVisual cloud API errors (@bachya - #75332) (airvisual docs) 
 Fix HKC device triggers (@bdraco - #75371) (homekit_controller docs) 
 Bump AIOAladdinConnect to 0.1.27 (@mkmer - #75400) (aladdin_connect docs) (dependency) 
 Bump pytomorrowio to 0.3.4 (@raman325 - #75478) (tomorrowio docs) (dependency) 
 Bump pySwitchbot to 0.14.1 (@pascalwinters - #75487) (switchbot docs) (dependency) 
 Fix Netgear update entity (@starkillerOG - #75496) (netgear docs) 
 Fix - Forcast.solar issue on saving settings in options flow without api key (@klaasnicolaas - #75504) (forecast_solar docs) 
 Fix failure to raise on bad YAML syntax from include files (@bdraco - #75510) 
 Fix incorrect Ambient PWS lightning strike sensor state classes (@bachya - #75520) (ambient_station docs) 
 Bump aioshelly to 2.0.1 (@thecode - #75523) (shelly docs) (dependency) 
 
 Release 2022.7.7 - July 26 
 
 Fix hvv departures authentication (@vigonotion - #75146) (hvv_departures docs) 
 Fix Epson wrong volume value (@pszafer - #75264) (epson docs) 
 Change monoprice config flow to sync (@OnFreund - #75306) (monoprice docs) 
 Round up for stream record lookback (@uvjustin - #75580) (stream docs) 
 Revert SimpliSafe auth flow to the quasi-manual OAuth method from 2021.11.0 (@bachya - #75641) (simplisafe docs) 
 Update pyotgw to 2.0.1 (@mvn23 - #75663) (opentherm_gw docs) (dependency) 
 Fix AssertionError in RainMachine (@bachya - #75668) (rainmachine docs) 
 
 Need help? Join the community! 
 Home Assistant has a great community of users who are all more than willing
to help each other out. So, join us! 
 Our very active Discord chat server is an excellent place to be
at, and don���t forget to join our amazing forums. 
 Found a bug or issue? Please report it in our issue tracker,
to get it fixed! Or, check our help page for guidance for more
places you can go. 
 Are you more into email? Sign-up for our Building the Open Home Newsletter
to get the latest news about features, things happening in our community and
other news about building an Open Home; straight into your inbox. 
 Breaking Changes 
 Below is a listing of the breaking change for this release, per subject or
integration. Click on one of those to read more about the breaking change
for that specific item. 

 
   
    
      Python 3.10 
       
      
      
       
    
     
 Home Assistant now ships with Python 3.10 for the following installation methods: 
 
 Home Assistant Operating System 
 Home Assistant Container 
 Home Assistant Supervised 
 
 You don���t have to do anything; this will all happen automatically. However,
this might be a breaking change in case you are using custom integration
that does not support Python 3.10 yet. 
 (@pvizeli - #73830) (documentation) 
 
   
 

 
   
    
      Bluetooth (multiple integrations) 
       
      
      
       
    
     
 Home Assistant is upgrading to Python 3.10 this release and comes
with a breaking change affecting multiple integrations. 
 Known affected integrations at the time of writing: 
 
 BeeWi SmartClim BLE sensor 
 Bluetooth Tracker 
 Elgato Avea 
 EQ3 Bluetooth Smart Thermostats 
 Leviton Decora 
 Mi Flora 
 Switchmate SimplySmart Home 
 Zengge 
 
 These integrations rely on the bluepy and pybluez libraries, which no longer
work in newer versions of Python. bluepy has seen its last update in
December 2018 and hasn���t
kept up with changes in the Python world.
Similar story with pybluez. 
 We can���t mitigate this issue. If you are using one of these integrations,
these will no longer work. We rather wanted to see a non-breaking solution,
but we saw no backward compatible path or other solutions to aid this. 
 If you would like to help fix or upgrade one of these integrations, we
would be grateful. We recommend migrating these integrations onto the
Bleak library instead. 
 (@pvizeli - #73830) (documentation) 
 
   
 

 
   
    
      Entity filters (multiple integrations) 
       
      
      
       
    
     
 All entity filters, as used by the following integrations: 
 
 Apache Kafka 
 Azure Event Hub 
 Google Pub/Sub 
 History 
 InfluxDB 
 Logbook 
 Recorder 
 
 Have been adjusted to make entity filters handle includes stronger than excludes. 
 Filters are now applied as follows when there are domain and glob includes
(may also have excludes): 
 
 Entity listed in entities include: include 
 Otherwise, entity listed in entities exclude: exclude 
 Otherwise, entity matches glob include: include 
 Otherwise, entity matches glob exclude: exclude 
 Otherwise, entity matches domain include: include 
 Otherwise: exclude 
 
 (@bdraco - #74080) (documentation) 
 
   
 

 
   
    
      Weather (multiple integrations) 
       
      
      
       
    
     
 This applies to all (weather) integrations providing weather entities. 
 Previously the units for Weather had not been corresponding correctly with
the documentation. These units are now aligned for pressure and wind speed: 
 
 If the unit system is metric, the default pressure unit is hPa,
and the default wind speed unit is km/h. 
 If the unit system is imperial, the default pressure unit is inHg,
and the default wind speed unit is mi/h. 
 
 (@gjohansson-ST - #73707) (documentation) 
 
   
 

 
   
    
      Eight Sleep 
       
      
      
       
    
     
 The Eight Sleep integration migrated to configuration
via the UI. Configuring Eight Sleep via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration is automatically imported on upgrade to this
release; and thus can be safely removed from your YAML configuration
after upgrading. 
 (@raman325 - #72570) (documentation) 
 
   
 

 
   
    
      Glances 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Glances
integration has been removed. 
 Glances is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@engrbm87 - #72706) (documentation) 
 
   
 

 
   
    
      Google Calendars 
       
      
      
       
    
     
 The Google Calendar google.scan_for_calendars service has been removed.
Similar functionality can be achieved with the
homeassistant.reload_config_entry service, which will reload the
integration and load all new calendars from the API. 
 (@allenporter - #73010) (documentation) 
 
 The Google Calendar add_event service is deprecated and will be removed in
a future Home Assistant release. 
 A new service create_event with equivalent functionality is its replacement,
which is an entity-based service that takes an entity as a target
(rather than a Google Calendar ID). 
 (@allenporter - #72473) (documentation) 
 
 Google Calendars no longer supports entity customizations in the UI
when google_calendars.yaml specifies the same entity multiple times. 
 (@allenporter - #73715) (documentation) 
 
   
 

 
   
    
      Hunter Douglas PowerView 
       
      
      
       
    
     
 Top Down/Bottom Up shades will now have an entity to control each motor.
You will need to manually remove any old entities by selecting the unavailable
entities from the Home Assistant Interface, selecting ���REMOVE ENTITY���, and
then confirming the removal by clicking ���REMOVE���. 
 
 If you have automations to set shade position based on entity ID, you will
need to reconfigure these as the new entities will be named differently. 
 If you only have automations set to trigger scenes you do not need to
reconfigure automations. 
 
 (@kingy444 - #62788) (documentation) 
 
   
 

 
   
    
      Islamic Prayer Times 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Islamic Prayer Times
integration has been removed. 
 Islamic Prayer Times is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@engrbm87 - [#7287248332]) (documentation) 
 
   
 

 
   
    
      Kostal Plenticore 
       
      
      
       
    
     
 The Kostal Plenticore now has number entities. Two existing sensors entities
have been promoted to this platform: ���Battery min Soc��� and
���Battery min Home Consumption���. 
 If you use these sensors entities in your automation, scripts, or dashboards,
you will need to adjust these for this change. 
 (@stegm - #64927) (documentation) 
 
   
 

 
   
    
      LG Soundbars 
       
      
      
       
    
     
 The LG Soundbars integration migrated to configuration
via the UI. The automatic discovery of the integration via legacy discovery
has been removed. 
 This change has no possible migration path; therefore, if you use this
integration, you will have to re-add it manually via the user interface. 
 (@MasonCrawford - #71153) (documentation) 
 
   
 

 
   
    
      Life360 
       
      
      
       
    
     
 Overview 
 The Life360 integration has been converted from the old ���legacy���
implementation (which uses known_devices.yaml) to the newer entity based
design, similar to what was done back in the 0.94.0 release to many other
device tracker integrations. 
 Due to this change, all your existing Life360 entities will become
non-functional, and there will be new entities, with different entity IDs,
that are functional. 
 Steps to replace old entities with new ones 
 
 Edit the known_devices.yaml file in your configuration directory to
remove any Life360-related entries. Or, if there are only Life360 entries in
this file, simply delete the file entirely. 
 Restart Home Assistant. All the old, non-functional Life360 entities
should now be gone. (If you are still seeing the old entities, try refreshing
your browser.) 
 Go to the Entities page (under Settings -&gt; Devices &amp; Services -&gt; Entities)
and change the entity IDs for the new Life360 entities as desired. 
 
 Removed/changed functionality 
 The previously deprecated YAML configuration of the Life360
integration has been removed. 
 Life360 is now configured via the UI. Any ���advanced��� options in
YAML configuration will be imported. Once the migration is complete,
any life360 entries in YAML configuration should be removed. 
 The following options are no longer supported: 
 
 circles 
 members 
 error_threshold 
 warning_threshold 
 max_update_wait (including the life360_update_overdue &amp; life360_update_restored events) 
 show_as_state: moving 
 
 Additionally, the following entity attributes have been changed: 
 
 Renamed: battery -&gt; battery_level 
 Removed: moving, raw_speed 
 
 If you have been using these attributes in your automations or script, you���ll
need to adapt them to this change. 
 (@pnbruckner - #72461 #73904) (documentation) 
 
   
 

 
   
    
      Mazda Connected Services 
       
      
      
       
    
     
 The start_engine, stop_engine, turn_on_hazard_lights,
turn_off_hazard_lights, start_charging, and stop_charging services are
removed from the Mazda integration. 
 They were deprecated in 2022.4 and replaced by button and switch entities. 
 (@bdr99 - #73403) (documentation) 
 
   
 

 
   
    
      Met Office 
       
      
      
       
    
     
 Met Office doesn���t provide precise visibility distance, only ranges - i.e.,
something like ���Very good - 20-40 km���. 
 This doesn���t fit into the weather entity model, so it���s now removed.
The old value is still available in a separate sensor provided
by this integration. 
 (@avee87 - #74314) (documentation) 
 
   
 

 
   
    
      Mikrotik 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Mikrotik
integration has been removed. 
 Mikrotik is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@engrbm87 - #72581) (documentation) 
 
   
 

 
   
    
      MySensors 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the MySensors
integration has been removed. 
 MySensors is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@MartinHjelmare - #72761) (documentation) 
 
   
 

 
   
    
      Nest 
       
      
      
       
    
     
 The Nest authentication method called ���Desktop���, ���Installed App��� or ���OOB��� auth
has been deprecated
by Google and is scheduled to break existing users in October. 
 As a result, the Home Assistant Nest integration setup has been streamlined
to help make the transition easier for users. See the integration
documentation for details. 
 The configuration of the OAuth application credentials for the Nest integration
has migrated to configuration via the UI. Configuring Nest OAuth application
credentials via YAML configuration has been deprecated and will be removed in
a future Home Assistant release. 
 If you were already using Web Auth, your existing Nest application credentials
in the YAML configuration are automatically imported on upgrade to this release;
and thus can be safely removed from your YAML configuration after upgrading. 
 (@allenporter - #73050) (documentation) 
 
   
 

 
   
    
      Notifications for Android TV / Fire TV 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Notifications for
Android TV / Fire TV integration has been removed. 
 Notifications for Android TV / Fire TV is now configured via the UI,
any existing YAML configuration has been imported in previous releases and
can now be safely removed from your YAML configuration files. 
 (@engrbm87 - #73227) (documentation) 
 
   
 

 
   
    
      NZBGet 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the NZBGet
integration has been removed. 
 NZBGet is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@epenet - #72424) (documentation) 
 
   
 

 
   
    
      Radio Thermostat 
       
      
      
       
    
     
 The Radio Thermostat integration migrated to configuration
via the UI. Configuring Radio Thermostat via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration is automatically imported on upgrade to this
release; and thus can be safely removed from your YAML configuration
after upgrading. 
 (@bdraco - #72874) (documentation) 
 
 Radio Thermostat���s hold mode is now configured using a switch. This replaces
the original YAML configuration option named hold_temp. 
 The integration now only synchronizes time when loaded if the hold mode
is not active. Synchronizing the time when the hold mode is active causes
the hold mode to disable unexpectedly. 
 (@bdraco - #73104) (documentation) 
 
   
 

 
   
    
      Scrape 
       
      
      
       
    
     
 The default scan interval of the scape sensor has been changed from 30 seconds
to a more reasonable 10 minutes; This prevents unneeded hammering of
websites by default. 
 (@balloob - #74285) (documentation) 
 
   
 

 
   
    
      Simplepush 
       
      
      
       
    
     
 The Simplepush integration migrated to configuration
via the UI. Configuring Simplepush via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration is automatically imported on upgrade to this
release; and thus can be safely removed from your YAML configuration
after upgrading. 
 (@engrbm87 - #73471) (documentation) 
 
   
 

 
   
    
      SkyBell 
       
      
      
       
    
     
 The SkyBell integration migrated to configuration
via the UI. Configuring SkyBell via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration is automatically imported on upgrade to this
release; and thus can be safely removed from your YAML configuration
after upgrading. 
 After upgrading, each Skybell will now have a device for each doorbell.
Also, it has become unnecessary to prefix all entities with ���SkyBell���,
this may change you existing entities after upgrading and you need to adjust
your automation, scripts and dashboard for this change. 
 (@tkdrob - #70887) (documentation) 
 
 The following SkyBell entity attributes have been split out into their own
sensors: last motion event, last button event, last check-in, motion threshold,
video profile, Wi-Fi SSID, Wi-Fi status. 
 If you rely on these attributes in your automations or scripts, you will need
to adapt them to this change. 
 (@tkdrob - #73089) (documentation) 
 
   
 

 
   
    
      SmartThings 
       
      
      
       
    
     
 The following power entity attributes from the climate entity for SmartThings
Air Conditioner have been removed and added as separate sensors: 
 
 power_consumption_start 
 power_consumption_end 
 power_consumption_power 
 power_consumption_energy 
 
 If you currently use these attributes in your automation or scripts,
you���ll need to adapt them to this change. 
 (@mbo18 - #72594) (documentation) 
 
   
 

 
   
    
      SMS notifications via GSM-modem 
       
      
      
       
    
     
 GSM signal sensor entity was replaced with a set of more granular ones.
The old entity will become unavailable after updating to this release. 
 (@PaulAnnekov - #70486) (documentation) 
 
   
 

 
   
    
      System Bridge 
       
      
      
       
    
     
 
 This integration now requires System Bridge 3.1.2 and above. Any older
version will no longer work. 
 BIOS Version, Idle, System, and User Load sensors have been removed.
These are no longer available from System Bridge data modules. 
 Command service has been removed. This has been removed from System Bridge
due to potential security issues. 
 Open path and URL are now separate services. If you are using the
old system_bridge.open service, you will need to update your
automation to use the new service(s). 
 GPU entities are from a new source, so they may have changed names slightly.
Any automations using these entities may need to be updated. 
 GPU fan speed is now measured in RPM instead of %. 
 
 (@timmo001 - #71218) (documentation) 
 
   
 

 
   
    
      Tautulli 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Tautulli
integration has been removed. 
 Tautulli is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@ludeeus - #74172) (documentation) 
 
 Entity attributes of Tautulli entities have now been moved to their own sensors. 
 If you currently use these attributes in your automation or scripts,
you���ll need to adapt them to this change. 
 (@tkdrob - #71712) (documentation) 
 
   
 

 
   
    
      Transmission 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Transmission
integration has been removed. 
 Transmission is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@engrbm87 - #72832) (documentation) 
 
   
 

 
   
    
      UniFi Protect 
       
      
      
       
    
     
 The new disk sensors pull from completely different data than the old ones.
They should be largely compatible for functionality, but orphaned sensors may
still be created. Any orphaned sensors can be safely deleted. 
 The sensors��� naming format has also changed to match what is shown in UniFi
Protect. Additionally, the extra state attribute for the model has
been completely removed since now the slot numbers match what UniFi
Protect displays. 
 (@AngellusMortis - #73104) (documentation) 
 
 Entities that provided an ���edit��� configuration interface for Protect devices
(like the HDR Switch or Recording Mode Select) have all now been replaced by
regular sensor entities; if you do not have write access to that UniFi Protect
Device. 
 These switches, select entities, etc., never actually worked previously since
the user did not have permission to change them, but you could read the status. 
 Any entities that are orphaned by this can be safely deleted. 
 (@AngellusMortis - #73765) (documentation) 
 
   
 

 
   
    
      Universal Media Player 
       
      
      
       
    
     
 An ���order of importance��� between the states of the children of
Universal Media Player has been added. The active media player might change
if some of the children are in ���playing��� and ���paused��� states,
depending on the children���s order. 
 (@koying - #68036) (documentation) 
 
   
 

 
   
    
      UPnP/IGD 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the UPnP/IGD
integration has been removed. 
 UPnP/IGD is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@epenet - #72410) (documentation) 
 
   
 

 
   
    
      VeSync 
       
      
      
       
    
     
 The air_quality and filter_life attributes have been removed from the fan
entities. Dedicated sensor entities have replaced these attributes. 
 If you are currently using these attributes in your automation or scripts,
you���ll need to adapt them to this change. 
 (@jetpacktuxedo - #72658) (documentation) 
 
 Vesync switches that support energy monitoring will have their: 
 
 Voltage attribute moved from the switch entity to a dedicated Voltage Sensor
entity 
 Weekly, monthly and yearly moved from the switch entity attributes into new
energy sensors. 
 
 If you used these entity attributes in your automation or scripts, you���d need
to adapt them to this change. 
 (@b3nj1 - #72570) (documentation) 
 
   
 

 
   
    
      Z-Wave JS 
       
      
      
       
    
     
 With this release, you will need to update your zwave-js-server instance. 
 
 If you use the zwave_js add-on, you need at least version 0.1.64. 
 If you use the Z-Wave JS 2 MQTT add-on, you need at least version 0.44.0. 
 If you use the zwavejs2mqtt Docker container, you need at least version 6.13.0. 
 If you run your own Docker container or some other installation method,
you will need to update your zwave-js-server instance to at least 1.20.0. 
 
 (@raman325 - #73707 #73904) (documentation) 
 
   
 
 If you are a custom integration developer and want to learn about breaking
changes and new features available for your integration: Be sure to follow our
developer blog. The following are the most notable for this release: 
 
 Avoiding reloading config entries while they are setting up 
 Deprecating Data Entry Flow constants 
 Number entity refactoring to support unit conversion 
 Weather entity refactoring to support unit conversions 
 
 Farewell to the following 
 The following integrations are also no longer available as of this release: 
 
 iAlarm XR has been removed on request by Antifurto365 (manufacturer). 
 Somfy has been previously deprecated and now removed. Its cloud API was
shut down on June 21st, 2022. Use the Overkiz integration
as a replacement. 
 
 All changes 
 Of course, there is a lot more in this release. You can find a list of
all changes made here: Full changelog for Home Assistant Core 2022.7 
"
link: "https://www.home-assistant.io/blog/2022/07/06/release-20227/"
category:
---
