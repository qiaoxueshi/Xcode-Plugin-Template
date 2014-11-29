# Xcode Plugin Template

Basic template for creating a plugin for Xcode 6+.

## Installation

1. Install using [Alcatraz](alcatraz.io)
2. Install manually
  * Copy to `~/Library/Developer/Xcode/Templates/Project Templates/Application Plug-in/`.   (Create `Templates/Project Templates/Application Plug-in` the subdirectories if they do not already exist.)
  * Restart Xcode
  * When creating a new Xcode plugin, create a new project and select Xcode Plugin from `OS X` > `Application Plug-in`.

## Usage

The default plugin file links against `AppKit` and `Foundation`, and, when built (and Xcode is restarted), creates a menu item labeled "Do Action" in the File menu. Pressing the menu item should open an alert. Customize at will!

**Note:** Compiling the template with Swift requires Xcode 6.1 or greater.


## Notes

- Add the build UUIDs for the versions of Xcode you wish to support to `DVTPlugInCompatibilityUUIDs` in `Info.plist`. This can be found by running:

  <pre>defaults read /Applications/Xcode.app/Contents/Info DVTPlugInCompatibilityUUID</pre>
