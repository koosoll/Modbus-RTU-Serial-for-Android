# Modbus-RTU-Serial-for-Android
This repository includes Android code that is needed to communicate modbus RTU serial through the microUSB port. 

For this code to work,there are specific android system files that need to be changed. There area few tablets out 
there that already include this change, but most do not.  To change any system files an Android device needs to be rooted.

The two files that need to be changed are:
  - android.hardware.usb.host.xml
  - tablet_core_hardware.xml
  
These files are located in the permissions folder. The file path to this folder is  "/etc/permissions/". 
  
The content for android.hardware.usb.host.xml needs to be:

<permissions>
  <feature name=?android.hardware.usb.host?/>
  </permissions>
  
  
The content for tablet_core_hardware.xml needs to be:

<?xml version="1.0" encoding="utf-8"?>
<!-- Copyright (C) 2010 The Android Open Source Project

     Licensed under the Apache License, Version 2.0 (the "License");
     you may not use this file except in compliance with the License.
     You may obtain a copy of the License at

          http://www.apache.org/licenses/LICENSE-2.0

     Unless required by applicable law or agreed to in writing, software
     distributed under the License is distributed on an "AS IS" BASIS,
     WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
     See the License for the specific language governing permissions and
     limitations under the License.
-->

<!-- These are the hardware components that all handheld devices
     must include. Devices with optional hardware must also include extra
     hardware files, per the comments below.

     Handheld devices include phones, mobile Internet devices (MIDs),
     Personal Media Players (PMPs), small tablets (7" or less), and similar
     devices.
-->
<permissions>
     <feature name="android.hardware.location" />
     <feature name="android.hardware.location.network" />
     <!--<feature name="android.hardware.sensor.compass" />-->
     <feature name="android.hardware.sensor.accelerometer" />
     <feature name="android.hardware.touchscreen" />
     <feature name="android.hardware.touchscreen.multitouch" />
     <feature name="android.hardware.touchscreen.multitouch.distinct" />
     <feature name="android.hardware.microphone" />
     <feature name="android.hardware.screen.portrait" />
     <feature name="android.hardware.screen.landscape" />
     <feature name="android.hardware.usb.host" />
     <feature name="android.software.app_widgets" />
     <feature name="android.software.home_screen" />
     <feature name="android.software.input_methods" />
     <!-- Feature to specify if the device supports adding device admins. -->
     <feature name="android.software.device_admin" />
     <!-- devices with GPS must include android.hardware.location.gps.xml -->
     <!-- devices with a rear-facing camera must include one of these as appropriate:
          android.hardware.camera.xml or
          android.hardware.camera.autofocus.xml or
          android.hardware.camera.autofocus-flash.xml -->
     <!-- devices with a front facing camera must include
          android.hardware.camera.front.xml -->
     <!-- devices with WiFi must also include android.hardware.wifi.xml -->
     <!-- devices with an ambient light sensor must also include
          android.hardware.sensor.light.xml -->
     <!-- devices with a proximity sensor must also include
          android.hardware.sensor.proximity.xml -->
     <!-- devices with a barometer must also include
          android.hardware.sensor.barometer.xml -->
     <!-- devices with a gyroscope must also include
          android.hardware.sensor.gyroscope.xml -->
     <!-- GSM phones must also include android.hardware.telephony.gsm.xml -->
     <!-- CDMA phones must also include android.hardware.telephony.cdma.xml -->
</permissions>




Once verified that these files are correct your android device will be ready to use. 



   
   
