# start-babylon-native
 一个 Babylon Native 脚手架，基于 C++ CMake 跨平台

## 简介
- 官网：https://www.babylonjs.com/native/
- 仓库：https://github.com/BabylonJS/BabylonNative

## 跨平台
![Babylon Native and Babylon React Native](https://github.com/BabylonJS/BabylonNative/blob/master/Documentation/Images/hybrid_app_spectrum.png)

### 1、Babylon.js
- Web：WebGL/WebGPU/WebXR

### 2、Babylon Native
> 使用 Node.js (约 20 MB)，使用 N-API 通讯
- Windows：DirectX
- macOS：Metal
- Linux
- iOS：Metal
- Android：OpenGL/Vulkan

### 3、Babylon React Native
> 使用 React Native + Babylon Native，使用 JSI 通讯
- iOS
- Android

## JS+Native 架构
![Babylon Native](https://miro.medium.com/v2/resize:fit:720/format:webp/1*0PkLts2H4m082-sr4bwILw.png)
