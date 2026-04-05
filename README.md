# Blink Shell (Fork)

Personal fork of [Blink Shell](https://github.com/blinksh/blink) for iOS — a professional, desktop-grade terminal leveraging Mosh and SSH.

Upstream: [blinksh/blink](https://github.com/blinksh/blink) | Fork: [tankbottoms/blink](https://github.com/tankbottoms/blink)

## Fork Changes

- Custom app icon (cat)
- Developer build crash fix (guarded RevenueCat init for empty API key)
- Tracks the `raw` branch from upstream

## Build

Requires Xcode with `xcode-select -p` pointing to `/Applications/Xcode.app/Contents/Developer`.

```bash
git clone --recursive https://github.com/tankbottoms/blink.git && \
    cd blink && ./get_frameworks.sh && ./get_resources.sh && \
    rm -rf Blink.xcodeproj/project.xcworkspace/xcshareddata/
```

```bash
cp template_setup.xcconfig developer_setup.xcconfig
# Edit developer_setup.xcconfig with your Apple developer ID
```

Open in Xcode, select your device, build and run.

To build without iCloud/Push Notifications/Keychain Sharing, disable those capabilities in the project settings before building.

See [BUILD.md](BUILD.md) for compiling all dependencies from source.

## Upstream

For full documentation, usage instructions, and the original changelog, see the [upstream repository](https://github.com/blinksh/blink).

## License

See [COPYING](COPYING) for license details. Original project by [Blink Shell](https://blink.sh).
