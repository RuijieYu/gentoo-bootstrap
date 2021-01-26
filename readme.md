# Gentoo Bootstrap

Currently the scripts assume that they reside on `/mnt/gentoo` from the outside, which is also the
path to `chroot` into.

# Bootstrapping from non-Gentoo Linux machines

Only Gentoo (and *possibly* its derivatives) ships the `mirrorselect` tool required for
bootstrapping. If Gentoo is used to bootstrap and `mirrorselect` is not yet installed, run the
following command as root (using `su`, `sudo` or the like) to install it, and then follow the
[handbook](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Base).

```bash
emerge --one-shot --ask app-portage/mirrorselect
```

If the bootstrapping machine is other Linux, simply `chroot` into the `/mnt/gentoo` directory, and
then run `emerge-webrsync` or `emerge --sync` as root before installing the package.

