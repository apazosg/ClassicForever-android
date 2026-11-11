# Versions and release notes

ClassicForever Android's own version numbering starts at **0.0.1**, independently of the versions of the projects it is based on.

## Version numbering

- **0.0.2, 0.0.3…:** bug fixes and minor adjustments.
- **0.1.0, 0.2.0…:** new features or significant improvements.
- **1.0.0:** the first version we decide to consider stable.

Each release uses the following names, substituting the appropriate version:

- App version: `0.0.1`.
- Tag: `v0.0.1`.
- Title: `ClassicForever Android 0.0.1`.
- File: `ClassicForever-Android-0.0.1.apk`.

Releases are published as regular GitHub releases. A version starting with `0` does not need to be marked as a *prerelease*: experimental limitations are explained in its notes. The app's update notifications check the latest published release, excluding those marked as *prerelease*.

## Language and release notes

All public repository documentation, the repository description, and release notes must be written in **English**. This rule applies to every future release as well.

Release notes describe functional changes in language app users can understand. They do not include commit lists or internal programming details. Omit empty sections and describe only verified features or results.

The first release presents the available features rather than comparing them with a previous release that does not exist. Subsequent releases explain changes relative to the previous public version.

The app displays the same release notes published on GitHub; no separate changelog is maintained.

```markdown
A brief summary of the highlights of this version.

## What's new
- You can now…

## Improvements
- It is now easier to…

## Fixes
- Fixed an issue that prevented…

## Known limitations
- Important issues that remain unresolved.

## Installation
Download and install the attached APK.
[Special instructions, only when needed.]
```

## Publishing a release

1. Set the visible version and increase Android's internal version code, keeping the app's package name and signing identity unchanged.
2. Prepare user-facing release notes in English using the format above.
3. Build and verify the signed APK.
4. Publish the tag, release notes, and APK in this repository.
5. Verify update detection from an older version and that the same release notes can be read within the app.

The initial installation of `0.0.1` over older builds is manual because those builds check the previous repository. Starting with `0.0.1`, the app checks releases in this repository.
