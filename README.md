# Tauri mobile alpha + Android
The template is only tested to run on linux and build for linux/android.

## Warning

Tauri mobile is currently in alpha state. Please be aware that breaking changes may happen, thus making the newest version incompatible with previous ones. I'll try to do my best to keep this template up to date.

## Prerequisites

Follow the [Tauri mobile guide on setting up linux](https://next--tauri.netlify.app/next/guides/getting-started/prerequisites/linux)


After you have added the prequisites, get the tauri cli ( 2.0 alpha version):

```
cargo install tauri-cli --version "^2.0.0-alpha"
```

We also are using `pnpm`, so have that installed too, or use npm:

```
npm install -g pnpm
```

## Development

First, clone this repository or use the Github template feature. then, `cd` into
the project directory to perform the following steps:

Download project dependencies:

```
pnpm i
```

Run `tauri dev` to compile dependencies and verify that the app will run locally,
before attempting to run on mobile.

```
cargo tauri dev
```

you should see something similar to the following:

<img src="example-desktop.png" alt="app screenshot on desktop" width="300"/>



after verifying that the app can actually run, setup the mobile features:

```
pnpm add -D internal-ip
```

```
cargo tauri android init
```

Plug in an android phone that is configured to sideload apps using debug mode 
and run the following command to send your application to your phone:

```
cargo tauri android dev
```

Alternatively you could set up an emulator.

Eventually(1 min+), the webview will time out and you may see the following:


<img src="example-android.jpeg" alt="app screenshot on android" width="250"/>
