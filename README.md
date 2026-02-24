This is a fork of the Devuan unstable mdadm (4.5) package intended to
build on daedalus and to have all systemd support files removed.


Present State
-------------
Builds and works on my daedalus system. The included patches have been
refreshed and all systemd support has been excised from the generated
package. 


Building
--------
Since I've been a Debian user since 1998, I'm still using the
documented method of that time to build Debian packages, that is, run

`fakeroot debian/rules binary`

from the top-level source directory. This will automatically apply all
patches in `debian/patches` if they weren't already applied. Applied
patches will be removed when making the `debian/rules` `clean`
target. The top-level scripts `build` and `cln` (to avoid name clashes
with `clean` targets in makefiles) can be used to invoke the package
building or directory cleaning commands with less typing.

Separate targets `patch` and `unpatch` exist to just apply or remove
patches without doing anything else.
