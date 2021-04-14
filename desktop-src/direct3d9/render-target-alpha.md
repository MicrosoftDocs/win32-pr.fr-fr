---
description: Le mélangeur de mémoires tampons de frames peut désormais fusionner les canaux alpha indépendamment de la fusion des canaux de couleur sur les cibles de rendu. Ce contrôle est activé avec un nouvel état de rendu, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Rendu de la cible Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520476"
---
# <a name="render-target-alpha-direct3d-9"></a><span data-ttu-id="9cecb-104">Rendu de la cible Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9cecb-104">Render Target Alpha (Direct3D 9)</span></span>

<span data-ttu-id="9cecb-105">Le mélangeur de mémoires tampons de frames peut désormais fusionner les canaux alpha indépendamment de la fusion des canaux de couleur sur les cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="9cecb-105">The frame buffer blender can now blend alpha channels independent from color-channel blending on render targets.</span></span> <span data-ttu-id="9cecb-106">Ce contrôle est activé avec un nouvel état de rendu, D3DRS \_ SEPARATEALPHABLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="9cecb-106">This control is enabled with a new render state, D3DRS\_SEPARATEALPHABLENDENABLE.</span></span>

<span data-ttu-id="9cecb-107">Lorsque D3DRS \_ SEPARATEALPHABLENDENABLE est défini sur **false** (qui est la condition par défaut), les facteurs et les opérations de fusion de cible de rendu appliqués à alpha sont les mêmes que ceux définis pour la fusion des canaux de couleurs.</span><span class="sxs-lookup"><span data-stu-id="9cecb-107">When D3DRS\_SEPARATEALPHABLENDENABLE is set to **FALSE** (which is the default condition), the render-target blending factors and operations applied to alpha are the same as those defined for blending color channels.</span></span> <span data-ttu-id="9cecb-108">Un pilote doit définir le \_ Cap SEPARATEALPHABLEND D3DPMISCCAPS pour indiquer qu’il peut prendre en charge la fusion alpha de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="9cecb-108">A driver needs to set the D3DPMISCCAPS\_SEPARATEALPHABLEND cap to indicate that it can support render-target alpha blending.</span></span> <span data-ttu-id="9cecb-109">Veillez à activer D3DRS \_ ALPHABLEND pour indiquer au pipeline que la fusion alpha est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9cecb-109">Be sure to enable D3DRS\_ALPHABLEND to tell the pipeline that alpha blending is needed.</span></span>

<span data-ttu-id="9cecb-110">Pour contrôler les facteurs dans le canal alpha des mélangeurs de rendu-cible, deux nouveaux États de rendu sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="9cecb-110">To control the factors in the alpha channel of the render-target blenders, two new render states are defined as follows:</span></span>


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



<span data-ttu-id="9cecb-111">À l’instar des D3DRS \_ SRCBLEND et D3DRS \_ DESTBLEND, ceux-ci peuvent être définis sur l’une des valeurs de l’énumération [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="9cecb-111">Like the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND, these can be set to one of the values in the [**D3DBLEND**](./d3dblend.md) enumeration.</span></span> <span data-ttu-id="9cecb-112">Les paramètres de fusion de source et de destination peuvent être combinés de plusieurs façons, selon les paramètres des membres SrcBlendCaps et DestBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="9cecb-112">The source and destination blend settings can be combined in several ways, depending on the settings in the SrcBlendCaps and DestBlendCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="9cecb-113">La fusion alpha s’effectue comme suit :</span><span class="sxs-lookup"><span data-stu-id="9cecb-113">The alpha blending is done as follows:</span></span>

<span data-ttu-id="9cecb-114">renderTargetAlpha = (alpha<sub>dans</sub> \* srcBlendOp) BlendOp (alpha<sub>RT</sub> \* destBlendOp)</span><span class="sxs-lookup"><span data-stu-id="9cecb-114">renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)</span></span>

<span data-ttu-id="9cecb-115">Où :</span><span class="sxs-lookup"><span data-stu-id="9cecb-115">Where:</span></span>

-   <span data-ttu-id="9cecb-116">Alpha<sub>dans</sub> est la valeur alpha d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9cecb-116">alpha<sub>in</sub> is the input alpha value.</span></span>
-   <span data-ttu-id="9cecb-117">srcBlendOp est l’un des facteurs de mélange dans [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="9cecb-117">srcBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="9cecb-118">BlendOp est l’un des facteurs de mélange dans [**D3DBLENDOP**](./d3dblendop.md).</span><span class="sxs-lookup"><span data-stu-id="9cecb-118">BlendOp is one of the blend factors in [**D3DBLENDOP**](./d3dblendop.md).</span></span>
-   <span data-ttu-id="9cecb-119">Alpha<sub>RT</sub> est la valeur alpha Render-cible.</span><span class="sxs-lookup"><span data-stu-id="9cecb-119">alpha<sub>rt</sub> is the render-target alpha value.</span></span>
-   <span data-ttu-id="9cecb-120">destBlendOp est l’un des facteurs de mélange dans [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="9cecb-120">destBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="9cecb-121">renderTargetAlpha est la valeur alpha fusionnée finale.</span><span class="sxs-lookup"><span data-stu-id="9cecb-121">renderTargetAlpha is the final blended alpha value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cecb-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cecb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cecb-123">Fusion alpha</span><span class="sxs-lookup"><span data-stu-id="9cecb-123">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 
