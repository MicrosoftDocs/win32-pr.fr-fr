---
description: La lumière ambiante est entourée d’une lumière qui rayonne dans toutes les directions. Pour plus d’informations sur la façon dont Direct3D utilise la lumière ambiante, voir mathématique d’éclairage (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: État d’éclairage ambiant (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111119"
---
# <a name="ambient-lighting-state-direct3d-9"></a>État d’éclairage ambiant (Direct3D 9)

La lumière ambiante est entourée d’une lumière qui rayonne dans toutes les directions. Pour plus d’informations sur la façon dont Direct3D utilise la lumière ambiante, voir [mathématique d’éclairage (Direct3D 9)](mathematics-of-lighting.md).

Une application C++ définit la couleur de l’éclairage ambiant en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) et en passant la valeur énumérée D3DRS \_ ambiante comme premier paramètre. Le deuxième paramètre est une valeur de couleur. La valeur par défaut est zéro.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
