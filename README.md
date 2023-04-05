# restinio-vcpkg-helloworld

restinio-vcpkg-helloworld is a simple example of using
[RESTinio](https://github.com/stiffstream/restinio) library via [vcpkg](https://vcpkg.io/).

# How to obtain and build

## Prerequisites

restinio-vcpkg-helloworld requires C++ compiler with C++14 support, vcpkg and CMake.

## Obtaining

Just clone restinio-vcpkg-helloworld from GitHub:

```sh
git clone https://github.com/stiffstream/restinio-vcpkg-helloworld
cd restinio-vcpkg-helloworld
```

## Building

### Obtaining the dependencies

restinio-vcpkg-helloworld uses only one library directly: RESTinio, all RESTinio's dependencies are handled by vcpkg automatically. To obtain RESTinio via vcpkg it's necessary to run the following command:

```sh
vcpkg install restinio
```

### Building

The build of restinio-vcpkg-helloworld is performed via CMake. Please note the usage of vcpkg's toolchain file:

```sh
cd restinio-vcpkg-helloworld
mkdir cmake_build
cd cmake_build
cmake -DCMAKE_TOOLCHAIN_FILE=<path-to-your-vcpkg>/scripts/buildsystems/vcpkg.cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=. ..
cmake --build . --target install
```

The resulting executable file `hello_world` (or `hello_world.exe` on Windows) will be in `bin` subfolder.

