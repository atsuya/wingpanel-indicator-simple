# simple-wingpanel-indicator

This is a simple implementation of Elementary OS Wingpanel indicator.

The code is taken from [Wingpanel repository](https://github.com/elementary/wingpanel/tree/master/sample), and a build file has been added so that the code in this repository can independently be compiled and installed.

# Building and Installation

You'll need the following dependencies:

* libwingpanel-2.0-dev
* meson
* valac

Run `meson` to configure the build environment and then `ninja` to build

    meson build --prefix=/usr
    cd build
    ninja

To install, use `ninja install`

    sudo ninja install
