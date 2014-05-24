## Run on old hardware!
The decision made in mid 2014 to remove native support for the ability to disable runtime options that REQUIRE the SSE2 instruction set.  Users of older hardware, like AMD Athlon XPs for example, need this feature.

This patch will revert issue [#187423002](https://codereview.chromium.org/187423002) and allow you to compile with the -Ddisable_sse2=1 switch again.

## Arch linux package
[Here](https://aur.archlinux.org/packages/chromium-no-sse2) is an Arch PKGBUILD that mirrors that of the official [extra]/chromium I maintain that has this patch enabled.

Thanks and enjoy.

## Contact me
Please [open an issue against this project](https://github.com/graysky2/chromium-no-sse2-patch/issues/new) if you're aware of an upstream change.
