---
title: "2022.6 - Gaining new insights!"
date: 2022-06-01 00:00:00 +0000
dateadded: 2023-01-31 09:17:01 +0100
description: "  
 ����  Hi there, Home Assistant Core 2022.6! 
 The June release brings insights! Insights on how you are doing with your
energy usage, and insights into what all the devices in your home are up to! 
 But that is not all June has to bring. Besides this release and the release party,
we have two additional events lined up for you this month! 
 On June 15, we will be hosting a Matter in Home Assistant workshop! 
 The workshop will show you what we���ve been up to and allow you to actually test it out by adding your first Matter device to your own instance!
I���m excited for this one; I���ve ordered the parts listed in the workshop details
for myself ����. 
 The day after, June 16, the second event: Let���s get loud! 
 This event is all about a new approach to home audio and music in an open
solution that values the Open Home. Join this event for the latest news and
audio demos from Home Assistant, ESPHome,
Raspiaudio, and��� something new! 
 Also: Hi Jacqueline Raaflaub! ���� Jacqueline has joined
Nabu Casa; she will help out with support and assist in moderating our community.
We are excited to have you, and welcome! 
 Anyways, this Home Assistant Core release is a nice release with a couple of
new features and lots of cleanups under the hood. Together with the upcoming
events, this is going to be one exciting month! 
 Enjoy the release (and upcoming events)! 
 ../Frenck 

 
 Comparing data in the energy dashboard 
 Logbooks have never been better! 
 Streamlining the OAuth2 experience 
 Calendar triggers with offsets 
 Improved scene editor 
 Database performance 
 Other noteworthy changes 
 New Integrations 
 Integrations now available to set up from the UI 
 Release 2022.6.1 - June 2 
 Release 2022.6.2 - June 4 
 Release 2022.6.3 - June 6 
 Release 2022.6.4 - June 7 
 Release 2022.6.5 - June 10 
 Release 2022.6.6 - June 14 
 Release 2022.6.7 - June 22 
 Need help? Join the community! 
 Breaking Changes 
 Farewell to the following 
 All changes 
 
 Missed our release party live stream on YouTube? Don���t worry! You can watch
the recording of it right here! 
  
 Comparing data in the energy dashboard 
 Did you use less or more energy than��� Yesterday? Last week? Month? Year?
We all want to know if we are on the right track, right? 
 This release introduces the capability to compare energy data against the
previous period directly from the energy dashboard! 
 Clicking the ���Compare data��� button in the top right of your
energy dashboard will instantly compare the period you
are currently viewing with the same period before that. It adds the
previous period to the graphs using a lighter bar color. 

 In the above screenshot, my energy usage of this week is compared with the week
before; since, a week is selected as the period to view. 
 The same also works for other graphs; for example, the screenshot below
shows the solar energy production for today compared with yesterday. 

  
 Logbooks have never been better! 
 The logbook received a significant overhaul this release. The backend of the
logbook got a lot of optimizations. Data processing has been polished and
optimized to make logbooks load super fast, creating an experience
that is as smooth as possible. 
 We added the logbook to more places as well. It is now shown on device and
area pages. That way, you can instantly see the last activity for that specific
device or, in case of an area, of all the devices in that area. 
 And on top of all that: Logbooks are now live! You can see events live on your
screen, while the logbook updates instantly when events are happing! 
 

The logbook on this device page, when motion is detected the logbook updates in real-time.
 
 Also new: The logbook can now show device events too! This is helpful
for entity-less logs, like device events of button presses. deCONZ,
Elk-M1 Control, Philips Hue, Lutron Cas��ta, Shelly,
and the Mobile App added support for this new feature. 
 Thanks @bdraco, for your hard work on the logbooks! 
 Streamlining the OAuth2 experience 
 Home Assistant has quite a few integrations that use the OAuth2 standard
to authenticate your Home Assistant instance with a third-party service. Some
examples are Home Connect, Spotify, Netatmo, Xbox, Withings, and Google Calendars. 
 OAuth2 can be pretty complex, as services often implement additional
requirements on top of the OAuth2 specifications. So, if ���OAuth Redirect URI���
gives you the shivers, you definitely will know what drama we are talking about.
Additionally, for most, you need to register a developer account, create
an application, get the client ID and secret and configure YAML ���� 
 This release aims to make this all easier and streamline this experience A LOT. 

 @allenporter has been busy adding support for managing OAuth2
application credentials directly from the UI! (screenshot above.) This removes
the need to edit YAML (and restart Home Assistant). Additionally, the UI
will now guide you through this all when setting up the integration. Awesome! 
 Also, we have extended My Home Assistant to be able to support OAuth2
authentication redirects! It���s fast, simple, privacy-aware, and nothing
for you to set up. It just works! No more redirect URI frustrations. ���� 
 We have updated the documentation of all integrations using OAuth2 to reflect
all these changes. 
 Calendar triggers with offsets 
 The last release, we introduced the calendar trigger;
in this release, the calendar trigger is extended with offset support! 
 Offsets can be helpful for use in automations, as it allows you to alert
ahead of the actual calendar event happening. For example, triggering a
notification the evening before trash day, a birthday reminder a week early,
or a reminder 15 minutes before a meeting. 

 
  Use the calendar trigger to schedule anything in your home! 
   
  Create a calendar and add events to it as a schedule, for example, for your
  thermostat or lights, and use an automation to trigger and adjust
  these devices based on the plan you have defined in that calendar! 
   
  This way, you can create complex schedules with repeating patterns
  and schedule exceptions, with the ease of using your calendar.
 
 Improved scene editor 
 Scenes are great for restoring states of multiple devices to a previous state,
e.g., to quickly set a lighting mood in a room, using an automation, script,
or a button on your dashboard. 
 When creating scenes, it creates those scenes based on the state of a whole
device (including all of its entities). However, what if you want to add
a specific entity to a scene and not the entire device? 
 Well, now you can! 

 It is a small but welcome improvement that makes it possible to include single
entities into a scene without adding the whole device. Of course, you can also
still add the entire device if you want to. 
 Database performance 
 This release builds on the database improvements from 2022.4.
Disk writes have been reduced to preserve SD card lifetimes and new APIs have been added,
which get event/historical data to the frontend even faster. 
 The database storage format is further optimized, with an additional size
reduction ranging from 25-40% for most installs on top of what has been gained
in previous releases. This is achieved by storing events more efficiently. 
 Data stored in the database before upgrading to this release isn���t compacted.
The size reduction will occur over time when new data gets recorded, and older
data gets purged. 
 If you are using SQLite (default) or MySQL, you will benefit from a faster date
parser, which speeds up multi-hour history and logbooks. 
 We recommend not to miss this release to ensure that future database changes
and migrations will be faster. 
 Other noteworthy changes 
 There is much more juice in this release; here are some of the other
noteworthy changes this release: 
 
 The System Health menu now shows database
information, including versions and estimated database size. The version
number of the OS Agent is now also listed. Thanks, @bdraco &amp; @ludeeus. 
 The ���Preload Camera��� setting shown on every camera feed has been moved! It
is now part of the entity settings, preventing unintentional toggling.
Thanks @bramkragten! 
 @goyney upgraded the Material Design Icons to version v6.7.96, providing
us with 100 new, fresh, and really useful icons! Thank you! 
 The this variable in template entities is now also available for use in
their actions! Thanks, @emontnemery. 
 A big shout out to @yosilevy, who has been improving support for
RTL languages (Right to Left) in the UI! Thank you! 
 @balloob added support for the media browser to the GStreamer and
VLC media player integrations. 
 The as_timedelta template
filter/function, added by @eifinger, allows you to convert many time strings
(including ISO8601) into a timedelta object. Awesome! 
 Lots of you asked for it; the ���YAML��� tab is now the first tab
shown in the developer tools. 
 @Noltari has been extending the QNAP QSW integration, adding support
for diagnostics, a reboot button, and binary sensors for anomaly detection. 
 Got a Ring doorbell? And want to fool the others in your house someone is
at the door? Now you can! Thanks to @grablair you can now trigger the ding!
This is useful for notifications, of course ;) 
 Tasmota covers now support tilting, thanks @emontnemery! 
 @rappenze added support for garage doors to Fibaro, nice! 
 The QR Code integration now works on all installation types,
thanks @cliffordwhansen! 
 Venstar now has CO2 and IAQ sensors when the thermostat supports it,
awesome @hall! 
 Using a NETGEAR? @starkillerOG added the speed test sensors! 
 
 New Integrations 
 We welcome the following new integrations this release: 
 
 Application Credentials, added by@allenporter 
 Big Ass Fans, added by @bdraco 
 Geocaching, added by @Sholofly &amp; @reinder83 
 iAlarmXR, added by @bigmoby 
 laundrify, added by @xLarry 
 Soundavo WS66i 6-Zone Amplifier, added by @ssaenger 
 YoLink, added by @matrixd2 
 
 Integrations now available to set up from the UI 
 The following integrations are now available via the Home Assistant UI: 
 
 Aladdin Connect, done by @mkmer 
 HERE Travel Time, done by @eifinger 
 Slack, done by @tkdrob 
 
 Release 2022.6.1 - June 2 
 
 Cleanup and use new MQTT_BASE_SCHEMA constants (@jbouwh - #72283) (mqtt docs) 
 Move MQTT config schemas and client to separate modules (@emontnemery - #71995) (mqtt docs) 
 Update MQTT tests to use the config entry setup (@jbouwh - #72373) (mqtt docs) 
 Remove announce workaround for Sonos (@jjlawren - #72854) (sonos docs) 
 Update frontend to 20220601.0 (@bramkragten - #72855) (frontend docs) 
 Ensure recorder shuts down when its startup future is canceled out from under it (@bdraco - #72866) (recorder docs) 
 Fix logbook not setting up with an recorder filter that has empty fields (@bdraco - #72869) (recorder docs) (logbook docs) 
 Only present history_stats state as unknown if the time is in the future (@bdraco - #72880) (history_stats docs) 
 Fix migration of MySQL data when InnoDB is not being used (@bdraco - #72893) (recorder docs) 
 Fix performance of logbook entity and devices queries with large MySQL databases (@bdraco - #72898) (logbook docs) 
 Fix reload of MQTT yaml config (@emontnemery - #72901) (mqtt docs) 
 Bump yolink-api to 0.0.6 (@matrixd2 - #72903) (yolink docs) 
 Fix logging &amp; exit code reporting to S6 on HA shutdown (@nojocodex - #72921) 
 Fix bug in caldav and avoid unnecessary copy of dataclass (@allenporter - #72922) (caldav docs) 
 Fix Hive authentication (@KJonline - #72929) (hive docs) 
 Only sync when HA is started up as we already sync at startup (@balloob - #72940) (cloud docs) 
 Fix misalignments between sql based filtering with the entityfilter based filtering (@bdraco - #72936) (recorder docs) 
 Only create auto comfort entities for BAF devices that support them (@bdraco - #72948) (baf docs) 
 
 Release 2022.6.2 - June 4 
 
 Fix statistics_during_period being incorrectly cached (@bdraco - #72947) (history docs) 
 Allow log template function to return specified default on math domain error (@XaF - #72960) 
 Bump pynetgear to 0.10.4 (@starkillerOG - #72965) (netgear docs) 
 Bump bimmer_connected to 0.9.4 (@rikroe - #72973) (bmw_connected_drive docs) 
 fjaraskupan: Don���t filter anything in backend (@elupus - #72988) (fjaraskupan docs) 
 Check ISY994 climate for unknown humidity value on Z-Wave Thermostat (@shbatm - #72990) (isy994 docs) 
 Fix google calendar bug where expired tokens are not refreshed (@allenporter - #72994) (google docs) 
 Provide Sonos media position if duration not available (@jjlawren - #73001) (sonos docs) 
 Bump pypck to 0.7.15 (@alengwenus - #73009) (lcn docs) 
 Fix missing historical context data in logbook for MySQL and PostgreSQL (@bdraco - #73011) (recorder docs) 
 Fix history stats not comparing all times in UTC (@bdraco - #73040) (history_stats docs) 
 
 Release 2022.6.3 - June 6 
 
 Throttle multiple requests to the velux gateway (@marcelveldt - #72974) (velux docs) 
 Bump wallbox to 0.4.9 (@hesselonline - #72978) (wallbox docs) 
 Fix fibaro cover detection (@rappenze - #72986) (fibaro docs) 
 Reduce branching in generated lambda_stmts (@bdraco - #73042) (recorder docs) 
 Send an empty logbook response when all requested entity_ids are filtered away (@bdraco - #73046) (logbook docs) 
 Bump aiolookup to 0.1.1 (@bdraco - #73048) (lookin docs) 
 Bump simplisafe-python to 2022.06.0 (@bachya - #73054) (simplisafe docs) 
 Fix unhandled exception when RainMachine coordinator data doesn���t exist (@bachya - #73055) (rainmachine docs) 
 Bump regenmaschine to 2022.06.0 (@bachya - #73056) (rainmachine docs) 
 Fix incompatiblity with live logbook and google_assistant (@bdraco - #73063) (logbook docs) 
 Fix elk attributes not being json serializable (@gwww - #73096) (elkm1 docs) 
 Mark counter domain as continuous to exclude it from logbook (@bdraco - #73101) (logbook docs) 
 Tomorrowio utc fix (@lymanepp - #73102) (tomorrowio docs) 
 Remove available property from Kodi (@Bikonja - #73103) (kodi docs) 
 Point iAlarm XR at PyPI fork (@balloob - #73143) (ialarm_xr docs) 
 Fix state_changes_during_period history query when no entities are passed (@bdraco - #73139) (recorder docs) 
 Remove unused code from logbook (@bdraco - #72950) (logbook docs) 
 
 Release 2022.6.4 - June 7 
 
 Fix errors when unjoining multiple Sonos devices simultaneously (@jjlawren - #73133) (sonos docs) 
 Bump async-upnp-client==0.31.1 (@StevenLooman - #73135) (upnp docs) (yeelight docs) (dlna_dmr docs) (samsungtv docs) (ssdp docs) (dlna_dms docs) 
 Use default None for voltage property of FritzDevice in Fritz!Smarthome (@mib1185 - #73141) (fritzbox docs) 
 Fix KeyError from ESPHome media players on startup (@jesserockz - #73149) (esphome docs) 
 Fix bugs with RainMachine zone run time sensors (@bachya - #73179) (rainmachine docs) 
 Fix creating unique IDs for WiFi switches in Fritz!Tools (@mib1185 - #73183) (fritz docs) 
 Bump pywemo to 0.9.1 (@esev - #73186) (wemo docs) 
 Remove sqlalchemy lambda_stmt usage from history, logbook, and statistics (@bdraco - #73191) (recorder docs) (logbook docs) 
 
 Release 2022.6.5 - June 10 
 
 Ensure netgear devices are tracked with one enabled config entry (@starkillerOG - #72969) (netgear docs) 
 Bump yolink-api to 0.0.8 (@matrixd2 - #73173) (yolink docs) 
 Fix Feedreader Atom feeds using updated date (@d0nni3q84 - #73208) (feedreader docs) 
 Hive auth fix for users (@KJonline - #73247) (hive docs) 
 Fix handling of connection error during Synology DSM setup (@mib1185 - #73248) (synology_dsm docs) 
 Bump regenmaschine to 2022.06.1 (@bachya - #73250) (rainmachine docs) 
 Improve Netgear logging (@starkillerOG - #73274) (netgear docs) 
 Fix polling frequency for Starling integration (@Dullage - #73282) (starlingbank docs) 
 Fix reloading themes crashing if no themes configured (@balloob - #73287) (frontend docs) 
 Bump version of pyunifiprotect to 3.9.0 (@AngellusMortis - #73168) (unifiprotect docs) 
 Bumps version of pyunifiprotect to 3.9.1 (@AngellusMortis - #73252) (unifiprotect docs) 
 Bumps version of pyunifiprotect to 3.9.2 to fix compat with protect 2.1.1 (@AngellusMortis - #73299) (unifiprotect docs) 
 Fix initial tilt value of MQTT cover (@emontnemery - #73308) (mqtt docs) 
 Fix wallbox sensor rounding (@hesselonline - #73310) (wallbox docs) 
 Improve MQTT reload performance (@emontnemery - #73313) (mqtt docs) 
 Guard MySQL size calculation returning None (@balloob - #73331) (recorder docs) 
 
 Release 2022.6.6 - June 14 
 
 Filter out forced updates in live logbook when the state has not changed (@bdraco - #73335) (logbook docs) 
 Fix zwave_js add node schemas (@raman325 - #73343) (zwave_js docs) 
 Hive Bump pyhiveapi to 0.5.10 for credentials fix (@KJonline - #73365) (hive docs) 
 Fix reload race in yeelight when updating the ip address (@bdraco - #73390) (yeelight docs) 
 Only update unifiprotect ips from discovery when the console is offline (@bdraco - #73411) (unifiprotect docs) 
 Fix smart by bond detection with v3 firmware (@marciogranzotto - #73414) (bond docs) 
 Bump aiohue to 4.4.2 (@balloob - #73420) (hue docs) 
 Fix fan support in nest, removing FAN_ONLY which isn���t supported (@allenporter - #73422) (nest docs) 
 Guard withings accessing hass.data without it being set (@balloob - #73454) (withings docs) 
 Fix max_value access for number platform in Overkiz (@tetienne - #73479) (overkiz docs) 
 
 Release 2022.6.7 - June 22 
 
 Ensure metoffice daily are returned once daily (@gordallott - #72440) (metoffice docs) 
 Fix thumbnail issues in Twitch integration (@bergdahl - #72564) (twitch docs) 
 Bump aiobafi6 to 0.6.0 to fix logging performance (@jfroy - #73517) (baf docs) (dependency) 
 Use IP address instead of hostname in Brother integration (@bieniu - #73556) (brother docs) 
 Bump growattServer to 1.2.2 (@muppet3000 - #73561) (growatt_server docs) (dependency) 
 Handle offline generators in oncue (@bdraco - #73568) (oncue docs) 
 Don���t attempt to reload MQTT device tracker (@emontnemery - #73577) (mqtt docs) 
 Fix handling of illegal dates in onvif sensor (@emontnemery - #73600) (onvif docs) 
 Fix voltage and current values for Fritz!DECT smart plugs (@mib1185 - #73608) (fritzbox docs) 
 Fix MQTT config schema to ensure correct validation (@jbouwh - #73619) (mqtt docs) 
 Fix calling permanent off with nexia (@bdraco - #73623) (nexia docs) (dependency) 
 Don���t verify ssl certificates for ssdp/upnp devices (@StevenLooman - #73647) (upnp docs) (ssdp docs) 
 Retry on SenseAPIException during sense config entry setup (@bdraco - #73651) (sense docs) 
 Fix AmbiClimate services definition (@maxgashkov - #73668) (ambiclimate docs) 
 Update aiomusiccast (@micha91 - #73694) (yamaha_musiccast docs) (dependency) 
 Fix CSRF token for UniFi (@Kane610 - #73716) (unifi docs) 
 Insteon bug fixes (@teharris1 - #73791) (insteon docs) 
 Fix Plugwise migration error (@frenck - #73812) (plugwise docs) 
 
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
 Below is a listing of the breaking changes for this release, per subject or
integration. Click on one of those to read more about the breaking change
for that specific item. 

 
   
    
      MQTT 
       
      
      
       
    
     
 Defining manually configured MQTT entities directly under the respective
platform keys (e.g., fan, light, sensor, etc.) is deprecated, and support
will be removed in Home Assistant Core 2022.9. 
 Manually configured MQTT entities should now be defined under the mqtt
configuration key in configuration.yaml instead of under the platform key. 
 As an example, this is now deprecated: 
   sensor:
  - platform: "mqtt"
    name: "My sensor"
    state_topic: "some-state-topic"
   
 The configuration needs to be updated to this format: 
   mqtt:
  sensor:
    - name: "My sensor"
      state_topic: "some-state-topic"
   
 (@jbouwh - #71676 #72183 #72281 #72249 #72271 #72167 #72165 #72251 #72279 #72268 #72272 #72273 #72274 #72278 #72270) (documentation) 
 
   
 

 
   
    
      Template filter/function defaults 
       
      
      
       
    
     
 The following template filters and functions will now error instead of returning
the input if the input is invalid and no default value is specified: 
 
 acos 
 as_timestamp 
 asin 
 atan 
 atan2 
 cos 
 float 
 int 
 log 
 multiply 
 round 
 sin 
 sqrt 
 strptime 
 tan 
 timestamp_custom 
 timestamp_local 
 timestamp_utc 
 
 Examples: 
 
 {{ "abc" | float }}: Will fail to render 
 {{ "abc" | float(default=5) }}: Will render as 5, no warning will be logged 
 {{ float("abc") }}: Will fail to render 
 {{ float("abc", default=5) }}: Will render as 5, no warning will be logged 
 
 (@emontnemery - #71687) (documentation) 
 
   
 

 
   
    
      OAuth2 (re-)authentications 
       
      
      
       
    
     
 Home Assistant will now use My Home Assistant to redirect the OAuth2 callback
over. 
 If you need to re-authenticate with an existing OAuth2 application in the future,
you might need to adjust the external application configuration. Please check
the documentation of the specific integration on how to configure this. 
 (@frenck - #72449) (documentation) 
 
   
 

 
   
    
      Home Assistant Container 
       
      
      
       
    
     
 If you run Home Assistant Container in Docker (e.g., using Portainer,
Docker (Compose), QNAP, and others), please make sure you are not specifying
an init process. 
 This can be an init configuration option in your Docker management tools or
Docker Compose, or the --init command line flag on the raw Docker command.
These should NOT be set, as Home Assistant ships with the S6 init system. 
 While you are at it, make sure you also do not set a cmd or entrypoint.
Setting these are not breaking, however, you should not set them. 
 (@pvizeli - #72425) (documentation) 
 
   
 

 
   
    
      1-Wire 
       
      
      
       
    
     
 Using the 1-Wire via SysBus, previously deprecated, has been removed;
this integration is being adjusted to comply with Architectural Decision
Record 0019; more information can be found here: 
 https://github.com/home-assistant/architecture/blob/master/adr/0019-GPIO.md 
 ������ Using the 1-Wire via OWServer is still supported! 
 (@epenet - #71232) (documentation) 
 
   
 

 
   
    
      Aladdin Connect 
       
      
      
       
    
     
 The Aladdin Connect integration migrated to configuration
via the UI. Configuring Aladdin Connect via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration is automatically imported on upgrade to this
release; and thus can be safely removed from your YAML configuration
after upgrading. 
 (@mkmer - #68304) (documentation) 
 
   
 

 
   
    
      BMW Connected Drive 
       
      
      
       
    
     
 The binary_sensor.&lt;your_vehicle&gt;_lights_parking has been removed. It is not
provided by API anymore. 
 The following sensors have been renamed. Existing sensors with historical data
and automations should be migrated automatically: 
 
 sensor.&lt;your_vehicle&gt;_charging_level_hv to sensor.&lt;your_vehicle&gt;_remaining_battery_percent 
 sensor.&lt;your_vehicle&gt;_fuel_percent to sensor.&lt;your_vehicle&gt;_remaining_fuel_percent 
 
 (@rikroe - #71827) (documentation) 
 
   
 

 
   
    
      Deluge 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Deluge
integration has been removed. 
 Deluge is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@tkdrob - #71487) (documentation) 
 
   
 

 
   
    
      Discord 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Discord
integration has been removed. 
 Discord is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@frenck - #71696) (documentation) 
 
   
 

 
   
    
      DuneHD 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the DuneHD
integration has been removed. 
 DuneHD is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@frenck - #71694) (documentation) 
 
   
 

 
   
    
      File Size 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the File Size
integration has been removed. 
 File Size is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@frenck - #71692) (documentation) 
 
   
 

 
   
    
      Google Calendars 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Google Calendars
integration has migrated to configuration via the UI. Configuring Google Calendars
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 All entity tracking state has been migrated to use the standard Home Assistant
entity enable/disable features in the user interface and system options. 
 (@allenporter - #72288) (documentation) 
 
 The found_calendar service has been removed from Google Calendars.
This service is an internal implementation detail of the integration
used for creating calendars found from the API,
which is now no longer exposed as a service. 
 (@allenporter - #72260) (documentation) 
 
   
 

 
   
    
      HERE Travel Time 
       
      
      
       
    
     
 The HERE Travel Time integration migrated to configuration
via the UI. Configuring HERE Travel Time via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration is automatically imported on upgrade to this
release; and thus can be safely removed from your YAML configuration
after upgrading. 
 (@eifinger - #69212) (documentation) 
 
   
 

 
   
    
      Home Connect 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Home Connect
integration has migrated to configuration via the UI. Configuring Home Connect
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #71988) (documentation) 
 
   
 

 
   
    
      Honeywell Lyric 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Honeywell Lyric
integration has migrated to configuration via the UI. Configuring Honeywell Lyric
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #72335) (documentation) 
 
   
 

 
   
    
      International Space Station (ISS) 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the International Space Station (ISS)
integration has been removed. 
 International Space Station (ISS) is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@frenck - #71693) (documentation) 
 
   
 

 
   
    
      Jandy iAqualink 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Jandy iAqualink
integration has been removed. 
 Jandy iAqualink is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@epenet - #72404) (documentation) 
 
   
 

 
   
    
      KNX 
       
      
      
       
    
     
 A new configuration key for KNX covers invert_updown can be set to
invert the up-down payload (binary) of covers independently of the
position percentage. 
 Previously up-down (move_long_address) payloads were inverted
when invert_position: true was configured. This now only inverts
the position_address and position_state_address payloads (%). 
 If you have used invert_position: true for covers, you would need to
add the new key to your YAML config to have the same behaviour as before. 
   knx:
  cover:
    - name: "Example cover"
      move_long_address: "3/0/0"
      move_short_address: "3/0/1"
      position_address: "3/0/3"
      position_state_address: "3/0/2"
      invert_updown: true  # &lt;- add this line to keep inversion of up/down payload
      invert_position: true
   
 (@farmio - #72012) (documentation) 
 
   
 

 
   
    
      Litter-Robot 
       
      
      
       
    
     
 The Litter-Robot vacuum entity will now enter an unavailable state when the
robot hasn���t sent an update recently. 
 (@natekspencer - #70810) (documentation) 
 
 The clean_cycle_wait_time_minutes, status_code, and last_seen attributes
have been removed from the vacuum entity as they are now available as individual
entities. 
 (@natekspencer - #71760) (documentation) 
 
   
 

 
   
    
      Logbook 
       
      
      
       
    
     
 If the stop and start event were fired within the exact same minute, we would
previously show it as restarted  in the logbook. When events crossed the
minute boundary (i.e., we fired stop at 11:30:59 and start at 11:31:04), it
would show separately as stopped and then start. 
 This change eliminates the inconstancy by always showing them as stopped and
started, which allows us to simplify how we generate logbook rows. 
 (@bdraco - #71600) (documentation) 
 
 The entity name in the logbook is now always shown with the current name instead
of the old name if it was renamed. If the entity no longer exists, we now show
the original entity_id instead, which aligns with the warning icon we already
display in the frontend when a state is missing or removed. 
 (@bdraco - #71895) (documentation) 
 
   
 

 
   
    
      Neato Botvac 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Neato Botvac
integration has migrated to configuration via the UI. Configuring Neato Botvac
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #72175) (documentation) 
 
   
 

 
   
    
      Netatmo 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Netatmo
integration has migrated to configuration via the UI. Configuring Netatmo
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #71884) (documentation) 
 
   
 

 
   
    
      Nexia 
       
      
      
       
    
     
 The zone status attribute has been removed from the climate entity. The zone
status is already available as a separate sensor, and it was producing duplicate
data in the state machine. 
 (@bdraco - #72176) (documentation) 
 
   
 

 
   
    
      Nexia/American Standard/Trane 
       
      
      
       
    
     
 Remove non-standard humidify_supported and dehumidify_supported attributes
from Nexia. 
 These attributes can already be inferred from the dehumidify_setpoint
or humidify_setpoint attributes. 
 As they took up space in the database every time any of the values changes, they
have now been removed. 
 (@bdraco - #71248) (documentation) 
 
   
 

 
   
    
      nVent RAYCHEM SENZ 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the nVent RAYCHEM SENZ
integration has migrated to configuration via the UI. Configuring nVent RAYCHEM SENZ
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #72338) (documentation) 
 
   
 

 
   
    
      Recorder 
       
      
      
       
    
     
 De-duplicate event data into a new event_data table 
 Data is no longer stored in the event.event_data column and instead
deduplicated into the event_data.shared_data column and joined on
event.data_id==event_data.data_id. 
 This is the same as we did with state attributes in 2022.4, as we can reduce
the size of the events table by ~8-14% on avg. 
 (@bdraco - #71135) (documentation) 
 
 
 All the data needed to fetch a state_changed event is now available in
the states table (along with state_attributes if needed). 
 Reduces overall database size by ~27% 
 Refactors logbook to work without the need for the state_changed events
rows (fetched from states). 
 Refactors purge to work without the need for linking the state_changed event. 
 Origin is now stored as an integer. 
 
 (@bdraco - #71165) (documentation) 
 
 The following attributes are no longer recorded for group entities: 
 
 entity_id 
 order 
 auto 
 
 These attributes provide no historical value since they are already
contained in the YAML configuration and only fill up the database. 
 (@bdraco - #71256) (documentation) 
 
 The recorder now refuses to set up if the database dialect is unsupported
or if the database dialect is supported, but the version is too old. 
 (@emontnemery - #70888) (documentation) 
 
   
 

 
   
    
      Scrape 
       
      
      
       
    
     
 The scape integration performance has been improved by using the lxml parser. 
 Testing (YMMV based on content and nesting): 
 
 For large documents (5000k tags) it was at least an order of magnitude faster. 
 For small documents, it was ~3x faster. 
 
 Users who are not using Home Assistant Operating System or Home Assistant
Container will need to ensure libxml2 and libxslt are installed. 
 For example, on Debian based Home Assistant Core installs, run:
sudo apt install libxml2 
 (@bdraco - #71087) (documentation) 
 
   
 

 
   
    
      Slack 
       
      
      
       
    
     
 The Slack integration migrated to configuration
via the UI. Configuring Slack via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration is automatically imported on upgrade to this
release; and thus can be safely removed from your YAML configuration
after upgrading. 
 (@tkdrob - #69880) (documentation) 
 
   
 

 
   
    
      Somfy 
       
      
      
       
    
     
 Somfy has replaced their Somfy Open API (cloud-based) with a local API
(which we Home Assistant users absolutely love). Somfy has now decided
to shut down its cloud API after June 21st, 2022. 
 Please migrate to use the Overkiz integration
as a replacement. 
 Unfortunately, a migration to Overkiz is not possible due to differences in the
authentication mechanism. 
 (@iMicknl - #71653) (documentation) 
 
   
 

 
   
    
      Sonos 
       
      
      
       
    
     
 The sonos.join and sonos.unjoin services will be removed in 2022.8 in favor
of the standard media_player.join and media_player.unjoin services. 
 (@jjlawren - #71226) (documentation) 
 
   
 

 
   
    
      Spotify 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Spotify
integration has migrated to configuration via the UI. Configuring Spotify
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #71871) (documentation) 
 
   
 

 
   
    
      Squeezebox (Logitech Media Server) 
       
      
      
       
    
     
 The Squeezebox player synchronization framework has been updated to use the
standard media_player.join and media_player.unjoin services. The
list of synchronized players is now stored in the group_members state
attribute. 
 The  squeezebox.sync and squeezebox.unsync services are now deprecated,
and will be removed in two releases in favor of the standard
services listed above. 
 The sync_group state attribute is deprecated in favor of group_members,
and will also be removed in two releases. 
 (@rajlaud - #70962) (documentation) 
 
   
 

 
   
    
      Templates 
       
      
      
       
    
     
 Support for white_value is deprecated in template light and will be removed
in Home Assistant Core 2022.9. 
 (@emontnemery - #71044) (documentation) 
 
   
 

 
   
    
      Trafikverket Train 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Trafikverket Train
integration has been removed. 
 Trafikverket Train is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@gjohansson-ST - #71410) (documentation) 
 
   
 

 
   
    
      Universal Devices ISY994 
       
      
      
       
    
     
 The auxiliary sensors for each Insteon device are now their own sensor entity
instead of an attribute on the parent entity. This makes them easier to find
and allows attributes to be de-duplicated in the database. 
 (@bdraco - #71254) (documentation) 
 
   
 

 
   
    
      Vera 
       
      
      
       
    
     
 The Vera integration previously migrated to configuration
via the UI. Configuring Vera via YAML configuration
has been deprecated and will be removed in a future Home Assistant release. 
 Your existing YAML configuration has already been automatically imported;
and thus can be safely removed from your YAML configuration
after upgrading. 
 (@epenet - #72418) (documentation) 
 
   
 

 
   
    
      Version 
       
      
      
       
    
     
 The Boards ���Intel NUC���, ���RaspberryPi��� (Raspberry Pi 1 devices),
and ���RaspberryPi Zero-W��� are no longer supported in Home Assistant OS. 
 They are also no longer available in the version integration.
Please remove the version integrations for those boards. 
 (@agners - #72085) (documentation) 
 
   
 

 
   
    
      Viessmann ViCare 
       
      
      
       
    
     
 The previously deprecated YAML configuration of the Viessmann ViCare
integration has been removed. 
 Viessmann ViCare is now configured via the UI, any existing YAML
configuration has been imported in previous releases and can now be safely
removed from your YAML configuration files. 
 (@epenet - #72408) (documentation) 
 
   
 

 
   
    
      Withings 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Withings
integration has migrated to configuration via the UI. Configuring Withings
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #71990) (documentation) 
 
   
 

 
   
    
      WLED 
       
      
      
       
    
     
 The previously deprecated WLED update button entity has been removed.
Please use the newly provided update entity instead. 
 (@frenck - #71775) (documentation) 
 
   
 

 
   
    
      Xbox 
       
      
      
       
    
     
 The configuration of the OAuth application credentials for the Xbox
integration has migrated to configuration via the UI. Configuring Xbox
OAuth application credentials via YAML configuration has been deprecated
and will be removed in a future Home Assistant release. 
 Your existing OAuth application credentials in the YAML configuration is
automatically imported on upgrade to this release; and thus can be safely
removed from your YAML configuration after upgrading. 
 (@allenporter - #71908) (documentation) 
 
   
 

 
   
    
      Z-Wave JS 
       
      
      
       
    
     
 With this release, you will need to update your zwave-js-server instance. 
 
 If you use the zwave_js add-on, you need to have at least version 0.1.60. 
 If you use the Z-Wave JS 2 MQTT add-on, you need to have at least version 0.41.0. 
 If you use the zwavejs2mqtt Docker container, you need to have at least version 6.10.0. 
 If you run your own Docker container, or some other installation method,
you will need to update your zwave-js-server instance to at least 1.17.0. 
 
 (@raman325 - #72395) (documentation) 
 
   
 
 If you are a custom integration developer and want to learn about breaking
changes and new features available for your integration: Be sure to follow our
developer blog. The following are the most notable for this release: 
 
 Logbook API removal of entity_matches_only flag 
 Media Player updates: enqueue changes, announce added 
 S6-Overlay 3.x update on our docker base images 
 ServiceInfo model improvements and deprecations 
 
 Farewell to the following 
 The following integrations are also no longer available as of this release: 
 
 Raspberry Pi GPIO has been previously deprecated and now removed.
More information can be found in Architectural Decision Record 0019. 
 
 All changes 
 Of course, there is a lot more in this release. You can find a list of
all changes made here: Full changelog for Home Assistant Core 2022.6 
"
link: "https://www.home-assistant.io/blog/2022/06/01/release-20226/"
category:
---
