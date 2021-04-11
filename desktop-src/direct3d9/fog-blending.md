---
description: La fusion de brouillard fait référence à l’application du facteur de brouillard au brouillard et aux couleurs d’objet pour produire la couleur finale qui apparaît dans une scène, comme indiqué dans formules de brouillard (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Fusion de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108402"
---
# <a name="fog-blending-direct3d-9"></a><span data-ttu-id="a4011-103">Fusion de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a4011-103">Fog Blending (Direct3D 9)</span></span>

<span data-ttu-id="a4011-104">La fusion de brouillard fait référence à l’application du facteur de brouillard au brouillard et aux couleurs d’objet pour produire la couleur finale qui apparaît dans une scène, comme indiqué dans [formules de brouillard (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="a4011-104">Fog blending refers to the application of the fog factor to the fog and object colors to produce the final color that appears in a scene, as discussed in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="a4011-105">L' \_ État de rendu D3DRS FOGENABLE contrôle la fusion de brouillard.</span><span class="sxs-lookup"><span data-stu-id="a4011-105">The D3DRS\_FOGENABLE render state controls fog blending.</span></span> <span data-ttu-id="a4011-106">Affectez la valeur **true** à cet état de rendu pour activer la fusion de brouillard, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a4011-106">Set this render state to **TRUE** to enable fog blending as shown in the following example code.</span></span> <span data-ttu-id="a4011-107">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="a4011-107">The default is **FALSE**.</span></span>


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



<span data-ttu-id="a4011-108">Vous devez activer la fusion de brouillard pour le brouillard de pixel et le brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="a4011-108">You must enable fog blending for both pixel fog and vertex fog.</span></span> <span data-ttu-id="a4011-109">Pour plus d’informations sur l’utilisation de ces types de brouillard, consultez [nuance de pixels (Direct3D 9)](pixel-fog.md) et [brouillard de vertex (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a4011-109">For information about using these types of fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4011-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4011-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4011-111">Types de brouillard</span><span class="sxs-lookup"><span data-stu-id="a4011-111">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



