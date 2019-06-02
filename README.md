## Backends for libGDX, easy to build

Since we have no regular libGDX releases anymore, it is a problem to fix backend behaviour that can't be overriden.
While there's always a way to work around bugs in the core project, this is often not possible in the backends.

This is where this repo comes in.

If you need to change build-in behaviour, but don't manage to get the complete libGDX repo to build, this repo is what you need.
For the moment based on the last officially announced libGDX version 1.9.8, but feel free to modify.


### How

* Clone this repo
* Type `gradlew install`
* Change your project's backend dependency to the one you wish


## Things that will be done

The following changes are future work to these backends. I am aiming to remain compatibility to
libGDX 1.9.8 until we have a more recent stable and useable version.

### All
- [ ] Possibility to override default behaviour with own subclasses (DI light)

### iOS
- [ ] Adopt new devices and iOS 12 enhancements

### GWT
- [ ] Adopt all fixes and enhancements that can be pulled to 1.9.8
- [ ] Change logging to JavaScript console
- [ ] [Switch to WebAudio](https://github.com/libgdx/libgdx/pull/4220)
- [ ] [Integrate faster bootstrap](https://github.com/MonsterOfCookie/libGDXGwtHtmlExample)
- [ ] Implement HttpResponse with byte[]