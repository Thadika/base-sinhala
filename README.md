# base-sinhala
base-sinhala is a Sinhala font build system with essential foptions such as interpolation and compiling.  

##Dependancies
* [Adobe Font Development Kit for OpenType](http://www.adobe.com/devnet/opentype/afdko.html)
* [Robofab](http://robofab.org/)- There is a issue with robofab glyph naming. If you use non Unix based operating system we reccomend using the Mooniak [fork](https://github.com/mooniak/robofab) of robofab.
* [UFOInstanceGenerator.py](https://github.com/adobe-type-tools/python-scripts/blob/master/FDK%20Extras/UFOInstanceGenerator.py) - This script should be placed in your FDK folder. (`FDK/tools/win` or `FDK/tools/mac` or `FDK/tools/linux`). We have done some changes to the script so it wont stop build due a failure of interpolation as this is supposed to be a quick-build system to test fonts during production. Hense we reccomend using the script in this repository.
* Python 2.7 or later

##How to use
* Add the two master UFO files in to `/masters` folder. The naming should be `<familyName>_0.ufo` and `<familyName>_1.ufo`.`_0.ufo` is light the master and `_1.ufo` is the bold master.
* Include the instance values in the `/masters/instances` file. These instances should comply with the STYLE_NAMES in `/config.py`. Add the family name to `/config.py` as well.
* Run the `build.py` with the command  `$python build.py`

##Notes
* Build process creates two folder named style and build. Style will contain interpolated instances of masters and build will contain final .OTF files.
* You can use merger.py to combine two UFO files into one.
* These scripts should work on any platform and tested on Windows 7, Mac OSX and Ubuntu.
* This work is inspired from ITF [base-devanagari-gf](https://github.com/itfoundry/base-devanagari-gf). Special thanks to @lianghai and ITF
