# ARLab
### an AR Experimental Application based on SLAM and Unity3D
![system](https://badgen.net/badge/Application/Augmented%20Reality/blue)
![env](https://badgen.net/badge/Environment/x64%2Farm64/green)
![slam](https://badgen.net/badge/Locator/SLAM/orange)
![unity](https://badgen.net/badge/Render/Unity/orange)

<br>

**[ARM64 Android Device]**
![android](Assets/Android.png)

**[X64 Windows Device with USB Camera]**
![intro](Assets/intro.png)

<br>

## Environment
- Windows 11
- Android 13
- Unity 2020.3.21f1
- Android Studio 2022.1.1
- Visual Studio 2019
- OpenCV 4.6
- ORB-SLAM2

## SLAM
- The system locator is built based on ORB-SLAM2 which simplified the `viewer` module. To config SLAM system, go to directory `${Unity_project}/Config/ORB.yaml`.

- View more details at `SLAM_lib/readme.md`.

## Unity
- The system render is based on Unity3D. The shared library of SLAM system built with Visual Studio 2019 is at directory `${Unity_project}/Assets/Plugins/locator.dll`.

- Press `PUT` button to re-put the AR model, which will look at the camera.Press `DEBUG` button to view track points on slam-system, the plane detected and the original point of the world-coordinate-system.

- At first time use, you may need to place `${Unity_project}/Assets/MainScene.unity` to the scene list and remove the original one.

## Android
- The system now is available on Android devices. You should check the `jnilibs` directory so that youc can build the application successfully. Especially, the `libc++_shared.so` is required but it is not included when exported from Unity3D.

- To use the app, don't forget to grant the camera permission. On the UI, you can press `PUT` button to re-put the AR model, which will look at the camera just as it done on windows. Press `DEBUG` button to view track points on slam-system, the plane detected and the original point of the world-coordinate-system.

- The Sparrow model will randomly change its animation from 5s to 15s. You can also manually change the animation by pressing the `CHANGE` button.

- **[NOTICE]** When first installing the app, you need to copy the `Config` folder to the `/storage/emulated/0/Android/data/com.labx.arlab/files/` directory so that the app can find config files. The zipped file of `Config` folder is in the `Assets` directory of the repo and also at the `release` page.

## On Working
- [ ] **MORE** interactive operations
- [ ] **MORE** beautiful user-interface
- [ ] **IMPROVE** the accuracy of plane detected on SLAM system
- [ ] **IMPORT** `Yolo` to solve the problem of *dynamic* objects and *covered* objects
- [x] **EXPORT** and build application for `Android` devices

## Contact
To contact with the author, please send email to `halc@bupt.edu.cn`

<br>

### Enjoy Your AR Experience!