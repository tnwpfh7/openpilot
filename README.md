0. This fork is for all people who love Comma's Openpilot. Thanks to ku7, xx979xx, tk211x, xps-genesis, atom, hoya, moksatang, mamul, neokii, oricialworks, sunnyhaibin, dragonpilot, shane, kegman, dnv26, move-fast and everyone helping me or contributing for HKGs.

1. Branches
 - OPKR: main branch, stable, not latest. This will be updated if test branch is done.
 - _test: test branches, not stable, latest, for testing new functions, codes, or the other things.
 - Old branches are in openpilot_bak repository.

2. How to Install
 - Use fork installer : Type https://opkr.tk/fork/opkr on custom URL window(Short URL. This will install OPKR branch directly.) or you can use Shane's fork installer(https://smiskol.com/fork)
 - Use a command : cd /data; mv openpilot openpilot_bak; git clone https://github.com/openpilotkr/openpilot.git -b OPKR; reboot

3. Setting Menu
 - Device(Function Name: Explanation)
   - Driving Camera: You can preview/unview Openpilot Driving Camera.
 - Network(Function Name: Explanation)
   - HotSpot on Boot: Turned Hotspot on when boot. (reboot required)
   - Use Legacy SSH Key: Use old ssh key access(below 0.8.2). (no reboot required)
 - Toggles(Function Name: Explanation)
   - Enable Lane selector Mode: Show a button on driving screen including LaneMode/LaneLess/AUTO. AUTO mode is automatically switched by a condition of lane recongnition. (no reboot required)
   - Enable Driver Monitoring: On/Off driver monitoring for the EON without filterless IR camera or Someone cannot use front cam due to uncertain reasons.(reboot required)
   - Enable Driving Log Record: Record driving logs to Local, not happen upload to server(reboot required)
   - Enable Sending Log to Server: Enable uploader to upload to server(reboot required)
   - Use Comma Stock UI: this use original Comma's UI. Also this can be applied on driving screen in realtime(click MaxSpeed box at top-left corner). (no reboot required)
 - Software(Function Name: Explanation)
   - Check for Updates: You can confirm new commits of your fork and also you can update it.
   - Commit(Local/Remote): Commit name of local(EON) and Remote.(run once when boot in manager.py, search gitcommit.sh at the file, internet connection required)
   - Git Pull On Boot: run 'git pull' command when boot.
   - Load Preset/Save Preset: Load your Parameters or Save Your Parameters. located /data/preset1 or /data/preset2. This function can save/load your settings of Menu)
   - Parameter Init: Retrieve you Changes of Menu to initial values.
   - Git Reset: Remove your local changes and inintalize to the first status of the branch.
   - Cancel Git Pull: Move one step back if git pull is not satisfied.
   - Panda Flashing: Run Panda flashing command manually. Basically this is not necessary on normal operation.
   - Change Repo/Branch: You can install others fork/branch thru typing Git ID, Git Repository, Git Branch.
 - UserMenu(Function Name: Explanation)
   - EON AutoShutdown: At Car ignition off, the device will be shutdown after the time.
   - EON ForceShutdown: The device will be shutdown by force at offroad status anyway in the time.
   - EON Volume Control(%): set device volume manually.
   - EON Brightness Control(%): set device brightness automatically/manually.
   - EON SCR Off Timer: The screen brigntess will be dark or blank after that time on driving.
   - Brightness at SCR Off(%): If you use the function(EON SCR Off Timer), you can choose a level of the brightness.
   - EON Detach Alert Sound: None/KOR/ENG, Turn this on to notify when your car ignition off. Purpose of this, to protect your device away from Sun when you forgot.
   - Enable Battery Charging Control: battery charging control btw min and max of your setting
   - Use Auto Screen Record: Screen Record works automatically. at stop, the screen record off, at departure, the screen record on
   - Number of Recorded Files: Count of files you want to record.
   - Recording Quality: Low/Mid/High/U-High, changed the resolution and bitrate.
   - Delete All Recorded Files: /sdcard/videos
   - Delete All Driving Logs: /sdcard/realdata
   - Driver Monitoring Mode: Defalut/Unsleep, Default is Comma's. If you choose Unsleep, this will alert warning faster than Comma's one. You can switch the Mode in driving screen in realtime(touch monitoring face at bottom-left corner), clear back is Default Mode. Light green back is Unsleep Mode.(no reboot required)
   - E2E EYE Threshold: I'm not sure this factor is being used at code actually.
   - Normal EYE Threshold: set the value below threshold of your face recognition.
   - Blink Threshold: I think this is important in the Driver Monitoring. Set the value below the threshold of your eyes blink recognition. Driver Monitoring camera shows the values of your face recognition, eyes and the other things. Preview 'Driver Camera' and then check the recognition value of your eye out and modify the value on Menu.
   - Navigation Select: Mappy(for Korea), Waze(for Global)
   - RUN Navigation on Boot: Run Navigation on Boot. If it runs well, will go to background after few seconds.
   - Display Date on Screen: shows the Device date
   - Display Time on Screen: shows the Device time
   - API Server: You can choose 3 servers, Retropilot, Comma, User's
   - User's API: Set this when you use own
   - Mapbox Style: Choose three styles of the Mapbox, Comma, OPKR(locallized in Korea), User's, if you want to your own, Edit the file with yours(/data/params/d/MapboxStyleCustom). Make your mapbox style at https://studio.mapbox.com/. If you publish the style you can use it.
   - Use Auto Resume at Stop: at Standstill, use auto resume when leadcar is moving.
   - Use Cruise Button Spamming: SCC set speed is changed up and down automatically. should be turn this on to use many functions related to this.
   - Cruise Start Mode: Set your custom Cruise mode when boot. There are 6 modes. OpenpilotStock/Dist+Curv/Dist/Curv/Oneway/CamSpeed only. OpenpilotStock is nothing to happen with button and not be changed with set speed. Dist+Curv is changed by distance to leadcar and curvature. Dist is distance only. Curv is curvature only. Oneway change camera offset to approach the edge of a road. CamSpeed is changing set speed only by value of camera sign(OSM, Mappy).
   - LaneChange Speed: minimum lane change speed
   - LaneChange Delay: Nudge/Nudgeless(adjust delay time to run)
   - LaneChange Time(km/h: value): How the lanechange fast, to aggressive, upper the value, in oppsite, lower
   - LeftCurv Offset: if you are unsatisfactory of the drive at Left Curve Section, this can move your car to left or right side.(no reboot required)
   - RightCurv Offset: if you are unsatisfactory of the drive at Right Curve Section, this can move your car to left or right side.(no reboot required)
   - Show BSM Status: Show sign when a car approaching from behind. Your car should have the function(BSM)
   - Max Steering Angle: Default is 90. If you want more, change this up. Some car is not acceptable the vaule above 90.
   - Str Angle Adjust: When you car keep a straight road, If the value of steering angle is not 0.0, adjust this to be 0.0
   - Stop Steer Assist on Turn Signals: Openpilot doesn't steer your car at the situation of not process of lane change.
   - Reset MaxSpeed Over CurrentSpeed: If your car speed upper than OP MaxSpeed, the OP MaxSpeed synchronize to your car speed.
   - Enable OSM SpeedLimit: Use OSM SpeedLimit(reboot required)
   - Use Stock SafetyCAM Speed: Some cars have the signal in CAN message. not for all HKG cars.
   - SpeedLimit Offset(% or +-): let speedlimt is 50, sometimes, you don't want to match exactly the scc set speed to the speedlimit 50. it can be up and down instead of original speedlimit.
   - SafetyCam SignType: You can select 2 options to show on the screen, circular type and retangular type of speedlimit sign.
   - SafetyCamDist Adj(%): Change the target distance if you are in the decel situation of safetycam.
   - Change Cruise Gap at Stop: Cruise Gap changed to 1 step for departure faster, it gets back to orignal Gap after few second.
   - VisionCurvDecel(ModelSpeed: CarSpeed): set speed is changed by Curvature of vision.
   - OSM CurvDecel(%): If OSM has the value of curv speed, up/down this value if you want to add/subtract.
   - Use Auto Engagement: When OP is in disengagement status, Auto engagement is enabled when your car is moving. Cruise Standby status is needed at least.
   - Auto Engage Speed(km/h): Engagement is enabled at the speed.
   - Use Auto RES while Driving: SCC speed automatically set again when releasing SCC.(reboot required)
   - AutoRES Option: CruiseSet/MaxSpeedSet, MaxSpeedSet: Your OP MAX Speed set with RES Set speed. CruiseSet:only set to current set speed, not changed OP MAX Speed.
   - AutoRES Condition: RelBrake/OnGas, RelBrake: SCC speed set again when you release from brake pedal. OnGas: SCC speed set again when you step gas pedal.
   - AutoRES Allow(sec): time to allow for AutoRES
   - RES Count at Standstill: Adjust RES CAN message count to start from StandStill. upper, if the departure is failed. lower, if your car generate cluster error or can error.(no reboot required)
   - Steer Wind Down: to mitiate torque at error status of your lkas
   - MainSwitch Openpilot ON/OFF: You can turn on/off OP using Cruise Button on steering wheel.
   - DEBUG UI 1: Show debug UI on screen. 2 lines bottom of screen.(no reboot required)
   - DEBUG UI 2: Show debug UI on screen. other lines except 2 lines bottom.(no reboot required)
   - Show TMUX Error: Turn this on, if you want to show tmux error on screen related to process such as controlsd, plannerd and so on.(reboot required)
   - Show LongControl LOG: show long control log at DEBUG UI 1.(no reboot required)
   - Use Smart Prebuilt: Your device can be booted quickly. The file, Prebuilt is removed when you do push 'CHECK' button on the Menu or type 'gi' command on command line, after then it will be created again when boot&compile is completed.(reboot required)
   - Use FingerPrint 2.0(reboot required)
   - Set LDWS Vehicles
   - Set DriveGear by Force: for cars don't have dbc info of gear(reboot required)
   - Turn Off Communication Issue Alarm: Turn this on if you do not want alert of communication error. Sometimes you could get an alarm with error commuication issue. I don't know actually what error is. seems a bug or uncertain reason.
   - Support WhitePanda: Turn this on if you use WhitePanda. this is related to issue stopping processes when you turn device off.(reboot required)
   - Ignore of Steering Warning: Some cars have Steerwarning, so that not engaged.
   - Ignore Can Error on ISG: for ISG cars. In order to ignore can error, if you want to prevent disengagement.
   - Set BatteryLess Eon: Screen doesn't show information of battery status.
   - Use GoogleMap for Mapbox: Use google map when you search your destination at a web browser.
   - Timezone setting(reboot required)
   - Enable Calibration by Force: developer for engagment test
   - Open Android Settings
   - SoftKey RUN/SET: softkey application
   - RUN Mixplorer: file manager application
   - CAR Force Recognition: If your car is not recognized, choose your car at this.(reboot required)
   - Pand Value Edit: not recommended. enough at current status.
 - Tuning(Function Name: Explanation)
   - CameraOffset: set your camera offset
   - PathOffset: i'm not sure this. but i recommend if you move your camera offset, adjust this as the value.
   - Use Live SteerRatio: Use Live Parameter value.
   - LiveSR Adjsut(%): in some cases, live parameter is higher than original steeratio, i set this to minus value to not steer aggressively.
   - SteerRatio: Your default SteerRatio
   - SteerRatioMax: Max SteerRatio if you use Varaible SteerRatio not Live SR.
   - SteerActuatorDelay: level how your car reacts to upcoming road curvature.
   - SteerRateCost: How your car make steer strong to turn with the road curvature. you want make it strong lower the value. too much low values, it will make the steering little unstable.
   - SteerLimitTimer: timer how long op hold the steer. and timer for alert.
   - TireStiffnessFactor: lower value makes your steer more aggressive.
   - SteerMaxDefault: SteerMax Default value
   - SteerMaxMax: SteerMax Max value if you use variable SteerMax.
   - SteerMaxV: multiply to the output scale. it effects steer saturation or others.
   - Use variable SteerMax: use variable steermax by road curvature. it works above 30km/h.
   - SteerDeltaUpDefault: how fast steer inside in certain timing scope.
   - SteerDeltaUpMax: max value if you use variable steerdelta
   - SteerDeltaDownDefault: how fast steer outside in certain timing scope.
   - SteerDeltaDownMax: max value if you use variable steerdelta
   - Use variable SteerDelta: use variable steerdelta by road curvature. it works above 30km/h.
   - SteerThreshold: driver steering torque threshold
   - LatControl(Reboot): PID/INDI/LQR
   - Use LiveTune and Show UI: this will show button on the screen, you can up/down the values of tune. it will be applied in realtime. you can also touch top-right corner(comma wheel icon) to show tune panel on the screen.
   - Tune Values: change and find appropriate values.
   - LONG CONTROL MENU(RadarHareness required)
    - Use DynamicTR: TR changed by car speed.
    - CruiseGap: set TR of other Cruise Gaps
    - Use Radar Long Assist: when your car approaches to lead car, use combined value both OP gas/brake and Radar one.
    - Adjust Stopping Distance: help stopping distance more close to lead car(not recommended)
    - Enable E2E Long: Use Comma E2E long, sometimes it is not comfortable. think it's earlier to release.

4. Additional Features except above or more things to explain.
 - It can change cruise mode pushing GAP Button at Cruise Standby status.(OpenpilotStock, Dist+Curv, Dist only, Curv only, OneWay mode, Speedlimit decelation mode only)
 - MapBox support, appreciate to Dragonpilot
 - Showing IP Address/SSID name
 - It has Cruise Button Spamming to adjust car set speed, it uses OP target speed to keep certain distance to lead car. It makes your car smooth when you approch to lead car and acceleration slower than stock.
 - SmartMDPS support
 - Auto Recognition if SCC bus is on 2.

![](https://user-images.githubusercontent.com/37757984/127420744-89ca219c-8f8e-46d3-bccf-c1cb53b81bb1.png)

Table of Contents
=======================

* [What is openpilot?](#what-is-openpilot)
* [Running in a car](#running-in-a-car)
* [Running on PC](#running-on-pc)
* [Community and Contributing](#community-and-contributing)
* [User Data and comma Account](#user-data-and-comma-account)
* [Safety and Testing](#safety-and-testing)
* [Directory Structure](#directory-structure)
* [Licensing](#licensing)

---

What is openpilot?
------

[openpilot](http://github.com/commaai/openpilot) is an open source driver assistance system. Currently, openpilot performs the functions of Adaptive Cruise Control (ACC), Automated Lane Centering (ALC), Forward Collision Warning (FCW) and Lane Departure Warning (LDW) for a growing variety of [supported car makes, models and model years](docs/CARS.md). In addition, while openpilot is engaged, a camera based Driver Monitoring (DM) feature alerts distracted and asleep drivers. See more about [the vehicle integration](docs/INTEGRATION.md) and [limitations](docs/LIMITATIONS.md).

<table>
  <tr>
    <td><a href="https://www.youtube.com/watch?v=mgAbfr42oI8" title="YouTube" rel="noopener"><img src="https://i.imgur.com/kAtT6Ei.png"></a></td>
    <td><a href="https://www.youtube.com/watch?v=394rJKeh76k" title="YouTube" rel="noopener"><img src="https://i.imgur.com/lTt8cS2.png"></a></td>
    <td><a href="https://www.youtube.com/watch?v=1iNOc3cq8cs" title="YouTube" rel="noopener"><img src="https://i.imgur.com/ANnuSpe.png"></a></td>
    <td><a href="https://www.youtube.com/watch?v=Vr6NgrB-zHw" title="YouTube" rel="noopener"><img src="https://i.imgur.com/Qypanuq.png"></a></td>
  </tr>
  <tr>
    <td><a href="https://www.youtube.com/watch?v=Ug41KIKF0oo" title="YouTube" rel="noopener"><img src="https://i.imgur.com/3caZ7xM.png"></a></td>
    <td><a href="https://www.youtube.com/watch?v=NVR_CdG1FRg" title="YouTube" rel="noopener"><img src="https://i.imgur.com/bAZOwql.png"></a></td>
    <td><a href="https://www.youtube.com/watch?v=tkEvIdzdfUE" title="YouTube" rel="noopener"><img src="https://i.imgur.com/EFINEzG.png"></a></td>
    <td><a href="https://www.youtube.com/watch?v=_P-N1ewNne4" title="YouTube" rel="noopener"><img src="https://i.imgur.com/gAyAq22.png"></a></td>
  </tr>
</table>


Running in a car
------

To use openpilot in a car, you need four things
* This software. It's free and available right here.
* One of [the 140+ supported cars](docs/CARS.md). We support Honda, Toyota, Hyundai, Nissan, Kia, Chrysler, Lexus, Acura, Audi, VW, and more. If your car is not supported, but has adaptive cruise control and lane keeping assist, it's likely able to run openpilot.
* A supported device to run this software. This can be a [comma two](https://comma.ai/shop/products/two), [comma three](https://comma.ai/shop/products/three), or if you like to experiment, a [Ubuntu computer with webcams](https://github.com/commaai/openpilot/tree/master/tools/webcam).
* A way to connect to your car. With a comma two or three, you need only a [car harness](https://comma.ai/shop/products/car-harness). With an EON Gold or PC, you also need a [black panda](https://comma.ai/shop/products/panda).

We have detailed instructions for [how to install the device in a car](https://comma.ai/setup).

Running on PC
------

All of openpilot's services can run as normal on a PC, even without special hardware or a car. To develop or experiment with openpilot you can run openpilot on recorded or simulated data.

With openpilot's tools you can plot logs, replay drives and watch the full-res camera streams. See [the tools README](tools/README.md) for more information.

You can also run openpilot in simulation [with the CARLA simulator](tools/sim/README.md). This allows openpilot to drive around a virtual car on your Ubuntu machine. The whole setup should only take a few minutes, but does require a decent GPU.


Community and Contributing
------

openpilot is developed by [comma](https://comma.ai/) and by users like you. We welcome both pull requests and issues on [GitHub](http://github.com/commaai/openpilot). Bug fixes and new car ports are encouraged. Check out [the contributing docs](docs/CONTRIBUTING.md).

Documentation related to openpilot development can be found on [docs.comma.ai](https://docs.comma.ai). Information about running openpilot (e.g. FAQ, fingerprinting, troubleshooting, custom forks, community hardware) should go on the [wiki](https://github.com/commaai/openpilot/wiki).

You can add support for your car by following guides we have written for [Brand](https://blog.comma.ai/how-to-write-a-car-port-for-openpilot/) and [Model](https://blog.comma.ai/openpilot-port-guide-for-toyota-models/) ports. Generally, a car with adaptive cruise control and lane keep assist is a good candidate. [Join our Discord](https://discord.comma.ai) to discuss car ports: most car makes have a dedicated channel.

Want to get paid to work on openpilot? [comma is hiring](https://comma.ai/jobs/).

And [follow us on Twitter](https://twitter.com/comma_ai).

User Data and comma Account
------

By default, openpilot uploads the driving data to our servers. You can also access your data through [comma connect](https://connect.comma.ai/). We use your data to train better models and improve openpilot for everyone.

openpilot is open source software: the user is free to disable data collection if they wish to do so.

openpilot logs the road facing cameras, CAN, GPS, IMU, magnetometer, thermal sensors, crashes, and operating system logs.
The driver facing camera is only logged if you explicitly opt-in in settings. The microphone is not recorded.

By using openpilot, you agree to [our Privacy Policy](https://comma.ai/privacy). You understand that use of this software or its related services will generate certain types of user data, which may be logged and stored at the sole discretion of comma. By accepting this agreement, you grant an irrevocable, perpetual, worldwide right to comma for the use of this data.

Safety and Testing
----

* openpilot observes ISO26262 guidelines, see [SAFETY.md](docs/SAFETY.md) for more details.
* openpilot has software in the loop [tests](.github/workflows/selfdrive_tests.yaml) that run on every commit.
* The code enforcing the safety model lives in panda and is written in C, see [code rigor](https://github.com/commaai/panda#code-rigor) for more details.
* panda has software in the loop [safety tests](https://github.com/commaai/panda/tree/master/tests/safety).
* Internally, we have a hardware in the loop Jenkins test suite that builds and unit tests the various processes.
* panda has additional hardware in the loop [tests](https://github.com/commaai/panda/blob/master/Jenkinsfile).
* We run the latest openpilot in a testing closet containing 10 comma devices continuously replaying routes.

Directory Structure
------
    .
    ????????? cereal              # The messaging spec and libs used for all logs
    ????????? common              # Library like functionality we've developed here
    ????????? docs                # Documentation
    ????????? opendbc             # Files showing how to interpret data from cars
    ????????? panda               # Code used to communicate on CAN
    ????????? third_party         # External libraries
    ????????? pyextra             # Extra python packages
    ????????? selfdrive           # Code needed to drive the car
        ????????? assets          # Fonts, images, and sounds for UI
        ????????? athena          # Allows communication with the app
        ????????? boardd          # Daemon to talk to the board
        ????????? camerad         # Driver to capture images from the camera sensors
        ????????? car             # Car specific code to read states and control actuators
        ????????? common          # Shared C/C++ code for the daemons
        ????????? controls        # Planning and controls
        ????????? debug           # Tools to help you debug and do car ports
        ????????? locationd       # Precise localization and vehicle parameter estimation
        ????????? logcatd         # Android logcat as a service
        ????????? loggerd         # Logger and uploader of car data
        ????????? modeld          # Driving and monitoring model runners
        ????????? proclogd        # Logs information from proc
        ????????? sensord         # IMU interface code
        ????????? test            # Unit tests, system tests, and a car simulator
        ????????? ui              # The UI

Licensing
------

openpilot is released under the MIT license. Some parts of the software are released under other licenses as specified.

Any user of this software shall indemnify and hold harmless Comma.ai, Inc. and its directors, officers, employees, agents, stockholders, affiliates, subcontractors and customers from and against all allegations, claims, actions, suits, demands, damages, liabilities, obligations, losses, settlements, judgments, costs and expenses (including without limitation attorneys??? fees and costs) which arise out of, relate to or result from any use of this software by user.

**THIS IS ALPHA QUALITY SOFTWARE FOR RESEARCH PURPOSES ONLY. THIS IS NOT A PRODUCT.
YOU ARE RESPONSIBLE FOR COMPLYING WITH LOCAL LAWS AND REGULATIONS.
NO WARRANTY EXPRESSED OR IMPLIED.**

---

<img src="https://d1qb2nb5cznatu.cloudfront.net/startups/i/1061157-bc7e9bf3b246ece7322e6ffe653f6af8-medium_jpg.jpg?buster=1458363130" width="75"></img> <img src="https://cdn-images-1.medium.com/max/1600/1*C87EjxGeMPrkTuVRVWVg4w.png" width="225"></img>

[![openpilot tests](https://github.com/commaai/openpilot/workflows/openpilot%20tests/badge.svg?event=push)](https://github.com/commaai/openpilot/actions)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/commaai/openpilot.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/commaai/openpilot/alerts/)
[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/commaai/openpilot.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/commaai/openpilot/context:python)
[![Language grade: C/C++](https://img.shields.io/lgtm/grade/cpp/g/commaai/openpilot.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/commaai/openpilot/context:cpp)
[![codecov](https://codecov.io/gh/commaai/openpilot/branch/master/graph/badge.svg)](https://codecov.io/gh/commaai/openpilot)
