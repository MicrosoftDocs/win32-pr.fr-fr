---
description: Le moteur d’éclairage Direct3D peut utiliser les données de couleur par vertex lors de l’éclairage si vous indiquez au runtime que les données sont présentes.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: État de la couleur de l' Per-Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385528"
---
# <a name="per-vertex-color-state-direct3d-9"></a><span data-ttu-id="eff8c-103">État de la couleur de l' Per-Vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="eff8c-103">Per-Vertex Color State (Direct3D 9)</span></span>

<span data-ttu-id="eff8c-104">Le moteur d’éclairage Direct3D peut utiliser les données de couleur par vertex lors de l’éclairage si vous indiquez au runtime que les données sont présentes.</span><span class="sxs-lookup"><span data-stu-id="eff8c-104">The Direct3D lighting engine can use per-vertex color data when performing lighting if you tell the runtime the data is present.</span></span> <span data-ttu-id="eff8c-105">Pour ce faire, activez l’état de rendu suivant :</span><span class="sxs-lookup"><span data-stu-id="eff8c-105">This is done by turning on the following render state:</span></span>


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



<span data-ttu-id="eff8c-106">Si la couleur par vertex est activée, les applications peuvent configurer la source à partir de laquelle le système récupère les informations de couleur pour un vertex.</span><span class="sxs-lookup"><span data-stu-id="eff8c-106">If per-vertex color is enabled, applications can configure the source from which the system retrieves color information for a vertex.</span></span> <span data-ttu-id="eff8c-107">Les \_ États de rendu D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE et D3DRS SPECULARMATERIALSOURCE \_ contrôlent respectivement les sources de composant de couleur ambiante, diffuse, émissif et spéculaire.</span><span class="sxs-lookup"><span data-stu-id="eff8c-107">The D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE render states control the ambient, diffuse, emissive, and specular color component sources, respectively.</span></span> <span data-ttu-id="eff8c-108">Chaque État peut être défini sur des membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , qui définit des constantes qui indiquent au système d’utiliser la matière actuelle, la couleur diffuse ou la couleur spéculaire comme source pour le composant de couleur spécifié.</span><span class="sxs-lookup"><span data-stu-id="eff8c-108">Each state can be set to members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type, which defines constants that instruct the system to use the current material, diffuse color, or specular color as the source for the specified color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eff8c-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eff8c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff8c-110">États de rendu</span><span class="sxs-lookup"><span data-stu-id="eff8c-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
