---
description: Alpha peut également être fourni dans un matériau. Pour activer Material alpha, définissez l’état de rendu de la lumière diffuse afin que le runtime utilise les composants de couleur diffuse de matériau plutôt que les composants de couleur de diffusion de vertex.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Matériau alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108394"
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

 

 



