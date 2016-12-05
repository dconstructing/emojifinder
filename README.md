# emojifinder
Android App to help find and use emoji

## Developing

Do not run `npm install` to install dependencies. Newer npm versions install all modules at the same level in the `node_modules` directory. It appears that this overwhelms the way nativescript uses node to process modules. It is better to install dependencies with `tns install`

1. Make sure your environment is setup for NativeScript - [Getting Started](http://docs.nativescript.org/start/getting-started)
 - This particular project does not require that you have NativeScript installed globally, so you can skip that step.

2. `npm run tns -- install` or (if nativescript is install globally) `tns install`

3. Delete `node_modules/nativescript/node_modules/log4js/node_modules/semver/semver.browser.js.gz` and `node_modules/nativescript/node_modules/log4js/node_modules/semver/semver.min.js.gz`
   - At least until nativescript uses log4js 1.0.1 or newer.

4. Delete `node_modules/emojione/assets` directory.
   - We don't need the actual images and they bloat the app size.

4. Add app icons as `ic_launcher.png`
```
app/App_Resources/Android/mipmap-xxxhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-xxhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-xhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-mhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-hhdpi/ic_launcher.png
```

To deploy to your device, run `npm run launch`, `npm run tns -- run android`, or (if nativescript is installed globally) `tns run android`

## Release

```
npm run tns -- build android --release --key-store-path /media/dcox/DUOLINK3/security/dconstructing-release-B.keystore --key-store-password <keystore password> --key-store-alias emoji --key-store-alias-password <keystore alias password>
```
Yeah, you really do have to type your password into the console.
