# SelectObjectOutliner
Library for outlining selected models.

### Modes
Works in two modes:
1. Material mode - based on a duplicated geometry and unshaded material. Simpler and faster, but bad looking. Works with the depth. 

![SelectObjectOutlinerMaterial](../master/img/SelectObjectOutlinerMaterial.jpg)

2. Filter mode - based on a filter. Nice looking. Slower. Disregards the depth. 

![SelectObjectOutlinerFilter](../master/img/SelectObjectOutlinerFilter.jpg)

#### Usage
```
//Declare
outliner=new SelectObjectOutliner();
//Init - using filter
outliner.initOutliner(SelectObjectOutliner.OUTLINER_TYPE_FILTER, 2, ColorRGBA.Yellow,rootNode,fpp, renderManager, assetManager, cam);
OR     
//Init - using material
//outliner.initOutliner(SelectObjectOutliner.OUTLINER_TYPE_MATERIAL, 2, ColorRGBA.Yellow,rootNode,fpp, renderManager, assetManager, cam);
...
CollisionResult closest = results.getClosestCollision();
Geometry nextGeo=closest.getGeometry();
outliner.select(selectedGeo);
...
outliner.deselect(selectedGeo); 
...
outliner.isSelected(selectedGeo); 
```

#### Credits

https://hub.jmonkeyengine.org/t/outliner-material-toon-outline/37610/7

https://hub.jmonkeyengine.org/t/share-my-select-spatial-toon-outline-effect-filter-shader/35929/14
