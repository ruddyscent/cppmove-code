# Example Codes in 'C++ Move Semantics - The Complete Guide' by Nicolai M. Josuttis

This repository provides a container environment to run the example code from the book [C++ Move Semantics - The Complete Guide]((https://www.cppmove.com/)) by [Nicolai M. Josuttis](https://www.josuttis.com/).

For more details about the book, visit the [official website](https://www.cppmove.com/). You can find purchase options of the book and download the original source code files from the site.

## How to Run the Container with Docker Compose

To run the container environment using Docker Compose, follow these steps:

### Architecture Compatibility
This setup has been tested on macOS with Apple Silicon (ARM architecture). If you are running on an x86_64 system (e.g., Intel-based macOS or Linux), modify the first line of the `Dockerfile` to use the appropriate base image:
```dockerfile
FROM ubuntu:24.04
```

### Build and Run the Docker Container
Use the following command to build the Docker image and start the container in the background (detached mode):
```sh
docker compose up --build -d
```

#### Explanation of the Command:
* `docker compose up`: Starts the containers defined in the `compose.yaml` file.
* `--build`: Rebuilds the Docker image before starting the containers. Use this option if you’ve made changes to the `Dockerfile` or source code.
* `-d`: Runs the container in detached mode, meaning it runs in the background.

After running this command, the container will be built and started, ready to execute the example code.

To stop the container, use:
```sh
docker compose down
```

## How to Build with CMake

This section explains how to build the project using CMake, a cross-platform build system.

### 1. Create a build directory
Create a separate build directory to keep your build files organized:
```sh
mkdir build
cd build
```
This keeps the project directory clean by isolating build artifacts.

### 2. Run CMake to configure the project
Configure the project with the following command:
```sh
cmake ..
```
#### Explanation of the Command:
* `cmake`: The command to run the CMake configuration process.
* `..`: Refers to the parent directory (where the main `CMakeLists.txt` file is located).

### 3. Build the project
Compile the project using this command:
```sh
cmake --build .
```
#### Explanation of the Command:
* `cmake --build`: Tells CMake to build the project.
* `.`: Refers to the current build directory.

After running this command, the binaries will be generated in the build directory.

To clean the build directory, use:
```sh
cmake --build . --target clean
```

## License
The code in this repository is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/deed.en).