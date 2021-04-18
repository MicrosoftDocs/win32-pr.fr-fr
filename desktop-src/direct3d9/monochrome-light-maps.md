---
description: Certaines cartes accélérateur 3D plus anciennes ne prennent pas en charge la fusion de texture à l’aide de la valeur alpha du pixel de destination.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Cartes de lumière monochromes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516337"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Cartes de lumière monochromes (Direct3D 9)

Certaines cartes accélérateur 3D plus anciennes ne prennent pas en charge la fusion de texture à l’aide de la valeur alpha du pixel de destination. Pour plus d’informations, consultez [fusion de texture alpha (Direct3D 9)](alpha-texture-blending.md) . En général, ces adaptateurs ne prennent pas en charge la fusion de texture multiple. Si votre application s’exécute sur un adaptateur tel que celui-ci, elle peut utiliser la fusion de texture multipasse pour effectuer un mappage de lumière monochrome.

Pour effectuer un mappage de lumière monochrome, une application stocke les informations d’éclairage dans les données alpha de ses textures de carte de lumière. L’application utilise les fonctionnalités de filtrage de texture de Direct3D pour effectuer un mappage de chaque pixel de l’image de la primitive à un Texel correspondant dans la carte de lumière. Elle définit le facteur de fusion source sur la valeur alpha du Texel correspondant.

L’exemple suivant montre comment une application peut utiliser une texture comme une carte d’éclairage monochrome :


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



Étant donné que les adaptateurs d’affichage qui ne prennent pas en charge la fusion alpha de destination ne prennent généralement pas en charge la fusion de texture multiple, cet exemple définit la carte de lumière comme première texture, qui est disponible sur toutes les cartes d’accélération 3D. L’exemple de code définit l’opération de couleur pour la phase de fusion de la texture afin de fusionner les données de texture avec la couleur existante de la primitive. Il sélectionne ensuite la première texture et la couleur existante de la primitive comme données d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Placage de lumière avec des textures](light-mapping-with-textures.md)
</dt> </dl>

 

 



