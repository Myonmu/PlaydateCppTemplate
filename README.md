# PlaydateCppTemplate

This is a template for setting up playdate cpp + playdate cpp extensions using CLion running on Windows.

The `.idea` folder is not omitted because it contains CMake configuration so that you don't need to set it up yourself.

The submodules contain small modifications over the original playdate cpp and playdate cpp extensions repositories. *For now, there is only one change*

## Prerequisites

- Install playdate sdk and **add it to environment variables**, which is  `PLAYDATE_SDK_PATH`
- Follow [5.2. Install Development Tools](https://sdk.play.date/2.4.2/Inside%20Playdate%20with%20C.html#_install_development_tools) to set up arm dev tools

## Anything else except cloning this repo?

Change your project name in `CMakeLists.txt` 