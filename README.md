# A-Font

Change your font systemwide! Be it a cute font, a normal font, or any fonts you find interesting, you can change it with A-Font!

> [!IMPORTANT]
> You won't receive any new updates after this one, unless there are any noticeable bugs. 
> (in reality, I don't know much so there's not much I can help with, but this is my first shot at Logos so I'll try)

## Installation

Grab a build in the Releases page and install it! 

## Building

In order to build A-Font for yourself, follow these steps:
---
1. Install Theos

Install Theos on your device:

```sh
bash -c "$(curl -fsSL https://raw.githubusercontent.com/theos/theos/master/bin/install-theos)"
```

<details>
    <summary>Windows users</summary>

    Install a Linux distro following [Microsoft's instructions](https://aka.ms/wslinstall)
</details>

2. Grab the SDK and copy it to your Theos SDKs directory

```sh
curl -LO https://github.com/Actionizer/apple-oses-sdks/releases/download/iOS-15.6/iPhoneOS15.6.sdk.zip
unzip iPhoneOS15.6.sdk.zip
cp -R iPhoneOS15.6.sdk $THEOS/sdks/
```

2. Clone the repository

```sh
git clone https://github.com/MineTurtlee/A-Font.git && cd A-Font
```

3. Adjust rootness based on your jailbreak

- Open the `control` file
- Change the rootness (Architecture):
    - Rootful: iphoneos-arm
    - Rootless: iphoneos-arm64

4. Build

```sh
make package FINALPACKAGE=1
```