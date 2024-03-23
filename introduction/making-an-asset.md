---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Making an Asset

### Preface

This page will teach you how to make a basic object(building) as a mod for Unturned. It will **not** teach you basics about asset making, only the barebones of what is needed for you to complete and put the asset ingame.&#x20;

### What makes up an Object?

* Nav - is the mesh that zombies uses as its navigation mesh. This mesh does not need roofs, frames(of windows, doors, etc). The mesh should be simple and the foundation should be expanded to be more of a ramp. Every ledge should be smoothed so that it does not have such a harsh corner like the ledge of a window should be more ramp like. Needs a Mesh Collider. Tag and layer: Navmesh.
* Clip(optional) - is the mesh that the server uses as the collision, the client does not use this mesh for the collision. Needs a Collider. Tag and layer: (Large, Medium, Small)
* Skybox(optional) - is the mesh that is rendered when the object is consider as a Landmark. This mesh should be very simple at around 30 triangles. It usually does not include an interior and is a primitive shape. Needs a Mesh Filter, and Mesh Renderer. Tag and layer: (Large, Medium, Small)
* Object - is the main model which contains the LODs. The name of the LODs should be "Model\_#" with # being the number(starts from zero). Optionally, you can add an Occlusion Area. The objects in that box will have a Lod Bias applied to it making it have lower details. Needs a LOD group, Mesh Filter, Mesh Renderer, and a Mesh Collider(or a primitive collider). The Mesh Collider is usually the LOD 1(second LOD). Tag and layer: (Large, Medium, Small)
* Slots(optional) - consists of Box Colliders. The possible names are Door, Gate, Slot(for barricades like windows). See measurements(replace with link to page here?) here. Tag and layer: Logic

#### Example

<figure><img src="../.gitbook/assets/475AB537-D115-4BF4-92AD-FA9D5863B0CB.jpeg" alt="Example hierarchy(sorry that you cant see it)" width="149"><figcaption><p>Exaple model</p></figcaption></figure>

### .Dat file
