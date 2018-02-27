# Agora client side AV capturing for streaming Android

*其他语言版本： [简体中文](README.zh.md)*

The Agora client side AV capturing for streaming Android Sample App is an open-source demo that shows how to build a video chat application via Agora Video SDK, and get raw data of audio and video streaming to push to RTMP server.

With this sample app, you can:

- Join / leave channel
- Get raw data of audio and video streaming from Agora Video SDK
- Merge raw data to push to RTMP server

A tutorial demo for Agora Video SDK can be found here: [Agora-Android-Tutorial-1to1](https://github.com/AgoraIO/Agora-Android-Tutorial-1to1)

You can find demo for iOS here: [Agora-client-side-AV-capturing-for-streaming-iOS](https://github.com/AgoraIO/Agora-client-side-AV-capturing-for-streaming-iOS)

## Running the App
**First**, create a developer account at [Agora.io](https://dashboard.agora.io/signin/), and obtain an App ID. Update "app/src/main/res/values/strings_config.xml" with your App ID.

```
<string name="private_app_id"><#YOUR APP ID#></string>
```

**Next**, integrate the Agora Video SDK and there are two ways to integrate:

- The recommended way to integrate:

First, add the address which can integrate the Agora Video SDK automatically through JCenter in the property of the dependence of the "app/build.gradle":
```
compile 'io.agora.rtc:full-sdk:2.0.0'
```
(This sample program has added this address and do not need to add again. Adding the link address is the most important step if you want to integrate the Agora Video SDK in your own application.)

Then, download the **Agora Video SDK** from [Agora.io SDK](https://www.agora.io/en/blog/download/). Unzip the downloaded SDK package and copy **IAgoraMediaEngine.h**/**IAgoraRtcEngine.h** under **libs/include** to **app/src/main/cpp/include/agora**.

- Alternative way to integrate:

First, download the **Agora Video SDK** from [Agora.io SDK](https://www.agora.io/en/download/). Unzip the downloaded SDK package and copy ***.jar** under **libs** to **app/libs**, **arm64-v8a**/**x86**/**armeabi-v7a** under **libs** to **app/src/main/jniLibs**,**IAgoraMediaEngine.h**/**IAgoraRtcEngine.h** under **libs/include** to **app/src/main/cpp/include/agora**.

Then, add the fllowing code in the property of the dependence of the "app/build.gradle":

```
compile fileTree(dir: 'libs', include: ['*.jar'])
```

**Finally**, open project with Android Studio, connect your Android device, build and run.

Or use `Gradle` to build and run.

## Developer Environment Requirements
- Android Studio 2.0 or above
- Real devices (Nexus 5X or other devices)
- Some simulators are function missing or have performance issue, so real device is the best choice

## Connect Us

- You can find full API document at [Document Center](https://docs.agora.io/en/)
- You can file bugs about this demo at [issue](https://github.com/AgoraIO/Agora-client-side-AV-capturing-for-streaming-Android/issues)

## License

The MIT License (MIT).
