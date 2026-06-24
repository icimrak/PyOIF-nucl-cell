# PyOIF-nucl-cell
This is an extension of the PyOIF module implementing the nucleated cell.
Simple replace the oif_classes.py file in the current PyOIF distribution.

## Acknowledgement
This code is part of the work funded by the EU NextGenerationEU through the Recovery and Resilience Plan for Slovakia under the project 09I03-03-V04-00705.

# CompoundCell

`CompoundCell` is a simple wrapper for a compound elastic object made from two existing `OifCell` objects: an outer membrane and an inner nucleus.

The class does not create new meshes. The membrane and the nucleus must already be created as separate `OifCell` instances. `CompoundCell` only connects them conceptually and defines a non-bonded Lennard-Jones interaction between their particle types.

## Purpose

Use `CompoundCell` when you want to simulate a deformable cell with two elastic parts:

- a cell membrane,
- a nucleus inside the cell,
- an interaction between the membrane and nucleus.

This is useful for modelling nucleated cells where the membrane and nucleus are represented by separate elastic meshes.



## Notes

`CompoundCell` is intentionally minimal. It only stores the two components and sets their Lennard-Jones interaction. It does not handle saving/loading, automatic nucleus placement, checking whether the nucleus is inside the membrane, or special visualization output.
