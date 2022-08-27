# KiCad SDK

environment for [reproducible builds](https://en.wikipedia.org/wiki/Reproducible_builds) of your PCB designs


## features
* Docker-based SDK definition, for stability
* separation of created and generated files (`build/`)
* handy `.gitignore` template
* automatically creating gerber files:
  - `*.zip`
  - `*.tar.gz`
* generating STL 3D model files (think: 3D printing and prototyping)
* generating [BOM](https://en.wikipedia.org/wiki/Bill_of_materials)
* storing MD5 of a PCB file, for reference


## usage

this section covers basic usage of the template.


### creating new project

copy content of `template` directory into your new project workspace.
put all your KiCad files there.


### building

run `./make` to trigger build.
note that 1st time you run it, SDK will be created, so it will take some time.
after that, image will be cached and using it will become much faster.

if you do not want/need to use Docker, you can also use your own, local SDK.
just use regular `make` instead of a wrapper `./make` script.

note that you can pass `-j$(nproc)` option to `make` to enable parallel building.
