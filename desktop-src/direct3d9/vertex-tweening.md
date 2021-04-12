---
description: L’interpolation de vertex fusionne deux positions fournies par l’utilisateur (ou normales).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolation de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200763"
---
# <a name="vertex-tweening-direct3d-9"></a><span data-ttu-id="9303f-103">Interpolation de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9303f-103">Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="9303f-104">L’interpolation de vertex fusionne deux positions fournies par l’utilisateur (ou normales).</span><span class="sxs-lookup"><span data-stu-id="9303f-104">Vertex tweening blends two user-provided positions (or normals).</span></span> <span data-ttu-id="9303f-105">L’interpolation s’exclut mutuellement de la fusion de vertex avec des poids.</span><span class="sxs-lookup"><span data-stu-id="9303f-105">Tweening is mutually exclusive from vertex blending with weights.</span></span> <span data-ttu-id="9303f-106">L’interpolation est effectuée avant l’éclairage et le découpage, et est activée en définissant D3DRS \_ VERTEXBLEND sur l' \_ interpolation D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="9303f-106">Tweening is performed before lighting and clipping, and is enabled by setting D3DRS\_VERTEXBLEND to D3DVBF\_TWEENING.</span></span> <span data-ttu-id="9303f-107">La position du vertex résultante est calculée par :</span><span class="sxs-lookup"><span data-stu-id="9303f-107">The resulting vertex position is computed by:</span></span>


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



<span data-ttu-id="9303f-108">La même approche est utilisée pour le calcul des normales.</span><span class="sxs-lookup"><span data-stu-id="9303f-108">The same approach is used for calculating normals.</span></span> <span data-ttu-id="9303f-109">Pour plus d’informations, consultez [utilisation de l’interpolation de vertex (Direct3D 9)](using-vertex-tweening.md).</span><span class="sxs-lookup"><span data-stu-id="9303f-109">For more information, see [Using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9303f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9303f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9303f-111">Fusion géométrique</span><span class="sxs-lookup"><span data-stu-id="9303f-111">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



