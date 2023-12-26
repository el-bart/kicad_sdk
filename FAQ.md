# FAQ

## STL export does not have components on PCB

this is a [KiCad design issue](https://forum.kicad.info/t/v6-step-3d-model-export-missing-components-or-completely-empty-board-is-exported/33847).
usually opening model in newer KiCad and updating paths solves the issue.

in case KiCad project has been imported from other tool (eg. Eagle CAD), some changes of elements enclosure types might be needed.


## STL export does not have screw holes

this is likely because you are using vias as a holes, yet [KiCad does not export vias](https://forum.kicad.info/t/step-export-missing-holes-and-metal/16598).
official way of fixing that is to use [mounting holes instead of vias](https://forum.kicad.info/t/create-a-mounting-hole/6737).
to do this in PCB editor press `A` and search for a proper shape, eg. `MountingHole_3.2mm_M3_Pad_TopBottom`.
