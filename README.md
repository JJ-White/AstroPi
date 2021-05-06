# High quality portable astrophotography without a PC

The aim for this project is to control a Raspberry Pi camera from a smartphone, tablet, 
or computer connected to the same network. Because my main application will be astrophotography
the controls will be focussed around long exposures or other controls specific to this field.

The project will have a back-end application that captures images using the provided settings
and present a RESTful API that a web front-end will use to preview exposures and adjust parameters.

I am also planning to integrate control for the [OpenAstroTracker](https://github.com/OpenAstroTech/OpenAstroTracker)
when I build one, to make this an all in one solution for astrophotography that doesn't need a Windows 
computer.

*As you can see there's not much here yet, but keep an eye out for progress and let me know if you're
interested in using such a solution or participating in its creation.*

## API

This section is a mockup of what the API could look like and will be updated as development continues.

Endpoint | Function
---------|----------
*/preview* | Get a preview image with the current settings, probably as a jpeg to save bandwidth.
*/preview/histogram* | Get a JSON object of the histogram distribution for the preview image.
*/preview/stretched* | Get an autostretched version of the preview image.
*/sequence* | Get and set settings for sequencing captures as a JSON object.
*/sequence/latest* | Get (a preview of) the last captured image of the sequence.
*/settings* | Get and set all available camera settings as a JSON object.

## Web Interface

The web interface component should work with the API of the backend to display images and change settings
to get the best possible exposures. The interface should work in a browser with different aspect ratios
and controls should be optimized for mobile use.

## Links

* [picamera](https://picamera.readthedocs.io/) - Python library used to control the Pi Camera
* [OpenAstroTracker](https://github.com/OpenAstroTech/OpenAstroTracker) - Open source astrophotography tracker
