---
description: Lorsqu’elles sont éclairées par une source de lumière, les surfaces de cache affichent une réflexion lumineuse diffuse.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Cartes de lumière diffuse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab6a85fb93bc1ebcc15735431c1d54be4482a1f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481544"
---
# <a name="diffuse-light-maps-direct3d-9"></a><span data-ttu-id="447da-103">Cartes de lumière diffuse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="447da-103">Diffuse Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="447da-104">Lorsqu’elles sont éclairées par une source de lumière, les surfaces de cache affichent une réflexion lumineuse diffuse.</span><span class="sxs-lookup"><span data-stu-id="447da-104">When illuminated by a light source, matte surfaces display diffuse light reflection.</span></span> <span data-ttu-id="447da-105">La luminosité de la lumière diffuse dépend de la distance à partir de la source de lumière et de l’angle entre la normale de la surface et le vecteur de direction de la source de lumière.</span><span class="sxs-lookup"><span data-stu-id="447da-105">The brightness of diffuse light depends on the distance from the light source and the angle between the surface normal and the light source direction vector.</span></span> <span data-ttu-id="447da-106">Les effets d’éclairage diffus simulés par les calculs d’éclairage produisent uniquement des effets généraux.</span><span class="sxs-lookup"><span data-stu-id="447da-106">The diffuse lighting effects simulated by lighting calculations produce only general effects.</span></span>

<span data-ttu-id="447da-107">Votre application peut simuler un éclairage diffus plus complexe avec des cartes de lumière de texture.</span><span class="sxs-lookup"><span data-stu-id="447da-107">Your application can simulate more complex diffuse lighting with texture light maps.</span></span> <span data-ttu-id="447da-108">Pour ce faire, ajoutez la carte de lumière diffuse à la texture de base, comme illustré dans l’exemple de code C++ suivant.</span><span class="sxs-lookup"><span data-stu-id="447da-108">Do this by adding the diffuse light map to the base texture, as shown in the following C++ code example.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a><span data-ttu-id="447da-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="447da-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="447da-110">Placage de lumière avec des textures</span><span class="sxs-lookup"><span data-stu-id="447da-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



