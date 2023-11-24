# Introduction

When creating 3D models for games, there are certain standards that you should follow. These standards will help you create better models and will make your models easier to work with. This document will go over the standards that you should follow when creating 3D models for games.

There is also an old but gold resource that you can check out. [Polycount](http://wiki.polycount.com/wiki/Modeling)

## Meshes with no geometry:

Sometimes you create a complex mesh and want to detach elements inside that mesh. You may detach all elements and the main mesh becomes an empty object and you forget to delete it. or maybe on some other ways you might end up having an empty object without any mesh. This will not heavily effect the performance of the game, but it is recommeded to have a clean and valid objects in your file.

## Meshes with no material:

You need to make sure that all meshes have a material assigned to them. If you have a mesh with no material, usually it will be assigned to the default material of the game engine with a default name like `DefaultMaterial` or `DefaultMaterial_0` or `Material_##`. Having these kind of materials in your game engine will make it harder to work with and will make it harder to find the materials that you need. So make sure to assign a material to all your meshes.

## Edges with no faces:

Sometimes when you delete some faces of a mesh, you might end up having some edges with no faces. You need to make sure that all edges have at least one face.

## Unit Setup:

Make sure you have an appropriate Unit Setup like meters, centimeters, inches, etc. This is important for the scale of your models and the physics of your game. For example, if you are using meters, then a 1x1x1 cube will be 1 meter in length, width, and height. If you are using centimeters, then a 1x1x1 cube will be 1 centimeter in length, width, and height.

[More info](https://resources.turbosquid.com/training/modeling/real-world-scale/)

## Topology:

Having T-Verts, N-Gons, and other bad topology can cause issues with your model. It can cause issues with UVs, baking, and other things.

[More info](https://resources.turbosquid.com/training/modeling/clean-edge-flow-t-vertices/)

[Are Ngons Really That Evil in 3D Modeling?](https://www.creativeshrimp.com/ngons-tutorial.html)

## Isolated Vertices:

Isolated vertices are vertices that are not connected to any other vertices. Make sure you don't have any isolated vertices in your model.

[More info](https://resources.turbosquid.com/training/modeling/isolated-vertices/)

## Overlapping vertices:

Make sure to weld vertices that are overlapping when they are in the same. This can cause issues with UVs, baking, and other things.
You can simply fix them by selecting all vertices and using the weld modifier in blender. [Blender Weld Modifier](https://docs.blender.org/manual/en/latest/modeling/modifiers/generate/weld.html)

## Non-manifold geometry:

Non-manifold geometry refers to any edge that is shared by more than two faces.

[More info](https://support.shapeways.com/hc/en-us/articles/360007107674-Tips-for-a-successful-manifold-3D-model)

## Applied Transforms:

Make sure to apply all transforms before exporting your model. If you don't apply the transforms, it can cause issues with the model when you import it into the game engine and your might look squashed, stretched, or rotated.

How to do it [in Blender](https://docs.blender.org/manual/en/latest/scene_layout/object/editing/apply.html#transforms)

<img src=https://github.com/QuVery/GameDevTechStandards/assets/6388730/9efffd5e-cb85-45ee-9c17-eb9bf3aa4f70 width=400>



## Z-fighting:

Z-fighting is when two faces are overlapping each other. These faces are fighting to be rendered. This can cause issues with your model.

[More info](http://wiki.polycount.com/wiki/Z-Fighting)

[More info](https://en.wikipedia.org/wiki/Z-fighting)

## Face Normals:

Make sure all your face normals are facing the correct direction.

[More info](<https://en.wikipedia.org/wiki/Normal_(geometry)>)
[Blender Tutorial to fix normals](https://www.youtube.com/watch?v=p4yDKp2MtlI) by Darkcaper
[Blender Tutorial to fix normals](https://www.youtube.com/watch?v=cn5BC3Vzcsc) by Ryan King Art

## UVs:

### UV Seams:

UV seams are where the UVs are cut. Make sure to place them in areas that are not visible to the player. For example, if you have a character model, you can place the UV seams on the back of the character. This will make the UVs easier to work with and will make the UVs look better.

### Overlapping UVs:

UV islands are the individual UVs for different parts of the model. Make sure they are not overlapping each other.

### UV Stretching:

UV stretching is when the UVs are stretched. This can cause issues with the textures. Make sure to minimize UV stretching unless it is intentional.

## Pivot Point:

Make sure the pivot point is in the center of the model or in a place that makes sense when working with the model. For example, if you have a tree, you want to make sure the pivot point is at the bottom of the tree. This will make it easier to place the tree in the game engine.

## Export the model in the scene origin:

Make sure your model is in the center of the scene because if it is not, it will be hard to work with in the game engine. For example if you have a rock model, you want to make sure it is in the center of the scene so that it is easy to place in the game engine.

## Reset Xform:

If you rotate, scale, or move your model when making it, these attributes will be with your model when you export it. This can make your model squashed, stretched, or rotated when you import it into the game engine. Make sure to reset the Xform before exporting your model. This will reset the rotation, scale, and position of your model to the initial state and your model in game, will be in the same state as when you first created it.

[More info](https://resources.turbosquid.com/training/training-scene-organization/resetting-transforms/)

## Model Direction:

In case our model needs to be directionally respected, such as a car, airplane, etc., the model direction is determined in coordination with the technical manager of the project. This coordination is determined according to the modeling tool and game engine, which are Z-Up or Y-up or left-hand-axis or right-hand-axis.
So make sure the model is facing the correct direction when you export it.

## Naming Conventions:

Make sure to name your model and its parts correctly. This will make it easier to work with in the game engine and in case you need to edit it later.

## Polycount:

Before you start modeling, make sure you know the polycount budget for your model. This will help you create a model that is optimized for the game engine.

## LODs:

If your model needs LODs, make sure to create them. You can simply use modifiers in blender to create LODs. [Blender LOD Tutorial](https://www.youtube.com/watch?v=DCcqnY-Fll4) by Jon Ilo
Usually naming convention for LODs is like this: `ModelName_LOD0`, `ModelName_LOD1`, `ModelName_LOD2`, etc.
Unless your team has a different naming convention.

## Collision:

If your model needs collision, make sure to create it. Here are some tutorials on how to create collisions.

[Create custom collision for Unreal in Blender](https://www.youtube.com/watch?v=EVuiOZnu7Gc) by bleakmill

[How To Make Custom Collisions in Unreal Engine (on imported models)](https://www.youtube.com/watch?v=0kzBgnKSBLE) by Buvesa Game Development

## Materials:

Materials and textures used in your models should be the standard materials and textures used in the project.
We never use Vray materials or miscellaneous plugins unless coordinated with the relevant technical team members.

## SubObjects:

If your model has multiple subobjects, try to merge them as much as possible before exporting the model to reduce the number of objects. Another important thing to consider is the naming of subobjects that are not merged. By reading the name of each subobject, we should understand what this object refers to.

## Vertex Color:

Sometimes we need to use vertex color in our models.
Vertex color is a color that is assigned to each vertex of a mesh. This color can be used for many things such as blending between textures, masking, etc. make sure to use vertex color properly and don't use it for unnecessary things.

## Modifiers:

If you are using modifiers in your model, make sure to apply them before exporting your model. This will make it easier to work with in the game engine.

## Smoothing Groups:

Smoothing groups are used to make different parts of the model smooth or hard. Make sure to use them properly. For example, if you have a curved surface, you want to make sure it is smooth. If you have a hard surface, you want to make sure it is hard. This will make your model look better and will make it easier to work with in the game engine.
