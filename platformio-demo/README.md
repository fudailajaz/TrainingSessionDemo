# PlatformIO Demo

Contents:

- [PlatformIO Demo](#platformio-demo)
  - [What is PlatformIO](#what-is-platformio)
  - [How to use PlatformIO](#how-to-use-platformio)
    - [`platformio.ini` - Project Configuration File](#platformioini---project-configuration-file)

## What is PlatformIO

On the Avionics team for Project Sunride, one of our tasks is the programming of the flight computer of the rocket. In the past, the Arduino IDE was used.

PlatformIO is a much better way of programming microcontrollers than the Arduino IDE. It is described as a “professional collaborative platform for embedded development”. It has many features that we can use to improve the quality of the code we write, and to work together as a team. 

## How to use PlatformIO

First, make sure that [VS Code](https://code.visualstudio.com/download) is installed with the [PlatformIO extension](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide) 

You can install the PlatformIO extension for VS code by searching for it in the "Extensions" tab on the left

![](images\install_pio_extension.png)

After installing PlatformIO to VS Code, you can create a new project by navigating to the PlatformIO tab on the left.

You can then open PIO Home (or it will open automatically)

To create a new project, click `new project`, then use the wizard to specify the name, board, framework and location for your project.

![](images\create_project.png)

VS Code will then open this project for you, or you can open it manually like any other project.

### `platformio.ini` - Project Configuration File

Based on the settings above, a configuration file would be generated that looks like this:

```ini
; Please visit documentation for options and examples
; https://docs.platformio.org/page/projectconf.html

[env:nanoatmega328]
platform = atmelavr
board = nanoatmega328
framework = arduino
```

The configuration file is split into sections, denoted by a `[header]`. Each section contains key/value pairs. Comments can be written in the file by using the `;` character.

Each project can have different _configuration environments_. These are declared using `[env:<name>]` sections. In the example above, one environment is defined, and it is called `nanoatmega328`. The environment definition contains 3 key-value pairs, which define the `platform`, `board`, and `framework` that the environment shall use. The project setup wizard chose these values for me when I selected the Arduino Nano board, but if you want to use another board you can do so by referring to the [PlatformIO boards documentation](https://docs.platformio.org/en/latest//boards/index.html).


