# Resin 3D Printer Calibration Suite

A collection of 3D models (STL and Lychee files) designed for resin 3D printer calibration. The suite includes models for both [build plate calibration](#build-plate-calibration) and [exposure time calibration](#peg-of-calibration-exposure-time-calibration-for-dimensional-accuracy), helping you determine the exposure time at which your prints are overexposed by no more than 0.02 mm in XY thickness.

## Build Plate Calibration

This suite includes a set of nine 1.5 mm-thick tiles. The tiles are intended to be placed as shown below: in the corners, along the edges, and in the center of your build plate, with each tile rotated accordingly. After printing, measure each tile using digital calipers.

Each tile includes a unique cutout, marked in the image below, allowing you to associate it with the corresponding location on the build plate.

![Build Plate Calibration Tiles](/img/plate.jpg)

Additionally, each tile includes a set of identical shallow cutouts that can help you roughly estimate the accuracy of your current exposure time.

The recessed and raised features on both sides of each tile, such as chevrons and lines, should match in thickness. In other words, the thinnest recessed feature on one end should match the thinnest raised feature on the other end.

If the recessed features are visibly larger, you are most likely significantly underexposing. If they are visibly smaller or closed, and the raised features appear too thick, the print is likely overexposed.

The same applies to the circular cutouts: the five smallest cutouts correspond to the small pegs located inside the larger cutouts.

However, this is only a rough estimate. For more precise exposure time calibration, use the dedicated *Peg of Calibration* model.

#### Results Interpretation

The difference between the thickest and thinnest tile should be approximately 0.1–0.15 mm. If the difference is greater, your build plate may be out of level.

The printed tiles should also be close to 1.5 mm in thickness, ideally slightly above that by 0.1–0.2 mm. If they are too thin, you may encounter layer compression issues, where the bottom layers do not adhere to the build plate correctly.

## Peg of Calibration: Exposure Time Calibration for Dimensional Accuracy

[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg