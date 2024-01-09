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
- Windows：D3D11 (default), D3D12, or Vulkan
- macOS：Metal
- iOS：Metal
- Android：OpenGL (default), Vulkan
- Linux：OpenGL (default), Vulkan

### 3、Babylon React Native
> 使用 React Native + Babylon Native，使用 JSI 通讯
- iOS
- Android

## JS+Native 架构
![Babylon Native](https://miro.medium.com/v2/resize:fit:720/format:webp/1*0PkLts2H4m082-sr4bwILw.png)

## 编译（交叉编译）
- git
- CMake
- node.js

### Windows
- Visual Studio 2019
- Python 3.0

```bash
# for x64
# 支持两种 JavaScript 引擎: Chakra (默认) 和 V8
cmake -B build/win32 -D NAPI_JAVASCRIPT_ENGINE=V8
# for x86
cmake -B build/win32_x86 -A Win32

# for UWP
cmake -B build/uwp_arm64 -D CMAKE_SYSTEM_NAME=WindowsStore -D CMAKE_SYSTEM_VERSION=10.0 -A arm64

# for HoloLens 2（XR）
# ...
```

### macOS/iOS
- Xcode 11
- Python 3.0

```bash
# for macOS
cmake -B build/macOS -G Xcode

# for iOS
# -D ENABLE_BITCODE=ON  启用 bitcode 
cmake -B build/iOS -G Xcode -D IOS=ON
```

### Android（on Windows）
- Android Studio
- Ninja

```bash
# for Android 5.0 with an OpenGL ES 3.0 compatible GPU
# 支持两种 JavaScript 引擎: V8 (默认) 和 JavaScriptCore
Android Studio
```

### Linux（on Ubuntu）
- Clang or GCC
- JavaScriptCore or V8

```bash
# 需要手动安装依赖
cmake -B build/Linux -G Ninja -D NAPI_JAVASCRIPT_ENGINE=V8
ninja
```
