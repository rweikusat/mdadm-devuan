This is a fork of the Devuan unstable mdadm (4.5) package intended to build on daedalus and to have all systemd support files removed.

Present State
-------------
Builds and works on my daedalus system. Some systemd support files won't be
installed anymore but two are still part of the mdadm package.


Building
--------
Since I've been a Debian user since 1998, I'm still using the
documented method of that time to build Debian packages, that is, run

`fakeroot debian/rules binary`

from the top-level source directory. This will automatically apply all
patches in debian/patches if they weren't already applied. Applied
patches will be removed when making the debian/rules `clean` target.

Separate `targets` patch and `unpatch` exist to just apply or remove
patches without doing anything else.
