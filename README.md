# cef.bin

 CEF Binaries for all available platforms.
 
 ## Goal
 
 Goal of this project is for any CEF wrapper to use these binaries so devleopers that might use those wrappers don't have to download themselves by automating this process. 
 
 Also, these CEF binaries will be coming directly from Soptify's autobuilds so they are mostly untouched by us.
 
 ## Supported Platforms
 
  - Windows
     - x64 (64-bit)
	 - x86 (32-bit)
	 - ARM&4
  - Linux
     - amd64/x86_64/x64 (all are same but some distributions uses a different name than x64)
	 - ARM
	 - ARM64
  - MacOS
     - x64 (intel)
	 - ARM64 (M1 and newer)
	 
 ## Build
 
 Requires Python 3.7 or newer. Also requires these python packages to be installed: `wget`
 
 Just run the python script with CEF version as argument. Also, include `--beta` for beta builds, otherwise it won't download.
 
 NOTE: CEF is **HUGE** (but like ~80MiB for each architecture, totaling ~720MiB huge), so it might take a while depending on your Internet connection.
 
 `python populate.py [CEF Version] [--beta]`
 
 Example: `python populate.py 105.3.18+gbfea4e1+chromium-105.0.5195.52`