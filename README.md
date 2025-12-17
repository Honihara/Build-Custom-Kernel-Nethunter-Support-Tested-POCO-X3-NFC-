## Build-Custom-Kernel-Nethunter-Support-Tested-POCO-X3-NFC-
This kernel is intended for educational purposes.

Download TERMUX DISINI 

Download Source Kernel Sesuai Versi Android, Disini Saya Pilih Source Kernel Dari Custom Rom Baikal OS Android 13.

1. Buka Aplikasi Termux ,Lalu Install Kali Linux Caranya Bisa Di Lihat DISINI

Lalu Copy Perintah Ini Ke Termux : 
apt install git clang gcc cmake ccache automake flex lzop bison gperf build-essential zip curl zlib1g-dev libxml2-utils bzip2 libbz2-dev libbz2-1.0 libghc-bzlib-dev squashfs-tools pngcrush schedtool dpkg-dev make optipng maven libssl-dev pwgen libswitch-perl policycoreutils minicom libxml-sax-base-perl libxml-simple-perl bc x11proto-core-dev libx11-dev libgl1-mesa-dev xsltproc unzip openssl gcc-aarch64-linux-gnu binutils lld default-jdk gnupg libc6-dev libncurses-dev libreadline-dev libgl1 g++ grep tofrodos python3-markdown libtinfo6 repo cpio kmod libelf-dev pahole clang-format clang-tidy clang-tools libc++-dev libc++1 libc++abi-dev libc++abi1 libclang-dev libclang1 liblldb-dev libllvm-ocaml-dev libomp-dev libomp5 llvm-dev llvm-runtime llvm libncurses5-dev ninja-build imagemagick git-lfs libsdl1.2-dev libxml2 lzop rsync schedtool squashfs-tools adb fastboot -yy

2. Setelah Selesai Kalian Edit File Build.sh Dengan Perintah 

$ nano Build.sh

Yang Di Edit Hanya : 
KBUILD_BUILD_USER="USER TERSERAH KALIAN "

KBUILD_BUILD_HOST="HOST TERSERAH KALIAN "

make O=out ARCH=arm64 Codename_defconfig 

Untuk Codename Samakan Dengan File Source Kernel Yang Berada Di Folder :
Source Kernel/arm/arm64/configs/DISINI

Lalu Ctrl+X+Y+Enter Untuk Menyimpan 


3. Pindahkan File build.sh Ke Source Kernel

Buka Terminal Ketikan : 

$ chmod +x build.sh

$ Bash build.sh

Lalu Perkecil Layar Termux Nya dengan Menyubit Layar Keluar Jika Ada Tampilan Menu Setting Kalian Bisa Samakan Setingan Nya Dengan Ini DISINI



