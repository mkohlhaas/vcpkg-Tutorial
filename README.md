### vcpkg Installation

```shell
$ sudo pacman -S vcpkg
```

```
The repository containing vcpkg recipes cannot legally be included, so you
will have to manually clone it to the $HOME/.local/share/vcpkg directory.

  git clone https://github.com/microsoft/vcpkg $VCPKG_ROOT

You are also responsible for manually updating this repository.

  git -C $VCPKG_ROOT pull

For CMake to recognize libraries provided by vcpkg, the above repository
includes a CMake module, which can be found at:

  $VCPKG_ROOT/scripts/buildsystems/vcpkg.cmake

This file can be copied to your CMake project directory and included in
CMakeLists.txt via include(vcpkg).

Alternatively, you can pass the following to CMake when configuring:

  -D CMAKE_TOOLCHAIN_FILE=$VCPKG_ROOT/scripts/buildsystems/vcpkg.cmake
```

Check package content with `pacman -Ql vcpkg`.

You can use `update-vcpkg` - defined in `.bashrc` for updating the git repository.

### Links

[Tutorial: Install and use packages with CMake](https://learn.microsoft.com/en-us/vcpkg/get_started/get-started?pivots=shell-bash)
