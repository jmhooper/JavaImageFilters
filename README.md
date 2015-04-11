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

Right now there are only 2 filters.
Hopefully more will follow.

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
