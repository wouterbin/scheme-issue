## requirements:

```
npm install -g cordova@6.5.0
npm install -g ios-deploy
```

## run:

in app directory:

```
cordova platforms add iOS
cordova run ios
```

'run ios' will likely fail, because no Team is set

```
open platforms/ios/app_name.xcodeproj
```

set the team and run

## reproduce

* Open the schemetest app
* click on 'OPEN REDIRECT APP'
* The redirect app will be opened
* After three seconds the redirect app opens the schemetest app again
* Then the schemetest app crashes

When XCode is attached you will see that it crashes on an infinite loop. The issue is in the GooglePlus.m:66

The issue can simply be fixed by returning false. But thats obviously not the right approach.
