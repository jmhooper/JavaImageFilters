# Image Filters

This project contains a number of image filters written in Java as well as an interface for using them.

## Usage

After cloning the repo, compile the `Main` class.
Then run it with the input file, output file, and desired filters as arguments.

```shell
javac Main.java
java Main input.png output.png --rainbow --artifacter
```

The input file can be any file `ImageIO` can read.
The output file must be a PNG.

## Filters

### Rainbow

This filter adjusts the the hue of pixels in the image based on where the pixel is horizontally.
The result is a rainbow like effect.

The command line argument for this filter is `--rainbow`.

| Before | After |
|--------|-------|
| ![Before](https://github.com/jmhooper/JavaImageFilters/blob/master/img/rainbow/before.png) | ![After](https://github.com/jmhooper/JavaImageFilters/blob/master/img/rainbow/after.png) |

### Artifacter

This filter compresses the image as a JPEG with a very low quality.
If you wish to adjust the quality you can set the property `compressionQuality` in `Artifacter.java`.

The command line argument for this filter is `--artifacter`.

| Before | After |
|--------|-------|
| ![Before](https://github.com/jmhooper/JavaImageFilters/blob/master/img/artifacter/before.png) | ![After](https://github.com/jmhooper/JavaImageFilters/blob/master/img/artifacter/after.png) |

### RGB Shifter

This filter shifts the red, green, and blue values for the image by a random amount.

The command line argument for this filter is `--rgb-shifter`.

| Before | After |
|--------|-------|
| ![Before](https://github.com/jmhooper/JavaImageFilters/blob/master/img/rgb-shifter/before.png) | ![After](https://github.com/jmhooper/JavaImageFilters/blob/master/img/rgb-shifter/after.png) |

### Repeater

This filter repeats the image along the X and Y axis.
To specify the number of repetitions, set the `X_REPEAT` and `Y_REPEAT` constants in Repeater.java

The command line argument for this filter is `--repeater`.

| Before | After |
|--------|-------|
| ![Before](https://github.com/jmhooper/JavaImageFilters/blob/master/img/repeater/before.png) | ![After](https://github.com/jmhooper/JavaImageFilters/blob/master/img/repeater/after.png) |

### RGB Shift Repeater

This filter combines the Repeater and RGB Shifter.
As it repeats the image, it applies the RGB Shifter filter to it.

The command line argument for this filter is `--rgb-shift-repeater`.

| Before | After |
|--------|-------|
| ![Before](https://github.com/jmhooper/JavaImageFilters/blob/master/img/rgb-shift-repeater/before.png) | ![After](https://github.com/jmhooper/JavaImageFilters/blob/master/img/rgb-shift-repeater/after.png) |
