# cef.bin

 Chromium Embedded Framework (CEF) Binaries for all available platforms.
 
 ## Goal
 
 Goal of this project is for any CEF wrapper (CefSharp, CefNet, CefGlue, etc.) to use these binaries so devleopers that might use those wrappers don't have to download themselves by automating this process. 
 
 Also, these CEF binaries will be coming directly from Spotify's autobuilds so they are mostly untouched by us.
 
 ## Supported Platforms
 
  - [x] Windows
     - [x] x64 (64-bit)
     - [x] x86 (32-bit)
     - [x] ARM&4
     - [ ] ARM
        - Microsoft is not offering 32-bit ARM support for any Windows versions we know so far.
  - [x] Linux
     - [x] x64 (amd64, x86_64)
     - [ ] x86 (i386)
        - Spotify stopped building for this platform.
     - [x] ARM
     - [x] ARM64
  - [x] MacOS
     - [x] x64 (intel macs)
     - [x] ARM64 (M1 and newer macs)
   - [ ] Other
     - Spotify only builds for the platforms above and we simply don't have enough hardware or understanding on how to build Chromium and CEF for other platforms.
	 
 ## Build
 
 Requires Python 3 or newer (we recommend the latest version). Also requires these python packages to be installed: `wget`
 
 Just run the python script with CEF version as argument. Also, include `--beta` for beta builds, otherwise it won't download.
 
 NOTE: CEF is **HUGE** (not as big as the Chromium repository but some of builds are as big as ~1.6GiB whilst some of them are ~256MiB big), so it might take a while depending on your Internet connection.
 
 `python populate.py [CEF Version] [--beta]`
 
 Example: `python populate.py 105.3.18+gbfea4e1+chromium-105.0.5195.52`
