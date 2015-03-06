# OpenRW

A project to re-implement gta3.exe, adding support for more platforms and fixing all of the bugs that have piled up.

**REQURIES A LEGITAMATE COPY OF GTA III PC TO RUN**, this project only functions with the original game's data.

## Building

Dependencies:

* Bullet
* GLM (0.9.5+)
* SFML (2.0+)
* Boost Test

Options:

* BUILD\_OLD\_TOOLS – Builds old, unmaintained tools (datadump & analyzer)

## Running

### rwgame

Implementation of the game itself.

* Options:
    * env: OPENRW\_GAME\_PATH, must be set to the folder containing "gta3.exe"
    * -w **n**, -h **n** sets initial window size

### rwviewer

File viewer for game data, open the folder containing "gta3.exe" and it will load the data.

Currently only supports viewing instance data, pending some rewriting.

## Documentation

Run Doxygen on the included Doxyfile to generate documentation.

## Things to do

* Make it work on Windows (shouldn't be too difficult for anyone with CMake and C++ experience)
* Write FindSFML and FindGLM scripts for cmake.
* Improve the vehicle dynamics
* Add more views to rwviewer
    * Handling data
    * Collision data
    * Animation scrubbing
* Improve file loading
    * One-off loaders should be moved out of GameData into some DATLoader or something.
    * Some error mechanism that allows for useful error messages.

## License

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

### Third Party Licenses

MAD is licensed under the GNU General Public License

* http://www.underbit.com/products/mad/

SFML is licensed under the zlib license

* http://www.sfml-dev.org/license.php

Bullet Physics is licensed under the zlib license

* http://bulletphysics.org/mediawiki-1.5.8/index.php/LICENSE