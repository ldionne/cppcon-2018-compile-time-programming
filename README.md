## Compile-time programming in C++20 and beyond @ CppCon 2018

This repository contains my [reveal.js][]-based presentation on compile-time
programming for [CppCon 2018][].

## Usage
Go to https://ldionne.com/cppcon-2018-compile-time-programming or open
`index.html` with your browser. A PDF version of the slides is in `slides.pdf`.

## Building the code samples
```sh
# Install the dependencies and get back the CMAKE_PREFIX_PATH to use
CMAKE_PREFIX_PATH="$(./code/dependencies/install.sh)"

# Usual CMake build, with a custom CMAKE_PREFIX_PATH for locally-installed dependencies
(mkdir build && cd build && cmake .. -GNinja -DCMAKE_PREFIX_PATH="${CMAKE_PREFIX_PATH}")
cmake --build build
```

## Running a local server
```sh
cd reveal
npm install # you can make sure that Python < 3 is used with `--python=python2.XYZ`
grunt serve --root=..
```

Then visit http://localhost:8000.

<!-- Links -->
[CppCon 2018]: https://cppcon.org
[reveal.js]: https://github.com/hakimel/reveal.js
