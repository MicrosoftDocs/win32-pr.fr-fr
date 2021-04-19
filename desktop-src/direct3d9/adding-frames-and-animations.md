---
description: Cette section montre comment ajouter des frames et des animations à un cube simple.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Ajout de frames et d’animations (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544200"
---
# <a name="adding-frames-and-animations-direct3d-9"></a>Ajout de frames et d’animations (Direct3D 9)

Cette section montre comment ajouter des frames et des animations à un cube simple.

## <a name="working-with-frames"></a>Utilisation des frames

Un frame est supposé prendre la structure suivante.


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



Placez le maillage de cube défini à l’intérieur d’un frame avec une transformation d’identité. Appliquez ensuite une animation à ce frame.


```
Frame CubeFrame {
FrameTransformMatrix {
1.000000, 0.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000,
0.000000, 0.000000, 1.000000, 0.000000,
0.000000, 0.000000, 0.000000, 1.000000;;
}
{CubeMesh}        // You could have the mesh inline, but this 
                  // uses an object reference instead.
}
```



## <a name="working-with-animations"></a>Utilisation des animations

Une animation est définie par un ensemble de clés. Une clé est une valeur de temps associée à une opération de mise à l’échelle, une orientation ou une position.


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



Les animations sont ensuite regroupées dans AnimationSets :


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



Maintenant, prenez le cube par le biais d’une animation.


```
AnimationSet AnimationSet0 {
Animation Animation0 {
{CubeFrame}    // Use the frame containing the cube.
AnimationKey {
2;             // Position keys
9;             // 9 keys
10; 3; -100.000000, 0.000000, 0.000000;;,
20; 3; -75.000000, 0.000000, 0.000000;;,
30; 3; -50.000000, 0.000000, 0.000000;;,
40; 3; -25.500000, 0.000000, 0.000000;;,
50; 3; 0.000000, 0.000000, 0.000000;;,
60; 3; 25.500000, 0.000000, 0.000000;;,
70; 3; 50.000000, 0.000000, 0.000000;;,
80; 3; 75.500000, 0.000000, 0.000000;;,
90; 3; 100.000000, 0.000000, 0.000000;;;
}
}
}
```



Pour plus d’informations, consultez les modèles [**animation**](animation.md) et [**AnimationSet**](animationset.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[X fichiers (hérités)](x-files--legacy-.md)
</dt> </dl>

 

 



