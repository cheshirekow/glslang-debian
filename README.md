# Debian Packaging for glslang

This repository contains debian packaging metadata for the [glslang][1]
reference frontend by Kronos. The upstream source tarballs are downloaded
directly from [github][2] and debian source packages are targeted for
[launchpad][3] as a PPA.

This repository includes my maintainer script which does the following:

1. Downloads the source tarball
2. Extracts the source tarball into a working area
3. Copies the debian directory into the extracted source
4. Symlinks the distro-specific changelog to `debian/changelog`
5. Creates a signed source package with `debuild`
6. Creates a binary package with `pbuilder`

By default it does this for the last three LTS releases: `trusty`, `xenial`,
and `bionic`.

The binary packages aren't used anywhere. They are built as a sanity check
prior to uploading to launchpad.

[1]: https://www.khronos.org/opengles/sdk/tools/Reference-Compiler/
[2]: https://github.com/KhronosGroup/glslang/releases
[3]: https://launchpad.net/~josh-bialkowski/+archive/ubuntu/glslang