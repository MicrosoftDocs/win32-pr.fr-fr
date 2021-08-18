---
description: Lorsqu’elles sont éclairées par une source de lumière, les surfaces de cache affichent une réflexion lumineuse diffuse.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Cartes clair diffus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fc2b5054a30bf8df703941b3cedf0810c378a5fb459d8c5783bb295ff9abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044447"
---
# <a name="diffuse-light-maps-direct3d-9"></a>Cartes clair diffus (Direct3D 9)

Lorsqu’elles sont éclairées par une source de lumière, les surfaces de cache affichent une réflexion lumineuse diffuse. La luminosité de la lumière diffuse dépend de la distance à partir de la source de lumière et de l’angle entre la normale de la surface et le vecteur de direction de la source de lumière. Les effets d’éclairage diffus simulés par les calculs d’éclairage produisent uniquement des effets généraux.

Votre application peut simuler un éclairage diffus plus complexe avec des cartes de lumière de texture. Pour ce faire, ajoutez la carte de lumière diffuse à la texture de base, comme illustré dans l’exemple de code C++ suivant.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Placage de lumière avec des textures](light-mapping-with-textures.md)
</dt> </dl>

 

 



