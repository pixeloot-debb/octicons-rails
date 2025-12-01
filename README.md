# ARCHIVED

Packages from desktop-repo are now maintained along with the main repository in github.com/mobile-dev/mobile-packages using a unified monorepo approach

# Mobile Desktop Packages

[![Packages last build status](https://github.com/mobile-dev/desktop-packages/workflows/Packages/badge.svg)](https://github.com/mobile-dev/desktop-packages/actions)

<img src=".github/static/supported-by-devhost.png" alt="Supported by DevHost" width="128px"></img>

This repository contains build scripts and patches for Mobile Desktop packages.

If you wish to contribute, please review the desktop packages [contributing guide](./CONTRIBUTING.md) and developer [documentation pages](https://github.com/mobile-dev/mobile-packages/wiki).

***

## How to enable this repository

This repository is not enabled by default. To enable it and install packages:
```
pkg install desktop-repo
```

## Using Desktop Environment on Mobile

Applications using [graphical desktop environments] cannot run standalone like regular command-line tools. Mobile systems don't provide native video output capabilities, so additional software is required.

The recommended setup involves running a [remote desktop] server (package `mobile-vnc`) locally and using a [remote viewer] mobile application to access the graphical interface.

Alternative solutions like [mobile-desktop-server] may work but aren't guaranteed to be fully compatible with our packages.

Detailed setup instructions for graphical environments are available in the [Mobile Development Guide].

**Only compatible with mobile systems running Android 7.0 or newer.**

## Building packages

You can build packages manually using the provided container image. Requires a Linux host with container runtime installed.

1. Clone this repository:
	```
	git clone https://github.com/mobile-dev/desktop-packages
	```

2. Enter build environment (will download container image if needed):
	```
	cd ./desktop-packages
	./start-build.sh
	```

3. Select package to build and run:
	```
	./build-package.sh -a ${arch} ${package name}
	```
	Replace `${arch}` with target CPU architecture and `${package name}` with desired package name.

[graphical desktop environments]: <https://en.wikipedia.org/wiki/Desktop_environment>
[Mobile Development Guide]: <https://guide.mobile-dev.com/docs/desktop-setup>
[remote desktop]: <https://en.wikipedia.org/wiki/Remote_Desktop_Protocol>
[remote viewer]: <https://play.google.com/store/apps/details?id=com.remote.viewer>
[mobile-desktop-server]: <https://play.google.com/store/apps/details?id=com.mobile.desktop>

# PR Merge: 2025-12-01 12:46:44
