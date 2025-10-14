# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

Precision-Kernel-Dynamics is a high-performance C++ engine designed for real-time filtering and smoothing of noisy coordinate tracking data (x,y,z). The project focuses on providing precision kernel dynamics for processing spatial data with minimal latency and maximum accuracy.

## Development Commands

Since this is a C++ project, common development workflows will likely include:

### Building
```bash
# Once build system is set up, typical commands:
make          # Build the project
make clean    # Clean build artifacts
make install  # Install the built artifacts
```

Or if using CMake:
```bash
mkdir build && cd build
cmake ..
make
```

### Testing
```bash
# Run tests (once test framework is integrated)
make test
# Or for specific test executables:
./build/test_runner
```

### Development Tools
```bash
# Static analysis and formatting
clang-format -i src/**/*.cpp src/**/*.h  # Format code
clang-tidy src/**/*.cpp                  # Static analysis
valgrind ./your_executable               # Memory leak detection
gdb ./your_executable                    # Debugging
```

## Architecture Notes

This project is designed as a high-performance data processing engine with focus on:

- **Real-time Processing**: Low-latency filtering and smoothing algorithms
- **Coordinate Data**: Specialized handling of (x,y,z) coordinate streams
- **Noise Reduction**: Advanced filtering techniques for noisy input data
- **Performance**: C++ implementation optimized for speed and efficiency

## Project Structure Expectations

Based on the C++ nature of the project, the codebase will likely develop into:

- `src/` - Source code files (.cpp, .h)
- `include/` - Header files for public API
- `tests/` - Unit and integration tests
- `examples/` - Usage examples and demos
- `docs/` - Technical documentation
- Build configuration files (Makefile, CMakeLists.txt, or similar)

## Key Considerations

- This project handles real-time data processing, so performance optimization is critical
- Memory management and avoiding memory leaks will be essential
- Consider SIMD optimizations for mathematical operations on coordinate data
- Thread safety may be important for real-time applications
- Precision and numerical stability are key for coordinate filtering algorithms

## License

The project is licensed under the Apache License 2.0.