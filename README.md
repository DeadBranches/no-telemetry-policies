# Disable Firefox Telemetry Programatically

Firefox checks for a file called `policies.json` every time it starts. If present, firefox applies the instructions within  before any profile settings.

### Usage
The file `policies.json` be located in a subdirectory named `distribution` relative to the Firefox root user profile directory on Windows. On macOS, `policies.json` must be located inside `Firefox.app/Contents/Resources/distribution` on macOS, or for Linux in either `firefox/distribution` or system wide `/etc/firefox/policies`.

### Installation on Windows
1. Locate the active profile root directory from `about:profiles`
2. Clone this repository into the distribution subfolder of your root profile directory
   ```
   mkdir -p <root-profile-directory>/distribution
   git clone git@github.com:DeadBranches/no-telemetry-policies.git <root-profile-directory>/distribution
   ```
