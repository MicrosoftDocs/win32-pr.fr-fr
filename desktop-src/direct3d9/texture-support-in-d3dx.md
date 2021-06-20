---
description: En savoir plus sur la prise en charge de la texture dans D3DX. D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Prise en charge de la texture dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404602"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Prise en charge de la texture dans D3DX (Direct3D 9)

D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.

## <a name="textures"></a>Textures

De nombreuses textures différentes sont prises en charge dans les rubriques suivantes.

-   Prise en charge standard de la texture mipmapped. Voir [génération automatique de des mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).
-   Prise en charge du mappage de cube. Consultez [mappage d’environnement cubique (Direct3D 9)](cubic-environment-mapping.md).
-   Prise en charge de la texture du volume. Consultez [ressources de texture de volume (Direct3D 9)](volume-texture-resources.md).
-   Prise en charge du mappage d’environnement. Voir [mappage d’environnement (Direct3D 9)](environment-mapping.md).
-   Prise en charge du mappage de relief. Voir placage [de relief (Direct3D 9)](bump-mapping.md).

### <a name="texture-color-conversion"></a>Conversion de couleur de texture

Lorsque vous utilisez l’une des fonctions D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx ou D3DXCreateVolumeTexturexxx, la conversion des couleurs devra peut-être être effectuée. Par exemple, une surface peut être de type RVBA et l’autre peut être UVWQ. Pour les cas de formats différents, la séquence de conversion est la suivante :

### <a name="mapping-rgba-to-uvwq"></a>Mappage de RVBA à UVWQ

-   R <-> U, le canal R est mappé au canal U, ou vice versa.
-   G <-> V, le canal G est mappé au canal V, ou vice versa.
-   B <-> W, le canal B est mappé au canal W, ou vice versa.
-   Une < > Q/L, un canal est mappé au canal Q ou L (en fonction de celui qui est disponible dans le format de destination), ou vice versa.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Mappage de l’UV au RVBA

-   U <-> R, le canal U est mappé au canal R, ou vice versa.
-   V <-> G, le canal V est mappé au canal G, ou vice versa.
-   1 <-> B, 1 est mappé au canal B, ou vice versa.
-   1 <-> A, 1 est mappé au canal A, ou vice versa.

Si un canal n’existe pas dans la source, il est supposé être 1 (à l’exception de A8, où R, G, B sont supposés être 0). Exemple :


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



