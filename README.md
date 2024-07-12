# pytRIBS
A pre-to-post processing python package designed to allow users to setup, simulate, and analyze TIN-based Real-time Integrated Basin Simulator (tRIBS) model runs through a python interface.
Note this packages is currently under development and is subject to further changes. Additionally, much of the functionality here has had limited testing, consequently responsibility is on the user to verify package functionality. 

## Release/Version Notes
PytRIBS uses semantic versioning. Currently, we are in the initial development phase--anything MAY change at any time and
this package SHOULD NOT be considered stable.
### Verison 0.5.0 (in developmet)
* Model class can be initialized with combination of Met, Soil, Land, and Mesh classes as well as an input file
### Version 0.4.0 (07/11/2024)
* added in functionality for met class, can now download and subset NLDAS data with watershed shapefile
* changed key_word in Model.options dictionary to keyword
* Updated Met Class including methods to download and merge NLDAS data.
* Changed waterbalance clacs to use ThetaS instead of porosity following tRIBS
* Converted geo to meta, and added Meta class.
* Added new function in read.py to read in *_Outlet.qout files
### Version 0.3.0 (5/03/2024)
* Removed tmodel/tresults, replaced with classes
* added new classes Soil, Mesh, Met, Land
* renamed mixins folder to shared
* created results/visualize.py
* created soil/soil.py --moved soil related content from preprocess to here.
* updated create_soil_map to return a soil table in .sdt format.
* updated read/write soil tables to include options for including texture.
### Version 0.2.0 (4/25/2024)
This minor update includes:
* updates to the infile_mixin, with updates for 
model documentation
* addition of Paul Tol's colormaps (https://personal.sron.nl/~pault/)
* In shared mixin:
  * added processor # to the attribute voronoi
  * added plot_mesh()
  * fixed other syntax bugs
* model.inout.py
  * added read added write_point_file()
  * fixed syntax bugs in several functions
* Fixed several bugs in preporcess.py and waterbalance.py
* Added create_animation() to Results()
