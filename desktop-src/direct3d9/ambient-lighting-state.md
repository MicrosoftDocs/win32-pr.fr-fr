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
# <a name="ambient-lighting-state-direct3d-9"></a><span data-ttu-id="2392c-104">État d’éclairage ambiant (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2392c-104">Ambient Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="2392c-105">La lumière ambiante est entourée d’une lumière qui rayonne dans toutes les directions.</span><span class="sxs-lookup"><span data-stu-id="2392c-105">Ambient light is surrounding light that radiates from all directions.</span></span> <span data-ttu-id="2392c-106">Pour plus d’informations sur la façon dont Direct3D utilise la lumière ambiante, voir [mathématique d’éclairage (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="2392c-106">For information about how Direct3D uses ambient light, see [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="2392c-107">Une application C++ définit la couleur de l’éclairage ambiant en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) et en passant la valeur énumérée D3DRS \_ ambiante comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="2392c-107">A C++ application sets the color of ambient lighting by invoking the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and passing the enumerated value D3DRS\_AMBIENT as the first parameter.</span></span> <span data-ttu-id="2392c-108">Le deuxième paramètre est une valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="2392c-108">The second parameter is a color value.</span></span> <span data-ttu-id="2392c-109">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="2392c-109">The default value is zero.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a><span data-ttu-id="2392c-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2392c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2392c-111">États de rendu</span><span class="sxs-lookup"><span data-stu-id="2392c-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
