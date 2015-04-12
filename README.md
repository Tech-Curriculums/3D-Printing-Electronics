# OpenSCAD Basics



## TODO:
* Make_a_shape.md
* Advanced options for shapes
  *r1 r2 for radius
  *make $fs lower in order to increase resolution
* Combining/Subtracting Shapes
  * include animations of each one to the right
* Movements.md & Animation section
  * translate([x,y,z])
  * rotate([x,y,z])
  * scale([x,y,z])
* Animation.md
  * FPS
  * steps (degrees)


## Combining/Subtracting Shapes

**Combine**

general, how to use:
```javascript
union(){
  thing1;
  thing2;
}
```

example:
```javascript
union () {
  cylinder(h = 40, r=20, $fs=0.1, center = true);
  cube(size = [40,20,10], center = true);
}
```

**Subtract**

basic syntax:
```javascript
difference() {
  thing1;
  thing2;
}
```
example:
```javascript
difference () {
  cylinder(h = 40, r=20, $fs=0.1, center = true);
  cube(size = [40,20,10], center = true);
}
```

**Get Intersection**

basic syntax:
```javascript
intersection() {
  thing1;
  thing2;
}
```

example:
```javascript
intersection () {
  cylinder(h = 40, r=20, $fs=0.1, center = true);
  cube(size = [40,20,10], center = true);
}
```

## Animations


```javascript
rotate([0,0,360*$t]){
  difference () {
    cylinder(h = 11, r=10, $fs=0.1, center = true);
    cube(size = [20,10,2], center = true);
  }
}
```


