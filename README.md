## Programming Club

This repo contains minimal templates to help develop a mobile app.

## Prepare source code

Create a github repo and add your project source code

## Add android build action

In your own code repo add a file `.github\actions\android-build.yml`

In this file paste the code

```yml
name: Android Build
on:
  workflow_dispatch:
  push:
    branches:
      - main
jobs:
  android_build:
    uses: supportingami/programming-club-builder/.github/workflows/android-build.yml@main
    with:
      dist-path: demo
      icon-path: logo.png
      app-name: Programming Club Demo
      app-id: club.programming.app
```

Update the values in the `with` section to provide your own app information

## Test

Once the code has been committed to the `main` branch you should see the triggered action run from within the GitHub Actions page

Once complete the action will populate an `android` zip folder that includes an apk that can be installed on any android device
