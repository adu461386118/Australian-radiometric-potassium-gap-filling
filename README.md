# Australian Radiometric Potassium Gap Filling

This repository contains the Python and shell scripts used for radiometric potassium gap filling, neural-network regression, prediction automation, raster mosaicking, and validation workflows.

The code was prepared for archiving with GitHub and Zenodo so that it can be cited with a DOI.

## Repository Structure

```text
gap-filling/
  DC_shift_mean.py
  DC_shift_mean.sh
  mosaic_K.py
  mosaic_K.sh

training_validation/
  nn_regression_keras_global_local.py
  predict_automation.py
  pred_parts.sh
  submit_with_optimal_epochs.py
  regression_oos_calculation_Landshark.py
  intersect_raster_with_shape.py
  bash_run.sh
  groups.sh
  merge.txt
  merge_proba_0.txt


Description
The gap-filling/ directory contains scripts for raster gap filling, DC-shift adjustment, and mosaicking of radiometric potassium prediction outputs.
The training_validation/ directory contains scripts for model training, prediction automation, validation against out-of-sample data, raster-vector intersection, and merging tiled prediction outputs. The neural-network model configuration is implemented in nn_regression_keras_global_local.py.
Some shell scripts were written for a high-performance computing environment and contain example PBS directives, module loads, and environment paths. These paths may need to be modified before running the scripts on another system.
Main Dependencies
The scripts require a Python/geospatial machine-learning environment with packages such as:
- Python 3
- NumPy
- Pandas
- SciPy
- Rasterio
- GeoPandas
- GDAL / OSGeo Python bindings
- TensorFlow / Keras
- Landshark
- GNU Parallel, for some shell workflows
Exact versions may depend on the target computing environment.
Notes
This repository contains code only. Large raster inputs, trained model outputs, intermediate HDF5 files, and generated GeoTIFF prediction products are not included.
The scripts assume access to external input data, including raster covariates, target point data, and trained model/checkpoint outputs.
