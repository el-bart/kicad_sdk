# release notes

## dev
* STEP -> STL conversion is now done using PrusaSlicer, instead of FreeCAD
* switched to use KiCad 7.0.8
* added `export_template` script, for eas of integration
* `*-backups` are now in `.gitignore`
* minor bugfixes and improvements

## v1.0
* Docker-based SDK definition, for stability.
* separation of created and generated files (`build/`).
* `.gitignore` template for KiCad generated files.
* automatically creating gerber files in `*.tar.gz` format.
* automatically creating gerber files in `*.zip` format.
* generating STL 3D model files.
* generating [BOM](https://en.wikipedia.org/wiki/Bill_of_materials).
* storing MD5 of a PCB file, for reference.
