# Resin 3D Printer Calibration Suite

A collection of 3D models (STL and Lychee files) designed for resin 3D printer calibration. The suite includes models for both [build plate calibration](#build-plate-calibration) and [exposure time calibration](#peg-of-calibration-exposure-time-calibration-for-dimensional-accuracy), helping you determine the exposure time at which your prints are overexposed by no more than 0.02 mm in XY thickness, or underexposed by no more than 0.01 mm.

The models have been optimized to use as little print time and resin as possible while still producing precise results.

# Build Plate Calibration

This suite includes a set of nine 1.5 mm-thick tiles. The tiles are intended to be placed as shown below: in the corners, along the edges, and in the center of your build plate, with each tile rotated accordingly. After printing, measure each tile using digital calipers.

![Build Plate Calibration Tile Placement](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/plate_layout.jpg)

Each tile includes a unique cutout, marked in the image below, allowing you to associate it with the corresponding location on the build plate.

![Build Plate Calibration Tiles](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/plate.jpg)

Additionally, each tile includes a set of identical shallow cutouts that can help you roughly estimate the accuracy of your current exposure time.

![Build Plate Calibration Tile](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/plate_tile.jpg)

The recessed and raised features on both sides of each tile, such as chevrons and lines, should match in thickness. In other words, the thinnest recessed feature on one end should match the thinnest raised feature on the other end.

If the recessed features are visibly larger, you are most likely significantly underexposing. If they are visibly smaller or closed, and the raised features appear too thick, the print is likely overexposed.

The same applies to the circular cutouts: the five smallest cutouts correspond to the small pegs located inside the larger cutouts.

However, this is only a rough estimate. For more precise exposure time calibration, use the dedicated [Peg of Calibration](#peg-of-calibration-exposure-time-calibration-for-dimensional-accuracy) model.

### Build Plate Results Interpretation

The difference between the thickest and thinnest tile should be approximately 0.1 to 0.15 mm. If the difference is greater, your build plate may be out of level.

The printed tiles should also be close to 1.5 mm in thickness, ideally slightly above that by 0.1 to 0.2 mm. If they are too thin, you may encounter layer compression issues, where the bottom layers do not adhere to the build plate correctly.

# Peg of Calibration: Exposure Time Calibration for Dimensional Accuracy

The Peg of Calibration model includes several calibration features for determining the correct exposure time for dimensional accuracy, as well as the resin's tensile strength and detail reproduction at that exposure time.

![Peg of Calibration model](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/long_raft.jpg)

The main calibration component is Peg herself.

![Peg of Calibration](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/peg.jpg)

After printing the model, snap Peg off the raft and try to fit her into the holes located on the other side of the model:

![Holes](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/holes.jpg)

The -0.02 hole is designed to test for underexposure, the +0.08 hole tests for overexposure, and the middle hole tells you whether your prints are dimensionally accurate. Refer to the [Peg of Calibration Results Interpretation](#peg-of-calibration-results-interpretation) section for more details.

Once you have determined the correct exposure time, you may want to check the other features to better understand the resin's parameters, such as tensile strength, detail reproduction, and overhang consistency.

![Lollipop Features](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/lollies.jpg)

Each pair of lollipop-like features tests a different mini-support thickness, with the values printed on the model above each pair. One lollipop has a 0.5 mm ball attached, while the other has a 0.75 mm ball. Each stick is exactly 1.5 mm long. Most likely, not all of them will print successfully with all resin types and/or lift and retract speed settings.

![Cutouts](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/cutouts.jpg)

The recessed and raised features for each set of cutouts should match in thickness: the thinnest raised chevron should match the thinnest recessed chevron, the thinnest raised line should match the thinnest recessed line, and the five smallest circular features should match the five raised circular features inside the larger cutouts. Refer to the image above to check whether all features printed correctly.

![Overhang Board](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/board.jpg)

The small board on one side of the model lets you test how well overhangs are reproduced with your resin. Check whether any of the holes are filled in and whether they have the correct shape. The checkerboard tiles should all touch at the corners and, ideally, have a flat bottom side.

On the left, you will find three wedge-shaped pieces designed to test how well overhangs are reproduced with the resin being tested. The bottom overhang is at 80 degrees, the middle one is at 82.5 degrees, and the top one is at 85 degrees. The top side should be completely flat and horizontal. The bottom side may show sagging and/or flaking with more flexible resins, so features like this on your models may require more densely placed supports.

![Raft](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/raft_1.5mm.jpg)

The final feature is the raft itself. The raft is 1.5 mm thick, so you may want to measure it with digital calipers to check how level your build plate is and whether there is any compression. If you printed multiple copies of the model, this works similarly to the [build plate calibration test](#build-plate-calibration).

Additionally, the flat, featureless part of the raft is designed to be used with RERF-style calibration, allowing you to digitally engrave the exposure value for each model, as shown below:

![RERF](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/rerf_layout.jpg)

If you do not plan to perform RERF calibration, or if your printer does not support it, you may want to use the version of the model with a shorter raft:

![Peg of Calibration Short Raft Model](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/short_raft.jpg)

### Peg of Calibration Results Interpretation

![Calibration](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/calibration.jpg)

Try to fit Peg in all three positions. If she:

- **Fits** in the **red** (-0.02) position, you are **underexposing** by more than 0.01 mm. **Increase your exposure time** and test again.
- **Does not fit** in the **dark green** (+0.08) position, you are **overexposing** by more than 0.04 mm. **Decrease your exposure time** and test again.
- **Fits** in the **dark green** (+0.08) position, but **does not fit** in the **middle light green** (6 mm) position, you are **overexposing** by more than 0.02 mm. **Decrease your exposure time slightly** and test again. Alternatively, you may leave it as is if the resin is very flexible and difficult to calibrate.
- **Fits** in the **middle light green** (6 mm) position and **does not fit** in the **red** (-0.02) position, your exposure time is correct and your prints should be dimensionally accurate.

# Army of Pegs: Exposure Uniformity Calibration

*This step is completely optional and admittedly a bit OCD. After determining the correct exposure time in one area of the build plate using a single [Peg of Calibration](#peg-of-calibration-exposure-time-calibration-for-dimensional-accuracy) model, you may want to see how that result compares across the rest of the build plate, if you are a complete lunatic, that is.*

Forty-five additional Peg models are provided in this suite. Each model has the same dimensions, but each one is uniquely marked on its flat top side:

![Pegs](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/pegs_cutouts.jpg)

They are intended to be distributed uniformly across the build plate, as shown in the image below, with each marking matched to its corresponding location on the plate:

![Pegs](https://github.com/b005t3r/Resin3DPrinterCalibrationSuite/blob/main/img/pegs_layout.jpg)

Print them using the previously calibrated exposure time. After printing, use them as described in the [Peg of Calibration Results Interpretation](#peg-of-calibration-results-interpretation) section to check how uniform your exposure is across the entire build plate. Adjust your exposure time if needed.

[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg