# Expo Camera onBarCodeScanned Callback Issue

This repository demonstrates a bug in Expo's Camera API where the `onBarCodeScanned` callback function intermittently fails to return barcode data.  The callback is triggered, but the `data` parameter is either missing or empty.

## Steps to Reproduce

1. Clone this repository.
2. Run the project using Expo Go.
3. Point the camera at a barcode.  Note that the results may be inconsistent. Sometimes the barcode will be correctly scanned, while other times it may return empty data.

## Potential Causes

* Timing issues in the `onBarCodeScanned` processing.
* Potential race conditions or unexpected behavior within the Expo Camera component.
* Hardware dependency, may be specific barcode scanners or camera hardware.