

## Fork of TA-Lib with ios cmake toolchain support 

Build for ios/sim/macos


    ```
    cmake . 

    cmake -B build-ios -DCMAKE_TOOLCHAIN_FILE=cmake/ios.toolchain.cmake -DPLATFORM=OS64 -DDEPLOYMENT_TARGET=18.0

    cmake -B build-ios-sim -DCMAKE_TOOLCHAIN_FILE=cmake/ios.toolchain.cmake -DPLATFORM=SIMULATORARM64 -DDEPLOYMENT_TARGET=18.0

    cmake -B build-macos -DCMAKE_SYSTEM_NAME=Darwin

    cmake --build build-ios --config Release
    cmake --build build-ios-sim --config Release
    cmake --build build-macos --config Release

    ```

### Apple Accelerate Optimizations

19 element-wise functions (ADD, SUB, MULT, DIV, SQRT, LN, LOG10, EXP, CEIL, FLOOR, SIN, COS, TAN, ASIN, ACOS, ATAN, SINH, COSH, TANH) are vectorized via Apple Accelerate (vDSP/vForce) on macOS and iOS, leveraging NEON SIMD under the hood. Enabled by default through the CMake option `TA_USE_ACCELERATE`; double-precision only (float variants fall back to scalar).

------
[![Discord chat](https://img.shields.io/discord/1038616996062953554.svg?logo=discord&style=flat-square)](https://discord.gg/Erb6SwsVbH)

[![main nightly tests](https://github.com/TA-Lib/ta-lib/actions/workflows/main-nightly-tests.yml/badge.svg)](https://github.com/TA-Lib/ta-lib/actions/workflows/main-nightly-tests.yml) [![dev nightly tests](https://github.com/TA-Lib/ta-lib/actions/workflows/dev-nightly-tests.yml/badge.svg)](https://github.com/TA-Lib/ta-lib/actions/workflows/dev-nightly-tests.yml)

# TA-Lib - Technical Analysis Library
This is now the official home for C/C++ TA-Lib (instead of SourceForge).

More info [https://ta-lib.org](https://ta-lib.org)

# You want a new TA Function implemented?
First step is to document the algorithm, with a sample of input/output in the [ta-lib-proposal-drafts]( https://github.com/TA-Lib/ta-lib-proposal-drafts ) repos.
