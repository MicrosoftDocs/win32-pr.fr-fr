---
description: Direct3D permet de sélectionner un mode d’ombrage à la fois.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Définition du mode d’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769908513d4388fafae73f5a6788aef37c3ac9456a00f2e3280c57e04c18b462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068959"
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

 

 
