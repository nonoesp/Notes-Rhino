Notes-Rhino
===========

Notes on Rhino, Grasshopper and Python.

# Commands

## Selection
`zs` Zoom selected objects.

`selall` Select all.

`toolbar reset` Resets the default configuration of the toolbars (needs restart of Rhino).

`sel`*+element* Add to current selection the specified objects (e.g. `seltext`, `selcrv`, `seldim` or `selleader`)

`CTRL + SHIFT + CLICK` Select a part of group or object (member, face, point, edge)


# Rhino Python

## Create a Point

```
import rhinoscriptsyntax as rs
rs.AddPoint(0, 0, 0)
```
