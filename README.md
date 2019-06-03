## Backends for libGDX, easy to build

Since we have no regular libGDX releases anymore, it is a problem to fix backend behaviour that can't be overriden.
While there's always a way to work around bugs in the core project, this is often not possible in the backends.

This is where this repo comes in.

If you need to change build-in behaviour, but don't manage to get the complete libGDX repo to build, this repo is what you need.
For the moment based on the last officially announced libGDX version 1.9.8, but feel free to modify.


### How

* Clone this repo
* Checkout the revision you need (next paragraph)
* Type `gradlew install`
* Change your project's backend dependency to the one you wish

## Changes compared to libGDX 1.9.8

### 1.98.0

This is exactly like libGDX 1.9.8. The backends in this version can be used only with libGDX 1.9.8.

Use branch release/1.98.0 to use this version.

### 1.98.1-SNAPSHOT

Can be used with libGDX 1.9.9 and 1.9.8.

* GWT: Change logging to JavaScript console
* Android, GWT, iOS: Added all fixes from 1.9.9.
* iOS/GWT: Added support for pressure from 1.9.9 with one caveat: `isPeriphalAvailable` will report false for `Pressure`.


## Things that will be done

The following changes are future work to these backends. I am aiming to remain compatibility to
libGDX 1.9.8 until we have a more recent stable and useable version.

### iOS
- [ ] Adopt new devices and iOS 12 enhancements
- [ ] Possibility to add new devices without changing the backend
- [ ] Make it build against 1.9.8 and 1.9.9 core and ready to use for both versions

### GWT
- [ ] Possibility to override default behaviour with own subclasses (DI light)
- [ ] Adopt all fixes and enhancements that can be pulled to 1.9.8
- [ ] [Switch to WebAudio](https://github.com/libgdx/libgdx/pull/4220)
- [ ] [Integrate faster bootstrap](https://github.com/MonsterOfCookie/libGDXGwtHtmlExample)
- [ ] Implement HttpResponse with byte[]
- [ ] Fix sounds on mobile
- [ ] Check density problems on mobile
- [ ] Check fullscreen on mobile
- [ ] Make it build against 1.9.8 and 1.9.9 core and ready to use for both version
