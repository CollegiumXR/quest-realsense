# Oculus Quest - Intel RealSense Integration
Integration of Intel RealSense depth cameras with the Oculus Quest standalone VR headset using Unity.


## Foreword

<br/>

This project consolidates the knowledge gained while attempting to power & operate a RealSense D435i camera directly from an Oculus Quest VR headset. 

At the time of this attempt (5th-12th of June 2019), no prior work on this specific problem was available in the public realm, and the solution wouldn't be possible without the valuable contribution of members of the Intel development team.

The discussion which led to the solution, is available [here](https://github.com/IntelRealSense/librealsense/issues/4155), for future reference.

Aim of this project is to describe the steps necessary to achieve the Quest-RealSense integration inside Unity 2019.x, as well as to provide simple and generic source code.


_George Adamopoulos_

_23 of June 2019_

<br/>

## Introduction
**Development environment:**

| Label | Info  |
|----------------------------|-----------------|
| Operating System & Version | Windows 10 1803 |
| Language                   | C#              | 
| Unity Version              | 2019.1.4f1      |
| Graphics API               | OpenGLES3       |
| Scripting API Version      | .NET 4.x        |

<br/>

**RealSense Depth Camera Information:**

| Label  |  Info  |
|----------------------------|-----------------|
| Camera Model               | D435i           |
| Firmware Version           | 5.11.6.200 +    | 
| SDK Version                | 2.22.0 +        | 

<br/>

**Oculus Quest Information:**

| Label  |  Info  |
|----------------------------|-----------------|
| Headset Model              | Quest (May 2019)|
| Headset Version            | 256550.6170.5 + | 
| Unity Package Version      | 1.36 +          | 



## Step 1: Project Setup (Windows)
### Prerequisites
This guide assumes that the necessary steps for setting-up the Unity development environment for the Oculus Quest have been completed, as described in the official Oculus Quest documentation: [[1]](https://developer.oculus.com/documentation/quest/latest/concepts/unity-build-android/) [[2]](https://developer.oculus.com/documentation/quest/latest/concepts/unity-mobileprep/)

The project should be able to produce a working Android .apk build, which runs on the Quest without issues, before proceeding to the next steps.

### Scripting Backend : Mono
Navigate to Unity's _Project Settings > Player > Other Settings_ and ensure that the Scripting Backend is set to **Mono**.
According to [this](https://github.com/IntelRealSense/librealsense/issues/4155#issuecomment-499363798) reply the RealSense library does not support Unity's IL2CPP library, at least at the time of writing this.

![](https://github.com/GeorgeAdamon/quest-realsense/blob/master/resources/img-scripting-backend.png)

### Importing RealSense Unity wrappers
This guide assumes that the latest Intel RealSense Unity wrappers [**package**](https://github.com/IntelRealSense/librealsense/releases/download/v2.20.0/realsense.unitypackage) can be imported succesfully in Unity without errors, and that one of the provided example projects can be run succesfully on a

## Step 2: Building the librealsense.aar Android library

## Step 3: Initializing the RsContext Java class from Unity

## Step 4: Using Quest-friendly shaders
