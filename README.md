# Taurine Haxx

⚠️ Warning ⚠️ I am not liable if you get bootlooped, if you bootloop do not blame me. 

Taurine Untethered

Based on [haxx](https://github.com/asdfugil/haxx)

## Usage

Requires: Existing Taurine jailbreak and iOS 14.0 - 14.6

### Get up and running

1. Install [Taurine Untethered](https://github.com/AppInstalleriOSGH/Taurine/raw/main/Taurine.ipa) with TrollStore
2. On the device, Copy `/System/Library/PrivateFrameworks/CoreAnalytics.framework/Support/analyticsd` to `/System/Library/PrivateFrameworks/CoreAnalytics.framework/Support/analyticsd.back`
3. Then replace `/System/Library/PrivateFrameworks/CoreAnalytics.framework/Support/analyticsd` with `/usr/bin/fileproviderctl`
4. Create an empty file at `/var/mobile/.untether`
5. Copy `fileproviderctl_internal` to `/usr/local/bin` on the device, mode should be 0755.
5. You're done! The jailbreak will start about 40 seconds after every boot, you can make it faster by changing the [sleep time](https://github.com/AppInstalleriOSGH/Taurine-Haxx/blob/main/fileproviderctl_internal.m#L13) to a lower number

### Disable

To disable the untether, do the following steps
1. Delete `/var/mobile/.untether`

### Removal

To remove the installation, do the following steps
1. Copy `/System/Library/PrivateFrameworks/CoreAnalytics.framework/Support/analyticsd` to `/usr/bin/fileproviderctl`
2. Move `/System/Library/PrivateFrameworks/CoreAnalytics.framework/Support/analyticsd.back` to `/System/Library/PrivateFrameworks/CoreAnalytics.framework/Support/analyticsd`
3. Delete `/var/haxx`, `/usr/local/bin/fileproviderctl_internal` as well as `/usr/local/bin/haxx`
