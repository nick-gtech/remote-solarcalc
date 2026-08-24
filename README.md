# Remote SolarCalc - Distribution Site

This repository hosts the public download page for **Remote SolarCalc**, an
Android application that sizes off-grid solar power systems for telecom towers
and other remote network equipment.

The page is served by GitHub Pages from the `main` branch at the repository
root. Visitors land on `index.html`, which describes the application, lists the
current version, and links to the signed release build.

## Contents
- `index.html` - the public download and installation page
- `app-release.apk` - the current signed release build (version 1.0, build 1)
- `.nojekyll` - serves the files exactly as committed

## Publishing a new release
1. Increment `versionCode` and `versionName` in the application project.
2. Build a signed release APK and verify it installs on a physical device.
3. Replace `app-release.apk` in this repository with the new build.
4. Update the version, size, date, release notes, and SHA-256 checksum in
   `index.html`.
5. Commit and push to `main`. GitHub Pages republishes the page automatically,
   usually within a minute.

The application source code is maintained in a separate GitLab repository. The
signing keystore is never stored in either repository.
