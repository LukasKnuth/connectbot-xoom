## connectbot-xoom

This is a fork of the original [connectbot project](http://code.google.com/p/connectbot/), which adds features and workarounds for better handling of the connectbot ssh client with the [Motorola Xoom External Keyboard](http://www.amazon.de/Motorola-Wireless-Tastatur-Xoom-Atrix/dp/B004VQPDOM/)

The development is based on the "tablet"-branch of the original project, although the "tablet"-branch has been made this projects new "master"-branch (so, there is no mobile version of this).

### Changes

The following changes have been made to the client:

* The "<,>,|" key in the lower right corner works now (to be used as on a normal keyboard)
* Pressing ALT+0 now sends the desired "}" instead of the wrong mapped ")"
* The interrupt-signal is now send when using CTRL+C (like in a Unix Terminal)
* The DEL-Key works now
* The END-Key works. Also, since there is no POS1-key on the keyboard, pressing SHIFT+END will set the cursor to the beginning of the current line
* The standard "Dead Key" behaviour of the CTRL and ALT keys has been removed (not needed, only made things worse)
* The "upper number row" now sends the signs printed on the actual keyboard, not `<Fx>`.

All these changes have been **made and tested with the german keyboard layout only!**. They *might* also work for the US version, although I didn't (and will not) test it!

## Compiling

To compile ConnectBot using Ant, you must specify where your Android SDK is via the local.properties file. Insert a line similar to the following with the full path to your SDK:

sdk.dir=/usr/local/android


## ProGuard Support

Download the ProGuard distribution from its website at http://proguard.sourceforge.net/ and place the proguard.jar into the "tools" subdirectory in the ConnectBot root directory.

When running ant to build ConnectBot and engage ProGuard, use:

ant proguard release
