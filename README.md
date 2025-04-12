# gnome-screenshot-no-flash-nixpkg-patch

The minimal no flash patch for the [gnome-screenshot](https://gitlab.gnome.org/GNOME/gnome-screenshot) on nixpkgs.  
It’s commonly used for Wayland screenshots, including [ponty/pyscreenshot](https://github.com/ponty/pyscreenshot).

nixos usage:
```
(gnome-screenshot.overrideAttrs
{patches = [(fetchpatch {
# other patches*
(fetchpatch {
url = "https://raw.githubusercontent.com/kjirc/gnome-screenshot-no-flash-nixpkg-patch/refs/heads/main/no_flash.patch";
hash = "sha256-5SJWqWsmRZcaaIr7N8x3M6JlWGvAhZSVpyF+uwSTopA="; }) ];
})
```

other patches* [gnome-screenshot/package.nix](https://github.com/NixOS/nixpkgs/blob/nixos-unstable/pkgs/by-name/gn/gnome-screenshot/package.nix)
