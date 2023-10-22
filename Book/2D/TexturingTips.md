# Textures

We try to use the lowest possible dimensions for textures in games. Pack homogeneous models into one texture, use the maximum possible space for UVs, and use tileable textures for repeatable parts of the models as much as possible.

## Transparency
We try not to use transparent images as much as possible for the sake of performance, and images that do not need transparency are output without the alpha channel.

## Dimensions
We always use power of 2 dimensions for textures. (32, 64, 128, 256, 512, 1024 or 2048) Unless coordinated with the technical team. These dimensions are the standard dimensions for textures in games as they are better fit into the memory of the GPU.