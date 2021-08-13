---
description: Alpha peut également être fourni dans un matériau. Pour activer Material alpha, définissez l’état de rendu de la lumière diffuse afin que le runtime utilise les composants de couleur diffuse de matériau plutôt que les composants de couleur de diffusion de vertex.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Matériau alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a70ed4a3f5bcaf38f4ace079af5b2e1804af0e24340e5004898c9ed26707d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798976"
---
# <a name="material-alpha-direct3d-9"></a>Matériau alpha (Direct3D 9)

Alpha peut également être fourni dans un matériau. Pour activer Material alpha, définissez l’état de rendu de la lumière diffuse afin que le runtime utilise les composants de couleur diffuse de matériau plutôt que les composants de couleur de diffusion de vertex.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



Initialisez le matériau avec une valeur alpha et définissez le matériau avant le dessin.


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion alpha](alpha-blending.md)
</dt> </dl>

 

 



