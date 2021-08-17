---
description: Votre application effectue généralement un rendu des scènes 3D plus réaliste si elle utilise des cartes de lumière colorées. Une carte de lumière colorée utilise les données RVB de la carte de lumière pour les informations d’éclairage.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Cartes d’éclairage de couleur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbff9fe246131fc90bda8ac9b5f1c49cd2413c412a7b3da5c013b1e936aa6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989299"
---
# <a name="color-light-maps-direct3d-9"></a>Cartes d’éclairage de couleur (Direct3D 9)

Votre application effectue généralement un rendu des scènes 3D plus réaliste si elle utilise des cartes de lumière colorées. Une carte de lumière colorée utilise les données RVB de la carte de lumière pour les informations d’éclairage.

L’exemple de code C++ suivant illustre le mappage de lumière avec les données de couleur RVB.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



Cet exemple définit la carte de lumière comme première texture. Il définit ensuite l’état de la première étape de fusion pour moduler les données de texture entrante. Elle utilise la première texture et la couleur actuelle de la primitive comme arguments de l’opération de modulation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Placage de lumière avec des textures](light-mapping-with-textures.md)
</dt> </dl>

 

 



