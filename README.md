# finalcdosx - Run FinalCD on Mac

[FinalCD](http://www.sonicillusions.co.uk/finalcd.htm) is a sample rate converter made by [Sonic Illusions](http://www.sonicillusions.co.uk). It has gained some popularity among mastering engineers due to its very high quality filtering. 

[Finalcdosx](https://www.electronicburger.com/software/finalcdosx/) provides a way to run FinalCD, which is Windows only, on Mac using [Wine.app](https://winebottler.kronenberg.org/specifications), which is a pre-built, self-contained Wine distribution for Mac. It's normally a part of [Winebottler](https://winebottler.kronenberg.org/), but for this specific use, all we need is Wine.app.

The script also provides a (very) basic GUI to select the file to convert and to set the filter parameters.

The script is tested with FinalCD v0.27 and Wine.app v1.8.6, on Mac OSX v10.11.6 (El Capitan). It should work fine with later (or earlier) versions of MacOS and Wine.app as well, at least up to MacOS 10.14 (Mojave). 

MacOS 10.15 (Catalina) and above will not work at all due to Wine not supporting these OS:es.

## Installation

1. Download Wine.app from http://winebottler.kronenberg.org/downloads
2. Drag Wine.app to Applications.
3. Download FinalCD from http://www.sonicillusions.co.uk/downloads.htm
4. Unzip FinalCD to a folder somewhere.
5. Download the finalcdosx script [here](https://www.electronicburger.com/software/finalcdosx/), save it to the FinalCD folder, and unzip it.
7. Run the script "finalcdosx" by double-clicking it in Finder, or run it from the terminal.

## Usage

See [this blogpost](https://www.electronicburger.com/blog/finalcdosx-finalcd-on-mac/) for more detailed instructions.

When the script is run, it will first check that finalcd.exe and Wine.app is present, and show an error and exit if either is missing. 

Then you can select which file to convert. See the FinalCD documentation for all supported formats. It can only convert one file at the time at the moment.

After that, you can select which filter to use. Again, check the FinalCD docs for what the different options mean.

Then select the output bit depth and whether or not dither should be applied. 

In the next dialog, you can manually edit the parameters sent to FinalCD. This is useful if you want to use any of the additional features of FinalCD that isn't supported by this script, like 88.2 kHz output. See the FinalCD documentation for more info. In the normal case you'd just press OK without changing anything.

The script will now attempt to run FinalCD, and will save the converted file at the same location as the original, with the same name but with "f_" prefixed.

That's it!

