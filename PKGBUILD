# Maintainer: Mario Lopez <mario@techmunchies.net>
pkgbase=mariolopjr
pkgname=(mariolopjr-base mariolopjr-desktop mariolopjr-neovim mariolopjr-gaming)
pkgver=1
pkgrel=1
pkgdesc="System config for Mario's systems"
arch=(any)
url="https://github.com/mariolopjr/arch-pkgs"
license=(MIT)
groups=(mariolopjr)

rootdir=$PWD

package_mariolopjr-base() {
    # Base packages
    depends=(base linux-firmware btrfs-progs grub grub-btrfs rsync
	    efibootmgr snapper reflector base-devel snap-pac zram-generator)

    # Extra general packages
    depends+=(
        zsh starship ripgrep exa fd wget fzf unzip zip dialog pacman-contrib bat ncdu
        pv zsh-completions watchexec tmux
    )

    # Debugging tools
    depends+=(
        lsof bind-tools mtr socat htop iotop openbsd-netcat strace tcpdump whois
        iftop dstat
    )

    # Filesystems
    depends+=(e2fsprogs exfat-utils dosfstools f2fs-tools)

    # Networking
    depends+=()

    # General tools
    depends+=(git jq ddrescue)

    # Docker
    depends+=(docker docker-compose dnsmasq)

    # Virtualization
    depends+=(qemu qemu-arch-extra virt-manager vagrant)

    # Automation tools
    depends+=()

    # Languages
    depends+=(rustup clang go)

    # Python tools
    depends+=(python-black python-pycodestyle python-pylint flake8 python-pip)

    # Node tools
    depends+=(nodejs prettier)

    # Text
    depends+=(vale)
}

package_mariolopjr-neovim() {
    provides=(vim vi)
    conflicts=(vim vi)
    replaces=(vim vi)

    depends=(mdaffin-base neovim python-msgpack python-pynvim)
    depends+=(
        bash-language-server
        dockerfile-language-server-bin
        gopls
        nodejs-svelte-language-server
        python-language-server
        rust-analyzer
        typescript-language-server-bin
        vim-language-server
        vscode-css-languageserver-bin
        vscode-html-languageserver-bin
        vscode-json-languageserver-bin
        yaml-language-server
    )
}

package_mariolopjr-desktop() {
    depends=(mariolopjr-base)

    # DE
    depends=(plasma-meta breeze breeze-grub kcmutils konsole
	    kdeplasma-addons quota-tools sddm rng-tools archlinux-themes-sddm)

    # Applications
    depends+=(
        firefox discord ktorrent guitarix
    )

    # Utility
    depends+=(
        redshift python-gobject pipewire scrot arandr x264
    )

    # Fonts
    depends+=(
        noto-fonts noto-fonts-cjk noto-fonts-emoji noto-fonts-extra
    )

    optdepends=(krita okular netdata mupdf-gl)
}

package_mariolopjr-gaming() {
    depends=(
        mariolopjr-desktop steam mgba-qt ppsspp pcsx2
    )
}
