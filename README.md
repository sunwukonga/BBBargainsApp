# Bebe Bargains React Native App 

This repository is meant to be used with it's environment at:
```
https://github.com/sunwukonga/docker-react-native.git
```

## Errata

If you see the following error message:
```
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:installDebug'.
> com.android.builder.testing.api.DeviceException: com.android.ddmlib.InstallException: Failed to finalize session : INSTALL_FAILED_UPDATE_INCOMPATIBLE: Package com.bbbargainsapp signatures do not match the previously installed version; ignoring!
```
You've probably installed this repository in multiple locations (i.e. different computers perhaps), but trying to use with the same physical device (phone). The solution is to delete the package from the phone first:
```
adb uninstall "com.bbbargainsapp"
```
The package name is helpfully supplied in the error message. Try again.
