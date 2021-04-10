---
description: 'L’exemple de code suivant montre comment utiliser la méthode IDirect3DDevice9 :: GetDepthStencilSurface pour récupérer un pointeur vers la surface de mémoire tampon de profondeur détenue par l’appareil.'
ms.assetid: cd5c158a-d2c4-4ced-aa6f-cd8c0e426a74
title: Récupération d’une mémoire tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae914b8506fd0c4169f0cfec0d78d7c3bd9b9d61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109599"
---
# <a name="retrieving-a-depth-buffer-direct3d-9"></a><span data-ttu-id="d7ea9-103">Récupération d’une mémoire tampon de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d7ea9-103">Retrieving a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="d7ea9-104">L’exemple de code suivant montre comment utiliser la méthode [**IDirect3DDevice9 :: GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) pour récupérer un pointeur vers la surface de mémoire tampon de profondeur détenue par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-104">The following code example shows how to use the [**IDirect3DDevice9::GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) method to retrieve a pointer to the depth-buffer surface owned by the device.</span></span>


```
LPDIRECT3DSURFACE9 pZBuffer;

m_d3dDevice->GetDepthStencilSurface( &pZBuffer );
```



## <a name="related-topics"></a><span data-ttu-id="d7ea9-105">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7ea9-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7ea9-106">Mémoires tampons de profondeur</span><span class="sxs-lookup"><span data-stu-id="d7ea9-106">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
