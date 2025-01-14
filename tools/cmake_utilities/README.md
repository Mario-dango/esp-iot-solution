# Cmake utilities

[![Component Registry](https://components.espressif.com/components/espressif/cmake_utilities/badge.svg)](https://components.espressif.com/components/espressif/cmake_utilities)

This component is aiming to provide some useful CMake utilities outside of ESP-IDF.

## Use

1. Add dependency of this component in your component or project's idf_component.yml.

    ```yml
    dependencies:
      espressif/cmake_utilities: "0.*"
    ```

2. Include the CMake file you needed in your component's CMakeLists.txt after idf_component_register, or your project's CMakeLists.txt

    ```cmake
    // Note: should remove .cmake postfix when using include(), otherwise the requested file will not found
    // Note: should place this line after `idf_component_register` function
    // Include the top CMake file which will include other CMake files
    include(cmake_utilities)

    // Or, only include the one you needed.
    include(package_manager)
    ```

3. Then you can use the corresponding CMake function which is provided by the CMake file.

## Supported features

1. [relinker](https://github.com/espressif/esp-iot-solution/blob/master/tools/cmake_utilities/docs/relinker.md)
2. [gen_compressed_ota](https://github.com/espressif/esp-iot-solution/blob/master/tools/cmake_utilities/docs/gen_compressed_ota.md)
3. [Link Time Optimization](https://github.com/espressif/esp-iot-solution/blob/master/tools/cmake_utilities/docs/gcc_lto.md)
