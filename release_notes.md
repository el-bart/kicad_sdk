# release notes

## dev
* ARM64 architecture support, when building container


## v2.3.1
* fixed download location for KiCad (permanent snapshot)
* more ignored elements in `.gitignore`


## v2.3
* added automated script to get latest KiCad `patch` version from a given family (`major.minor`)
* using KiCad 7.0 (7.0.11 at the moment of the release)


## v2.2
* using KiCad 7.0.10 now
* BOM `instances` field is now sorted properly
* added drill file preview as an SVG
* gerber now generates drill files by default, too


## v2.1
* user's "home directory" is now preserved between interactive KiCad runs for convenience (automated runs still use temp dir for reproducibility)
* ignoring `~*` backup files from KiCad 7.0
* added `FAQ.md` with known problems and solutions


## v2.0
* switched to use KiCad 7.0.8
* moving most of the heavy-lifting to `kicad-cli` in the backend
* added `./kicad` helper to start kicad from SDK, in GUI mode
* `./make` wrapper now uses `./sdk` that can also start KiCad GUI
* STEP -> STL conversion is now done using PrusaSlicer, instead of FreeCAD
* added `export_template` script, for eas of integration
* `*-backups` are now in `.gitignore`
* added SVG generation of shematics and each PCB layer
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
