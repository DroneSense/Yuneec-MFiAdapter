# Yuneec-MFiAdapter

This repo contains all the pieces needed to talk to the ST10C Remote Controller. The source of this framework can be fetched using command:
```
git clone https://github.com/YUNEEC/Yuneec-MFiAdapter.git
```
This repo also uses submodule c_library_v2, which should be fetched using command:
```
git submodule update --init
```
An example usage of these frameworks can be found in [YUNEEC/MFiExample](https://github.com/YUNEEC/MFiExample/). More information about the ST10C Remote Controller can be found [here](https://developer.yuneec.com/documentation/127/Remote-Controller).

## Frameworks

In an iOS app, the frameworks below need to be added to the "Embedded Binaries":

   - `BaseFramework`
   - `CocoaAsyncSocket`
   - `FFMpegDecoder`
   - `FFMpegDemuxer`
   - `FFMpegLowDelayDecoder`
   - `FFMpegLowDelayDemuxer`
   - `MediaBase`
   - `MFiAdapter`
   - `YuneecDataTransferManager`
   - `YuneecMFiDataTransfer`
   - `YuneecRemoteControllerSDK`
   - `YuneecWifiDataTransfer`

### Use Carthage to get the framework

To use the MFiAdapter in your iOS application, you can pull in this framework using [Carthage](https://github.com/Carthage/Carthage).

To install carthage, it's easiest to use [Homebrew](https://brew.sh/):

```
brew install carthage
```

Then to add the framework: 

* Create the file `Cartfile` in your app's repository with below's content:

```
# Require the iOS framework of Yuneec-MFiAdapter
github "YUNEEC/Yuneec-MFiAdapter" "master"
```

Then, to pull in the library and build it, run Carthage in your app's repository:

```
carthage update
```

This command needs to be re-run if you want to udpate the framework.  

* Or create the file `Cartfile.resolved` in your app's repository with below content:

```
# Require the iOS framework of Yuneec-MFiAdapter
github "YUNEEC/Yuneec-MFiAdapter" "some-commit"
```

Then, to pull in the library and build it, run Carthage in your app's repository:

```
carthage bootstrap --platform ios --use-ssh
```

This command also needs to be re-run if you want to update the framework.  
