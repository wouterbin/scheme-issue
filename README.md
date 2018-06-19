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
