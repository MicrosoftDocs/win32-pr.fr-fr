---
description: En cas d’éclairage par une source de lumière, objets brillants-ceux qui utilisent des matériaux extrêmement réfléchissants-recevoir des surbrillances spéculaires.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Cartes de lumière spéculaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55b4bf34baae0e73c2d072d62470533fc99827a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095293"
---
# <a name="specular-light-maps-direct3d-9"></a>Cartes de lumière spéculaire (Direct3D 9)

En cas d’éclairage par une source de lumière, objets brillants-ceux qui utilisent des matériaux extrêmement réfléchissants-recevoir des surbrillances spéculaires. Dans certains cas, les surbrillances spéculaires produites par le module d’éclairage ne sont pas exactes. Pour produire une mise en évidence plus attrayante, de nombreuses applications Direct3D appliquent des cartes de lumière spéculaire aux primitives.

Pour effectuer un mappage de lumière spéculaire, ajoutez la carte de lumière spéculaire à la texture de la primitive, puis Modulez (multipliez le résultat par) la carte de lumière RVB.

L’exemple de code suivant illustre ce processus en C++.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Placage de lumière avec des textures](light-mapping-with-textures.md)
</dt> </dl>

 

 



