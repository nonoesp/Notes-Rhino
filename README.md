Notes-Rhino
===========

Notes on Rhino, Grasshopper and Python.

# Commands

### Selection Commands

`zs` Zoom selected objects.

`selall` Select all.

`sel`*+element_type* Add to current selection the specified objects (e.g. `selcrv`, `seltext`, `selcrv`, `seldim` or `selleader`)

## General Commands

`hide` or `show` Hides or shows selected geometry.

`lock` or `unlock` Locks selected geometry, or unlocks all locked [and visible] geometry.

`toolbar reset` Resets the default configuration of the toolbars (needs restart of Rhino).

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

## Rhynamo

### Packages

To install packages downloaded manually, add them into the following folder:

`C:\Users\{USERNAME}\AppData\Roaming\Dynamo.7\packages`

## License

Notes-Rhino is licensed under the MIT license. (http://opensource.org/licenses/MIT)

## Me

I tweet at [@nonoesp](http://www.twitter.com/nonoesp) and blog at [nono.ma/says](http://nono.ma/says). I would love to hear about it if you find these notes are useful. Thanks!
