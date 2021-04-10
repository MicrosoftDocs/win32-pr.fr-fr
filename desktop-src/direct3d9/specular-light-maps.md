---
description: En cas d’éclairage par une source de lumière, objets brillants-ceux qui utilisent des matériaux extrêmement réfléchissants-recevoir des surbrillances spéculaires.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Cartes de lumière spéculaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55b4bf34baae0e73c2d072d62470533fc99827a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846278"
---
# <a name="specular-light-maps-direct3d-9"></a><span data-ttu-id="de0b4-103">Cartes de lumière spéculaire (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="de0b4-103">Specular Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="de0b4-104">En cas d’éclairage par une source de lumière, objets brillants-ceux qui utilisent des matériaux extrêmement réfléchissants-recevoir des surbrillances spéculaires.</span><span class="sxs-lookup"><span data-stu-id="de0b4-104">When illuminated by a light source, shiny objects - those that use highly reflective materials - receive specular highlights.</span></span> <span data-ttu-id="de0b4-105">Dans certains cas, les surbrillances spéculaires produites par le module d’éclairage ne sont pas exactes.</span><span class="sxs-lookup"><span data-stu-id="de0b4-105">In some cases, the specular highlights produced by the lighting module is not accurate.</span></span> <span data-ttu-id="de0b4-106">Pour produire une mise en évidence plus attrayante, de nombreuses applications Direct3D appliquent des cartes de lumière spéculaire aux primitives.</span><span class="sxs-lookup"><span data-stu-id="de0b4-106">To produce a more appealing highlight, many Direct3D applications apply specular light maps to primitives.</span></span>

<span data-ttu-id="de0b4-107">Pour effectuer un mappage de lumière spéculaire, ajoutez la carte de lumière spéculaire à la texture de la primitive, puis Modulez (multipliez le résultat par) la carte de lumière RVB.</span><span class="sxs-lookup"><span data-stu-id="de0b4-107">To perform specular light mapping, add the specular light map to the primitive's texture, then modulate (multiply the result by) the RGB light map.</span></span>

<span data-ttu-id="de0b4-108">L’exemple de code suivant illustre ce processus en C++.</span><span class="sxs-lookup"><span data-stu-id="de0b4-108">The following code example illustrates this process in C++.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a><span data-ttu-id="de0b4-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de0b4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de0b4-110">Placage de lumière avec des textures</span><span class="sxs-lookup"><span data-stu-id="de0b4-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



