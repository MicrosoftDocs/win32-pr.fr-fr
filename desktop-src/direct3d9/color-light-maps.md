---
description: Votre application effectue généralement un rendu des scènes 3D plus réaliste si elle utilise des cartes de lumière colorées. Une carte de lumière colorée utilise les données RVB de la carte de lumière pour les informations d’éclairage.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Cartes de lumière de couleur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483176"
---
# <a name="color-light-maps-direct3d-9"></a><span data-ttu-id="93da4-104">Cartes de lumière de couleur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="93da4-104">Color Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="93da4-105">Votre application effectue généralement un rendu des scènes 3D plus réaliste si elle utilise des cartes de lumière colorées.</span><span class="sxs-lookup"><span data-stu-id="93da4-105">Your application will usually render 3D scenes more realistically if it uses colored light maps.</span></span> <span data-ttu-id="93da4-106">Une carte de lumière colorée utilise les données RVB de la carte de lumière pour les informations d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="93da4-106">A colored light map uses the RGB data in the light map for its lighting information.</span></span>

<span data-ttu-id="93da4-107">L’exemple de code C++ suivant illustre le mappage de lumière avec les données de couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="93da4-107">The following C++ code example demonstrates light mapping with RGB color data.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



<span data-ttu-id="93da4-108">Cet exemple définit la carte de lumière comme première texture.</span><span class="sxs-lookup"><span data-stu-id="93da4-108">This example sets the light map as the first texture.</span></span> <span data-ttu-id="93da4-109">Il définit ensuite l’état de la première étape de fusion pour moduler les données de texture entrante.</span><span class="sxs-lookup"><span data-stu-id="93da4-109">It then sets the state of the first blending stage to modulate the incoming texture data.</span></span> <span data-ttu-id="93da4-110">Elle utilise la première texture et la couleur actuelle de la primitive comme arguments de l’opération de modulation.</span><span class="sxs-lookup"><span data-stu-id="93da4-110">It uses the first texture and the current color of the primitive as the arguments to the modulate operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93da4-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93da4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93da4-112">Placage de lumière avec des textures</span><span class="sxs-lookup"><span data-stu-id="93da4-112">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



