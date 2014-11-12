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

## Importing the RhinoScriptSyntax

There code should be added before any snippets using the *rs* library (e.g. rs.AddPoint([0, 0, 0]).

## Add a Point

```
# Add a Point at (0,0,0)
rs.AddPoint([0, 0, 0])
```

## Add a Line
```
# Add a Line from the point (0, 0, 0) to (0, 0, 1)
rs.AddLine([0, 0, 0], [0, 0, 1])
```
