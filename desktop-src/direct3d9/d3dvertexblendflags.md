---
description: Définit les indicateurs utilisés pour contrôler le nombre ou les matrices que le système applique lors de la fusion de vertex multimatrix.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Énumération D3DVERTEXBLENDFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322870"
---
# <a name="d3dvertexblendflags-enumeration"></a><span data-ttu-id="43b12-103">Énumération D3DVERTEXBLENDFLAGS</span><span class="sxs-lookup"><span data-stu-id="43b12-103">D3DVERTEXBLENDFLAGS enumeration</span></span>

<span data-ttu-id="43b12-104">Définit les indicateurs utilisés pour contrôler le nombre ou les matrices que le système applique lors de la fusion de vertex multimatrix.</span><span class="sxs-lookup"><span data-stu-id="43b12-104">Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b12-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43b12-105">Syntax</span></span>


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a><span data-ttu-id="43b12-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="43b12-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="43b12-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**Désactivation de D3DVBF \_**</span><span class="sxs-lookup"><span data-stu-id="43b12-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="43b12-108">Désactiver la fusion de vertex ; Appliquez uniquement la matrice universelle définie par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index de l’état de la transformation est 0.</span><span class="sxs-lookup"><span data-stu-id="43b12-108">Disable vertex blending; apply only the world matrix set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation state is 0.</span></span>

</dd> <dt>

<span data-ttu-id="43b12-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="43b12-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF\_1WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="43b12-110">Activez la fusion de vertex entre les deux matrices définies par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index pour les États de transformation est 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="43b12-110">Enable vertex blending between the two matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="43b12-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="43b12-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF\_2WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="43b12-112">Activez la fusion de vertex entre les trois matrices définies par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index pour les États de transformation est 0, 1 et 2.</span><span class="sxs-lookup"><span data-stu-id="43b12-112">Enable vertex blending between the three matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, and 2.</span></span>

</dd> <dt>

<span data-ttu-id="43b12-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="43b12-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF\_3WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="43b12-114">Activez la fusion de vertex entre les quatre matrices définies par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index pour les États de transformation est 0, 1, 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="43b12-114">Enable vertex blending between the four matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, 2, and 3.</span></span>

</dd> <dt>

<span data-ttu-id="43b12-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**\_Interpolation D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="43b12-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF\_TWEENING**</span></span>
</dt> <dd>

<span data-ttu-id="43b12-116">La fusion de vertex s’effectue à l’aide de la valeur assignée à D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="43b12-116">Vertex blending is done by using the value assigned to D3DRS\_TWEENFACTOR.</span></span>

</dd> <dt>

<span data-ttu-id="43b12-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="43b12-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF\_0WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="43b12-118">Utilisez une matrice unique avec un poids de 1,0.</span><span class="sxs-lookup"><span data-stu-id="43b12-118">Use a single matrix with a weight of 1.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43b12-119">Notes</span><span class="sxs-lookup"><span data-stu-id="43b12-119">Remarks</span></span>

<span data-ttu-id="43b12-120">Les membres de ce type sont utilisés avec l' \_ État de rendu D3DRS VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="43b12-120">Members of this type are used with the D3DRS\_VERTEXBLEND render state.</span></span>

<span data-ttu-id="43b12-121">La fusion géométrique (mélange de vertex multimatrix) requiert que votre application utilise un format de vertex qui a des poids de fusion (bêta) pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="43b12-121">Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.</span></span>

## <a name="requirements"></a><span data-ttu-id="43b12-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43b12-122">Requirements</span></span>



| <span data-ttu-id="43b12-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43b12-123">Requirement</span></span> | <span data-ttu-id="43b12-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="43b12-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43b12-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="43b12-125">Header</span></span><br/> | <dl> <span data-ttu-id="43b12-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="43b12-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b12-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b12-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b12-128">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="43b12-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="43b12-129">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="43b12-129">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> <dt>

[<span data-ttu-id="43b12-130">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="43b12-130">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="43b12-131">**D3DTS \_ worldn**</span><span class="sxs-lookup"><span data-stu-id="43b12-131">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="43b12-132">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="43b12-132">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
