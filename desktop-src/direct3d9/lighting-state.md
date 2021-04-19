---
description: Si vous ne vous contentez pas d’un nuanceur de sommets ou d’un nuanceur de pixels, vous pouvez choisir d’utiliser le moteur d’éclairage dans le Runtime.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: État d’éclairage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515301"
---
# <a name="lighting-state-direct3d-9"></a><span data-ttu-id="544f2-103">État d’éclairage (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="544f2-103">Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="544f2-104">Si vous ne vous contentez pas d’un nuanceur de sommets ou d’un nuanceur de pixels, vous pouvez choisir d’utiliser le moteur d’éclairage dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="544f2-104">If you do not light with a vertex shader or a pixel shader, you may choose to use the lighting engine in the runtime.</span></span> <span data-ttu-id="544f2-105">Le moteur d’éclairage exige que les données de vertex contiennent des normales par vertex ; les vertex sans données normales génèrent un produit scalaire de zéro dans tous les calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="544f2-105">The lighting engine requires that the vertex data contains per-vertex normals; vertices without normal data will generate a dot product of zero in all lighting computations.</span></span> <span data-ttu-id="544f2-106">Les calculs d’éclairage sont traités plus en détail dans l' [éclairage mathématique (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="544f2-106">The lighting calculations are covered in more detail in [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="544f2-107">Pour activer le moteur d’éclairage, utilisez :</span><span class="sxs-lookup"><span data-stu-id="544f2-107">To enable the lighting engine, use:</span></span>


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a><span data-ttu-id="544f2-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="544f2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="544f2-109">États de rendu</span><span class="sxs-lookup"><span data-stu-id="544f2-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



