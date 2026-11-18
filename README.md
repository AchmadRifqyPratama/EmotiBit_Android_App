# EmotiBit Android App

Android app for streaming data from an [EmotiBit](https://www.emotibit.com/) wearable biometric sensor over Wi-Fi and plotting it in real time.

> Fork of [EmotiBit/EmotiBit_Android_App](https://github.com/EmotiBit/EmotiBit_Android_App), released under the MIT License (see [`LICENSE`](LICENSE)).

## Features

- Discovers EmotiBit devices on the local network and connects to them over **UDP**. Classes are in `Network/`.
- Parses the EmotiBit data packets (`Datas/`). Supported data types:
  - 3-axis accelerometer, gyroscope and magnetometer
  - EDA / EDL / EDR
  - humidity, temperature and thermistor
  - PPG red / IR / green
  - battery level and status messages
- Plots live data with [GraphView](https://github.com/jjoe64/GraphView) (`Drawing/PlotDatas.java`).
- Sends control commands to the device (`Network/ActionSender.java`).
- Includes a Google Maps screen (`MapsActivity`).

## Tech stack

- Java, Android Support Library 28
- `compileSdk`/`targetSdk` 28, `minSdk` 23
- GraphView 4.2.2, Google Play Services Maps 16.0.0

## Build

1. Open the project in Android Studio and let Gradle sync.
2. To use the map screen, add a Google Maps API key in `app/src/debug/res/values/google_maps_api.xml` (and in `release`).
3. Connect the phone and the EmotiBit to the same Wi-Fi network, then run the `app` configuration.

The project uses the old Android Support Library and Gradle plugin versions from 2019, so a recent Android Studio may ask to upgrade them.
