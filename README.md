# Quick Assistent

Quick Assistent is a small Windows desktop assistant with web search, voice input,
application launching, and local replies to common greetings and small-talk messages.

## Build

Run `build_exe.bat` on Windows. It creates `dist\Quick Assistent.exe`.

## Publish an update

1. Set the new release number in `version.txt` (for example, `1.0.1`).
2. Commit and push that change to `main`.
3. Create and push a matching version tag (for example, `v1.0.1`).

GitHub Actions builds the EXE and attaches it to a GitHub Release. Installed EXEs
check the latest release at startup. When a newer version is published, users must
download and install it before the assistant opens. The updater downloads the
release asset, verifies its size and available SHA-256 digest, replaces the running
EXE after it exits, and starts the updated version.
