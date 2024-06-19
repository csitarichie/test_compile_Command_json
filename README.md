# Clion Compile command Json issues 

# Install latest XCode with all possible SDKs. (more the better to see the isssue).

### gereate compile_command run:

```bash
./generate-xcode-compilation-database.sh xcodebuild -configuration Debug -arch arm64e build
```
then open the gereated `compile_command.json` file in Clion as project

you will see all the SDK are in the indexer shearch path eg:
```bash
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_AppIntents_AppKit.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_AppIntents_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_AuthenticationServices_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_AVKit_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_CoreData_CloudKit.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_CoreData_CloudKit.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_DeviceActivity_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_GroupActivities_AppKit.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_LocalAuthentication_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_ManagedAppDistribution_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_MapKit_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_MusicKit_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_PassKit_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_PhotosUI_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_QuickLook_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_SceneKit_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_SpriteKit_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_StoreKit_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_SwiftData_CoreData.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_SwiftData_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/_Translation_SwiftUI.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accelerate.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accelerate.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accelerate.framework/Frameworks/vecLib.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accelerate.framework/Frameworks/vImage.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accessibility.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accessibility.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accounts.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Accounts.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AddressBook.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AddressBook.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AdServices.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AdServices.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AdSupport.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AdSupport.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AGL.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AGL.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppIntents.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppIntents.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppKit.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppKit.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppleScriptKit.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppleScriptKit.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppleScriptObjC.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppleScriptObjC.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/ATS.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/ATSUI.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/ColorSync.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/ColorSync.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/CoreGraphics.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/CoreGraphics.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/CoreText.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/CoreText.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/HIServices.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/ImageIO.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/ImageIO.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/PrintCore.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/QD.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/ApplicationServices.framework/Frameworks/SpeechSynthesis.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppTrackingTransparency.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AppTrackingTransparency.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AudioToolbox.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AudioToolbox.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AudioUnit.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AudioUnit.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AudioVideoBridging.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AudioVideoBridging.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AuthenticationServices.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AuthenticationServices.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AutomaticAssessmentConfiguration.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AutomaticAssessmentConfiguration.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Automator.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/Automator.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVFAudio.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVFAudio.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVFoundation.framework/Frameworks/AVFAudio.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVFoundation.framework/Frameworks/AVFAudio.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVFoundation.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVFoundation.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVKit.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVKit.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVRouting.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/AVRouting.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BackgroundAssets.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BackgroundAssets.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BackgroundTasks.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BackgroundTasks.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BrowserEngineCore.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BrowserEngineCore.framework/Modules
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BrowserEngineKit.framework/Headers
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX14.5.sdk/System/Library/Frameworks/BrowserEngineKit.framework/Modules
```
