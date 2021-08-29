---
description: 'L’exemple de code suivant montre comment utiliser la méthode IDirect3DDevice9 :: GetDepthStencilSurface pour récupérer un pointeur vers la surface de mémoire tampon de profondeur détenue par l’appareil.'
ms.assetid: cd5c158a-d2c4-4ced-aa6f-cd8c0e426a74
title: Récupération d’une mémoire tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad335dae0441d61110c7c1275a01544e1834a8b3846fb442f5adab6b3169044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628299"
---
# <a name="retrieving-a-depth-buffer-direct3d-9"></a>Récupération d’une mémoire tampon de profondeur (Direct3D 9)

L’exemple de code suivant montre comment utiliser la méthode [**IDirect3DDevice9 :: GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) pour récupérer un pointeur vers la surface de mémoire tampon de profondeur détenue par l’appareil.


```
LPDIRECT3DSURFACE9 pZBuffer;

m_d3dDevice->GetDepthStencilSurface( &pZBuffer );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de profondeur](depth-buffers.md)
</dt> </dl>

 

 
