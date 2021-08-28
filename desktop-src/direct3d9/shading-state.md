---
description: Direct3D prend en charge l’ombrage plat et l’ombrage Gouraud. La valeur par défaut est l’ombrage Gouraud. Pour contrôler le mode de trame actuel, votre application C++ spécifie un membre du type énuméré D3DSHADEMODE pour l' \_ État de rendu D3DRS SHADEMODE.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: État de l’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f28514fefbf39e75bd84a0ae56324fd859f0fd85fa4a25449e349ce592ab3b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727599"
---
# <a name="shading-state-direct3d-9"></a>État de l’ombrage (Direct3D 9)

Direct3D prend en charge l’ombrage plat et l’ombrage Gouraud. La valeur par défaut est l’ombrage Gouraud. Pour contrôler le mode de trame actuel, votre application C++ spécifie un membre du type énuméré [**D3DSHADEMODE**](./d3dshademode.md) pour l' \_ État de rendu D3DRS SHADEMODE.

L’exemple de code C++ suivant illustre le processus de définition de l’état d’ombrage en mode d’ombrage plat.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
