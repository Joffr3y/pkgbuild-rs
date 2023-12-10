# Examples for pkgbuild-rs

## download
A fake downloader that pretends to download sources defined in a PKGBUILD, it does not actually download them, but demonstrates how you can implement your download logic natively in Rust.

## dump_all
Parse all PKGBUILDs in arguments and dump the result onto stdout.

## printsrcinfo
Parse a PKGBUILD in argument and print the info almost like how `makepkg --printsrcinfo` does, note that some fields like `desc` are missing by design, as the library currently doesn't dump and parse those fields.

## vercmp
Parse two package versions into native `PlainVersion`s and compare them with the same logic pacman uses internally. The details are printed to stderr, and the stdout behaviour is the same as `vercmp` on Arch.