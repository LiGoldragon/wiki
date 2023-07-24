## NixOS on WSL
Step 1: Install WSL 2
Per Microsoft’s documentation:

- Open PowerShell as an admin by right-clicking on it and selecting “Run as administrator.”

- Run `wsl --install`

Step 2: Install NixOS
Per NixOS-WSL’s documentation:

- Download the installer listed in NixOS-WSL’s 22.05 release.

- Move the file where you want your NixOS installation to live. I put it in `C:\Users\<my username>\AppData\Local\NixOS`, which I think follows Windows’s conventions.

- Open PowerShell as a normal user, change to the directory you just made, and run `wsl --import NixOS . nixos-wsl-installer.tar.gz --version 2`

Run wsl -d NixOS to start NixOS. It’ll run through initial setup, then hang on “Starting systemd…” Press Ctrl + C to get back to PowerShell, and then run `wsl --shutdown` followed by `wsl -d NixOS` to get back into NixOS.

[source](https://forrestjacobs.com/nixos-on-wsl/)
