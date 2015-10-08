Notes-Rhino
===========

Notes on Rhino, Grasshopper and Python.

This guide is part of the [Getting Architecture Done](http://www.gettingarchitecturedone.com/?utm_source=github&utm_medium=Notes-Rhino) project. Follow [@GettingArchDone](http://twitter.com/GettingArchDone) on Twitter or [Facebook](http://facebook.com/gettingarchitecturedone) to keep updated.

# Articles

* [Scripting in Rhino Python: Introduction](http://nono.ma/says/scripting-in-rhino-python-introduction)
* [Scripting in Rhino Python: Switching Units](http://nono.ma/says/scripting-in-rhino-python-switching-units)

# Commands

### Selection Commands

`untrim` Untrim a trimmed surface and recover the original one from which it was created.

`zs` Zoom selected objects.

`selall` Select all.

`sel`*+element_type* Add to current selection the specified objects (e.g. `selcrv`, `seltext`, `selcrv`, `seldim` or `selleader`)

### Commands at Startup

Just by adding simple codes at the end of the shortcut path, you can make Rhino run commands at startup, or customize things [removing the splash screen for example].

#### Run Grasshopper at Startup and Remove Splash Screen

```
 /runscript="!_grasshopper" /nosplash
```

## General Commands

`hide` or `show` Hides or shows selected geometry.

`lock` or `unlock` Locks selected geometry, or unlocks all locked [and visible] geometry.

`toolbar reset` Resets the default configuration of the toolbars (needs restart of Rhino).

`CTRL + SHIFT + CLICK` Select a part of group or object (member, face, point, edge)


# Rhino Scripting with Python

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

## Filter List to Distinct Values

This can be easily done with Python, but there is a component named *Create Set* in Grasshopper which does exactly the same.

```
distinctValuesList = set(myList)
```

## Switch Unit System between Meters and Milimeters

This script basically switches the units of the current document between meters and milimeters. The important function is *rs.UnitSystem(),* which returns the current unit measure -- or sets it if we give parameters to the function.

```
import rhinoscriptsyntax as rs

if rs.UnitSystem() == 2:
    # Current unit is mm, Switch to m
    rs.UnitSystem(4, False, True)
else:
    # Current unit is m, switch to mm
    rs.UnitSystem(2, False, True)
```

# Rhino Scripting with C Sharp

To get started with some Rhino Common scripting in C#.

Useful getters

```
Point3d.Origin
Plane.XYWorld
Vector3d.ZAxis
```

Polyline

```
Polyline polyline = new Polyline(points); // Creates a polyline from a list of points
polyline.ToList(); // Retrieves the vertices of the polyline
```

Vector

```
Vector3d vector = new Vector3d(1.0, 1.0, 0.0);
vector.Length; // Retrieves the vector's length = 1.42
vector.Unitize(); // Unitizes the vector
vector.Length; // Should output 1
```

## Rhynamo

### Packages

To install packages downloaded manually, add them into the following folder:

`C:\Users\{USERNAME}\AppData\Roaming\Dynamo.7\packages`

## License

Notes-Rhino is licensed under the MIT license. (http://opensource.org/licenses/MIT)

## Me

I tweet at [@nonoesp](http://www.twitter.com/nonoesp) and blog at [nono.ma/says](http://nono.ma/says). I would love to hear about it if you find these notes are useful. Thanks!
