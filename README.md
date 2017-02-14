# Cubo.scad
Module OpenSCAD pour tronquer les angles des cubes

Coller le fichier "Cubo.scad" dans le même répertoire que le fichier scad 
Pour importer la librairie :

use <Cubo.scad>;

// le premier parametre : [x,y,z] comme pour cube([x,y,z])
// le 2eme : La liste des angles qui seront tronqués. Il y en a 12
// le 3eme : La largeur du coté tronqué

// quelques exemples d'utilisation :

cubo([10,10,5], [1,2,3,4,5,6,7,8,9,10,11,12], 1.5);

translate([15, 0, 0]){
    difference(){
        cubo([10,20,5], [2,3], 3);
        translate([5,10,-1]) cylinder(r=2, h=7, $fn=12);
    }
}

translate([-15, 0, 0]){
    difference(){
        cube([10,20,15]);
        translate([3,3,3]) cubo([10,20,50], [1,5], 3);
    }
}

// Modif


