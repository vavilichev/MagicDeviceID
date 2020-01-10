# MagicDeviceID
This is magic DeviceID tool. It works different on the different platforms. The complicatest way is on iOS devices. It generate magic unique password and save it in iTunes with App name like login-password pair. In the future I want to improve this tool and give it optional method that saves this deviceId in the Google Play to link ID with Google Play account.

Spoiler: the main author of the tool is not me. The main part was taken here: https://github.com/HuaYe1975/Unity-iOS-DeviceID

> UDID solution for Android/iOS.
> 
> **About DeviceID**
> - It will create a uuid string and save it to keychain for ios
> - It will return mac address's MD5 (ADID when >= API Level23) for android
> - return SystemInfo.deviceUniqueIdentifier for other platforms.
> 
>
> **How to use**
>
> It is so easy to use it on unity:
> 
> Call 'GetDeviceID' method with callback (deviceId returns)
> ```
> DeviceIDManager.GetDeviceID((deviceid) => {
>       if (!string.IsNullOrEmpty(deviceid))
>           deviceID.text = deviceid;
> });
> ```
> Note
> You'd better change the value of macroes in KeyChain.mm for ios:
> ```
> #define SERVICE_NAME    @"my_service_name"
> #define IDENTIFIER      @"my_app_identifier"
> #define ACOUNT_ID       @"my_account"
> ```
