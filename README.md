
# Install WSL on Windows 10
Use Powershell in Windows
Install ubuntu on wsl on non C drive (F: or E: wherever you have space)

$mkdir WSL

$cd WSL

$Invoke-WebRequest -Uri https://aka.ms/wslubuntu2204 -OutFile Ubuntu.appx -UseBasicParsing

$move .\Ubuntu.appx .\Ubuntu.zip

$Expand-Archive .\Ubuntu.zip

$.\Ubuntu.exe

Give the username and password.

Run below commands to make the build environment ready

$sudo apt-get update -y

$sudo apt-get update -y

$sudo apt-get install gcc -y

$sudo apt-get install build-essential -y




# Download Buildroot
$git clone --depth=1 https://github.com/buildroot/buildroot

$cd buildroot

$make qemu_aarch64_virt_defconfig

Install any dependencies sudo apt install commands if you get any error

This will create default configuration

$make menuconfig

This is used customize the build root configuration.
Select the externl downloaded and installed toolchain in configurtion to save the build time 

$make
