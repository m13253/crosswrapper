# CrossWrapper

Wrap calls to your cross compiler toolchain

## Why CrossWrapper?

Some Makefiles have hard-coded `gcc` in its configuration, which is unsuitable if you need to do cross compile.

CrossWrapper can redirect calls to `gcc` to `${HOST}-gcc` so that the cross compiler works even with hard-coded Makefiles.

## Usage

CrossWrapper works on Linux. Make sure that GNU coreutils are installed on your system.

Then type `./activate`, followed by your "host" tuple.

It will scan your current `$PATH` to create wrapper commands. It may take some seconds if you have a lot of commands installed.

It will start a new shell (by default, bash). When you type something like `gcc` in the new shell, `${HOST}-gcc` will be actually invoked. 

When you finished, type `exit`.

## Support for BSD/OS X?

I am not sure how to do that. If you managed to get it work, please contribute to this project by sending a pull request at GitHub.

Use it as your own risk if you want to use CrossWrapper on any other platform than Linux with GCC toolchain and GNU coreutils.

## License

This program is licensed under MIT license. Refer to the file `COPYING` for more details.
