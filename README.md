## Backends for libGDX, easy to build

Since we have no regular libGDX releases anymore, it is a problem to fix or extend backend behaviour that can't be overriden.
While there's always a way to work around bugs in the core project, this is often not possible in the backends.

This is where this repo comes in.

If you need to change build-in behaviour, but don't manage to get the complete libGDX repo to build, don't want to 
build your very own version or don't want to use snapshot versions, this repo is what you need. Check my own additions to see
what else is changed.


### How to build

* Clone this repo
* Checkout the revision you need (next paragraph)
* Type `gradlew install`
* Change your project's backend dependency to the one you wish

### How to use as a dependency

In case you don't want to change something here yourself, but just want to use some of the additions, you can also use a Jitpack dependency.
Don't forget to add Jitpack as a repo to your project:

    allprojects {
	    repositories {
		    ...
		    maven { url 'https://jitpack.io' }
	    }
    }

## For use with libGDX 1.9.11 core

### 1.911.0

Checkout branch [release/1.911.0](https://github.com/MrStahlfelge/gdx-backends/tree/release/1.911.0) to use this version, or use
the following dependencies for GWT:

      implementation 'com.github.MrStahlfelge.gdx-backends:gdx-backend-gwt:1.911.0'
      implementation 'com.github.MrStahlfelge.gdx-backends:gdx-backend-robovm:1.911.0'

Additions compared to official backends for 1.9.11:
* GWT: Switched to WebAudio, fixes sounds for mobiles too. [Original PR by @barkholt](https://github.com/libgdx/libgdx/pull/4220). See [current PR](https://github.com/libgdx/libgdx/pull/5659) for more information.
* GWT: Faster bootstrap process by lazy loading assets. See [current PR](https://github.com/libgdx/libgdx/pull/5677) for more information.
* GWT: Fixed density problems on mobile with new config setting. See [current PR](https://github.com/libgdx/libgdx/pull/5691)
* GWT: Pulled feature policy implementation by @SimonIT. [Pending PR](https://github.com/libgdx/libgdx/pull/5784)
* iOS: Handles hardware keyboard events like on other platforms [Pending PR](https://github.com/libgdx/libgdx/pull/6132)

## Work still to do

### GWT
- [ ] Move resizable browser window support into the backend, no template hazzle any more
- [ ] Electron extensions

## For use with libGDX 1.9.10 core, or if you are still on 1.9.8 or 1.9.9...

See readme on branch [release/1.910.2](https://github.com/MrStahlfelge/gdx-backends/tree/release/1.910.2)
