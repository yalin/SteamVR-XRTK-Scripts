# SteamVR-XRTK-Scripts
 SteamVR and XR Interaction Toolkit scripts to work them together

 Credit: The Ghost Howls

 https://skarredghost.com/2020/09/25/steamvr-unity-xr-interaction-toolkit-input/

 ---
## Summary of the tutorial above

### Presequties:
1.	Download SteamVR – XR Pluging tarball
    * https://github.com/ValveSoftware/unity-xr-plugin/releases
    * [com.valvesoftware.unity.openvr-1.1.4.tgz]
2.	Download SteamVR
    * https://github.com/ValveSoftware/steamvr_unity_plugin/releases
    * [steamvr_2_7_3.unitypackage]

### Steps:
1.	Settings; Package Manager; Enable Preview Packages
2.	Settings; XR Plugin Management; Install
3.	Package manager; Unity Registry; XR Interaction Toolkit; Install
4.	Settings; Player; Active input handling; Both
5.	Package Manager + install from tarball; Install (Valve)Unity-XR-Plugin [com.valvesoftware.unity.openvr-1.1.4.tgz]
6.	Assets; Import package; Custom package; [steamvr_2_7_3.unitypackage]
7.	Window; Steam Input;
8.	Copy “<PROJECT_FOLDER>/ Library/PackageCache/com.unity.xr.interaction.toolkit@1.0.0-pre.4” to “C:/”
9.	Package Manager; XR Interaction Toolkit; Uninstall
10.	Copy back “C:/com.unity.xr.interaction.toolkit@1.0.0-pre.4” under “<PROJECT_FOLDER>/Assets/”
    * If it gives error about “InputSystem” then Package manager; Unity Registry; Input System; Install
11.	Under xr file; Select -> Runtime/ Unity.XR.Interaction.Toolkit
    * Inspector (Unity tab); Assembly Definition Reference; Add two new; SteamVR, SteamVR_Actions; Apply
12.	Modify “Runtime\Interaction\Controllers\XRController.cs”
13.	Modify “Runtime\XR\InputHelpers.cs”
14.	Create “Runtime\Interaction\InputDeviceWrapper.cs”