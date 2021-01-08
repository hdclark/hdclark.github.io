## `DICOMautomaton` Builds

### Latest Continuous Integration Build

The most recent CI build artifact is available here: **[DICOMautomaton-x86_64.AppImage](DICOMautomaton-x86_64.AppImage)**.

This artifact corresponds to the latest successful build on <https://travis-ci.com/github/hdclark/DICOMautomaton/builds>.

Notes and caveats:

- This is not an official release. It may be lacking functionality, and is almost certainly not optimized.
  See <https://gitlab.com/hdeanclark/DICOMautomaton/> or <https://github.com/hdclark/DICOMautomaton> for sources and build scripts.

- The CI build environment is currently based on Debian stable. Attempting to run on systems with older `glibc`s will likely fail.

- `AppImage`s require `FUSE` support, so running in Docker will not work. However, `AppImages` can be extracted and run without requiring `FUSE`:

    $>  ./DICOMautomaton-x86_64.AppImage --appimage-extract
    
    $>  ./squashfs-root/usr/bin/dicomautomaton_dispatcher -h
    
- The `AppImage` currently expects graphical components to be available. It will fail if `libGL` or `X` are incompatible or missing.
