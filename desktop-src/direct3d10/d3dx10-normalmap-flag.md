---
description: Ces indicateurs permettent de contrôler la façon dont D3DX10ComputeNormalMap génère des mappages normaux. N’importe quel nombre de ces indicateurs peut être ou, ensemble, dans n’importe quelle combinaison.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Énumération D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531346"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a><span data-ttu-id="5ec06-104">D3DX10 \_ NORMALMAP \_ Flag (énumération)</span><span class="sxs-lookup"><span data-stu-id="5ec06-104">D3DX10\_NORMALMAP\_FLAG enumeration</span></span>

<span data-ttu-id="5ec06-105">Ces indicateurs permettent de contrôler la façon dont [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) génère des mappages normaux.</span><span class="sxs-lookup"><span data-stu-id="5ec06-105">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="5ec06-106">N’importe quel nombre de ces indicateurs peut être ou, ensemble, dans n’importe quelle combinaison.</span><span class="sxs-lookup"><span data-stu-id="5ec06-106">Any number of these flags may be OR'd together in any combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec06-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ec06-107">Syntax</span></span>


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="5ec06-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5ec06-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ec06-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NORMALMAP \_ miroir \_ U**</span><span class="sxs-lookup"><span data-stu-id="5ec06-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="5ec06-110">Indique que les pixels du bord de la texture sur l’axe des U doivent être mis en miroir, pas renvoyés à la ligne.</span><span class="sxs-lookup"><span data-stu-id="5ec06-110">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="5ec06-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NORMALMAP \_ miroir \_ V**</span><span class="sxs-lookup"><span data-stu-id="5ec06-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="5ec06-112">Indique que les pixels du bord de la texture sur l’axe V doivent être mis en miroir, pas renvoyés à la ligne.</span><span class="sxs-lookup"><span data-stu-id="5ec06-112">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="5ec06-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**\_Miroir d3dx10 NORMALMAP \_**</span><span class="sxs-lookup"><span data-stu-id="5ec06-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="5ec06-114">Identique à D3DX10 \_ NORMALMAP \_ miroir \_ U \| d3dx10 \_ NORMALMAP \_ MIRROR \_ V.</span><span class="sxs-lookup"><span data-stu-id="5ec06-114">Same as D3DX10\_NORMALMAP\_MIRROR\_U \| D3DX10\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="5ec06-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NORMALMAP \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="5ec06-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="5ec06-116">Inverse la direction de chaque normal.</span><span class="sxs-lookup"><span data-stu-id="5ec06-116">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="5ec06-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**\_Occlusion de \_ calcul d3dx10 \_ NORMALMAP**</span><span class="sxs-lookup"><span data-stu-id="5ec06-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="5ec06-118">Calcule le terme d’occlusion par pixel et l’encode en alpha.</span><span class="sxs-lookup"><span data-stu-id="5ec06-118">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="5ec06-119">Une valeur alpha de 1 signifie que le pixel n’est pas masqué de quelque façon que ce soit, et une valeur alpha de 0 signifie que le pixel est complètement masqué.</span><span class="sxs-lookup"><span data-stu-id="5ec06-119">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ec06-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ec06-120">Requirements</span></span>



| <span data-ttu-id="5ec06-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ec06-121">Requirement</span></span> | <span data-ttu-id="5ec06-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ec06-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec06-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ec06-123">Header</span></span><br/> | <dl> <span data-ttu-id="5ec06-124"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec06-124"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec06-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ec06-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec06-126">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="5ec06-126">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




