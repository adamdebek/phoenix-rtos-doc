# Building script

To build Phoenix-RTOS system image build.sh script is used. The simplest way to build the image is the following command.
```bash
TARGET=ia32-generic phoenix-rtos-build/build.sh all
```

As you can see there can be other arguments like `all`

You can also use the `clean` argument to clean last build artifacts.
```bash
TARGET=ia32-generic phoenix-rtos-build/build.sh clean all
```
When you want to compile only the new changes and save time you don't have to use it.

The `all` argument specifies that all system components for a given target should be compiled.
For example, in ia32-generic target `all` means `core fs image project test ports`
You can also choose what components do you want to build, for example the following command will build system image without test and ports components.
```bash
TARGET=ia32-generic phoenix-rtos-build/build.sh core fs image project
```

For ia32-generic target running system in a separate window isn't the only option. There is the possibility to run it in a terminal, in that case, you have to set a few other variables.

```bash
TARGET=ia32-generic CONSOLE=serial SYSPAGE='psh pc-ata uart16550' ./phoenix-rtos-build/build.sh all
```

After the build completes, the disk image and all files needed to run it will be created and placed in the _boot directory.

## See also

1. [Phoenix-RTOS toolchain](toolchain.md)
2. [Phoenix-RTOS reference project repository](project.md)
3. [Table of Contents](../README.md)