# base-sinhala
base-sinhala is a Sinhala font build system with essential foptions such as interpolation and compiling.  

##Dependancies
* [Adobe Font Development Kit for OpenType](http://www.adobe.com/devnet/opentype/afdko.html)
* [Robofab](http://robofab.org/)- There is a issue with robofab glyph naming. If you use non Unix based operating system we reccomend using the Mooniak [fork](https://github.com/mooniak/robofab) of robofab.
* [UFOInstanceGenerator.py](https://github.com/adobe-type-tools/python-scripts/blob/master/FDK%20Extras/UFOInstanceGenerator.py) - This script should be places in your FDK folder. (FDK/tools/win or FDK/tools/mac or FDK/tools/linux). We have done some changes to the script so it wont stop build due a failure of interpolation. Hense we reccomend using the script in this repository.
