## Run on old hardware!  The decision was made in mid 2014 to
remove native support for the ability to disable runtime options
that REQUIRE the SSE2 instruction set.  Users of older hardware,
like AMD Athlon XPs for example, need this feature.

A patch for v35/v36 will revert issue
[#187423002](https://codereview.chromium.org/187423002) and allow
you to compile with the -Ddisable_sse2=1 switch again.

## Arch linux package for v36
[Here](https://aur.archlinux.org/packages/chromium-no-sse2) is an
Arch PKGBUILD that mirrors that of the official [extra]/chromium I
maintain that has this patch enabled.

For v38 code for support non-sse2 x86 machines was removed and more
intrusive patches are required. Also build on x86 was broken
completely due to SSE4.1 intrinsics which can't be compiled on x86
at all, so a separate patch removes SSE4\* instructions on x86.

ATM SSE4 patch is working and SSE2 one is in the process (it should
be applied on top of SSE2 one).
