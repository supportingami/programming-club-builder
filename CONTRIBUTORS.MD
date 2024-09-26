## Contributors

### Running this example

To run the example in local browser, you can use `npm start` command.

```bash
npm start
```

### Building for Android

First time running on android will require adding the Android platform and generating icons

```bash
npx cap add android
npx capacitor-assets generate
```

Once the platform has been added code can be compiled and imported into the android app

```bash
npm run build
npx cap sync
```

The android version can now be run locally using Android Studio, or built into an app bundle file to run on device using Github Actions
