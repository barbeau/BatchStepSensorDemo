# BatchStepSensor

This is the sample project from the Android SDK that demonstrates the
[step detector](https://source.android.com/devices/sensors/composite_sensors.html#detector) and [step counter](https://source.android.com/devices/sensors/composite_sensors.html#counter) hardware sensors.

You must have a device that supports Sensor [TYPE_STEP_DETECTOR](http://developer.android.com/reference/android/hardware/Sensor.html#STRING_TYPE_STEP_DETECTOR) and [TYPE_STEP_COUNTER](http://developer.android.com/reference/android/hardware/Sensor.html#STRING_TYPE_STEP_COUNTER) to run the project.

## Build Setup

### Prerequisites for both Android Studio and Gradle

1. Set the `JAVA_HOME` environmental variables to point to your JDK folder (e.g. `C:\Program Files\Java\jdk1.6.0_27`)

### Building in Android Studio

1. Download and install the latest version of [Android Studio](http://developer.android.com/sdk/installing/studio.html).
2. Run Android Studio (Windows users may need to `Run as administator` when installing Android SDK components).
3. At the welcome screen select `Import Project`, browse to the location of this repository and double-click it.
4. Open the Android SDK Manager (Tools->Android->SDK Manager) and under the currently used SDK version (see `compileSdkVersion` in [`BatchStepSensorSample/build.gradle`](BatchStepSensorSample/build.gradle)) add a checkmark next to `Google APIs` then select `Install n packages`. `n` may be 1 or more if other updates are available.
5. Connect a [debugging enabled](https://developer.android.com/tools/device.html) Android device to your computer or setup an Android Virtual Device (Tools->Andorid->AVD Manager).
6. Click the green play button (or Alt+Shift+F10) to build and run the project!

### Building from the command line using Gradle

1. Download and install the [Android SDK](http://developer.android.com/sdk/index.html). Make sure to install the Google APIs for your API level (e.g. 17), the Android SDK Build-tools version for your `buildToolsVersion` version, the Android Support Repository and the Google Repository.
2. Set the `ANDROID_HOME` environmental variable to your Android SDK location.
3. To build and push the app to the device, run `gradlew installDebug` from the command line at the root of the project
4. To start the app, run `adb shell am start -n com.example.android.batchstepsensor/.MainActivity` (alternately, you can manually start the app)