# emojifinder
Android App to help find and use emoji

## Developing

1. Make sure your environment is setup for NativeScript - [Getting Started](http://docs.nativescript.org/start/getting-started)
 - This particular project does not require that you have NativeScript installed globally, so you can skip that step.

2. `npm install`

3. `npm run tns platform add android`

4. Add app icons as `ic_launcher.png`
```
app/App_Resources/Android/mipmap-xxxhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-xxhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-xhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-mhdpi/ic_launcher.png
app/App_Resources/Android/mipmap-hhdpi/ic_launcher.png
```

To deploy to your device, run `npm run launch`
