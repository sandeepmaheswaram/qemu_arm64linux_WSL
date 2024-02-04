
# Install WSL on Windows 10
Install ubuntu on wsl


# Download Buildroot
git clone --depth=1 https://github.com/buildroot/buildroot

cd buildroot

make qemu_aarch64_virt_defconfig

This will create default configuration

make menuconfig

This is used customize the build root configuration.
Select the externl downloaded and installed toolchain in configurtion to save the build time 

make
