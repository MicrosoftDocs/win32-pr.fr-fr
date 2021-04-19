---
description: Direct3D prend en charge l’ombrage plat et l’ombrage Gouraud. La valeur par défaut est l’ombrage Gouraud. Pour contrôler le mode de trame actuel, votre application C++ spécifie un membre du type énuméré D3DSHADEMODE pour l' \_ État de rendu D3DRS SHADEMODE.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: État de l’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544193"
---
# <a name="shading-state-direct3d-9"></a><span data-ttu-id="12b3a-105">État de l’ombrage (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="12b3a-105">Shading State (Direct3D 9)</span></span>

<span data-ttu-id="12b3a-106">Direct3D prend en charge l’ombrage plat et l’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="12b3a-106">Direct3D supports both flat and Gouraud shading.</span></span> <span data-ttu-id="12b3a-107">La valeur par défaut est l’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="12b3a-107">The default is Gouraud shading.</span></span> <span data-ttu-id="12b3a-108">Pour contrôler le mode de trame actuel, votre application C++ spécifie un membre du type énuméré [**D3DSHADEMODE**](./d3dshademode.md) pour l' \_ État de rendu D3DRS SHADEMODE.</span><span class="sxs-lookup"><span data-stu-id="12b3a-108">To control the current shading mode, your C++ application specifies a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type for the D3DRS\_SHADEMODE render state.</span></span>

<span data-ttu-id="12b3a-109">L’exemple de code C++ suivant illustre le processus de définition de l’état d’ombrage en mode d’ombrage plat.</span><span class="sxs-lookup"><span data-stu-id="12b3a-109">The following C++ code example demonstrates the process of setting the shading state to flat shading mode.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a><span data-ttu-id="12b3a-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12b3a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12b3a-111">États de rendu</span><span class="sxs-lookup"><span data-stu-id="12b3a-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
