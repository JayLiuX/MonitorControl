<img src=".github/Icon-cropped.png" width="200" alt="App icon" align="left"/>

<div>
<h3>MonitorControl</h3>
<p>Controls your external display brightness and volume and shows native OSD.
Use menubar extra sliders or the keyboard, including native Apple keys!</p>
<a href="https://github.com/MonitorControl/MonitorControl/releases"><img src=".github/macos_badge_noborder.png" width="175" alt="Download for macOS"/></a>
</div>

<br/><br/>

<div align="center">
<a href="https://github.com/MonitorControl/MonitorControl/releases"><img src="https://img.shields.io/github/downloads/MonitorControl/MonitorControl/total.svg?style=flat" alt="downloads"/></a>
<a href="https://github.com/MonitorControl/MonitorControl/releases"><img src="https://img.shields.io/github/release-pre/MonitorControl/MonitorControl.svg?style=flat" alt="latest version"/></a>
<a href="https://github.com/MonitorControl/MonitorControl/blob/master/License.txt"><img src="https://img.shields.io/github/license/MonitorControl/MonitorControl.svg?style=flat" alt="license"/></a>
<a href="https://github.com/MonitorControl/MonitorControl"><img src="https://img.shields.io/badge/platform-macOS-blue.svg?style=flat" alt="platform"/></a>

<br/>
<br/>

<img src=".github/screenshot.png" width="824" alt="Screenshot"/><br/>

</div>

<hr>

> [!WARNING]
> MonitorControl v4.2.0 [may crash](https://github.com/MonitorControl/MonitorControl/issues/1663) on certain configurations running macOS 15 Sequoia. Additionally, this version will not automatically update to the [latest app version](https://github.com/MonitorControl/MonitorControl/releases). To resolve the issue and ensure future updates, please upgrade manually.

## Download

Go to [Releases](https://github.com/MonitorControl/MonitorControl/releases) and download the latest `.dmg`, or you can install via Homebrew:
```shell
brew install --cask monitorcontrol
```

## Major features

- Control your display's brightness, volume and contrast!
- Shows native OSD for brightness and volume.
- Supports multiple protocols to adjust brightness: DDC for external displays (brightness, contrast, volume), native Apple protocol for Apple and built-in displays, Gamma table control for software dimming, shade control for AirPlay, Sidecar and Display Link devices and other virtual screens.
- Supports smooth brightness transitions.
- Seamlessly combined hardware and software dimming extends dimming beyond the minimum brightness available on your display.
- Synchronize brightness from built-in and Apple screens - replicate Ambient light sensor and touch bar induced changes to a non-Apple external display!
- Sync up all your displays using a single slider or keyboard shortcuts.
- Allows dimming to full black.
- Support for custom keyboard shortcuts as well as standard brightness and media keys on Apple keyboards.
- Dozens of customization options to tweak the inner workings of the app to suit your hardware and needs (don't forget to enable `Show advanced settings` in app Settings).
- Simple, unobtrusive UI to blend in to the general aesthetics of macOS.
- **One of the best app of its kind, completely FREE.**

For additional features, more advanced brightness control with XDR/HDR brightness upscaling and support for more Mac models and displays, check out [BetterDisplay](https://github.com/waydabber/BetterDisplay#readme)!

### Screenshots (Settings)

<div align="center">
<img src=".github/pref_1.png" width="392" alt="Screenshot"/>
<img src=".github/pref_2.png" width="392" alt="Screenshot"/>
<img src=".github/pref_3.png" width="392" alt="Screenshot"/>
<img src=".github/pref_4.png" width="392" alt="Screenshot"/>
</div>

## How to install and use the app

1. [Download the app](https://github.com/MonitorControl/MonitorControl/releases)
2. Copy the MonitorControl app file from the .dmg file to your Applications folder
3. Click on the `MonitorControl` app
4. Add the app to `Accessibility` under `System Settings` » `Privacy & Security` as prompted (this is required only if you wish to use the native Apple keyboard brightness and media keys - if this is not the case, you can safely skip this step).
5. Use your keyboard or the sliders in the app menu (a brightness symbol in the macOS menubar as shown on the screenshot above) to control your displays.
6. Open `Settings…` for customization options (enable `Show advanced settings` for even more options).
7. You can set up custom keyboard shortcuts under the `Keyboard` in Settings (the app uses Apple media keys by default).
8. If you have any questions, go to [Discussions](https://github.com/MonitorControl/MonitorControl/discussions)!

### macOS compatibility

| MonitorControl version | macOS version     |
| ---------------------- | ----------------- |
| v4.0.0                 | Catalina 10.15*   |
| v3.1.1                 | Mojave 10.14      |
| v2.1.0                 | Sierra 10.12      |

_* With some limitations - full functionality available on macOS 11 Big Sur or newer._

For macOS Sequoia compatibility [v4.3.2 or newer](https://github.com/MonitorControl/MonitorControl/releases) is required!

### Supported displays

- Most modern LCD displays from all major manufacturers supported implemented DDC/CI protocol via USB-C, DisplayPort, HDMI, DVI or VGA to allow for hardware backlight and volume control.
- Apple displays and built-in displays are supported using native protocols.
- LCD and LED Televisions usually do not implement DDC, these are supported using software alternatives to dim the image.
- DisplayLink, Airplay, Sidecar and other virtual screens are supported via shade (overlay) control.

Notable exceptions for hardware control compatibility:

- DDC control using the built-in HDMI port of the 2018 Intel Mac mini, the built-in HDMI port of all M1 Macs (MacBook Pro 14" and 16", Mac Mini, Mac Studio) and the built-in HDMI port of the entry level M2 Mac mini are not supported. Use USB-C instead or get [BetterDisplay](https://betterdisplay.pro) for full DDC control over HDMI with these Macs as well for free. Software-only dimming is still available for these connections.
- Some displays (notably EIZO) use MCCS over USB or an entirely custom protocol for control. These displays are supported with software dimming only.
- DisplayLink docks and dongles do not allow for DDC control on Macs, only software dimming is available for these connections.

Compatibility with 

- f.lux users: please activate `Avoid gamma table manipulation` under `Settings` » `Displays`! This step is not needed if you use Night Shift.
- [BetterDisplay](https://betterdisplay.pro/) users: either activate `Avoid gamma table manipulation` in MonitorControl or turn off `Allow color table adjustments` in BetterDisplay (under Settings/Displays/Overview). You might want to disable native keyboard control either in MonitorControl or BetterDisplay, depending on which app you want to use for brightness control and dimming.

## Contributing to the project

- You can help out [by contributiong to the project with your one-time donation or by being a regular Sponsor](https://opencollective.com/monitorcontrol)!
- If you want, you can fork the code, make improvements and submit a pull request to improve the app. Accepting a PR is solely in the hands of the maintainer - before making fundamental changes expecting it to be accepted, please consult the maintainer of the project!


## How to build

### Required

- Xcode
- [Swiftlint](https://github.com/realm/SwiftLint)
- [SwiftFormat](https://github.com/nicklockwood/SwiftFormat)
- [BartyCrouch](https://github.com/Flinesoft/BartyCrouch) (for updating localizations)

### Build steps

- Clone the project via this Terminal command:

```sh
git clone https://github.com/MonitorControl/MonitorControl.git
```

- If you want to clone one of the branches, add `--single-branch --branch [branchname]` after the `clone` option.
- You're all set! Now open the `MonitorControl.xcodeproj` with Xcode! The dependencies will automatically get downloaded once you open the project. If they don't: `File > Packages > Resolve Package Versions`

### Third party dependencies

- [MediaKeyTap](https://github.com/MonitorControl/MediaKeyTap)
- [Settings](https://github.com/sindresorhus/Settings)
- [SimplyCoreAudio](https://github.com/rnine/SimplyCoreAudio)
- [KeyboardShortcuts](https://github.com/sindresorhus/KeyboardShortcuts)
- [Sparkle](https://github.com/sparkle-project/Sparkle)

## Hall of Honor

### Current maintainer of the project

- [@waydabber](https://github.com/waydabber), developer of [BetterDisplay](https://github.com/waydabber/BetterDisplay#readme).

### Former maintainers, special contributors

- [@the0neyouseek](https://github.com/the0neyouseek) - previous (now honorary) maintainer
- [@JoniVR](https://github.com/JoniVR) - previous (now honorary) maintainer
- [@alin23](https://github.com/alin23) (generally spearheaded M1 DDC support and figured out a many of the caveats)
- [@mathew-kurian](https://github.com/mathew-kurian/) (original developer)
- [@Tyilo](https://github.com/Tyilo/) (fork)
- [@Bensge](https://github.com/Bensge/) - (used some code from his project [NativeDisplayBrightness](https://github.com/Bensge/NativeDisplayBrightness))
- [@nhurden](https://github.com/nhurden/) (for the original MediaKeyTap)
- [@kfix](https://github.com/kfix/ddcctl) (for ddcctl)
- [@reitermarkus](https://github.com/reitermarkus) (for Intel DDC support)
- [javierocasio](https://www.deviantart.com/javierocasio) (app icon background)
