---
description: Le moteur d’éclairage combine la couleur matérielle, la couleur du vertex et les informations d’éclairage pour générer une couleur par vertex.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Fusion de texture alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513149"
---
# <a name="alpha-texture-blending-direct3d-9"></a>Fusion de texture alpha (Direct3D 9)

Le moteur d’éclairage combine la couleur matérielle, la couleur du vertex et les informations d’éclairage pour générer une couleur par vertex. Une fois interpolées, cela génère une couleur par pixel qui est écrite dans la mémoire tampon de trame. Si une application active la fusion de texture, la couleur de pixel devient une combinaison du pixel actuel dans la mémoire tampon de frame et une couleur de texture.

Cette formule détermine la couleur finale du pixel fusionné :


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



Où :

-   La couleur est la couleur de pixel de sortie.
-   TexelColor est la couleur d’entrée après le filtrage de texture.
-   SourceBlend est le pourcentage de la couleur de pixel finale qui est constitué de la couleur Texel source.
-   CurrentPixelColor est la couleur du pixel actuel.
-   DestBlend est le pourcentage de la couleur de pixel finale qui est constitué de la couleur de pixel actuelle.

L’équation de fusion finale est définie en appelant [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) et en spécifiant l’état de rendu Blend (D3DRS \_ BLENDXXX) avec un facteur de fusion correspondant ([**D3DBLEND**](./d3dblend.md)). Les valeurs de SourceBlend et DestBlend sont comprises entre 0,0 (transparent) et 1,0 (opaque) inclus. En outre, une application peut contrôler la transparence d’un pixel en définissant la valeur alpha dans une texture. Dans ce cas, utilisez ce qui suit :


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



L’équation de fusion entraîne la transparence du pixel rendu. Les valeurs par défaut sont :


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion de texture](texture-blending.md)
</dt> <dt>

[Filtrage de texture (Direct3D 9)](texture-filtering.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
