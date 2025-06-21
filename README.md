# Disable Firefox Telemetry Programatically

Firefox checks for a file called policies.json every time it starts. If it finds one, it applies the instructions before any profile is opened. That way, nothing ever leaks. 

### Usage
The file must sit in a folder named `distribution` that lives beside the executable on Windows, inside Firefox.app/Contents/Resources on macOS, or in firefox/distribution (or /etc/firefox/policies for a system-wide install) on Linux.

### Installation
1. Locate the active profile local directory from `about:profiles`
2. Clone this repository into the distribution subfolder of your local profile directory
   ```
   mkdir -p <local-profile-directory>/distribution
   git clone git@github.com:DeadBranches/no-telemetry-policies.git <local-profile-directory>/distribution
   ```
