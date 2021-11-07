# Welcome!

There are some general rules to keep the code nice and tidy:
- [Naming Convention](#naming-convention)
- [Comments](#comments)
  - [File Header](#file-header)
  - [Function Header](#function-header)
- [Commits](#commits)
- [Release Management](#release-management)
- [License](#license)

# Naming Convention
The main language in this repo is `c++`. We use features from `c++17`.
Some remarks in the naming convention when programming the firmware:
- Use **namespaces** to group related code.
- Follow the core guidelines published by [ISOCPP](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md)

# Comments
We use the *doxygen* documentation flags in the headers, to make them more readable. Although we do not export the documentation as *html*, the flags
are useful, because *VSCode* recognizes them, and renders them when hovering over the function name.

In general try to code like the person who is reading your code knows where you live. :wink:

## File Header
The file header gives a short description of what the file does. Also the [license](#license) information is added here.

Example:
```c
/**
 ==============================================================================
 * @file    filename.c
 * @author  name
 * @version Vx.x
 * @date    dd-Month-yyyy
 * @brief   Description
 ==============================================================================
 */
 ```
## Function Header
A function header gives a short **description**, defines the **inputs** and the **return value**. Addtitional **details** are optional:

```c
/**
 * @brief Descritpion
 * @param input1 Description of input, if any.
 * @param input2 Description of input, if any.
 * @return Description of th return value, if any.
 */
 ```
 Possible `@details` are:
 - *interrupt handler*
 - *inline function*
 
 You can also use additional comments:
 - `@todo`: Note what has to be done
 - `@deprecated`: Why this function is no longer used.
 
# Commits
- Commit messages should be clear and concise 
- Use **English** as far as possible.
- Use the # to close issues. 
- *Present* tense is **not** required. 

Symbols for commits:
- :art: `:art:` Improvements in the *User Experience*
- :bug: `:bug:` Bugfix
- :racehorse: `:racehorse:` Performance Improvement
- :wrench: `:wrench:`Minor Improvement or Fix
- :mag: `:mag:` Made Code More Readable
- :8ball: `:8ball:` Changes in Unit Tests
- :memo: `:memo:` Improved Documentation
- :nut_and_bolt: `:nut_and_bolt:` Hardware Uploads and Fixes

# Release Management
*Tags* are used for the release management. The tag number is:
- **v***Major.Minor.Bugfix*

A **bugfix** fixes one problem in the firmware **without** introducing new functionality. A **minor** release
introduces **new** functionality. A **major** release bundles minor releases. Document minor and major release in the [Changelog](Changelog.md). Bugfixes are included by their issue id if there are any.

> A release with release notes is only published on **major** changes. Every **minor** change is included in the
changelog. Bugfixes are just pushed as tags.

# License

The following should be included in every file header:
> Adjust the name of the author according to who created the file.
```c
/**
 * OTP-15 joVario 2.0 Firmware
 * Copyright (c) 2021 Sebastian Oberschwendtner, sebastian.oberschwendtner@gmail.com
 * Copyright (c) 2021 Jakob Karpfinger, kajacky@gmail.com
 *
 *
 * This program is free software: you can redistribute it and/or modify
 * it under the terms of the GNU General Public License as published by
 * the Free Software Foundation, either version 3 of the License, or
 * (at your option) any later version.
 *
 * This program is distributed in the hope that it will be useful,
 * but WITHOUT ANY WARRANTY; without even the implied warranty of
 * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 * GNU General Public License for more details.
 *
 * You should have received a copy of the GNU General Public License
 * along with this program.  If not, see <https://www.gnu.org/licenses/>.
 *
 */
 ```
