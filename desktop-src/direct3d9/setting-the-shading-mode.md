---
description: Direct3D permet de sélectionner un mode d’ombrage à la fois.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Définition du mode d’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482081"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>Définition du mode d’ombrage (Direct3D 9)

Direct3D permet de sélectionner un mode d’ombrage à la fois. Par défaut, l’ombrage Gouraud est sélectionné. En C++, vous pouvez modifier le mode d’ombrage en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) . Définissez le paramètre d' *État* sur D3DRS \_ SHADEMODE. Le paramètre *State* doit être défini sur un membre de l’énumération [**D3DSHADEMODE**](./d3dshademode.md) . Les exemples de code suivants illustrent la façon dont le mode d’ombrage actuel d’une application Direct3D peut être défini en mode ombré plat ou Gouraud.


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ombrage](shading.md)
</dt> </dl>

 

 
