---
title: 'How to protect AdBlock from being disabled by the system'
published: true
taxonomy:
    category:
        - docs
---

In some cases, apps won't stay in the background ("alive" or in a sleep mode) due to Android OS optimization function, or so called "battery save mode" — this function can kill background applications. It may be inconvenient to relaunch them each time they are getting closed. To avoid the background app termination you need to follow these steps which we described separately for each manufacturer (version) of Android OS. Note that instructions for different manufacturers are mostly very similar.

**List of manufacturers with different versions of Android OS:**

* [Xiaomi](#Xiaomi)

* [Samsung](#Samsung)

* [Huawei](#Huawei)

* [Meizu](#Meizu)

* [Nokia](#Nokia)

* [Oneplus](#Oneplus)

* [Android stock devices Pixel/Nexus/Essential](#Google)

<a id="Xiaomi"></a>
## Xiaomi

To set up AdBlock's background work for Xiaomi devices you should pay attention to Battery and Permissions.

- Tap on the *Recent tasks* button and swipe AdBlock down to make options *visible* (as presented on the screenshot):

<img src="/images/xiaomirecent.png" width="300">

- Tap on the *lock* icon. This will stop Xiaomi from closing AdBlock automatically. It should look like this:

<img src="/images/xiaomilocked.png" width="300">

- Go to *"Battery"*

- Select *"battery saver"* app 

- Find and select AdBlock

- Set up the following *"Background settings"*:

<img src="/images/xiaomirest.png" width="300">

- Go to *"Permissions"*

- Select *"Autostart"*

- Make sure that autostart function is enabled for AdBlock:

<img src="/images/xiaomiautostart.png" width="300">

<a id="Samsung"></a>

## Samsung

For Samsung devices, there is no huge need for setting up the background work, but if in your case the application is getting closed or disappears from the recent tasks after a while, do the following:

 - Tap on the *Recent tasks* button, tap on the *Additional settings* icon. It should look like this:
 
 <img src="/images/samsungoptions.png" width="300">

 - Tap on *Lock Apps*:
 
 <img src="/images/samsunglockapps.png" width="300">
 
  - Tap on the lock icon 
 
 <img src="/images/samsunglock.png" width="300">
 
 <a id="Huawei"></a>
 
 ## Huawei
 
Huawei devices are the easiest to set up, it is enough to perform two simple steps to lock the application in the background so it won't be terminated by battery saving or background killer process.
 
  - Tap on the *Recent tasks* button:
  
  <img src="/images/huaweirecentapps.png" width="300">
  
  - Tap on the lock icon:
  
   <img src="/images/huaweilock.png" width="300">
   
Besides, to set up the background work of your app more effectively, you should open device settings and do the following:
   
- Go to *Advanced Settings* > then open *Battery Manager* > Set *Power plan* to "Performance";
- Then choose *Protected apps* in the *Battery Manager* and check if your app is Protected;
- Go to *Apps* in the main settings and click on AdBlock there > choose *Battery* > enable *Power-intensive prompt* and *Keep running after screen is off*;
- Then in the *Apps* section open *Settings* (at the bottom) > *Special access* > choose *Ignore battery optimization* > press *Allowed* > *All apps* > find AdBlock on the list and set it to *Deny*

And here are some specific settings for different Huawei devices:

#### Huawei P9 Plus:

Open device settings > *Apps* > *Settings* > *Special access* > choose *Ignore battery optimization* > select *Allow* for your app.

#### Huawei P20, Huawei Honor 9 Lite and Huawei Mate 9 Pro:

Open device settings > *Battery* > *App launch* > then set your app to *Manage manually* and make sure everything is turned on.
  
   
<a id="Meizu"></a> 
   
 ## Meizu
 
Meizu has almost the same approach to the background process limitations as Huawei and Xiaomi. So you can avoid disabling the background work of AdBlock and any other app by adjusting the following settings:

- Go to *Advanced Settings* > then open *Battery Manager* > set *Power plan* to "Performance";
- Then choose *Protected apps* in the *Battery Manager* and check if your app is Protected;
- Go to *Apps* section and click on AdBlock there > choose *Battery* > enable *Power-intensive prompt* and *Keep running after screen is off*;
 
<a id="Nokia"></a> 
   
 ## Nokia
 
Nokia on Android O and P disables any background process after 20 minutes if the screen is off.
 
Here is what you need to do in order to prevent killing the background process of your app:

- Go to device settings > open *Apps* > choose *See all apps*;
- Then tap on the right top corner menu > choose *Show system*;
- Find *Power saver* in the app list, select it and tap on *Force stop*. It will remain stopped until the next restart.

From now on, background apps are supposed to work smoothly and use the standard Android battery optimizations.

**There is an alternative solution for background work optimization which is more appropriate for advanced users. You will find the instructions below.**

#### Nokia 1 (Android Go) 

- Uninstall the com.evenwell.emm package via the following adb commands:

`adb shell`
`pm uninstall --user 0 com.evenwell.emm`

#### Other Nokia models 

- Uninstall the com.evenwell.powersaving.g3 package via the following adb commands:

`adb shell`
`pm uninstall --user 0 com.evenwell.powersaving.g3`

<a id="Oneplus"></a>    
   
 ## Oneplus

Devices with OxygenOS on board are the most problematic, with its OS-sepcific cache cleaning and free RAM, including OS optimization. In addition, OxygenOS can interrupt the application's work if you do not use it for a while. To avoid these unwanted consequences, follow these steps: 
 
 - Go to Settings
 
 - Battery > Battery optimization
 
 - Find the app you want to keep awake all the time
 
 - Tap on it and select "Don't optimize" option
 
 - Tap "Done" to save
 
 - Open recent apps menu (as showed on this screenshot):
 
 <img src="/images/onepluslock.png" width="300">

- Lock AdBlock application:

<img src="/images/oneplusdots.png" width="300">

> On some OnePlus phones there is also a thing called App Auto-Launch and Deep Optimisation which essentially prevents apps from working in the background. Please disable it for your app.

And here is one more thing to try:
 
 - Open device settings > *Battery* > *Battery optimization* > switch to the *All apps* list (top menu) > choose your app > activate *Don’t optimize*
 
 - Open device settings > *Battery* > *Battery Optimisation* > three dots > *Advanced Optimisation* > Disable Deep Optimisation

<a id="Google"></a>

## Android stock devices Pixel/Nexus/Essential

Android stock OS normally does not conflict with applications working in the background, but if you are facing any issues you will need to switch on the "Always on VPN" mode.

 - Go to Settings - Network and Internet
 
 <img src="/images/vpn_1.png" width="300">

 - Tap on "VPN" and choose AdBlock
 
 <img src="/images/vpn_2.png" width="300">
 
 - Set up "Always on VPN" mode
 
 <img src="/images/vpn_3.png" width="300">