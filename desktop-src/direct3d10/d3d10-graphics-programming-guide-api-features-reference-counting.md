---
description: Les fonctions set de Direct3D 10 ne contiennent pas de référence à un objet enfant d’appareil.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Comptage de références (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335453"
---
# <a name="reference-counting-direct3d-10"></a>Comptage de références (Direct3D 10)

Les fonctions set de Direct3D 10 ne contiennent pas de référence à un objet enfant d’appareil. Cela signifie que chaque application doit contenir une référence à un objet enfant d’appareil tant que l’objet doit être lié au pipeline. Lorsque le décompte de références d’un objet tombe à zéro, l’objet est supprimé du pipeline et détruit. Ce style d’exploitation de référence est également connu sous le nom d’exploitation de référence faible, car chaque emplacement de liaison de pipeline contient une référence faible à l’interface/l’objet qui lui est lié.

Par exemple :


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





Différences entre Direct3D 9 et Direct3D 10 :

- Dans Direct3D 9, les fonctions set contiennent une référence aux objets appareil ; dans Direct3D 10, les fonctions set ne contiennent pas de référence aux objets enfants de l’appareil.



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités de l’API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




